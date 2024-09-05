# RightTrim

Bu fonksiyon bir karakter dizisinin sağ tarafındaki boşluk karakterlerini atmaktadır.\
\
Kullanımı

```
Function RightTrim(
  S As String  ' işlem gören ifade
)As String
```

Parametreler\
_S_\
Sağ tarafındaki boşlukları atılacak olan string ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri parametre olarak verilmiş olan karakter dizisinin sağ tarafındaki boşlukları atıldıktan sonraki halidir.\
\
Dikkat Edilecek Hususlar\
Fonksiyon string ifadeler üzerinde kullanılmalıdır, ve geri dönüş değeri yine bir string ifadedir.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim sonuç As String
	
  karakter_dizisi:= "Bu bir örnektir.                "
  sonuç:= RightTrim(karakter_dizisi)
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Burada karakter\_dizisi içine "Bu bir örnektir. " atandıktan sonra RightTrim() fonksiyonuna girilir. Ve ekrana sonuç yani "Bu bir örnektir." yazdırılır.
