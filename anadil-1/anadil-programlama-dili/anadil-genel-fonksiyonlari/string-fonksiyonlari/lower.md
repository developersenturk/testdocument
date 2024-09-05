# Lower

Bu fonksiyon bir karakter ifadesindeki harflerin hepsini küçük harfe dönüştürür.\
Kullanımı

```
Function Lower(
  S As String  ' işlem görecek ifade
)As String
```

Parametreler\
_S_\
Bütün karakterleri küçük harfe dönüştürülecek olan string ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri bütün karakterleri küçük harf olan sonuç string ifadesidir.\
\
Dikkat Edilecek Hususlar\
Karakter ifadesindeki harflerin küçük yada büyük harf olması önemli değildir. Her şekilde geriye küçük harf şeklinde dönmektedir.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim sonuç As String
	
  karakter_dizisi:= "Bu Bir Örnektir"
  sonuç:= Lower(karakter_dizisi)
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Yukarıdaki kod parçası karakter dizisi içindeki ifadenin bütün karakterlerini küçük harfe dönüştürerek ekrana "bu bir örnektir" yazar.\
\
İlgili komutlar: Upper LowerTR UpperTR
