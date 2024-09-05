# SetProp

Bu method ile OLE Automation nesnesine property değeri verilir.\
\
**Kullanımı**

```
OLEObject.SetProp(
  Prop As String  ' Property
  Value As Bool   ' Property değeri
) As Object
```

**Parametreler**\
_Prop_\
OLE nesnesine geçirilmek istenen property\
_Value_\
OLE nesnesine geçirilmek istenen property'nin değeridir.\
Kullanılan property'e göre Value değişkeninin tipi Boolean, Anavariant veya Object olabilir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemli değildir.\
\
**Dikkat Edilecek Noktalar**\
Bu method ile OLE Automation nesnesine property değeri verilir. Kullanılan property'e göre Value değişkeninin tipi Boolean, Anavariant veya Object olabilir.

```
Dim font As Object
Dim myrange As Object
  .
  .
  .
  font:=myrange.GetProp("Font")
  font.SetProp("Name", "Arial")
  font.SetProp("Size", 16)
  font.SetProp("ColorIndex", 13)
```

Yukarıdaki örnekte, OLE nesnesindeki Font property'si alınarak, Name, Size ve ColerIndex propertylerine değer gönderilir.
