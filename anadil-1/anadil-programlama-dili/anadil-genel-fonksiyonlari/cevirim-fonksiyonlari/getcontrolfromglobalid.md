# GetControlFromGlobalId

Bu fonksiyon herhangi bir kontrol nesnesi ile ilgili GlobalID değerinini vermek suretiyle bu nesnenin tanımlandığı kod sınırları dışında; kullanılabilmesini sağlamaktadır.\
\
Kullanımı

```
Function GetControlFromGlobalId(
  GlobalId As String  ' kontrol nesnesi ID değeri
)As Object
```

Parametreler\
_GlobalId_\
Control nesnesine ulaşabilmek için gerekli olan tanımlama bilgisi\
\
Geri Dönüş Değeri\
Geri dönüş değeri control nesnesinin kendisini ifade etmekte olan nesnedir. Bu nesne sayesinde control'e ilişkin her türlü işlem karşı tarafta yapılabilmektedir.\
\
Dikkat Edilecek Noktalar\
Bir kontrolün ait olduğu Anadil® kodu dışarsından da ulaşımı uygulama geliştirici açısından oldukça büyük kolaylıklar sağlamaktadır. Bu işlemi başarı ile uygulayabilmek için, mesela bir servis içersinden control'e ulaşmak istiyorsak; servis çağrılması ile ilgili işlemleri başarılı olarak tamamlayabilmememiz gerekmektedir.\
\
Ayrıca bu fonksiyon kullanımı diğer Anadil® nesnelerinin, bir uygulamadan diğerine taşınması sırasında da uygulanmaktadır. Yani başka nesneler mesela bir form nesnesi veya grid nesnesi de servisler aracılığıyla taşınabilmektedir.\
\
Bu fonksiyonun burada tanıtımının verilmesinin amacı, özellikle kontrol nesnelerinin uygulamalar arasında taşınma gereksinimidir.
