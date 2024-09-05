# ABS

Bir sayısal ifadenin mutlak değerini bulan fonksiyondur.\
\
Kullanımı

```
Function ABS(
  Value As Number	' mutlak değeri alınmak istenen sayı
)As Number
```

Parametreler\
_Value_\
Mutlak değeri alınacak olan sayısal ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüşte sayının mutlak değeri alınmış hali dönecektir.\
\
Dikkat Edilecek Hususlar\
Bu fonksiyon, pozitif veya negatif bir sayısal ifadenin mutlak değerini alarak, sonucun daima pozitif dönmesini sağlamaktadır. Verilen ifadenin mutlaka sayısal olması gerekmektedir.\
\
Örnek

```
Function F()
  Dim sayı1 As Number
  Dim sonuç As Number
  sayı1:= -10
  sonuç:= ABS (sayı1)
  MessageBox(STR(sonuç),"Örnek",MB_OK)
EndFunction
```

Örnek Açıklaması\
Sayı1 değişkenlerine -10 değeri atandıktan sonra ABS() fonksiyonuna girilir. Ve ekrana sonuç yani 10 yazdırılır.
