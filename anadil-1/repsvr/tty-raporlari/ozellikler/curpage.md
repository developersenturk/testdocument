# CurPage

CurPage property'si o anda aktif olan raporun sayfa numarasını almaya yarar.\
\
**Kullanımı**

```
ReportObject.CurPage As Number
```

**Geri Dönüş Değeri**\
Geri dönüş değeri aktif sayfanın numarasıdır.\
\
**Dikkat Edilecek Noktalar**\
CurPage property'si o anda aktif olan raporun sayfa numarasını almaya yarar.\
\
**Örnek**

```
Dim r As report
Dim PageNum As Number
  PageNum := r.CurPage
```
