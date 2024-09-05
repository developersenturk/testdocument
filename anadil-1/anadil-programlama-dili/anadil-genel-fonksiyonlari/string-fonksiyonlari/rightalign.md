# RightAlign

Bu fonksiyon sonuç uzunluğu verilmek suretiyle verilen bir karakter ifadesini sağa dayalı olarak oluşturur.\
\
Kullanımı

```
Function RightAlign(
  S As String,      ' işlem görecek olan ifade
  Toplam As Number  ' sonuç ifadenin toplam uzunluğu
)As String
```

Parametreler\
_S_\
Sağa dayalı olarak oluşturulacak olan string ifade.\
_Toplam_\
String ifadenin yerleştirileceği uzunluk.\
\
Geri Dönüş Değeri\
Geri dönüş değeri sağa dayalı olarak yerleştirilmiş olan sonuç ifadenin kendisidir.\
\
Dikkat Edilecek Hususlar\
Bu fonksiyon kullanılırken sonuç ifade oluşturulurken başlangıç ifadesinin soluna boşluk karakterleri eklenmektedir. Bu yüzden verilen toplam uzunluk değeri ifadenin başlangıç uzunluğundan büyük olmalıdır.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim sonuç As String
  karakter_dizisi:= "Always Framework"
  sonuç:= RightAlign(karakter_dizgisi,20) 
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Yukarıdaki kod parçasının işletimi sonucunda karakter\_dizisi içindeki ifadenin değeri\
"Always Framework" iken RightAlign fonksiyonuna girildikten sonra oluşan değer yani\
" Always Framework" Sonuç değişkenine atanır.
