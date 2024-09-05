# SearchFolder

Bu property grid sütunu hücrelerin için Browser'dan yapılacak bilgi transferinde kullanılacak Folder(klasör) tanımlanmasını sağlamaktadır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir ve yazılabilir bir özelliktir.\
\
**Kullanımı**

```
MyGridColObject.SearchFolder As String
```

\
**Dikkat Edilecek Noktalar**\
Document-centric(belge merkezli) yapıya sahip olan Always®, belgeleri veritabanında saklamaktadır. Saklamanın yanında, belgelerin yönetimini ve organizasyonunu rahat bir şekilde yapabilmek de gerekmektedir. Bu işlemleri ise "Browser" dediğimiz Always® uygulaması gerçekleştirmektedir.\
\
Geliştirici, istediği taktirde kullanıcının işlerini daha da kolaylaştırmak için, Browser yardımıyla, bilgi girişi esnasında özel bir arama işlemi uygulayabilmektedir. Bu işlemse belgelerin kendi aralarında özel bağlantıları olduğunda uygulanmaktadır. Örneğin bir belge, bünyesinde başka bir belgenin sahip olduğu karakteristik bilgiye ihtiyaç duyduğunda; hedeflenen belgeye Browser yardımıyla ulaşılabilir ve özel bilgi bu sayede transfer edilebilir.\
\
Grid sütunlarında yer alan hücre içeriklerinin doldurulması sırasında istenildiğinde, Browser üzerinden birden fazla belge detayına ilişkin bilgi drag-drop(sürükle-bırak) işlemi ile yapılabilmektedir. Bunun anlamı ise birden fazla grid satırı bilgisinin aynı anda Browser'dan alınabilmesi demektir.
