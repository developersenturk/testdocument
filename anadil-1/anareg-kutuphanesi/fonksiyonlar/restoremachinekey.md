# RestoreMachineKey

Bu fonksiyon, daha önce SaveMachineKey fonksiyonu ile ilgili dosyaya saklanmış entryi, HKEY\_LOCAL\_MACHINE üzerinde aynı entry üzerine yeniden yükler.

**Kullanımı**

```
Function RestoreMachineKey(
  RegPath As String,		' Restore edilecek registry path
  FileName As String		' Restore from filename
) As Boolean
```

**Parametreler**\
_RegPath_\
HKEY\_LOCAL\_MACHINE altında saklanan entry bilgisinin yol ifadesi\
_FileName_\
Registry entry hiyerarşisinin alınacağı dosyayı belirtir.\
\
**Geri Dönüş Değeri**\
İşlemin başarılı olması durumunda TRUE, olmaması durumunda da FALSE döner.\
