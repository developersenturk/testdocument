# RestoreUserKey

Bu fonksiyon, daha önce SaveUserKey fonksiyonu ile ilgili dosyaya saklanmış entryi, HKEY\_CURRENT\_USER üzerinde aynı entry bölümüne yeniden yükler.

**Kullanımı**

```
Function RestoreUserKey(
  RegPath As String,		' Restore edilecek registry path
  FileName As String		' Restore from filename
) As Boolean
```

**Parametreler**\
_RegPath_\
HKEY\_CURRENT\_USER altında saklanan entry bilgisinin yol ifadesi\
_FileName_\
Registry entry hiyerarşisinin alınacağı dosyayı belirtir.\
\
**Geri Dönüş Değeri**\
İşlemin başarılı olması durumunda TRUE, olmaması durumunda da FALSE döner.\
