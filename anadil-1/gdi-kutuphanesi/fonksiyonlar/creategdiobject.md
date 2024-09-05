# CreateGDIObject

Bu fonksiyon bir GDI nesnesi elde edilebilmesini sağlamaktadır.\
\
**Kullanımı**

```
Function CreateGDIObject() As Object
```

**Parametreler**\
Fonksiyonun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, içeriği GDI nesnesi olan nesnedir.\
\
**Dikkat Edilecek Hususlar**\
GDI kütüphanesinde uygulanmakta olan tek fonksiyondur.\
\
Bu fonksiyon ile yapılan işlem, GDI nesnesi oluşturmak suretiyle ICON ve BITMAP kullanımının geliştirilmekte olan Always® uygulamasında gerçekleştirebilmektir. Nesne ilk elde edildiğinde herhangi bir içeriğe sahip değildir.\
\
Daha sonra .LoadIcon() ve .LoadBitmap() metodları ile nesnenin içeriği belirlenecek ve uygulama içersinde ICON ve BITMAP'ler kullanılabilecektir. Metodların her kullanımı ile GDI nesnesinin daha önceki içeriği silinmekte ve yeni içerik ile değiştirilmektedir.\
\
ICON uygulamasında bu fonksiyonun kullanımı event dahilinde daha önceden yapıldığı için bu fonksiyonun kullanımı daha çok BITMAP'ler için uygulanmaktadır.
