# CurLine

CurLine property'si o anda aktif olan satır numarasını almaya yarar.\
\
**Kullanımı**

```
ReportObject.CurLine As Number
```

**Geri Dönüş Değeri**\
Geri dönüş değeri aktif satırın numarasıdır.\
\
**Dikkat Edilecek Noktalar**\
CurLine property'si o anda aktif olan satır numarasını almaya yarar.\
\
**Örnek**

```
Dim r As report
Dim LineNum As Number
  LineNum := r.CurLine
  if LineNum = 0 Then
    Sayfabaşı()
  Endif
```
