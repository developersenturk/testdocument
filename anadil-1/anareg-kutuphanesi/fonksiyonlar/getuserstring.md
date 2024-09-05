# GetUserString

Bu fonksiyon Registry veri tabanında HKEY\_CURRENT\_USER altındaki bir anahtar saha içersindeki entry dahilindeki karakter bilginin değerini vermektedir.\
\
**Kullanımı**

```
Function GetUserString(
  Path As String 	' entry yol bilgisi
) As String
```

**Parametreler**\
_Path_\
HKEY\_CURRENT\_USER altında saklanan entry bilgisinin yol ifadesi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri öğrenmek istediğimiz entry bilginin içeriğidir.\
\
**Dikkat Edilecek Hususlar**\
Fonksiyonun kullanımı sonucunda, Registry veri tabanından okuma işlemi gerçekleşmektedir. Okunmakta olan entry "SOFTWARE/Model" altında yer alan anahtar saha içersindedir. Bu işlemse HKEY\_CURRENT\_USER altında "SOFTWARE/Model" yol bilgisinin ardından verdiğiniz entry'e ait yol bilgisi eklenmesiyle sağlanmaktadır. Yani okumakta olduğumuz karakter bilginin ait olduğu entry'nin tam yol bilgisi "SOFTWARE/Model/anahtar\_saha/entry" şeklindedir.\
\
Eğer verdiğiniz yol bilgisindeki entry mevcut değilse veya verdiğimiz yol bilgisi yanlışsa işlem sonunda karakter olarak boş string yani "" değeri elde edilmektedir.
