# LeftAlign

Bu fonksiyon sonuç uzunluğu verilmek suretiyle verilen bir karakter ifadesini sola dayalı olarak oluşturur.\
\
Kullanımı

```
Function LeftAlign(
  S As String,      ' işlem görecek ifade
  Toplam As Number  ' sonuç ifadenin toplam uzunluğu
)As String
```

Parametreler\
_S_\
Sola dayalı olarak oluşturulacak olan string ifade.\
_Toplam_\
String ifadenin yerleştirileceği uzunluk.\
\
Geri Dönüş Değeri\
Geri dönüş değeri sola dayalı olarak yerleştirilmiş olan sonuç ifadenin kendisidir.\
\
Dikkat Edilecek Hususlar\
Bu fonksiyon kullanılırken sonuç ifade oluşturulurken başlangıç ifadesinin sağına boşluk karakterleri eklenmektedir. Bu yüzden verilen toplam uzunluk değeri ifadenin başlangıç uzunluğundan büyük olmalıdır.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim sonuç As String
	
  karakter_dizisi:= "Always Framework"
	
  sonuç:=LeftAlign(karakter_dizisi, 20) 
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Yukarıdaki kod parçasının işletimi ile karakter\_dizisi içindeki ifadenin değerini "Always Framework" iken LeftAlign fonksiyonuna girildikten sonra oluşan değer yani "Always Framework " Sonuç değişkenine atanır.
