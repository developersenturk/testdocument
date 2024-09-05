# Mid

Bu fonksiyon bir karakter ifade içersinden belli bir uzunluktaki string ifadenin ayrılması işleminde kullanılır.\
\
Kullanımı

```
Function MID(
  S As String,      ' işlem görecek ifade
  İlk As Number,    ' başlangıç karakteri
  Toplam As Number  ' toplam karakter sayısı
)As String
```

Parametreler\
_S_\
İçinden kelime veya kelime grubu alınacak olan string ifadedir.\
_İlk_\
Alınacak olan kelime veya kelime grubunun, string ifade içindeki başlangıç pozisyonunu bellirten nümerik index değeridir.\
_Toplam_\
String ifade içinden başlangıç pozisyonundan itibaren toplam kaç karakter alınacağını belirten nümerik bir değerdir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri sonuçta elde edilecek olan string ifadenin kendisidir.\
\
Dikkat Edilecek Hususlar\
MID fonksiyonu karakter ifadesinin başlangıç pozisyonundan itibaren karakter sayısı kadar olan kısmını alır. İndex numarası da 1(bir) 'den itibaren başlamaktadır.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim sonuç As String
  Dim karakter_sayısı As Number
  Dim başlangıç As Number
  karakter_dizisi:= "Bu bir örnektir"
  başlangıç:= 7
  karakter_sayısı:= 5
  sonuç:= MID(karakter_dizisi,başlangıç,karakter_sayısı)
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Yukarıdaki kod parçası "Bu bir örnektir" karakter dizisinde 7. karakterden başlayarak sağa doğru 5 karakteri ayırarak ekrana "örnek" yazmaktadır.
