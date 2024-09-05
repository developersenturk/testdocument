# Belge Nesneleri

Document-centric yapıya sahip olan Always® altındaki uygulamaların büyük çoğunluğu belgeler etrafında gerçekleşmektedir. Belgeler client-server ortamında, kullanıcının verdiği bilgilerin saklandığı nesneler olmaktadır. Kullanıcı açısından belgeler sahip oldukları form görüntüleri ile özdeşleşmiştirler. Geliştirici açısından ise belgeler formların üzerindeki kontrollerin içerdiği saf bilgilerdir.

Belge içerisindeki kontrol nesnelerinin sahip olduğu bilgilerin veritabanı ile sürekli bağlantısı bulunmakta, bunların bir şekilde veritabanından kullanıcıya veya kullanıcıdan veritabanına iletilmesi gerekmektedir. Belge nesne event'leri bu noktada kullanılmakta ve her türlü veritabanı-kullanıcı veri akışı bu event işletimleri sayesinde yapılmaktadır.

Yapılması gereken event işlemlerinin neler olması geliştiricinin sorumluluğundadır. Bir belge oluşturulurken yapılması gereken ilk iş belgenin yer alacağı modülün önceden oluşturulmasıdır. Modülün görevi belgeleri belli bir şekilde organize etmek ve Always®'e tanıtabilmektir. Her belge için ise bir modül kavramı, geliştiricilere tavsiye edilen uygulama şeklidir.

Daha sonra Modül ve Belge nesneleri etrafında gereken event kodları yazılacaktır. Bu event kodlarının yazılmasına ilişkin şablon şeklindeki bilgiler Imagine® altında Event-Wizard uygulaması yardımıyla kolaylıkla elde edilebilmektedir.
