# \* (Çarpma) Operatörü

Bu operatör iki sayısal ifade arasında çarpma işlemi uygulamaktadır.\
**Kullanımı**\
\<sonuç\_değer> := \<sayısal\_ifade> \* \<sayısal\_ifade>\
**Açıklama**\
Çarpma işleminde Number(sayı) tipinden başka bir tip kullanılamaz.\
Bir çarpma işlemi sonrasında ortaya çıkan sonuç değeri yine sayısal bir ifadedir.\
\
Örnek

```
Function F()
  Dim sayı1 As Number
  Dim sonuç As Number
  sayı1:= 5
  sonuç:= 9 * sayı1
  MessageBox(Str(sonuç), "Sonuç Değeri", MB_OK)
EndFunction
```

\
**Örnek Açıklaması**\
Yukarıdaki örnek uygulamada sayı1 değişkenine 5 değeri atanmakta daha sonra ise 9 ile çarpılmak suretiyle ortaya çıkan ifade sonuç değişkenine eşitlenmektedir. Son olarak da, sonuç değişkeni MessageBox fonksiyonu ile ekranda görüntülenmektedir.
