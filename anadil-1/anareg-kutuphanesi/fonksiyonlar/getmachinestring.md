# GetMachineString

Bu fonksiyon Registry veri tabanında HKEY\_LOCAL\_MACHINE altındaki bir anahtar saha içersindeki entry dahilindeki karakter bilginin değerini vermektedir.\
\
**Kullanımı**

```
Function GetMachineString(
  Path As String 	' entry yol bilgisi
)As String
```

**Parametreler**\
_Path_\
HKEY\_LOCAL\_MACHINE altında saklanan entry bilgisinin yol ifadesi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri öğrenmek istediğimiz entry bilginin içeriğidir.\
\
**Dikkat Edilecek Hususlar**\
Fonksiyonun kullanımı sonucunda, Registry veri tabanından okuma işlemi gerçekleşmektedir. Okunmakta olan entry "SOFTWARE/Model" altında yer alan anahtar saha içersindedir. Bu işlemse HKEY\_LOCAL\_MACHINE altında "SOFTWARE/Model" yol bilgisinin ardından verdiğiniz entry'e ait yol bilgisi eklenmesiyle sağlanmaktadır. Yani okumakta olduğumuz karakter bilginin ait olduğu entry'nin tam yol bilgisi

"SOFTWARE/Model/anahtar\_saha/entry" şeklindedir.\
\
Eğer verdiğiniz yol bilgisindeki entry mevcut değilse veya verdiğimiz yol bilgisi yanlışsa işlem sonunda karakter olarak boş string yani "" değeri elde edilmektedir.
