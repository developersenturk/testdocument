# GetFolderFromStructuredName

Bu fonksiyon klasör adından klasör Id elde edilmesini sağlar.\
\
**Kullanımı**

```
Function GetFolderFromStructuredName(
  FolderName As String
) As Number
```

**Parametreler**\
_FolderName_\
Klasörün adı veya kısa ismi.\
\
**Dikkat Edilecek Hususlar**\
Verilen klasör adı, klasör adların listesinde taranır, bulunamazsa, kısa isimler listesinde aranır.\
\
**Örnek**\
Aşağıdaki örnekte RootFolder ın klasör id si elde ediliyor ve Malzeme Yönetimi klasörü ana klasörün altına ekleniyor.

```
  
    cd:=CreateColDef() 
    AddBrowseFolderExLang(GetFolderFromStructuredName(""),#
                    "Malzeme Yönetimi",#
                    "",#
                    "",cd,FALSE,"",22000455)
```

**İlişkili başlıklar:**\
[AddBrowseFolderExLang](addbrowsefolderexlang.md)\
[CreateColDef](createcoldef.md)\
[AddFolderAlias](addfolderalias.md)\
