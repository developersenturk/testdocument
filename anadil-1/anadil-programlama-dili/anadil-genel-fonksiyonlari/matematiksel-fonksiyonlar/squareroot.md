# SquareRoot

Bir sayısal ifadenin karekökünü bulan fonksiyondur.\
\
Kullanımı

```
Function SquareRoot(
  Value As Number  ' karekökü alınmak istenilen sayı
)As Number
```

Parametreler\
_Value_\
Karekökü alınacak olan sayısal ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri verilen sayının karekökü olan sayısal ifadedir.\
\
Dikkat Edilecek Hususlar\
Giriş değeri olarak verilen ifadenin sayısal olması gerekmektedir. Ayrıca negatif olan bir sayının karekökünü almak mümkün değildir.\
\
NULL olan bir ifadenin karekökü alınamaz.\
\
Örnek

```
  Dim sayı1 As Number
  Dim sonuç As Number
  sayı1:= 100
  sonuç:= SquareRoot(sayı1)
  MessageBox(STR(sonuç),"",MB_OK)
```

Örnek Açıklaması\
Sayı1 değişkenlerine 100 değeri atandıktan sonra SquareRoot fonksiyonuna girilir. Ve ekrana sonuç yani 10 sayısı yazdırılır.
