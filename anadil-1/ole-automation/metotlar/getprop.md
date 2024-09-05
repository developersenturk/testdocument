# GetProp

Bu method, OLE Automation nesnesinden property çağırmaya yarar.\
\
**Kullanımı**

```
OLEObject.GetProp(
  Name As String   ' Çağırılan Property adı.
  Value As Number  ' Parametre değeri
) As String
```

**Parametreler**\
_Name_\
OLE Automation nesnesinde bulununan ve çağırılmak istenen property adı\
_Value_\
Çağırılmak istenen property'nin parametre değeri\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri çağırılan property'e göre değişir.\
\
**Dikkat Edilecek Noktalar**\
Bu method, OLE Automation nesnesinden Property çağırmaya yarar. Çağırılan Property'nin arguman sayısı bir ise GetProp Methodunda parametre değeri vermek mümkündür. Ancak, argüman sayısının birden fazla olması durumunda parametre göndermek için AddParam Methodu kullanılmalıdır.\
Örnek

```
Dim myrange As Object
Dim Font As Object
  .
  .
  .
   font:=myrange.GetProp("Font")
   font.SetProp("Name", "Arial")
  veya
  range.AddParam("HelloWord")
  range.CallMethod("InsertAfter")
```

şeklinde kullanılabilir.
