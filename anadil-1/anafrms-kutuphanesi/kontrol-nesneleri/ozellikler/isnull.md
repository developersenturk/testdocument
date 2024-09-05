# IsNull

Bu property kontrol nesnelerinin NULL bir içeriğe sahip olmalarını kontrol etmektedir.\
\
**Uygulandığı Nesneler**\
Edit-box kontrol nesnesi.\
\
**Uygulama Biçimi**\
Hem okunabilir hem de yazılabilir bir property'dir.\
\
**Kullanımı**

```
ControlObject.IsNull As Bool
```

\
**Dikkat Edilecek Noktalar**\
Veri giriş-çıkışı işlemlerinde kontrol nesnelerinin değerlerinin NULL olup olmadıkları bu özellik ile belirlenmektedir. Eğer bir kontrol nesnesi NULL içeriğe sahipse bu property'sinde True değerine sahip olacaktır. Ayrıca yazılabilir de olduğundan bir kontrolün içeriği de rahatlıkla Anadil® ile NULL olarak ifade edilebilir. Bununla beraber property değeri hiçbir zaman False değeri ile set edilemez. Yani geliştirici kontrol içeriğini doğrudan "NULL değildir" şeklinde belirleyemez.\
\
RDBMS yani ilişkisel veri tabanları ile çalışırken en önemli özelliklerden biri veritabanında saklanan bilgilerin istenildiğinde NULL şekilde ifade edilebilmeleridir. SQL Server tabanlı olarak çalışan ve bir uygulama geliştirme platformu olan Always® de NULL desteğini geliştirilere ve dolayısıyla kullanıcılarına sunmaktadır. Always® altında geliştirilen uygulamalar veri tabanında NULL verilere sahip olabilmektedirler. Always®'in de uygulama geliştirme dili olan Anadil® de NULL bilgi giriş-çıkışını geliştiriciye temin etmektedir.\
\
NULL bilgiler özel bir karakteristiğe sahiptirler. Ne sayı olarak sıfıra eşittirler, ne de string olarak boº stringtirler. Onlar sadece NULL olduklarından diğer veri tipleri ile karşılaştırmaları da anlamsızdır ve karşılaştırmanın sonucu da NULL olacaktır.
