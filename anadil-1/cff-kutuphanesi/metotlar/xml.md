# XML

Bu method CFF nesnesini, XML nesnesine dönüştürmektedir.\
\
**Kullanımı**

```
CFFObject.xml(
   ) As Object
```

\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlem başarılı ise XML nesnesidir.\
\
**Örnek**

```
  Dim oXML As Object
  Dim oCFF As Object
  .
  .
  .
 'CFF Object XML e dönüştürülüyor
  oXML:=CFF.xml()
  oXML.Dump("c:/Always/oxml.xml",0)
  

  'XML Object CFF e dönüştürülüyor
  oCFF:=oXML.cff()
  oCFF.DumpCFF()
```
