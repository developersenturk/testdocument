# AddBrowseFolderExLang

Bu fonksiyon Browser a yeni bir klasör ekler.\
\
**Kullanımı**

```
Function AddBrowseFolderExLang(
  ParentFolder As Number,
  FolderName As String,
  ModuleId As String,
  DocTypeName As String,
  ColDef  As Object,
  bHidden As String,
  SortName As String,
  nResourceId As Number
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
_SortName_\
Aynı seviyedeki klasörlerin sıralamasını bu alan belirler.\
\
_nResourceId_\
Klasör adının resource kodu. Çok dilli kullanımlarda, taskbarda bulunan Locale değişikliği Always tarafından algılanır. Ilgili dile ait karşılıklar caption.dll kütüphanesinde mevcut ise, kullanıcıya görünen ifadeler ilgili dildeki ifadeler ile değiştirilir. Klasör isimleri de bu değişime girer. nResourceId bu amaçla kullanılır.\
\
**Geri Dönüş Değeri**\
Yaratılan klasörün id si geri döner.\
**Örnek**\


```
  
    cd:=CreateColDef() 
    AddBrowseFolderExLang(GetFolderFromStructuredName(""),#
                    "Malzeme Yönetimi",#
                    "",#
                    "",cd,FALSE,"12.00", 22000200)
```

**İlişkili başlıklar:**\
[CreateColDef](createcoldef.md)\
[AddFolderAlias](addfolderalias.md)\
[GetFolderFromStructuredName](getfolderfromstructuredname.md)\
