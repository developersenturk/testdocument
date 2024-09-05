# GetCurrentSelection

Tree View nesnesinde, o anda seçili olan folder'ın numarasını döndürür.\
\
**Uygulandığı Nesneler**\
Tree View nesnesi.\
\
**Kullanımı**

```
TreeViewControlObject.GetCurrentSelection
```

**Dikkat Edilecek Noktalar**\
Tree View nesnesinde, seçilmiş olan bir folder'ın altına yeni bir folder veya item eklemek istenildiğinde gerekli olacak, seçilmiş folder'ın Id'sini döndürür. Bu sayede eklenmek istenen yeni folder'a seçilmiş olan folder'ın Id'si geçirilerek seçili folder'ın altında yeni bir folder veya Item yaratmak mümkün olacaktır.
