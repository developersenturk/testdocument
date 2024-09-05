# - (Çıkarma) Operatörü

Bu operatör iki sayısal ifade arasında çıkarma işlemi uygulamaktadır.\
Kullanımı\
\<sonuç\_değer> := \<sayısal\_ifade> - \<sayısal\_ifade>\
Açıklama\
Çıkarma işleminde Number(sayı) tipinden başka bir tip kullanılamaz.\
Bir çıkarma işlemi sonrasında ortaya çıkan sonuç değeri yine sayısal bir ifadedir.\
\
Örnek

```
Function F()
  Dim sayı1 As Number
  Dim sonuç As Number
  sayı1:= 20 - 5
  sonuç:= 115 - sayı1
  MessageBox(Str(sonuç), "Sonuç Değeri", MB_OK)
EndFunction
```

**Örnek Açıklaması**

Yukarıdaki örnek uygulamada ilk etapta sayı1 değişkenine 20' den 5' in çıkarılması sonucu 15 değeri atanmakta ardından ise 115' den, sayı1 değeri çıkarılarak sonuç değişkenine atanmaktadır. Son olarak ise sonuç değeri ekranda görüntülenmektedir.
