# DEFAULT

Bu fonksiyon ANADİL ile DLL (Dynamic Link Library )' ler arasında bağlantı kurma işlemini gerçekleştirmektedir.\
\
Kullanımı

```
Function DEFAULT() As Boolean
```

Parametreler\
Fonksiyonun parametresi yoktur.\
\
Geri Dönüş Değeri\
Geri dönüş değeri Mantıksal bir değerdir. İşlemin başarılı olması halinde True, başarısızlık durumunda ise False değeri olarak geri dönmektedir.\
\
Dikkat Edilecek Hususlar\
Anadil® ile yazılan fonksiyonlarda bazı durumlarda DLL işletimine ihtiyaç duyulduğunda kullanılmakta olan fonksiyondur. DLL kullanımı için yapılması gereken ise hedeflenen DLL'in öncelikle Always executable içersine dahil edilmesi gerekmektedir. DLL alınırken ise static olarak dahil bir kerede fonksiyonların alınabileceği gibi, Run-Time anında her çalışma sırasında da DLL'e bağlanılması mümkündür.\
\
DLL fonksiyonları kullanımı içinse, Anadil® altında DLL'den export edilmiş olan fonksiyon isimleri ile aynı isimli Anadil® fonksiyonları tanımlanır ve bu fonksiyonların içinden de sadece Default() fonksiyonu çağrılır. Böylece Anadil® program kontrolü artık DLL fonksiyonuna geçer. Ne zaman DLL fonksiyonu işletimini bitirirse kontrol tekrar Anadil® 'e döner ve Anadil® işletimi kaldığı yerden devam eder.
