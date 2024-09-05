# / (Bölme) Operatörü

Bu operatör iki sayısal ifade arasında bölme işlemi uygulamaktadır.\
**Kullanımı**\
\<sonuç\_değer> := \<sayısal\_ifade> / \<sayısal\_ifade>\
**Açıklama**\
Bölme işleminde Number(sayı) tipinden başka bir tip kullanılamaz.\
Bir bölme işlemi sonrasında ortaya çıkan sonuç değeri yine sayısal bir ifadedir.\
\
Örnek

```
Function F()
  Dim sayı1 As Number
  Dim sonuç As Number
  sayı1:= 25
  sonuç:= 100 / sayı1
  MessageBox(Str(sonuç), "Sonuç Değeri", MB_OK)
EndFunction
```

**Örnek Açıklaması**

Yukardaki örnek uygulamada ilk etapta sayı1 değişkenine 25 değeri atanmakta daha sonra ise bölme işlemi gerçekleştirilmektedir. Son olarak ise ortaya çıkan sonuç değeri MessageBox fonksiyonu ile Always® terminalinde görüntülenmektedir.
