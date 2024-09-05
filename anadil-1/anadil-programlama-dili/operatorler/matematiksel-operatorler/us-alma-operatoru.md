# ^(Üs Alma) Operatörü

Bu operatör bir sayısal ifadenin herhangi bir dereceden üssünü almaktadır.\
**Kullanımı**\
\<sonuç\_değer> := \<sayısal\_ifade1> ^ \<sayısal\_ifade2>\
**Açıklama**\
Üs alma işleminde birinci sayısal ifade, ikinci sayısal ifade kadar kendisi ile çarpılmaktadır.\
Bölme işleminde Number(sayı) tipinden başka bir tip kullanılamaz. Bir bölme işlemi sonrasında ortaya çıkan sonuç değeri yine sayısaldır.\
\
**Örnek**

```
Function F()
	  Dim sayı1 As Number
	  Dim sonuç As Number
	  sayı1:= 8
    sonuç:= 2^sayı1
    MessageBox(Str(sonuç), "Sonuç Değeri", MB_OK)
EndFunction
```

**Örnek Açıklaması**

Yukarıdaki örnek uygulamada ilk etapta sayı1 değişkenine 8 değeri atanmakta daha sonra ise üs alma işlemi ile sayı1'in 8. Dereceden üssü alınmaktadır. Son olarak ise ortaya çıkan sonuç değeri MessageBox fonksiyonu ile Always® terminalinde görüntülenmektedir.
