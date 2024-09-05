# GetObjectFromGlobalId

Bu fonksiyon nesnenin tanımlayıcısından yola çıkarak bir nesnenin kendisinin elde edilmesini sağlamaktadır.\
\
Kullanımı

```
Function GetObjectFromGlobalId(
  s_bilgi As String  ' nesneyi tanımlayan bilgi
)As Object
```

Parametreler\
_s\_bilgi_\
Always® altında bütün oluşturulan nesnelerin sahip olduğu unique tanımlayıcı bilgidir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri tanımlayıcıdan nesneyi oluşturan fonksiyonun verdiği sonuç nesnesidir.\
\
Dikkat Edilecek Hususlar\
Nesnelerin taşınabilmesi sayesinde, bir nesne herhangi bir Always® uygulamasından bir servise iletilebilmektedir. Hatta kaynak uygulamanın kendisi de bir servis olabilmektedir. Nesnelerin bu şekilde taşınması ile nesneye ilişkin her türlü işlem servis tarafından yapılabilmektedir.\
\
Nesnelerin servislere iletilmesi ise GlobalObjectID bilgilerinin parametre olarak taşınması şeklinde başarılmaktadır. Kaynak uygulamadan servise gelen bu bilgi, fonksiyon kullanımı ile tekrar bir nesneye dönüştürülmektedir. Bu nesne ise kaynak uygulamadaki nesnenin kendisidir. Bu sayede nesne, bir uygulamadan diğer bir servise taşınmış olmaktadır.
