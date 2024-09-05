# GetMachineNumberEx

Bu fonksiyon Registry veri tabanında HKEY\_LOCAL\_MACHINE altındaki bir anahtar saha içersindeki entry sayı bilgisinin değerini vermektedir.\
\
**Kullanımı**

```
Function GetMachineNumber(
  Path As String,	' entry yol bilgisi
  Default As Number	' default değer
)As Number
```

**Parametreler**\
_Path_\
HKEY\_LOCAL\_MACHINE altında saklanan entry bilgisinin yol ifadesi\
_Default_\
HKEY\_LOCAL\_MACHINE altında saklanan entry bilgisinin bulunamaması durumunda fonksiyonun vereceği geri dönüş değeridir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri öğrenmek istediğimiz entry bilginin içeriğidir.\
\
**Dikkat Edilecek Hususlar**\
Fonksiyon kullanımı ile ilgili kurallar GetMachineNumber() fonksiyonu ile aynıdır. Aradaki fark ise verdiğiniz yol bilgisindeki entry mevcut değilse veya verdiğimiz yol bilgisi yanlışsa işlem sonunda sayı olarak elde edilecek değer Default parametresi ile verilen değerdir.
