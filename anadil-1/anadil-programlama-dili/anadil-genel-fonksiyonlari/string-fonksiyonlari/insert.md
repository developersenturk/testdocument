# Insert

Bu fonksiyon bir karakter dizisi içersine başka bir karakter dizisini ekler.\
\
Kullanımı

```
Function Insert(
  S As String,          ' işlem görecek ifade
  Başlangıç As Number,  ' başlangıç karakteri
  Eklenen As String     ' eklenecek ifade
)As String
```

Parametreler\
_S_\
İçine kelime veya kelime grubu eklenecek olan string ifadedir.\
_Başlangıç_\
İçine eklenecek olan kelime veya kelime grubunun S string ifadesi içinde soldan kaçıncı karakterden itibaren başlayacağını belirten nümerik değerdir.\
_Eklenen_\
Eklenen string ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri birinci ifadeye ekleme işlemi sonucunda ortaya çıkan sonuç string ifadedir.\
\
Dikkat Edilecek Hususlar\
Ekleme işleminde verilen başlangıç index pozisyonun değeri 0(sıfır) 'dan küçük veya karakter ifadesinin uzunluğundan büyük olamaz. İndexleme de 1(bir) 'den itibaren başlamaktadır.\
\
Örnek

```
  Dim ilk_ifade As String
  Dim eklenen_ifade As String
  Dim sonuç As String
  Dim başlangıç As Number
  ilk_ifade:= "Bu örnektir"
  eklenen_ifade:= "bir "
  başlangıç:= 4
  sonuç:= Insert(ilk_ifade, başlangıç, eklenen_ifade)
  MessageBox(sonuç,"Örnek",MB_OK)
```

Örnek Açıklaması\
Yukarıdaki kod parçası "Bu örnektir" karakter dizisinde soldan 4. karakterden itibaren "bir " kelimesini ekleyerek ekrana "Bu bir örnektir" yazar.
