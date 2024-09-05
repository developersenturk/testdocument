# Modül Nesneleri

Modül nesneleri Always® işletilebilir uygulamaları arasında yer alan 4 çeşit nesneden biridir. Yeni bir uygulamaya başlarken proje türü olarak seçilmekte olan bir türdür. Dosya şeklinde diğer Always® uygulamaları ile aynı dizinde yer almaktadır. Kendilerine ait özel kimlik bilgileri, Always run-time anında ayrılmalarını sağlamaktadır.

Bünyelerinde barındırdıkları belge nesneleri sayesinde form tabanlı document-centric uygulamaların gerçekleştirilmektedir. Bir modül birden fazla belge nesnesini içerebildiği halde, işlemleri karmaşıklıktan kurtarmak amacıyla bizim tavsiyemiz bir modül=bir belge yaklaşımıdır.

Always® ilk açıldığında bulunduğu dizin üzerindeki executable olarak gördüğü parçalarını, tarama işlemine tutmaktadır. Bu taramadan etkilenen nesnelerden biri de modül nesneleridir. Bu tarama işlemine ise register etme olayı denmektedir. Always® tarafından taranan ve register edilen modüller, sahip oldukları belgelerin de Always® tarafından tanınması ile fonksiyonel kimliklerini kazamaktadırlar. Böylece artık belge nesneleri kullanıcı tarafından işletilebilir olmaktadır.

Always® gerçek işletim esnasında, modül nesnelerini doğrudan yükleme yerine, talebe dayalı yükleme ve kullanma şeklinde bir mimariye sahiptir. Buna göre eğer modül nesnesinin sahip olduğu belge nesnelerinden biri kullanıcı tarafından çağrılacak olursa; öncelikle belgenin dahil olduğu modül nesnesi yüklenm ekte ve daha sonra da belge nesnesi Always® tarafından kullanıcı karşısına getirilmektedir. Aynı mantıkla, eğer bir modülün desteklediği en son belge nesnesi aktivasyonu, kullacı tarafından sonlandırılması halinde, ait olduğu modül nesnesi de Always® ortamından download edilmekte yani temizlenmektedir.
