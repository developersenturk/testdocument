# GetMachineStringEx

Bu fonksiyon Registry veri tabanında HKEY\_LOCAL\_MACHINE altındaki bir anahtar saha içersindeki entry dahilindeki karakter bilginin değerini vermektedir.\
\
**Kullanımı**

```
Function GetMachineString(
  Path As String,		' entry yol bilgisi
  Default As String		' default değer
)As String
```

**Parametreler**\
_Path_\
HKEY\_LOCAL\_MACHINE altında saklanan entry bilgisinin yol ifadesi\
_Default_\
HKEY\_LOCAL\_MACHINE altında saklanan entry bilgisinin bulunamaması durumunda elde edilecek geri dönüş değeridir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri öğrenmek istediğimiz entry bilginin içeriğidir.\
\
**Dikkat Edilecek Hususlar**\
Fonksiyon kullanımı ile ilgili kurallar GetMachineString() fonksiyonu ile aynıdır. Aradaki fark ise verdiğiniz yol bilgisindeki entry mevcut değilse veya verdiğimiz yol bilgisi yanlışsa işlem sonunda string olarak elde edilecek değer Default parametresi ile verilen ifadedir.
