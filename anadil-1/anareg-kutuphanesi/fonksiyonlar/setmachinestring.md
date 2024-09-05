# SetMachineString

Bu fonksiyon istenilen karakter bilginin Registry veri tabanında HKEY\_LOCAL\_MACHINE altındaki bir anahtar saha içersindeki entry dahilinde kayıt edilmesini sağlamaktadır.\
\
**Kullanımı**

```
Function SetMachineString(
  Path As String,	' entry yol bilgisi
  İfade As String	' entry değeri
)
```

**Parametreler**\
_Path_\
HKEY\_LOCAL\_MACHINE altında saklanan entry bilgisinin yol ifadesi\
_İfade_\
Entry içersine yazmak istediğiniz string formatındaki bilgi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Fonksiyonun kullanımı sonucunda, Registry veri tabanına kayıt yapılırken anahtar sahalar mutlaka "SOFTWARE/Model " altında oluşturulmaktadır. Bu işlemse HKEY\_LOCAL\_MACHINE altında "SOFTWARE/Model" yol bilgisinin ardından verdiğiniz entry'e ait yol bilgisi eklenmesiyle sağlanmaktadır. Yani kaydını yaptığınız karakter formatındaki bilginin ait olduğu entry'nin tam yol bilgisi

"SOFTWARE/Model/anahtar\_saha/entry" şeklindedir.\
\
İşlem sonunda entry'nin kayıttan önceki içeriği yeni bilgi ile değiştirilmektedir. Eğer verdiğiniz yol bilgisindeki entry mevcut değilse önce oluşturulması sağlanmakta ve sayı belirtilen entry içersine yine kayıt edilebilmektedir.\
\
Kayıt işlemi sırasında birbirini izleyen şekilde birden fazla anahtar saha ismi verilmek suretiyle yapılan kayıtların ağaç yapısında dallandırılabilmeleri de mümkündür.\
\
Direkt olarak bir entry ve değerini vererek yani "SOFTWARE/Model" altında bir entry oluşturup değer ataması yapamazsınız. Mutlaka en az bir anahtar saha belirtmeniz gerekmektedir.
