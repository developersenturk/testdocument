# UpperTR

Bu fonksiyon bir karakter ifadesindeki TÜRKÇE harflerin hepsini TÜRKÇE büyük harfe dönüştürür.\
\
Kullanımı

```
Function UpperTR(
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
Karakter ifadesindeki harflerin küçük yada büyük harf olması önemli değildir. Her şekilde geriye büyük harf şeklinde dönmektedir.\
\
Örnek

```
Function muhfis_Cevir_Click(f As Object)
 'This is called when the button is clicked.
  Dim karakter_dizisi As String
  Dim sonuç As String
  
  karakter_dizisi:= "ŞİŞLİDE BÜYÜK ÇÖP YIĞINLARI"
  sonuç:= LowerTR(karakter_dizisi)
  outm("")
  outm("---------------------------------------------------")
  OUTM("LowerTR ( ŞİŞLİDE BÜYÜK ÇÖP YIĞINLARI )")
  OUTM("LowerTR ( " & sonuç)

  'MessageBox(sonuç,"Örnek",MB_OK)

  karakter_dizisi:= "şişlide büyük çöp yığınları"
  sonuç:= UpperTR(karakter_dizisi)
  outm("")
  outm("---------------------------------------------------")
  OUTM("UpperTR ( şişlide büyük çöp yığınları )")
  OUTM("UpperTR ( " & sonuç)
  outm("")
  outm("---------------------------------------------------")

EndFunction

```

Örnek Açıklaması\
Yukarıdaki kod parçası, tüm TÜRKÇE karakterleri içeren ifadenin bütün karakterlerini büyük harfe dönüştürerek terminalde sonucu gösterir.\
\
İlgili komutlar: LowerTR\
Lower\
Upper
