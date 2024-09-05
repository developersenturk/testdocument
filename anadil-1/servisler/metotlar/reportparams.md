# ReportParams

ReportParams Methodu, bir raporun parametrelerini belirleyebilmek için rapora ait parametreler penceresinin açılmasını sağlar.\
\
**Kullanımı**

```
AlwaysCallObject.ReportParams(
  ReportName As String  ' Rapor adı
) As Bool
```

**Parametreler**\
_ReportName_\
Parametre penceresi açılması istenen rapor adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
ReportParams Methodu, bir raporun parametrelerini belirleyebilmek için rapora ait parametreler penceresinin açılmasını sağlar.\
\
**Örnek**

```
Dim alw As Object
  alw:=GetAlwaysCallObject()
  alw.ReportParams("banka_listesi")
  alw.ReportPreview("banka_listesi")
```

Yukarıdaki örnekte Banka Listesi raporunun parametre penceresi açılmakta ve Parametre değerleri girildikten sonra Rapor öngörmeye alınmaktadır.
