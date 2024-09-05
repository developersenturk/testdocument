# Left

Bu fonksiyon bir karakter ifade içersinden soldan itibaren istenilen kadar karakteri ayırmada kullanılır.\
\
Kullanımı

```
Function Left(
  S As String,      ' işlem görecek ifade
  Toplam As Number  ' toplam karakter sayısı
)As String
```

Parametreler\
_S_\
İçinden karakter ayrılacak olan string ifadedir.\
_Value_\
Soldan itiberen kaç karakter alınacağını belirten sayısal değerdir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri ayrılmış olan sonuç string ifadenin kendisidir.\
\
Dikkat Edilecek Hususlar\
Left fonksiyonu, karakter ifadesinin sol tarafından itibaren karakter sayısı kadar olan kısmını alır. Fonksiyon mutlaka string ifadelerle kullanılmalıdır.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim sonuç As String
  Dim karakter_sayısı As Number
	
  karakter_dizisi:= "Bu bir örnektir"
  karakter_sayısı:= 6
	
  sonuç := LEFT(karakter_dizisi,karakter_sayısı)
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Yukarıdaki kod parçası "Bu bir örnektir" karakter dizgisinde soldan 6 karakteri ayırarak ekrana "Bu bir" yazar.
