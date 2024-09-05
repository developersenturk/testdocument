# CallMethod

Bu method, OLE Automation nesnesinden method çağırmaya yarar.\
\
**Kullanımı**

```
OLEObject.CallMethod(
  Name As String   ' Çağırılan Methodun adı.
  Value1 As Number  ' Parametre1 değeri (opsiyonel)
  Value2 As Number  ' Parametre2 değeri (opsiyonel)
  ...
  ValueN As Number  ' ParametreN değeri (opsiyonel)
) As String
```

**Parametreler**\
_Name_\
OLE Automation nesnesinde bulununan ve çağırılmak istenen methodun adı\
_Value_\
Çağırılmak istenen methodun parametre değeri veya degerleri. Ilgili methodun birden fazla parametresi olabilir. Bu durumda tüm parametreler verilebilir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri çağırılan methoda göre değişir.\
\
**Dikkat Edilecek Noktalar**\
Bu method, OLE Automation nesnesinden Method çağırmaya yarar. Çağırılan Methodun arguman sayısı bir ise CallMethod Methodunda parametre değeri vermek mümkündür. Ancak, argüman sayısının birden fazla olması durumunda parametre göndermek için AddParam Methodu kullanılmalıdır.

**Örnek**

```
Dim Range As Object
  .
  .
  .
  range.CallMethod("InsertAfter", "Hello World")
  veya
  range.AddParam("HelloWord")
  range.CallMethod("InsertAfter")
```

şeklinde kullanılabilir.
