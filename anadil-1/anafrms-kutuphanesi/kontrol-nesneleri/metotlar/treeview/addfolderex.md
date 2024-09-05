# AddFolderEx

Bu method, tree view'a bitmap sıranosu ile birlikte folder ekler.\
\
Uygulandığı Nesneler\
Tree view kontrolleri.\
\
**Kullanımı**

```
ControlObject.AddFolderEx(
  ParentID  ' parent folder'ın  id'si
  Name      ' eklenecek folder'ın ismi
 BitmapSıraNo 'Folder için kullanılacak bitmap sıranosu
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

AddFolderEx(0, "RootFolder", 1) ' 1 : birinci sıradaki bitmap örnek olarak verilmiştir.\
\
şeklinde mümkündür.
