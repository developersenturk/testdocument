# CFFCreate

Bu fonksiyon bir CFF nesnesinin oluşturulmasını sağlamaktadır.\
\
**Kullanımı**

```
Function CFFCreate(
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
CFF nesnelerinin kullanılmadan önce mutlaka oluşturulmaları gerekmektedir. Fakat döküman işlemlerinde kullanılan, dökümana ait CFF hazır olarak event dahilinde, parametre olarak gelmektedir. Bu yüzden de çoğu zaman CFF yaratılması işlemi otomatik olarak gerçekleşecektir.\
\
CFF'e verdiğimiz isimse daha sonra yapacağımız referanslarda kullanılmaktadır.
