# Upper

Bu fonksiyon bir karakter ifadesindeki harflerin hepsini büyük harfe dönüştürür.\
\
Kullanımı

```
Function Upper(
  S As String  ' işlem görecek ifade
)As String
```

Parametreler\
_S_\
Bütün karakterleri büyük harfe dönüştürülecek olan string ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri bütün karakterleri büyük harf olan sonuç string ifadesidir.\
\
Başlangıç Dikkat Edilecek Hususlar\
karakter ifadesindeki harflerin küçük yada büyük harf olması önemli değildir. Her şekilde geriye büyük harf şeklinde dönmektedir.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim sonuç As String
  
  karakter_dizisi:= "Bu Bir Örnektir"
  sonuç:= Upper(karakter_dizisi)
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Yukarıdaki kod parçası karakter dizisi içindeki ifadenin bütün karakterlerini büyük harfe dönüştürerek ekrana "BU BİR ÖRNEKTİR" yazar.\
\
İlgili komutlar: Lower\
