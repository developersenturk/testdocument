# SaveText

Bu method Database TEXT Object datasını, database'e kaydeder. 255 karakterden büyük TEXT bilgiyi ilgili TEXT kolonuna saklayabilmek için kullanılır.

**Kullanımı**

```
BLOObject.SaveText(
  RsObject,  ' SQL statement
  FieldName  ' Column adı
) As Bool
```

**Parametreler**\
_RsObject_\
SQL statement\
_FieldName_\
Column adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, booleandır.\
\
**Dikkat Edilecek Konular**\
Bu method Database Text Object datasını, veritabanına kaydeder. Veritabanı tablosundaki ilgili kolonun veri tipinin text (ntext degil) olması gerekmektedir.

```
  Dim oXML as Object
  Dim oBlo as Object
  Dim  Rs as object

  'ilgili tabloda text adinda data tipi text olan bir kolon oldugu varsayiliyor
  rs:=PrepareStmDirect("update wrk_hesap_plani set text=? where r_sayac=36056")

  oXML:=CreateXML()              
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  .
  .
  .
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("ZZZZZZZZZZZZZZZZ")

  'Burada Blo object yaratmaya gerek yok. oXML.blo() komutu yaratiyor zaten
  'oBlo:=CreateBlo() 
  
  'BLO Text object, XML Text object e donusturuluyor
  oBlo:=oXML.blo()
  
  'SaveText methodu oBlo yu rs parametresine (?) baglar
  oBlo.SaveText(rs, "text")
  rs.ExecuteStm()
  
  rs.Close()
  oXML.Close()
  oBlo.Close()

```

**Örnek2**

```

Text kolonu bilgisinin okunması

  rs:=PrepareStmDirect("Select text from wrk_hesap_plani where r_sayac=36056")
  if  Rs.ExecuteStm() Then
      oBlo:=CreateBlo()
      oBlo.Load(rs, "text")
      oXML:=CreateXML()
      
      'BLO Text object, XML Text object e donusturuluyor
      oXML:=oBlo.xml()
      oXML.Dump("c:\Always\text1.txt",0)
  Endif
```
