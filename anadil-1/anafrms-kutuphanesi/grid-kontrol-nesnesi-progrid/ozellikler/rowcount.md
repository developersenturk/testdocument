# RowCount

Bu property, grid kontrol nesnesinin sahip olduğu satır sayısını içermektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Uygulama Biçimi**\
Sadece okunabilir bir özelliktir.\
\
**Kullanımı**

```
MyGridObject.RowCount As Number
```

\
**Dikkat Edilecek Noktalar**\
Grid nesnelerinin ilk oluşturulmalarından itibaren sahip oldukları satır sayıları bulunmaktadır. Bu sayı MyGrid.Init() metod uygulaması ile verilen başlangıç satır sayısı olmaktadır.\
\
Grid nesnesinin sahip olduğu satırların tümü kullanıldıktan sonra ise yine MyGrid.Init() metodu ile verilen genişleme satır sayısı kadar Grid kendini genişletmektedir. Genişleme sonrası bu property içeriği o andaki toplam satır sayısı olmaktadır.
