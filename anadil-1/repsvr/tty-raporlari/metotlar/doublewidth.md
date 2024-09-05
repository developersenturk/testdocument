# DoubleWidth

Bu method raporda yazdırılan yazı tipinin genişletilmiş olmasını sağlar.\
\
**Kullanımı**

```
ReportObject.DoubleWidth() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
DoubleWidth methodu raporda yazdırılan yazı tipinin o satır için genişletilmiş olmasını sağlar. Eğer isteniyorsa, NextLine dan sonra tekrar DoubleWidth methodu tekrar kullanılmalıdır.\
\
**Örnek**

```
Dim r As report
  r.DoubleWidth()
  r.Write("1. örnek",20,TTYALIGN_LEFT)
  r.Space(2)
  r.Write("2. örnek",20,TTYALIGN_LEFT)
  r.NextLine()
  r.DoubleWidth()
  r.Write("1. örnek",20,TTYALIGN_LEFT)
  .
  .
```
