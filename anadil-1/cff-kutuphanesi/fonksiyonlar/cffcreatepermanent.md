# CFFCreatePermanent

Bu fonksiyon boş bir CFF nesnesi yaratır.\
\
**Kullanımı**

```
Function CFFCreatePermanent(
  CFFName As String  ' CFF nesnesinin ismi
)As Object
```

**Parametreler**\
_CFFName_\
Oluşturulacak olan CFF nesnesine verilen isim\
\
**Geri Dönüş Değeri**\
CFF Always® dahilinde nesne olarak ele alınmakta ve geri dönüş değeri olan nesne de bu CFF'in kendisi olmaktadır.\
\
**Dikkat Edilecek Hususlar**\
CFFCreatePermanent fonksiyonu ile yaratılan CFF global bir CFF'tir.\
\
CFF'e verdiğimiz isimse daha sonra yapacağımız referanslarda kullanılmaktadır.
