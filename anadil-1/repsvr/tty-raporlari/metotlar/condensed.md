# Condensed

Bu method raporda yazdırılan yazı tipinin sıkıştırılmış olmasını sağlar.\
\
**Kullanımı**

```
ReportObject.Condensed() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Condensed methodu raporda yazdırılan yazı tipinin o satır için sıkıştırılmış olmasını sağlar. Eğer isteniyorsa, NextLine dan sonra tekrar Condensed methodu kullanılmalıdır.\
\
**Örnek**

```
Dim r As report
  r.Condensed()
  r.Write("1. örnek",20,TTYALIGN_LEFT)
  r.Space(2)
  r.Write("2. örnek",20,TTYALIGN_LEFT)
  r.NextLine()
  r.Condensed()
  r.Write("1. örnek",20,TTYALIGN_LEFT)
  .
  .
```
