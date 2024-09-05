# GetUserNumber

Bu fonksiyon Registry veri tabanında HKEY\_CURRENT\_USER altındaki bir anahtar saha içersindeki entry sayı bilgisinin değerini vermektedir.\
\
**Kullanımı**

```
Function GetUserNumber(
  Path As String 	' entry yol bilgisi
)As Number
```

\
**Parametreler**\
_Path_\
HKEY\_CURRENT\_USER altında saklanan entry bilgisinin yol ifadesi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri öğrenmek istediğimiz entry bilginin içeriğidir.\
\
**Dikkat Edilecek Hususlar**\
Fonksiyonun kullanımı sonucunda, Registry veri tabanından okuma işlemi gerçekleşmektedir. Okunmakta olan entry'ler "SOFTWARE/Model" altında yer alan anahtar sahalar içersindedir. Bu işlemse HKEY\_CURRENT\_USER altında "SOFTWARE/Model" yol bilgisinin ardından verdiğiniz entry'e ait yol bilgisi eklenmesiyle sağlanmaktadır. Yani okumakta olduğumuz sayının ait olduğu entry'nin tam yol bilgisi

"SOFTWARE/Model/anahtar\_saha/entry" şeklindedir.\
\
Eğer verdiğiniz yol bilgisindeki entry mevcut değilse veya verdiğimiz yol bilgisi yanlışsa işlem sonunda sayı olarak 0 değeri elde edilmektedir.
