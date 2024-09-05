# SetOleObject

Bu method, bir ole kontrol üzerinde OLE nesnesi yaratır.\
\
**Kullanımı**

```
ControlObject.SetOLEObject(
  ObjectName As String  ' Yaratılacak nesne adı
) As Bool
```

**Parametreler**\
_ObjectName_\
Yaratılacak nesne adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri OLE nesnesidir.\
\
**Dikkat Edilecek Noktalar**\
Bu method, bir ole kontrol üzerinde OLE nesnesi yaratır.

```
  ControlObject.SetOLEObject("Excel.Application")
```
