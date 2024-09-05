# ShowServiceCallErrors

ShowServiceCallErrors Methodu, CallServiceTransacted methodu ile biriktirilmiş olan SQL hatalarını bir dialogbox içerisinde gösterir.\
\
**Kullanımı**

```
ServiceObject.ShowServiceCallErrors() As Bool
```

**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
ShowServiceCallError Methodu, CallServiceTransacted methodu ile biriktirilmiş olan SQL hatalarını bir dialogbox içerisinde gösterir.\
\
**Örnek**

```
Dim srv As Object
  if Not srv.CallServiceTransacted() Then
    srv.ShowServiceCallErrors()
  Endif
```

Yukarıdaki örnekte SQL'dan dönen hatalar, bir Dialog box içerisine yazdırılmaktadır.
