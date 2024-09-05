# Null2Zero

Bu fonksiyon Number tipindeki bir değişkenin değeri NULL ise sıfır döndürür değilse sayısal değeri döndürür.\
\
Kullanımı

```
Function Null2Zero(
  Num As Number  ' işlem görecek ifade
)As Number
```

Parametreler\
Num\
NULL olup olmadığı kontrol edilecek Number tipindeki değişken.\
\
Geri Dönüş Değeri\
Num parametresinin değeri NULL ise geri dönüş değeri 0 (sıfır) dır. Null değilse Num parametresinin kendi değeri geri döner.\
\
Dikkat Edilecek Hususlar\
Parametre olarak verilen değer mutlaka Number formatındaki bir ifade olması gerekmektedir.\
\
Örnek

```
  Dim sonuç As Number
  Dim sayı As Number
  sayı:=15
  sonuç:= Null2Zero(sayı)
  MessageBox(STR(sonuç),"Sonuç 15 olmalı",MB_OK)
  SetNull(@sayı) 'sayıyı Null yapalım
  sonuç:= Null2Zero(sayı1)
  MessageBox(STR(sonuç),"Sonuc 0 (sıfır )  olmalı",MB_OK)
```
