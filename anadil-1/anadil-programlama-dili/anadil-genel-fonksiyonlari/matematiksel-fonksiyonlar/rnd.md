# RND

Bu fonksiyon random (rastgele) bir sayı üretmektedir.\
\
Kullanımı

```
Function RND(
  Value As Number  ' üst limit değeri
)As Number
```

Parametreler\
_Value_\
Rasgele üretilecek olan sayının maximum değerini belirten sayıdır.\
\
Geri Dönüş Değeri\
Geri dönüş değeri rastgele üretilmiş olan sayıdır.\
\
Dikkat Edilecek Hususlar\
Genel olarak rastgele sayı üretiminde alt limit ve üst limit değerleri bulunmaktadır. Bu fonksiyonda ise 0(sıfır) alt limit değeri olarak alınmakta, fonksiyona parametre olarak verilen sayı ise üst limit değeri olmaktadır.\
\
Örnek

```
  Dim sayı1 As Number
  Dim sonuç As Number
  sayı1:= 100
  sonuç:= RND(sayı1)
  MessageBox(STR(sonuç),"Örnek",MB_OK)
```

Örnek Açıklaması\
Yukarıdaki örnek kodun işletimi sonucunda 0 ile 100 arasında rasgele bir sayı üretilir ve ekrana sonuç yazdırılır.
