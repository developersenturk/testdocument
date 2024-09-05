# Adres @ Operatörü

Bu operatör herhangi bir fonksiyona parametre geçirme işlemlerinde kullanılmaktadır.\
**Kullanımı**\
Function Name(@değişken\_ismi)\
**Açıklama**\
Operatörün kullanımı ile bir fonksiyona gönderilen parametrenin fonksiyon içerisindeyken uğradığı değişimin geri dönüşte korunmasını sağlamaktadır. Eğer operatör kullanılmadan parametre geçirilecek olursa, parametrenin hedef fonksiyon içerisinde uğradığı değişimler geri dönüşte yok olmaktadır.\
\
**Örnek**

```
Function F()
 Dim sayı1 As Number
  ..
  sayı1:= 10
  Test(sayı1)
  MessageBox(STR(sayı1), #
  	"@ Operatörü kullanılmadan önce",MB_OK)
  Test(@sayı1)
  MessageBox(STR(sayı1), #
  	"@ Operatörü kullanılarak elde edilen değer", #
  			MB_OK)
EndFunction
Function Test(sayı1)
 Dim sayı2 As Number
  sayı2:= 11
  sayı1:= sayı1*sayı2
EndFunction
```

**Örnek Açıklaması**\
Yukarıdaki örnek uygulamada önce sayı1 değişkenine 10 değeri atama işlemi gerçekleştirilmektedir. Daha sonra ise @ operatörünü kullanmadan ve kullanarak iki defa ayrı ayrı Test() fonksiyonu çağrılmaktadır.\
Test() fonksiyonunun işletimi sırasında sayı1 değişkeni 110 değerini almaktadır fakat @ operatörü kullanılmaması durumunda parametrenin yeni değeri fonksiyondan geri dönüşte korunamamaktadır. Bu değişimler ve oluşan farklar MessageBox() fonksiyonu yardımıyla gösterilmeye çalışılmıştır.
