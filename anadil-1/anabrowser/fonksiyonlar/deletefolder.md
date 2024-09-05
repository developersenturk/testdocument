# DeleteFolder

İlgili klasörü yok eder.\
\
**Kullanımı**

```
Function DeleteFolder(
  FolderID As Number
)As Bool
```

**Parametreler**\
_FolderID_\
Yok edilecek klasörün id si.\
\
**Geri Dönüş Değeri**\
TRUE/FALSE şeklindedir.\
\
**İlişkili başlıklar:**\
[AddBrowseFolderExLang](addbrowsefolderexlang.md)\
[CreateColDef](createcoldef.md)\
[GetFolderFromStructuredName](getfolderfromstructuredname.md)\
\
Örnek\
\


```
    DeleteFolder(GetFolderFromStructuredName("Parti Tanımları")
```
