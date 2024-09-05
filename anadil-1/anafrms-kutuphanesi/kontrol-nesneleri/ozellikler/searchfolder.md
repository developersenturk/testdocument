# SearchFolder

Bu property yardımıyla kontrol nesnesi içeriğinin veritabanından arama ile bulunması işleminde, aranılacak "Folder" belirlenmektedir.\
\
**Uygulandığı Nesneler**\
Edit-box kontrol nesnesi.\
\
**Uygulama Biçimi**\
Sadece yazılabilir bir property'dir.\
\
**Kullanımı**

```
ControlObject.SearchFolder As String
```

\
**Dikkat Edilecek Noktalar**\
Document-centric(belge merkezli) yapıya sahip olan Always®, belgeleri veritabanında saklamaktadır. Saklamanın yanında, belgelerin yönetimini ve organizasyonunu rahat bir şekilde yapabilmek de gerekmektedir. Bu işlemleri ise "Browser" dediğimiz Always® uygulaması gerçekleştirmektedir.\
\
Geliştirici, istediği taktirde kullanıcının işlerini daha da kolaylaştırmak için, Browser yardımıyla, bilgi girişi esnasında özel bir arama işlemi uygulayabilmektedir. Bu işlemse belgelerin kendi aralarında özel bağlantıları olduğunda uygulanmaktadır. Örneğin bir belge, bünyesinde başka bir belgenin sahip olduğu karakteristik bilgiye ihtiyaç duyduğunda; hedeflenen belgeye Browser yardımıyla ulaşılabilir ve özel bilgi bu sayede transfer edilebilir.\
\
Unutulmaması gereken başka bir husus da kontrolün .SearchFolder property değeri tanımlamak aslında daha sonra uygulanacak olan aynı kontrolün Search() metodu için ön adımdır. Search metodunun veya "drag\_drop" işlemi ile ilgili \<Formİsmi>\_\<Kontrolİsmi>\_Find event'inin çalışması bu property ile verilen, doğru Browser yol bilgisine bağlıdır.\
\
Bu property değerini belirlemek için en uygun yer ise formun \_Open event'i olmaktadır.
