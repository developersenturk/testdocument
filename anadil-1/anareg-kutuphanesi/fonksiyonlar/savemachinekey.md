# SaveMachineKey

Bu fonksiyon HKEY\_LOCAL\_MACHINE üzerinde verilen registry tree yi verilen dosyaya kaydeder. Özellikle kullanıcıların basılı form, rapor ve browser ayarlarının saklanabilmesi ve yeniden yüklenebilmesi için geliştirilmiştir. Yardımcı programlar bölümünde bu fonksiyonu kullanan bir utility bulunmaktadır.

**Kullanımı**

```
Function SaveMachineKey(
  RegPath As String,		' Registry path
  FileName As String		' Saklanacak filename
) As Boolean
```

**Parametreler**\
_RegPath_\
HKEY\_LOCAL\_MACHINE altında saklanan entry bilgisinin yol ifadesi\
_FileName_\
Registry entry hiyerarşisinin saklanacağı dosyayı belirtir.\
\
**Geri Dönüş Değeri**\
İşlemin başarılı olması durumunda TRUE, olmaması durumunda da FALSE döner.\
\
**Dikkat Edilecek Hususlar**\
Resmi belgelerin printer ayarlarının registrydeki entry hiyerarşisinin, periyodik olarak ilgili filename ile yedeklenmesi tavsiye edilir.\
