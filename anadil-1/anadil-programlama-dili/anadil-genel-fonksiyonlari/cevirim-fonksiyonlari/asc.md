# ASC

Bu fonksiyon herhangi bir karakterin ASCII kodunu bulmaktadır.\
\
Kullanımı

```
Function ASC(
  S As String  ' ASCII kodu istenilen karakter
)As Number
```

Parametreler\
_S_\
ASCII kodu bulunacak olan string formatındaki bir karakterdir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri ASCII kodlarından biri olmakta dolayısıyla 0-255 arası nümerik bir değerdir.\
\
Dikkat Edilecek Hususlar\
Sadece bir karakterin ASCII kodunu bulabilen bir fonksiyondur. Eğer birden fazla karakter varsa bütün karakterlerin tek tek bu fonksiyon ile ASCII kodlarının sorgulanması gerekmektedir.\
\
Örnek

```
  Dim sonuç As Number
  Dim sayı1 As String
  sayı1:="A"
  sonuç:= ASC(sayı1)
  MessageBox(STR(sonuç),"Örnek",MB_OK)
```

Örnek Açıklaması\
Sayı1 değişkeni içerisindeki "A" string karakterinin ASCII kodu bulunarak ekrana yazdırılmaktadır.
