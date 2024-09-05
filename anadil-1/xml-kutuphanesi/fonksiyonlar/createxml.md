# CreateXML

Bu fonksiyon bir XML nesnesi elde edilebilmesini sağlamaktadır.\
\
**Kullanımı**

```
Function CreateXML() As Object
```

**Parametreler**\
Fonksiyonun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, içeriği XML nesnesi olan nesnedir.\
\
**Dikkat Edilecek Hususlar**\
XML kütüphanesinde uygulanmakta olan tek fonksiyondur.\
\
Bu fonksiyon ile yapılan işlem, her türlü XML dökümanının ifade edilebileceği ve işleme sokulabileceği bir Anadil® XML nesnesi oluşturmaktır. Nesne ilk elde edildiğinde herhangi bir içeriğe sahip değildir.\
\
Daha sonra .Append() ve .AppendXML() metodları ile nesnenin içeriği oluşturulacak ve uygulama içerisinde kullanılabilecektir. Metodların her kullanımı ile XML nesnesinin ihtiyaç duyduğu memory dinamik olarak genişletilmektedir.\
