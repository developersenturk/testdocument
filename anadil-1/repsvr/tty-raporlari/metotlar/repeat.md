# Repeat

Bu method ile belirtilen bir text yada karakter tekrar edilir.\
\
**Kullanımı**

```
ReportObject.Repeat(
  NumRepeat As Number  'Tekrar sayısı
  Text As String       'Tekrar edilecek text
) As Bool
```

**Parametreler**\
\
_NumRepeat_\
Karakter yada textin tekrar sayısı\
\
_Text_\
Tekrar edilecek text ya da karakter\
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
  r.Write("Bu bir örnektir",20,TTYALIGN_LEFT)
  r.NextLine()
  r.Repeat("-",20)
```

Yukarıdaki örnekte yazdırılan text'in alt satırında "-" karakteri 20 kez tekrarlanmaktadır.
