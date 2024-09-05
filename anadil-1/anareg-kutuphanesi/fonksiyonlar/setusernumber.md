# SetUserNumber

Bu fonksiyon istenilen sayı bilgisinin Registry veri tabanında HKEY\_CURRENT\_USER altındaki bir anahtar saha içersindeki entry dahilinde kayıt edilmesini sağlamaktadır.\
\
**Kullanımı**

```
Function SetUserNumber(
  Path As String,	' entry yol bilgisi
  Sayı As Number 	' entry değeri
)
```

**Parametreler**\
_Path_\
HKEY\_CURRENT\_USER altında saklanan entry bilgisinin yol ifadesi\
_Sayı_\
Entry içersine yazmak istediğiniz sayı.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Fonksiyonun kullanımı sonucunda, Registry veri tabanına kayıt yapılırken anahtar sahalar mutlaka "SOFTWARE/Model" altında oluşturulmaktadır. Bu işlemse HKEY\_CURRENT\_USER altında "SOFTWARE/Model" yol bilgisinin ardından verdiğiniz entry'e ait yol bilgisi eklenmesiyle sağlanmaktadır. Yani kaydını yaptığınız sayının ait olduğu entry'nin tam yol bilgisi

"SOFTWARE/Model/anahtar\_saha/entry" şeklindedir.\
\
İşlem sonunda entry'nin kayıttan önceki içeriği yeni bilgi ile değiştirilmektedir. Eğer verdiğiniz yol bilgisindeki entry mevcut değilse önce oluşturulması sağlanmakta ve sayı belirtilen entry içersine yine kayıt edilebilmektedir.\
\
Kayıt işlemi sırasında birbirini izleyen şekilde birden fazla anahtar saha ismi verilmek suretiyle yapılan kayıtların ağaç yapısında dallandırılabilmeleri de mümkündür.\
\
Direkt olarak bir entry ve değerini vererek yani "SOFTWARE/Model" altında bir entry oluşturup değer ataması yapamazsınız. Mutlaka an az bir anahtar saha belirtmeniz gerekmektedir.
