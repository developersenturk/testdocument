# Preview

Preview property'si çalışmakta olan raporun öngörme(preview) olup olmadığını anlamaya yarar.\
\
**Kullanımı**

```
ReportObject.Preview As Bool
```

**Geri Dönüş Değeri**\
Geri dönüş değeri, booleandır.\
\
**Dikkat Edilecek Noktalar**\
Preview property'si çalışmakta olan raporun öngörme(preview) olup olmadığını anlamaya yarar.\
\
**Örnek**

```
  Dim r As Report
 
  if (r.Preview) Then
       outm("Rapor su an öngörme modundadır")
  else
       outm("Rapor su an print modundadır")
  Endif
```
