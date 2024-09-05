# Condensed

Condensed property'si bir sayfadaki yazı tipinin sıkıştırılmış olup olmadığını anlamaya yarar.\
\
**Kullanımı**

```
ReportObject.Condensed As Bool
```

**Geri Dönüş Değeri**\
Geri dönüş değeri, booleandır.\
\
**Dikkat Edilecek Noktalar**\
Condensed property'si bir sayfadaki yazı tipinin sıkıştırılmış olup olmadığını anlamaya yarar.\
\
**Örnek**

```
Dim r As Report
 
  if r.Condensed = FALSE Then
    r.Condensed()
    r.Write("Bu bir örnektir")
    .
    .
  Endif
```
