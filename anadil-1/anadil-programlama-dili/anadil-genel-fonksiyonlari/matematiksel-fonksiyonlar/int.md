# INT

Bir sayısal ifadenin ondalık kısmını atarak, tamsayıya çeviren fonksiyondur.\
\
Kullanımı

```
Function INT(
  Value As Number  ' ondalıklı kısmı atılacak olan sayı
)As Number
```

Parametreler\
_Value_\
Ondalık kısmı atılacak olan sayısal ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri ilk sayının tam sayı karşılığı olan nümerik sayıdır.\
\
Dikkat Edilecek Hususlar\
Sayılar yuvarlanırken aslında sadece ondalık kısım atılmaktadır. Mesela 2.99 sayısı INT fonksiyonu işletimi sonucunda 2.0 sayısı geri döndürülmektedir. Eğer ondalığı olmayan bir sayı INT fonksiyonuna input olarak verilirse geri dönüşteki tam sayı yine aynı sayıdır.\
\
Null olan ifade ilk değer olarak verildiğinde ise sonuç sayısı yine NULL bir ifadedir.\
\
Örnek

```
  Dim sayı1 As Number
  Dim sonuç As Number
  sayı1:= 22 / 7
  sonuç:= INT(sayı1)
  MessageBox(STR(sonuç),"Örnek",MB_OK)
```

Örnek Açıklaması\
Sayı1 değişkenlerine 22/7 ondalık değerler atandıktan sonra INT() fonksiyonuna girilir. Ve ekrana sonuç yani 3 yazdırılır. Esasen sayı1' in değeri 3.142857142 'dir.
