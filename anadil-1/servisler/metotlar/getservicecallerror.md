# GetServiceCallError

GetServiceCallError Methodu, CallServiceTransacted ile biriktirilmiş olan SQL hatalarını teker teker almaya yarar.\
\
**Kullanımı**

```
ServiceObject.CallServiceCallError(
  ErrorIndex  As Number  'Hata index numarası
) As String
```

**Geri Dönüş Değeri**\
Geri dönüş değeri stringdir.\
\
**Dikkat Edilecek Noktalar**\
GetServiceCallError Methodu, CallServiceTransacted ile biriktirilmiş olan SQL hatalarını teker teker almaya yarar.\
\
**Örnek**

```
Dim srv As Object
Dim numerr As Number
Dim errstr As String
  if not srv.CallServiceTransacted() Then
    numerr:=1
    While True
      errstr:=srv.GetServiceCallError(numerr)
      if errstr="" Then
        Exit
      EndIf
      f.results.AddToList(errstr)
      numerr:=numerr+1   
    Wend
  Endif
```

Yukarıdaki örnekte SQL'dan dönen hatalar, bir List box içerisine yazdırılmaktadır.
