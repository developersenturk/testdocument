# Right

Bu fonksiyon bir karakter ifade içersinden sağdan itibaren belli bir uzunluktaki karakteri ayırmada kullanılır.\
\
Kullanımı

```
Function Right(
  S As String,      ' işlem görecek ifade
  Toplam As Number  ' toplam karakter sayısı
)As String
```

Parametreler\
_S_\
İçinden karakter ayrılacak olan string ifadedir.\
_Toplam_\
Sağdan itiberen kaç karakter alınacağını belirten nümerik bir değerdir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri ayrılmış olan sonuç string ifadenin kendisidir.\
\
Dikkat Edilecek Hususlar\
RIGHT fonksiyonu, karakter ifadesinin sağ tarafından itibaren karakter sayısı kadar olan kısmını alır. Fonksiyon mutlaka string ifadelerle kullanılmalıdır.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim sonuç As String
  Dim karakter_sayısı As Number
  karakter_dizisi:= "Bu bir örnektir"
  karakter_sayısı:= 8
  sonuç := RIGHT(karakter_dizisi,karakter_sayısı)
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Yukarıdaki kod parçası "Bu bir örnektir" karakter dizisinden sağdan itibaren 8 karakteri ayırarak ekrana "örnektir" yazar.
