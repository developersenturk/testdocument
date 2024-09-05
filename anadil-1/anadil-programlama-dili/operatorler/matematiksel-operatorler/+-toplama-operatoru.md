# + (Toplama) Operatörü

Bu operatör iki sayısal ifade arasında toplama işlemi uygulamaktadır.\
**Kullanımı**\
\<sonuç\_değer> := \<sayısal\_ifade> + \<sayısal\_ifade>\
**Açıklama**\
Toplama işleminde Number(sayı) tipinden başka bir tip kullanılamaz.\
Bir toplama işlemi sonrasında ortaya çıkan sonuç değeri yine sayısal bir ifadedir.\
\
**Örnek**

```
Function F()
  Dim sayı1 As Number
  Dim sonuç As Number
  sayı1:= 20 + 5
  sonuç:= sayı1 + 75
  MessageBox(Str(sonuç), "Sonuç Değeri", MB_OK)
EndFunction
```

**Örnek Açıklaması**

Yukarıdaki örnek uygulamada ilk etapta sayı1 değişkenine 20 ile 5' in toplamı olan 25 değeri atanmaktadır. Daha sonra ise sayı1 değişkeni 75 ile toplanarak sonuç değişkenine eşitlenmektedir. Son olarak ise sonuç değeri ekranda görüntülenmektedir.
