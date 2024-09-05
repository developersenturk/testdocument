# LeftTrim

Bu fonksiyon bir karakter dizisinin sol tarafındaki boşluk karakterlerini atmaktadır.\
\
Kullanımı

```
Function LeftTrim(
  S As String  ' işlem görecek ifade
)As String
```

Parametreler\
_S_\
Sol tarafındaki boşlukları atılacak olan string ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri parametre olarak verilmiş olan karakter dizisinin sol tarafındaki boşlukları atıldıktan sonraki halidir.\
\
Dikkat Edilecek Hususlar\
Fonksiyon string ifadeler üzerinde kullanılmalıdır, ve geri dönüş değeri yine bir string ifadedir.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim sonuç As String
  karakter_dizisi:= "           Bu bir örnektir."
  sonuç:= LeftTrim(karakter_dizisi)
  MessageBox(STR(sonuç),"Örnek",MB_OK)
```

Örnek Açıklaması\
Burada karakter\_dizisi içine " Bu bir örnektir." atandıktan sonra LeftTrim() fonksiyonuna girilir. Ve ekrana sonuç yani "Bu bir örnektir." yazdırılır.
