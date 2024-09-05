# Length

Bu fonksiyon bir karakter dizisinin uzunluğunu bulmaktadır.\
\
Kullanımı

```
Function Length(
  S As String  ' işlem görecek ifade
)As Number
```

Parametreler\
_S_\
Uzunluğu bulunacak olan string ifade.\
\
Geri Dönüş Değeri\
Geri dönüş değeri string ifadenin uzunluğu olan sayısal değerdir.\
\
Dikkat Edilecek Hususlar\
Fonksiyona parametre olarak mutlaka string ifade verilmelidir.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim sonuç As Number
  karakter_dizisi:= "Bu bir örnektir"
  sonuç:= Length(karakter_dizisi)
  MessageBox(STR(sonuç),"Örnek",MB_OK)
```

Örnek Açıklaması\
Burada karakter\_dizisi içine "Bu bir örnektir" atandıktan sonra Length() fonksiyonu işletilir ve ekrana sonuç yani 15 yazılır.
