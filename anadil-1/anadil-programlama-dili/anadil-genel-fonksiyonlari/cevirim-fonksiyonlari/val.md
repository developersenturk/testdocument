# VAL

Bu fonksiyon String tipindeki bir değişkeni, number tipine dönüştürmektedir.\
\
Kullanımı

```
Function VAL(
  S As String  ' işlem görecek ifade
)As String
```

Parametreler\
S\
Sayısal tipe dönüştürülecek olan string formatındaki ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri fonksiyondan çıkış olarak beklediğimiz string tipindeki amaç değişkenidir.\
\
Dikkat Edilecek Hususlar\
Parametre olarak verilen değer mutlaka string formatındaki bir ifade olması gerekmektedir.\
\
Örnek

```
  Dim sonuç As Number
  Dim sayı1 As String
  sayı1:="10"
  sonuç:= VAL(sayı1)
  MessageBox(STR(sonuç),"Örnek",MB_OK)
```

Örnek Açıklaması\
Sayı1 değişkeni içerisindeki "10" string ifadesi number tipine dönüştürülerek sonuç değişkenine eşitlenmekte ve ekrana yazdırılırken tekrar string tipine dönüştürülmektedir.
