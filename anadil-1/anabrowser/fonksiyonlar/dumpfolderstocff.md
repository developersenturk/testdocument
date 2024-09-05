# DumpFoldersToCFF

Tüm klasörleri CFF e dump eder.\
\
**Kullanımı**

```
Function DumpFoldersToCFF(
  CFF As Object
)As Bool
```

**Parametreler**\
_CFF_\
Tarayıcının dump edileceği CFF nesnesi. Daha önce yaratılmış olmalıdır\
\
**Geri Dönüş Değeri**\
TRUE/FALSE şeklindedir.\
\
**İlişkili başlıklar:**\
[AddBrowseFolderExLang](addbrowsefolderexlang.md)\
[CreateColDef](createcoldef.md)\
[GetFolderFromStructuredName](getfolderfromstructuredname.md)\
\
**Örnek**

```
      Dim hCFF As Object

      hCFF := CffCreate("BrowserDump")
      DumpFoldersToCFF( hCFF)
      hCFF.DumpCFF() ' c:\Always\CFF.TXT e bakabilirsiniz
```
