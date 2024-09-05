# SetImageList

Bu method, tree view da kullanılabilecek bitmap listesini belirler.\
\
Uygulandığı Nesneler\
Tree view kontrolleri.\
\
**Kullanımı**

```
ControlObject.SetImageList(
  BitmapObject  
)
```

**Parametreler**\
_BitmapObject_\
Bitmap object from LoadBitmap\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri Boolean'dır.\
\
**Dikkat Edilecek Noktalar**\
Tree view kontrol nesnesine bitmap listesi eklemek için kullanılan bir methoddur.

Örnek

```
Bitmap file : TreeBitmap.bmp : 
Sıra numaraları : 0, 1, 2, 3, 4, 5
0 : Item icin bitmap
1: Folder Closed
2: Folder Expanded

Bmp:=CreateGDIObject()
Bmp.LoadBitmap("TreeBitmap") 'TreeBitmap load ediliyor
tr.SetImageList(Bmp) ' Bitmap i tr adindaki treeview a set eder

RootFolder:=tr.AddFolderEx(0, "Şirket", 1) ' treeview a 1 nolu bitmap i eşleştir
tr.Expand(RootFolder)
bExpandAll:=False
tr.CurrentSelection:=RootFolder
```
