# AddUpdateField

Bu metod ile yazılan bir UPDATE query statement için kayıt değerleri verilmektedir.\
\
**Kullanımı**

```
RSObject.AddUpdateField(
  ColName As Strin          ' table column ismi
  Value As <Variant>  ' yeni row değeri
)
```

**Parametreler**\
_ColName_\
Table içersindeki güncelleme işleminde verilecek column ismidir.\
_Value_\
Verilen column ismine karşılık gelen yeni güncellenecek row değeridir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Bu metod ile BuildUpdateStm() fonksiyonunun kullanımı ile ortaya konulan RS nesnesinde, UPDATE statement içersindeki yeni table row değerleri verilmektedir. Verilen row değerleri SQL Server tarafından ilgili table içerisinde yeni değerler ile güncellenecektir.\
\
Metod kullanımında table'da yer alan sadece bir column ismi verilmelidir.\
\
Ayrıca value değerinin variant olması, bu değerin string, number veya date olabileceğini hatta NULL içeriğe sahip olabileceği anlamına gelmektedir.
