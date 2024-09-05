# StartBrowser

Tarayıcıyı başlatır. Always in normal kullanıcı arayüzü ile başlatıldığı durumda bu fonksiyonun kullanılmasına gerek bulunmamaktadır. ALWRUN ile arka planda servislerin çalıştırılması durumunda, altyapının temel fonksiyonlarının (ConnectionManager, FolderManager, ColdefManager, UserFolderManager) başlatılmış olması gerekmektedir.\
\
**Kullanımı**

```
Function StartBrowser(
)As Bool
```

**Parametreler**\
Parametresi bulunmamaktadır.\
\
**Geri Dönüş Değeri**\
TRUE/FALSE şeklindedir.\
\
**İlişkili başlıklar:**\
[AddBrowseFolderExLang](addbrowsefolderexlang.md)\
[CreateColDef](createcoldef.md)\
[GetFolderFromStructuredName](getfolderfromstructuredname.md)\
\
**Örnek**\
\
Aşağıdaki örnekte TNM\_FIRMA\_KONTROL.SER servisinin StartService fonksiyonu ALWRUN (Batch modunda çalışan Always) ile başlatılıp başlatılmadığını kontrol ederek, eğer ALWRUN modunda ise StartBrowser ile tarayıcının çalışmasını sağlamaktadır.

```
Function StartService(Service As Object, Cci As Object) As Bool

  if GetEnvVar("WIZARD_RUNNING")="Yes" Then
    ' We are now running in browser wizard !
    StartBrowser()
    StartService:=True
    Return
  EndIf
  ... 
```
