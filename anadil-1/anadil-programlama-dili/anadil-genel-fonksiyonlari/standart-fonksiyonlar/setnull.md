# SetNull

Bu fonksiyon String, Number veya Date olan değişkenlerin içeriğini NULL yapmaktadır.\
\
Kullanımı

```
Function SetNull(@Değişken)
```

Parametreler\
_Değişken_\
İçeriği NULL olarak eşitlenecek olan Number, String veya Date olan değişkendir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri önemsizdir.\
\
Dikkat Edilecek Hususlar\
NULL kullanım biçimi özellikle RDBMS sistemleri için çok büyük bir önem teşkil etmektedir. NULL ne string olarak boş string ifadeye ne de sayı olarak sıfıra eşit olduğundan bir değişkeni içerik olarak NULL şeklinde ifade etmek bu özel fonksiyon sayesinde başarılmaktadır.\
\
Burada dikkat edilecek başka bir husus sadece _String, Number_ ve _Date_ olan değişkenler bu fonksiyon yardımıyla NULL içeriğe eşitlenebilmektedir.\
\
Örnek

```
Function F()
  Dim temp As Number
  temp:= 100
  MessageBox(Str(temp), "Önce", MB_OK+MB_ICONINFORMATION)
  SetNull(@temp)
  If IsNull(temp) Then
    MessageBox("Değişkenin içeriği NULL.", #
    "Sonra", #
    MB_OK+MB_ICONINFORMATION)
  EndIf
EndFunction
```

Örnek Açıklaması\
Yukarıdaki kodun işletilmesiyle içeriği 100 olan sayının önce içeriği NULL yapılmakta, daha sonra da içeriğinin NULL olması başka bir fonksiyonla test edilmektedir.
