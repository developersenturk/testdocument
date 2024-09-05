# CurrentParent

Tree View nesnesinde, o anda geçerli olan üst folder'ın numarasını döndürür.\
\
**Uygulandığı Nesneler**\
Tree View nesnesi.\
\
**Kullanımı**

```
TreeViewControlObject.CurrentParent
```

\
**Dikkat Edilecek Noktalar**\
Tree View nesnesinde, bir folder'ın altına yeni bir folder eklemek istenildiğinde gerekli olacak, üst folder'ın Id'sini döndürür. Bu sayede eklenmek istenen yeni folder'a Parent Folder'ın Id'si geçirilerek o parent folder'ın altında yeni bir folder yaratmak mümkün olacaktır.
