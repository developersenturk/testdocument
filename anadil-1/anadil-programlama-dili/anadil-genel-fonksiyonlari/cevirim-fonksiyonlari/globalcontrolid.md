# GlobalControlId

Bu property kontrol nesnelerinin tanımlayıcısıdır.\
\
Uygulandığı Nesneler\
Bütün kontrol nesneleri.\
\
Uygulama Biçimi\
Sadece okunabilir bir property'dir.\
\
Kullanımı

```
ControlObject.GlobalControlId As String
```

\
Dikkat Edilecek Noktalar\
Her kontrol nesnesinin sahip olduğu bu özellik, kendisi için Always® dahilinde ayırıcı bir tanımlayıcı olarak hizmet vermektedir. Yani bütün Always® dahilinde yer alan her kontrol nesnesinin unique bir GlobaLiD değeri bulunmaktadır.\
\
GlobalControlId değerleri, string formatında olup, bunlar sayesinde her kontrol nesnesi kullanıldığı veya tanımlandığı Anadil® program kodu sınırlarını aşabilmektedir.\
\
Bir uygulama geliştirme platformu olan Always® ve dahilindeki Anadil® kodunda hiçbir zaman bağımsız parçaların sahip olduğu kontrol nesneleri, direkt olarak bir parçadan diğer parçaya taşınamamaktadır. Bu parçalar örneğin bir servis ile bir modül olabilir.\
\
Kontrol nesnelerini doğrudan taşımak yerine onların GlobalControLiD değerleri sayesinde, onların karşı tarafta kullanılabilmesini sağlanmakta, kontrol nesnelerine ilişkin her türlü işlem karşı tarafta da yapılabilmektedir.\
\
Bu tür bir işlem nerede yararlı olabilir diyorsanız eğer; örnek olarak sürekli aynı şekilde yapılan işlerin bir tek servis ile aynı yerden yapılabilmesini verebiliriz. Sürekli aynı kodu tekrar tekrar yazmaktansa, tekrarlanan kodu bir defada bir servis içersinde yazıp, ihtiyacımız olan yerlerde bu servisin çağrılması suretiyle işlemi yapmak, uygulama geliştirici açısından da işleri oldukça kolaylaştıracaktır.
