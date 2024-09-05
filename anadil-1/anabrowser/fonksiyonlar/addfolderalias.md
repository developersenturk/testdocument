# AddFolderAlias

İlgili klasöre kısa isim verir.\
\
**Kullanımı**

```
Function AddFolderAlias(
  FolderID As Number
  Alias As String
)As Bool
```

**Parametreler**\
_FolderID_\
Kısa isim verilecek klasörün id si.\
\
_Alias_\
Kısa string ifade.\
\
**Geri Dönüş Değeri**\
TRUE/FALSE şeklindedir.\
\
**İlişkili başlıklar:**\
**İlişkili başlıklar:**\
[AddBrowseFolderExLang](addbrowsefolderexlang.md)\
[CreateColDef](createcoldef.md)\
[GetFolderFromStructuredName](getfolderfromstructuredname.md)\
\
**Örnek**\
\


```
    AddFolderAlias(AddBrowseFolderExLang(GetFolderFromStructuredName("/Malzeme Yönetimi/"),#
                    "Parti Tanımları",#
                    "MAL_Ana_Parti_Tanimi",#    
                    "MAL_Ana_Parti_Tanimi",cd,View,"1.10",22000201),"Parti Tanımları")
   
    AddFolderAlias(AddBrowseFolderExLang(GetFolderFromStructuredName("/Malzeme Yönetimi/"),#
                    "Malzeme Sınıfları",#
                    "",#
                    "",cd,TRUE, "1.11",22000202),"Malzeme Sınıfları")
```
