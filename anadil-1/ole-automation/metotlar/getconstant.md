# GetConstant

Bu method ile OLE Automation nesnesinde tanımlanmış olan Constant değerleri Imagine'den almak mümkündür.\
\
**Kullanımı**

```
OLEObject.GetConstant(
  Name   ' Constant adı
) As Object
```

**Parametreler**\
_Name_\
OLE Automation nesnesinde tanımlanmış sabit adı\
\
Geri Dönüş Değeri\
Geri dönüş değeri önemli değildir.\
\
**Dikkat Edilecek Noktalar**\
Bu method ile OLE Automation nesnesinde tanımlanmış olan Constant değerleri Imagine'den almak mümkündür.

```
Dim range As Object
Dim para As Object
Dim Obj As Object
  obj:=CreateOleObject("Word.Application")
  range.AddParam(1)
  para:=range.GetProp("Paragraphs")
  para.SetProp("Style", obj.GetConstant("WdStyleHeading1"))
```
