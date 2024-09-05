# MAX

Bu fonksiyon verilen iki sayıdan büyük olanını bulmaktadır.\
\
Kullanımı

```
Function MAX(
  Value1 As Number,  ' birinci sayı
  Value2 As Number   ' ikinci sayı
)As Number
```

Parametreler\
_Value1_\
Karşılaştırılacak olan sayılardan ilki.\
_Value2_\
Karşılaştırılacak olan sayılardan ikincisi.\
\
Geri Dönüş Değeri\
Fonksiyonun işletimi sonunda karşılaştırma işlemi yapılacak ve büyük olan sayı geri dönüş değeri olacaktır.\
\
Dikkat Edilecek Hususlar\
Bu fonksiyonda sayısal ifadelerden başka ifadelerle kullanılamaz. Eğer bir sayı ile NULL karşılaştırılırsa işlemin sonucu yine NULL olacaktır.\
\
Örnek

```
  Dim sayı1 As Number
  Dim sayı2 As Number
  Dim sonuç As Number
  sayı1:= 10
  sayı2:= 8
  sonuç:= MAX(sayı1,sayı2)
  MessageBox(STR(sonuç),"Örnek",MB_OK)
```

Örnek Açıklaması\
Sayı1 ve sayı2 değişkenlerine sırasıyla 10 ve 8 değerleri atandıktan sonra MAX() fonksiyonu işletilmekte ve sonuç değişkeni büyük olan sayıya yani 10'a eşitlenmektedir.
