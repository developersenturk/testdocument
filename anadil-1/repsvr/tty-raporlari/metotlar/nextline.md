# NextLine

Rapor sayfasında alt satıra geçmeyi sağlar.\
\
**Kullanımı**

```
ReportObject.NextLine() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
NextLine Methodu, rapor sayfasında bir sonraki satıra geçmeyi sağlar.\
\
**Örnek**

```
Dim r As report
  r.Write("Bu bir örnektir")
  r.NextLine()
  r.Write("Bu da bir örnektir")	
```

Yukarıdaki örnekte yazdırılan iki text farklı iki satırda yer almaktadır.
