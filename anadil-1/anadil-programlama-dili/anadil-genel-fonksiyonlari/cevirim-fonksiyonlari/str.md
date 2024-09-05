# STR

Bu fonksiyon Number tipindeki bir değişkeni, String tipine dönüştürmektedir.\
\
Kullanımı

```
Function STR(
  Value As Number  ' işlem görecek ifade
)As String
```

Parametreler\
_Value_\
String tipine dönüştürülecek olan sayısal ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri fonksiyondan çıkış olarak beklediğimiz string tipindeki amaç değişkenidir.\
\
Dikkat Edilecek Hususlar\
Parametre olarak verilen değer mutlaka sayısal bir ifade olması gerekmektedir. Always® genel olarak sayı değişkenlerini virgülden sonra yani ondalık kısımda 6 adet 0 olacak şekilde ele almaktadır. Fakat sayının string karşılığı STR fonksiyonu ile çevirime uğradığında sayının ondalık kısmında en sağdaki fazlalık sıfırlar atılmaktadır.\
\
Örnek

```
  Dim sayı1 As Number
  Dim sonuç As String
  sayı1:=10
  sonuç:= STR(sayı1)
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Sayı1 değişkeni içerisindeki 10.000000 sayısal ifadesi string tipine dönüştürülerek sonuç değişkenine eşitlenmekte ve Mesaj kutusu ile ekrana string formatında "10" ifadesi yazılmaktadır.
