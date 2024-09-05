# AddParam

Bu method, OLE Automation nesnesine parametre gönderir. Bu parametre CallMethod, SetProp veya GetProp Methodlarıyla kullanılır.\
\
**Kullanımı**

```
OLEObject.AddParam(
  Name As String   ' Parametre adı.
  Value As Number  ' Parametre değeri
) As Bool
```

**Parametreler**\
_Name_\
CallMethodla çağırılan OLE nesnesine ait bir methodun parametresinin adıdır.\
_Value_\
CallMethodla çağırılan OLE nesnesine ait bir methodun parametresine gönderilecek değerdir.\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemli değildir.\
\
**Dikkat Edilecek Noktalar**\
Bu method, OLE Automation nesnesine parametre göndermeye yarar.\
AddParam methodu ile gönderilen değerler içsel bir mekanizmada toplanarak CallMethod,SetProp veya GetProp methodlarıyla OLE Automation nesnesinde bulunan methodlara parametre göndermek için kullanılır.

```
Dim Range As Object
Dim myRange As Object
Dim para As Object
  Range:=doc.CallMethod("Range")
  range.AddParam(1)  
  para:=range.GetProp("Paragraphs")
  range.CallMethod("InsertAfter", "Hello World")
  myrange:=para.GetProp("Range")
  myrange.AddParam("Start",1)
  myrange.AddParam("End",5)
  font:=myrange.GetProp("Font")
  font.SetProp("Name", "Arial")
  font.SetProp("Size", 20)
  font.SetProp("ColorIndex", 10)
```
