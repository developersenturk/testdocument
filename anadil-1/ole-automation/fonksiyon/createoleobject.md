# CreateOLEObject

Bu fonksiyon bir OLE Automation nesnesi yaratır.\
\
**Kullanımı**

```
Function CreateOLEObject(
  ObjectName  ' Yaratılacak OLE nesnesinin ismi
) As Object
```

**Parametreler**\
_ObjectName_\
Yaratılacak OLE nesnesinin ismi\
\
**Geri Dönüş Değeri**\
Geri dönüş OLE nesnesidir.\
\
**Dikkat Edilecek Noktalar**\
Bu fonksiyon bir OLE Automation nesnesi yaratır.

```
Dim myOLE As Object
  myOLE := CreateOLEObject(\"Word.Application\")
```
