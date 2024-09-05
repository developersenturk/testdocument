# FindStr

Bir karakter dizisi içinde başka bir karakter veya karakter dizisininin aranılmasını sağlayan fonksiyondur.\
\
Kullanımı

```
Function FindStr(
  S As String,  ' işlem görecek karakter dizisi
  K As String   ' aranılan karakter dizisi
)As Number
```

Parametreler\
_S_\
İçinde kelime veya kelime grubu aranacak olan string ifadedir.\
_K_\
String ifade içinde aranacak olan karakter veya karakter grubunu belirten string ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri eğer aranılan string ifade bulunduysa, ilk ifade içerisinde başlangıçtan itibaren kaçıncı karakterden sonra yer aldığını gösteren sayısal değerdir.\
\
Dikkat Edilecek Hususlar\
Aranılan karakter dizisi içersinde sayısal ifadeler de yer alabilmektedir. Eğer işlem başarısızsa sonuç olarak 0(sıfır) sayısı geri dönecektir.\
\
İndexleme numarası 1(bir) 'den itibaren başlamaktadır.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim aranan_dizi As String
  Dim sonuç As Number
  karakter_dizisi:="Bu bir örnektir."
  aranan_dizi:="bir"
  sonuç:= FindStr(karakter_dizisi, aranan_dizi)
  MessageBox(STR(sonuç),"Örnek",MB_OK)
```

Örnek Açıklaması\
Burada karakter\_dizisi içine "Bu bir örnektir" ve aranan\_ dizi içine de "bir" string ifadesini atadıktan sonra FindStr() fonksiyonuna girilir. Ve ekrana sonuç yani "4" yazdırılır.
