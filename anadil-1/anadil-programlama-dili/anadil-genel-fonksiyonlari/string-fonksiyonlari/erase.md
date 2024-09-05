# Erase

Bir karakter dizgisinin içinden istenilen karakter veya karakterlerin silinmesi işlemini yapan fonksiyondur.\
\
Kullanımı

```
Function ERASE(
  S As String,      ' işlem görecek karakter dizisi
  İlk As Number,    ' başlangıç karakteri
  Toplam As Number  ' silinecek karakter sayısı
)As String
```

Parametreler\
_S_\
İçinden karakter veya karakter grubu çıkarılacak olan string ifadedir.\
_İlk_\
Çıkarılacak olan kelime veya kelime grubunun, string ifade içindeki başlangıç index numarasını belirten nümerik bir değerdir.\
_Toplam_\
String ifade içinden başlangıç index numarasından itibaren kaç karakter çıkarılacağını belirten nümerik bir değerdir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri ilk karakter dizisinin içersinden silme işlemi yapıldıktan sonra geri kalan sonuç karakter dizisidir.\
\
Dikkat Edilecek Hususlar\
Belirtilen bir string ifade içinde, verilen pozisyondan itibaren karakter sayısı kadar karakterin silinmesi işlemi yapılır. Karakter tipinin içinde sayısal ifade ve/veya semboller bulunabilir.\
\
Ayrıca indexleme numarası 1(bir) 'den itibaren başlamaktadır.\
\
Örnek

```
  Dim karakter_dizisi As String
  Dim başlangıç As Number
  Dim karakter_sayısı As Number
  Dim sonuç As String
  karakter_dizisi:="Bu bir örnektir."
  başlangıç:= 4
  karakter_sayısı:=3
  
  sonuç:= ERASE(karakter_dizgisi, başlangıç, karakter_sayısı)
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Burada karakter\_dizisi içine "Bu bir örnektir" ifadesi eşitlenmekte, daha sonra da 4. Index numarasından itibaren toplam 3 karakter silinmekte ve ekrana sonuç yani 'Bu örnektir.' ifadesi yazdırılmaktadır.
