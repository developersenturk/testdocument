# CFF

Bu method XML nesnesini, CFF nesnesine dönüştürmektedir.\
\
**Kullanımı**

```
XMLObject.cff(
   ) As Object
```

\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlem başarılı ise CFF nesnesidir.\
\
**Örnek**

```
  Dim oXML As Object
  Dim oCFF As Object
  .
  .
  .
 'CFF Object XML e dönüştürülüyor
  oXML:=oCFF.xml()
  oXML.Dump("c:/Always/oxml.xml",0)
  

  'XML Object CFF e dönüştürülüyor
  oCFF:=oXML.cff()
  oCFF.DumpCFF()
```
