# ReportSetup

ReportSetup Methodu, bir rapora ait kolon, satır ve karakter özelliklerinin belirtildiği yazıcı ayarları penceresini açar.\
\
**Kullanımı**

```
AlwaysCallObject.ReportSetup(
  ReportName As String  ' Rapor adı
) As Bool
```

**Parametreler**\
_ReportName_\
Setup ayarı yapılacak rapor adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
ReportSetup Methodu, bir rapora ait kolon, satır ve karakter özelliklerinin belirtildiği yazıcı ayarları penceresini açar.

```
Dim alw As Object
  alw.ReportSetup("banka_listesi")
  alw.ReportPreview("banka_listesi")
```
