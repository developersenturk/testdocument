# AddFolder

Bu method, tree view'a folder ekler.\
\
Uygulandığı Nesneler\
Tree view kontrolleri.\
\
**Kullanımı**

```
ControlObject.AddFolder(
  ParentID  ' parent folder'ın  id'si
  Name      ' eklenecek folder'ın ismi
)
```

**Parametreler**\
_ParentID_\
Folder'ın eklendiği parent folderın id'si\
_Name_\
Eklenen folder'ın tree view da görünmesi istenilen ismi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri Number'dır.\
\
**Dikkat Edilecek Noktalar**\
Tree view kontrol nesnesine folder eklemek için kullanılan bir methoddur. ParentId'e 0 değeri geçirildiğinde, Root Folder oluşmaktadır. Bir başka deyişle root folder'ı oluşturmak ancak,

AddFolder(0, "RootFolder")\
\
şeklinde mümkündür.
