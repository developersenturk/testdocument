# Dump (XML)

Bu method XML nesnesini, TEXT veya BINARY olarak, belirlenen dosyaya kaydeder.\
\
**Kullanımı**

```
XMLObject.Dump(
  szFileName As String   ' örneğin : c:\Always\test.jpg
  nFileType   As Number  ' 0 : TEXT     1 : BINARY
 ) As Bool
```

**Parametreler**\
_szFileName_\
XML nesnesinin dump edileceği dosya ismi.

```
nFileType
XML nesnesinin ve dosyanın tipi :
    0 : TEXT dosya   : txt, htm, html gibi  
    1 : BINARY dosya : jpg, bmp, zip, gif  gibi

```

\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlem başarılı ise TRUE, değilse FALSE ifadedir.\
