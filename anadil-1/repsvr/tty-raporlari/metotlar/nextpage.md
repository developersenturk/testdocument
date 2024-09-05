# NextPage

Bu method raporda yeni bir sayfa açmayı sağlar.\
\
**Kullanımı**

```
ReportObject.NextPage() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
NextPage Methodu, raporda yeni bir sayfa açmayı sağlar.\
\
**Örnek**

```
Dim r As report
  r.Write("Bu bir örnektir",20,TTYALIGN_LEFT)
  r.NextPage()
  r..Write("Bu bir örnektir",20,TTYALIGN_LEFT)
```
