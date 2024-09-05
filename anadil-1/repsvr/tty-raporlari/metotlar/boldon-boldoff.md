# BoldOn - BoldOff

Bu metodlar raporda yazdırılan yazı tipinin kalın olup olmamasını sağlar.\
\
**Kullanımı**

```
ReportObject.BoldOn() As Bool
ReportObject.BoldOff() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
BoldOn metodu raporda yazdırılan yazı tipinin o satır için kalın olmasını sağlar. Eğer vazgeçilirse BoldOff metodu kullanılmalıdır.\
\
**Örnek**

```
Dim r As report
  r.BoldOn()
  r.Write("1. örnek",20,TTYALIGN_LEFT)
  r.Space(2)
  r.Write("2. örnek",20,TTYALIGN_LEFT)
  r.NextLine()
  r.BoldOff()
  r.Write("1. örnek",20,TTYALIGN_LEFT)
  .
  .
```
