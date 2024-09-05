# AddItemEx

Bu method, tree view'a bitmap sırası ile birlikte item ekler.\
\
**Uygulandığı Nesneler**\
Tree view kontrolleri.\
\
**Kullanımı**

```
ControlObject.AddItemEx(
  ParentID  ' parent folder'ın  id'si
  Name      ' eklenecek item'ın ismi
  BitmapSıraNo      ' Item ile birlikte kullanılacak bitmap in sıranosu
)
```

**Parametreler**\
_ParentID_\
Item'ın eklendiği parent folderın id'si\
_Name_\
Eklenen Item'ın tree view da görünmesi istenilen ismi\
_BitmapSıraNo_\
Item ile birlikte kullanılacak bitmap in sıranosu\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri Number'dır.\
\
**Dikkat Edilecek Noktalar**\
Tree view kontrol nesnesinde bulunan bir folder'a item eklemeye yarayan bir methoddur. ParentId parametresinde Parent Folder'ın Id'si verilmelidir. Eğer ParentId parametresine 0 değeri verilirse, Root Item oluşacaktır. Bitmap sıranosu, SetImageList methodu ile verilen bitmap listesindeki sıranodur.
