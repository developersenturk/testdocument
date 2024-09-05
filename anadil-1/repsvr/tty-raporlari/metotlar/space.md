# Space

Rapor sayfasına boşluk karakterini ekler.\
\
**Kullanımı**

```
ReportObject.Space(
  NumSpaces  As Number  ' boşluk karakter sayısı
) As Bool
```

**Parametreler**\
_NumSpaces_\
Raporda verilecek boşluk karakter sayısı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Space Methodu, rapor sayfasına boşluk karakterini ekleme işlemi yapar.\
\
**Örnek**

```
Dim r As report
  r.Write("Bu bir örnektir")
  r.Space(2)
  r.Write("Bu da bir örnektir")	
```

Yukarıdaki örnekte yazdırılan iki text arasına 2 karakterlik boşluk eklenmiştir.
