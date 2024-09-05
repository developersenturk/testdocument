# GotoLine

Bu method raporda yeni bir satıra gitmeyi sağlar.\
\
**Kullanımı**

```
ReportObject.GotoLine(
  LineIndex As Number  ' Gidilecek satır numarası
) As Bool
```

**Parametreler**\
_LineIndex_\
Gidilecek satır numarası\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
GotoLine Methodu, raporda istenen bir satıra erişebilmeyi sağlar.\
\
**Örnek**

```
Dim r As report
  r.Write("Bu bir örnektir",20,TTYALIGN_LEFT)
  r.GotoLine(10)
  r.Write("Bu bir örnektir",20,TTYALIGN_LEFT)
```
