# IsNum

Bu fonksiyon bir değişkenin içeriğinin NUMBER olup olmadığını test etmektedir.\
\
Kullanımı

```
Function IsNum(
  Var As Type  ' işlem görecek ifade
)As Bool
```

Parametreler\
_Var_\
NUMBER olup olmadığı kontrol edilecek değişkendir. String, Number veya Date olabilmektedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri Boolean olup eğer değişkenin içeriği NUMBER ise True olmakta, aksi durumda False olarak gerçekleşmektedir.\
\
Dikkat Edilecek Hususlar\
Fonksiyona parametre olarak verilen içeriği NUMBER olup olmadığı test edilecek ifade mutlaka _String, Number_ veya _Date_ olmalıdır.\
\
Örnek

```
Function F()
  Dim temp As Number
  temp:= 100
  MessageBox(Str(temp), "Önce", MB_OK+MB_ICONINFORMATION)
  SetNull(@temp)
  If IsNum(temp) Then
    MessageBox("Değişkenin içeriği NUMBER.", #
               "Sonra", #
    MB_OK+MB_ICONINFORMATION)
  Else
    MessageBox("Değişkenin içeriği NUMBER DEĞİL", #
               "Sonra", #
    MB_OK+MB_ICONINFORMATION)
  EndIf
EndFunction
```

Örnek Açıklaması\
Burada bir sayı değişkeni içeriği 100 olarak eşitlenmekte daha sonra da içeriği NULL yapılmaktadır. En son kısımda da içeriğin NUMBER olması kontrol edilmekte ve sonuç son kullanıcıya gösterilmektedir.
