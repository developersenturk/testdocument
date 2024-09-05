# Null2Space

Bu fonksiyon String tipindeki bir değişkenin değeri NULL ise space döndürür değilse değişkenin kendi string değerini döndürür.\
\
Kullanımı

```
Function Null2Space(
  S As String  ' işlem görecek ifade
)As String
```

Parametreler\
S\
NULL olup olmadığı kontrol edilecek String tipindeki değişken.\
\
Geri Dönüş Değeri\
S parametresinin değeri NULL ise geri dönüş değeri space dir. Null değilse S parametresinin kendi string değeri geri döner.\
\
Dikkat Edilecek Hususlar\
Parametre olarak verilen değer mutlaka String tipindeki bir ifade olması gerekmektedir.\
\
Örnek

```
  Dim sonuç As String
  Dim s As String
  s:="text"
  sonuç:= Null2Space(s)
  MessageBox(sonuç,"Sonuç text olmalı",MB_OK)
  SetNull(@s) ' Null yapalım
  sonuç:= Null2Space(s)
  MessageBox(sonuç,"Sonuc space olmalı",MB_OK)
```
