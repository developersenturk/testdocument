# LRC

Bu fonksiyon bir verilen string ifadenin LRC değerini hesaplar ve tek karakter olarak geri döndürür.\
\
**Kullanımı**

```
Function LRC(
    szString As String
) As String
```

**Parametreler**\
_szString_ LRC değeri bulunacak string ifade.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, LRC karakteridir.\
\
**Dikkat Edilecek Hususlar**

```
255 karakterden daha uzun string ifadelerin LRC karakterine ihtiyaç duyulduğunda, 
ilk elde edilen LRC karakteri, sonraki string ifadenin başına konulmalı ve 
LRC fonksiyonu tekrar çağırılmalı.
Örnek:

Dim LRC As String
Dim szString1 As String
Dim szString2 As String

szString1:="MODEL BİLGİ İŞLEM"
szString2:="ENTERPRISE MODEL"

'szString1 ifadesinin LRC karakteri hesaplaniyor
LRC:=LRC(szString1)

'szString1 ifadesinin LRC karakteri szString2 ifadesinin başına ekleniyor.
szString2:=LRC & szString2

'Sonuç olarak szString1 + szString2  ifadesinin LRC karakteri bulunmuş oluyor.
LRC:=LRC(szString2) 



LRC hesaplama Yöntemi
LRC karakteri, verilen string ifadedeki tüm karakterlerin binary XOR lanması sonucunda elde edilir.
Örnek:

szStr :="ABCDEF"
LRC := (((((A XOR B ) XOR C ) XOR D ) XOR E ) XOR F )

```
