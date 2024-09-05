# GetActiveOleObject

Bu fonksiyon o anda bir çalışan uygulamanın OLE Automation nesnesi getirir.\
\
**Kullanımı**

```
Function GetActiveOleObject(
  ObjectName  As String' O anda çalışan OLE nesnesinin ismi
) As Object
```

**Parametreler**\
_ObjectName_\
O anda çalışan, aktif edilecek OLE nesnesinin ismi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri OLE nesnesidir.\
\
**Dikkat Edilecek Noktalar**\
Bu fonksiyon o anda bir çalışan OLE Automation nesnesini getirir.

```
Dim myOLE As Object
  myOLE := GetActiveOleObject(\"Word.Application\")
```
