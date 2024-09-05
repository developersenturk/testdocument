# Load

Bu metod veritabanındaki Binary Link Object verisini veya büyük TEXT bilgisini BLO nesnesine doldurur.

**Kullanımı**

```
BLOObject.Load(
  RsObject,  ' rs nesnesi
  FieldName  ' Kolon adı
) As Bool
```

**Parametreler**\
_RsObject_\
rs nesnesi\
_FieldName_\
Kolon adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, booleandır.\
\
**Dikkat Edilecek Konular**\
Bu metod veritabanındaki Binary Link Object datasını veya büyük TEXT bilgisini BLO nesnesine doldurur. Eger metod, XML benzeri 255 karakterden büyük text kayıtlar için kullanılıyorsa, veritabanı tablosundaki ilgili kolonun veri tipinin text (ntext degil) olması gerekmektedir. Ve çalıştırılan SELECT cümlesinde BLO/XML/TEXT kolon adının son sırada yazılmış olması gerekmektedir. Örneğin: text veri tipindeki kolonun adı xml olsun:

```
Select  a, b, c, d, xml from tnm_xml where r_sayac=1
şeklinde olmalıdır.
```

```
Dim stm As Object
Dim myblo As Object
  stm:=PrepareStmDirect("Select FieldName from Table where KeyField=?")
  stm.SetParam(KeyValue)
  stm.ExecuteStm()
  If stm.MoveNext() Then
    myblo:=CreateBlo()
    myblo.Load(stm, FieldName)
  EndIf
```
