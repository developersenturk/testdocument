# AddItem

Bu method, tree view'a item ekler.\
\
Uygulandığı Nesneler\
Tree view kontrolleri.\
\
**Kullanımı**

```
ControlObject.AddItem(
  ParentID  ' parent folder'ın  id'si
  Name      ' eklenecek item'ın ismi
)
```

**Parametreler**\
_ParentID_\
Item'ın eklendiği parent folderın id'si\
_Name_\
Eklenen Item'ın tree view da görünmesi istenilen ismi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri Number'dır.\
\
**Dikkat Edilecek Noktalar**\
Tree view kontrol nesnesinde bulunan bir folder'a item eklemeye yarayan bir methoddur. ParentId parametresinde Parent Folder'ın Id'si verilmelidir. Eğer ParentId parametresine 0 in değeri verilirse, Rool Item oluşacaktır.
