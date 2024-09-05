# ValueDate

Bu property grid hücreleri nesnelerinin, Date(tarih) tipindeki bilgileri, kullanıcıya gösterimi(output) veya kullanıcıdan alımı(input) ile ilgili işlemleri düzenlemektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Hücre nesneleri.\
\
**Uygulama Biçimi**\
Hem okunabilir hem de yazılabilir bir property'dir.\
\
**Kullanımı**

```
GridCellObject.ValueDate As Date
```

**Dikkat Edilecek Noktalar**\
Property'nin görevi, Date şeklindeki ifadelerin, kullanıcı için hücre nesnesi tarafından içerik olarak kullanılmasını temin etmektir. Eğer input alınıyorsa bu özellik "okunabilir" olarak kullanılacak, diğer durumda kullanıcıya bir number değer gösterimi esnasında "yazılabilir" olarak uygulanacaktır.\
\
Eğer verilen ifade Date değilse, hücre nesnesi içerik olarak NULL gösterecektir. Ayrıca input olarak yapılan uygulamalarda da, kullanıcının herhangi bir etkide bulunmadığı kontrol nesneleri de, bu property içeriğinde NULL içeriğe sahip olacaklardır.
