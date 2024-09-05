# Normal

Normal property'si bir sayfadaki yazı tipinin Normal olup olmadığını anlamaya yarar.\
\
**Kullanımı**

```
ReportObject.Normal As Bool
```

**Geri Dönüş Değeri**\
Geri dönüş değeri, booleandır.\
\
**Dikkat Edilecek Noktalar**\
Normal property'si bir sayfadaki yazı tipinin Normal olup olmadığını anlamaya yarar.\
\
**Örnek**

```
Dim r As Report
 
  if r.Normal= FALSE Then
    r.Normal()
    r.Write("Bu bir örnektir")
    .
    .
  Endif
```
