# BLO

Bu method XML nesnesini, BLO nesnesine dönüştürmektedir.\
\
**Kullanımı**

```
XMLObject.blo(
   ) As Object
```

\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlem başarılı ise BLO nesnesidir.\
\
**Örnek**\


```
  Dim rs as object
  Dim oXML as Object
  Dim oBlo as Object

  'ilgili tabloda text adinda data tipi text olan bir kolon oldugu varsayiliyor
  rs:=PrepareStmDirect("update wrk_hesap_plani set text=? where r_sayac=36056")

  oXML:=CreateXML()              
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  oXML.Append("123456789 ABCDEF")
  .
  .
  .
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
