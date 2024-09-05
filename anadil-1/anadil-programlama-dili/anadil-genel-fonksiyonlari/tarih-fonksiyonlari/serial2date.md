# Serial2Date

Bu fonksiyon sayısal olarak verilen bir değişkenin tarih olarak karşılığını vermektedir\
\
Kullanımı

```
Function Serial2Date(
  Sayı As Number  ' işlem görecek ifade
)As Date
```

Parametreler\
_Sayı_\
Tarih tipine dönüştürülecek olan string ifade.\
\
Geri Dönüş Değeri\
Geri dönüş değeri fonksiyondan çıkış olarak beklediğimiz tarih tipindeki amaç değişkenidir.\
\
Dikkat Edilecek Hususlar\
Sayısal ifedeleri tarihsel karşılığını almak özellikle tarihler arasında işlem yaparken gerekli olmaktadır. Burada verilen sayı 1 olursa 1 Ocak 1980 tarihi elde edilecektir.\
\
Bu fonksiyon, Date2Serial() fonksiyonunda olduğu gibi bir üst limit tarih değerine sahip değildir. Yani 1 Ocak 1980 tarihinden, Anadil® Number tipinin elverdiği ölçüde, büyük sayıların tarihsel olarak karşılığını elde edebilirsiniz.\
\
Örnek

```
  Dim d As Date
  d:= Serial2Date(Date2Serial(Str2Date("19/02/1996")) + 50)
  MessageBox(Date2Str(d),"19 Şubat'tan 50 gün sonrası",MB_OK)
```

Örnek Açıklaması\
"19/02/1996" karakter ifadesi, bu fonksiyonla tarih tipine dönüştürüldükten sonra, bu tarih tipi Date2Serial() fonksiyonu ile sayısal hale getirilmektedir. Daha sonra 50 gün sonrası için toplama işlemi gerçekleştirilmekte ve sonuçta elde edilen sayı tekrar tarihsel şekle dönüştürülmektedir. Elde edilen tarih değişkeni MessageBox ile ekranda gösterilmektedir.
