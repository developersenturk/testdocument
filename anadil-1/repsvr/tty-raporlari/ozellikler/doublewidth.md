# DoubleWidth

DoubleWidth property'si bir sayfadaki yazı tipinin genişletilmiş olup olmadığını anlamaya yarar.\
\
**Kullanımı**

```
ReportObject.DoubleWidth As Bool
```

**Geri Dönüş Değeri**\
Geri dönüş değeri, booleandır.\
\
**Dikkat Edilecek Noktalar**\
DoubleWidth property'si bir sayfadaki yazı tipinin sıkıştırılmış olup olmadığını anlamaya yarar.\
\
**Örnek**

```
Dim r As Report
 
  if r.DoubleWidth= FALSE Then
    r.DoubleWidth()
    r.Write("Bu bir örnektir")
    .
    .
  Endif
```
