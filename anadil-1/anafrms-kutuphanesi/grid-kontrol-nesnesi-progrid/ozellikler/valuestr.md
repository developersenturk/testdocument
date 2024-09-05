# ValueStr

Bu property grid hücreleri nesnelerinin, string tipindeki bilgileri, kullanıcıya gösterimi(output) veya kullanıcıdan alımı(input) ile ilgili işlemleri düzenlemektedir.\
\
**Uygulandığı Nesneler**\
\
Grid kontrol nesnesi bünyesinde yer alan Grid Hücre nesneleri.\
\
**Uygulama Biçimi**\
Hem okunabilir hem de yazılabilir bir property'dir.\
\
**Kullanımı**

```
GridCellObject.ValueStr As String
```

**Dikkat Edilecek Noktalar**\
Property'nin görevi, string şeklindeki ifadelerin, kullanıcı için hücre nesnesi tarafından içerik olarak kullanılmasını temin etmektir. Eğer input alınıyorsa bu özellik "okunabilir" olarak kullanılacak, diğer durumda kullanıcıya bir String değer gösterimi esnasında "yazılabilir" olarak uygulanacaktır.\
\
Eğer verilen ifade string değilse, kontrol nesnesi içerik olarak NULL gösterecektir. Ayrıca input olarak yapılan uygulamalarda da, kullanıcının herhangi bir etkide bulunmadığı hücre nesneleri de, bu property içeriğinde NULL içeriğe sahip olacaklardır. Tabi ki NULL input bilgi alınması ise, hücrenin dahil olduğu grid sütunu nesnesinin .AllowNull property değerine bağlıdır.
