# ValueStr

Bu property kontrol nesnelerinin, string tipindeki bilgileri, kullanıcıya gösterimi(output) veya kullanıcıdan alımı(input) ile ilgili işlemleri düzenlemektedir.\
\
**Uygulandığı Nesneler**\
Edit-box ve Static kontrol nesneleri.\
\
**Uygulama Biçimi**\
Hem okunabilir hem de yazılabilir bir property'dir.\
\
**Kullanımı**

```
ControlObject.ValueStr As String
```

**Dikkat Edilecek Noktalar**\
Form üzerinde yerleştirilen bütün kontrol nesneleri, kullanıcıdan bir input değeri alabilmek veya bir output değerini son kullanıcıya bildirmek işlevindedir. Yani kullanıcı ya bir bilgi verecektir ya da bir bilgi alacaktır.\
\
.ValueStr property'sinin görevi, string şeklindeki ifadelerin, kullanıcı için kontrol nesnesi tarafından içerik olarak kullanılmasını temin etmektir. Eğer input alınıyorsa bu özellik "okunabilir" olarak kullanılacak, diğer durumda kullanıcıya bir string değer gösterimi esnasında "yazılabilir" olarak uygulanacaktır.\
\
Eğer verilen ifade string değilse, kontrol nesnesi içerik olarak NULL gösterecektir. Ayrıca input olarak yapılan uygulamalarda da, kullanıcının herhangi bir etkide bulunmadığı kontrol nesneleri de, bu property içeriğinde NULL içeriğe sahip olacaklardır.
