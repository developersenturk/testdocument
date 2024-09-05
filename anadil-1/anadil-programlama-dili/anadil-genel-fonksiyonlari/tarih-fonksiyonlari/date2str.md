# Date2Str

Bu fonksiyon Tarih tipindeki bir değişkeni, string tipine dönüştürmektedir.\
\
Kullanımı

```
Function Date2Str(
  D As Date  ' işlem görecek ifade
)As String
```

Parametreler\
_D_\
String tipine dönüştürülecek olan tarih değişkeni.\
\
Geri Dönüş Değeri\
Geri dönüş değeri fonksiyondan çıkış olarak beklediğimiz string tipindeki amaç değişkenidir.\
\
Dikkat Edilecek Hususlar\
Parametre olarak verilen değer mutlaka tarih şeklinde bir ifade olması gerekmektedir.\
\
Örnek

```
  Dim d As Date
  Dim s As String
  d:=Str2Date("15/08/1974")
  s:=Date2Str(d)
  MessageBox(s,"Örnek",MB_OK)
```

Örnek Açıklaması\
"15/08/1974" karakter ifadesi, bu fonksiyonla tarih tipine dönüştürüldükten sonra, bu tarih tipi Date2Str() fonksiyonu ile tekrar string tipine dönüştürülerek ekrana yazılmaktadır.
