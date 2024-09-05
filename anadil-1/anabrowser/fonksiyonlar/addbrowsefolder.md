# AddBrowseFolder

Bu fonksiyon Browser a yeni bir klasör ekler.\
\
**Kullanımı**

```
Function AddBrowseFolder(
  ParentFolder As Number,
  FolderName As String,
  ModuleId As String,
  DocTypeName As String,
  ColDef  As Object,
  bHidden As String
) As Number
```

**Parametreler**\
_ParentFolder_\
Klasörün bağlı olacağı üst klasörün klasör id si\
\
_FolderName_\
Yaratılan klasörün adı\
\
_ModuleId_\
Klasörde listelenecek belgelerin modül id si.\
\
_DocTypeName_\
Klasörde listelenecek belgelerin doküman tip Id si.\
\
_ColDef_\
Ilgili Kolon Tanım Nesnesi.\
\
_bHidden_\
Klasörün gizli olup olmadığını belirtir.\
\
**Geri Dönüş Değeri**\
Yaratılan klasörün id si geri döner.\
\
**Dikkat Edilecek Hususlar**\
AddBrowseFolderExLang isimli fonksiyonu kullanmanız tavsiye edilir.\
\
**Örnek**\


```
  
    cd:=CreateColDef() 
    AddBrowseFolder(GetFolderFromStructuredName(""),#
                    "Malzeme Yönetimi",#
                    "",#
                    "",cd,FALSE)
```

**İlişkili başlıklar:**\
[AddBrowseFolderExLang](addbrowsefolderexlang.md)\
[CreateColDef](createcoldef.md)\
[AddFolderAlias](addfolderalias.md)\
[GetFolderFromStructuredName](getfolderfromstructuredname.md)\
