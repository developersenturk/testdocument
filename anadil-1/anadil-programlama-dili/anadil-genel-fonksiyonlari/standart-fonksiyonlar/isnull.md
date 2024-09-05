# IsNull

Bu fonksiyon bir değişkenin içeriğinin NULL olup olmadığını test etmektedir.\
\
Kullanımı

```
Function IsNull(
  Var As Type  ' işlem görecek ifade
)As Bool
```

Parametreler\
_Var_\
NULL olup olmadığı kontrol edilecek değişkendir. String, Number veya Date olabilmektedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri Boolean olup eğer değişkenin içeriği NULL ise True olmakta, aksi durumda False olarak gerçekleşmektedir.\
\
Dikkat Edilecek Hususlar\
Fonksiyona parametre olarak verilen içeriği NULL olup olmadığı test edilecek ifade mutlaka _String, Number_ veya _Date_ olmalıdır.\
\
Örnek

```
Function F()
  Dim temp As Number
  temp:= 100
  MessageBox(Str(temp), "Önce", MB_OK+MB_ICONINFORMATION)
  SetNull(@temp)
  If IsNull(temp) Then
    MessageBox("Değişkenin içeriği NULL.", #
               "Sonra", #
    MB_OK+MB_ICONINFORMATION)
  EndIf
EndFunction
```

Örnek Açıklaması\
Burada bir sayı değişkeni içeriği 100 olarak eşitlenmekte daha sonra da içeriği NULL yapılmaktadır. En son kısımda da içeriğin NULL olması kontrol edilmekte ve sonuç son kullanıcıya gösterilmektedir.
