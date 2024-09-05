# ItalicOn - ItalicOff

Bu metodlar raporda yazdırılan yazı tipinin yatay olup olmamasını sağlar.\
\
**Kullanımı**

```
ReportObject.ItalicOn() As Bool
ReportObject.ItalicOff() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
ItalicOn metodu raporda yazdırılan yazı tipinin o satır için yatık olmasını sağlar. Eğer vazgeçilirse ItalicOff metodu kullanılmalıdır.\
\
**Örnek**

```
Dim r As report
  r.ItalicOn()
  r.Write("1. örnek",20,TTYALIGN_LEFT)
  r.Space(2)
  r.Write("2. örnek",20,TTYALIGN_LEFT)
  r.NextLine()
  r.ItalicOff()
  r.Write("1. örnek",20,TTYALIGN_LEFT)
  .
  .
```
