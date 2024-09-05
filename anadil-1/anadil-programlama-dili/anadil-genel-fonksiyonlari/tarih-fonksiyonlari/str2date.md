# Str2Date

Bu fonksiyon String tipindeki bir değişkeni, Tarih tipine dönüştürür.\
Kullanımı

```
Function Str2Date(
  S As String  ' işlem görecek ifade
)As Date
```

Parametreler\
S\
Tarih tipine dönüştürülecek olan string ifade.\
Geri Dönüş Değeri\
Geri dönüş değeri fonksiyondan çıkış olarak beklediğimiz tarih tipindeki amaç değişkenidir.\
Dikkat Edilecek Hususlar\
Parametre olarak verilen değer mutlaka string bir ifade olması gerekmektedir.\
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
