# CHR

Bu fonksiyon ASCII kodu verilerek, string formatındaki tek karakteri bulmaktadır.\
\
Kullanımı

```
Function CHR(
  Value As Number  ' karakterin ASCII kodu
)As String
```

Parametreler\
_Value_\
Karakteri karşılığı bulunacak olan sayısal ASCII kod değeridir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri ASCII koda karşılık gelmekte olan string formatındaki tek bir karakterdir.\
\
Dikkat Edilecek Hususlar\
Verilen ASCII kod değeri 0-255 arasında olması gerekmektedir.\
\
Örnek

```
  Dim sonuç As String
  Dim sayı1 As Number
  sayı1:= 65
  sonuç:= CHR(sayı1)
  MessageBox(STR(sonuç),"Örnek",MB_OK)
```

Örnek Açıklaması\
Sayı1 değişkeni içerisindeki 65 nümerik ifadesinin ASCII karşılığı bulunularak ekrana "A" karakteri yazdırılmaktadır.
