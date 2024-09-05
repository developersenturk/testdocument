# GetObjectGlobalId

Bu fonksiyon herhangi bir Anadil® nesnesine ilişkin küresel tanımlayıcı bilginin elde edilebilmesini sağlamaktadır.\
\
Kullanımı

```
Function GetObjectGlobaLID(
  h_nesne As Object  ' tanımlayıcısı alınacak nesne
)As String
```

Parametreler\
_h\_nesne_\
İki uygulama arasında taşınmak istenilen nesnenin kendisidir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri söz konusu kontrol nesnesi için ayırıcı nitelik taşımakta olan tanımlayıcı bilgidir.\
\
Dikkat Edilecek Hususlar\
Always® platformunun geliştiriciye sağladığı kolaylıklardan biri de geliştirilen Anadil kodlarının paylaşılabilir olmasıdır. Paylaşılan kodların uygulama sahası da servisler aracılığıyla yapılmaktadır. Servislerin bu şekilde başka bir uygulama tarafından çağrılması işleminde parametreler aracılığıyla bilgi transferi gerçekleştirilmektedir.\
\
Değişken bilgilerin taşınması yanında nesnelerin kaynak uygulamadan servislere geçirilmesi de bazı durumlarda gerekmekte olan bir işlemdir. Bu tür bir durumda nesnelerin uygulamalar arasında geçirilmesi için burada verilen ObjectID bilgisi kullanılmaktadır. Nesnenin taşınması kaynak uygulama tarafından taleb edildiğinden, bu fonksiyon da nesnenin bulunduğu kaynak uygulama tarafından kullanılmaktadır.\
\
ObjectID bilgisi String şeklinde nesneleri global olarak tanımlamakta olan bilgi olup, Always® bunun sayesinde bütün nesneleri unique bir şekilde ayırmaktadır. Bu bilginin parametre şeklinde geçirilmesi ile nesnenin kaynak uygulamadan, hedeflenen servis uygulamasına geçirilmesi sağlanmakta ve bu sayede nesne üzerinde her türlü işlem servis tarafından gerçekleştirilmektedir. Örnek olarak Modüller dahilindeki belge işlemlerinde, kontrol nesnelerine ilişkin bazı işlemlerin servisler aracılığla tek bir merkezden başarılması nesne taşınmasının güzel bir uygulamasıdır.
