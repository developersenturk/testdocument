# Equals := Operatörü

Bu operatör değişkenlere değer atama işleminde kullanılmaktadır.\
**Kullanımı**\
\<değişken> := \<içerik>\
**Açıklama**\
Atama işlemlerinde operatörün sağında değişken tipi, solunda ise o değişkene vermek istediğimiz değer yer almaktadır.\
Bir değişkene, bir içerik ataması yapıldığında , o değişkenin eski değeri kaybolmakta ve yerini yeni değere bırakmaktadır.\
Değişkenin türü atanan ifade ile aynı olmalıdır. Yani değişken sayısal ise ifadenin de sayısal, mantıksal ise mantıksal, karakter ise karakter olması gerekir.\
**Örnek**

```
Function F()
  Dim sonuç As Number
  Dim sayı1 As Number
  Dim mesaj As String
  sayı1:= 100
  sonuç:= 50*sayı1
  mesaj:= "Sonuç sayısının içeriği " & Str(sonuç) & " dir."
  MessageBox(mesaj, "Örnek Uygulama", MB_OK)
EndFunction
```

\
**Örnek Açıklaması**\
Sayı1 değişkenine 100 değeri atanmakta ve daha sonra da sonuç değişkenine, sayı1 değişkeni ile 50 sayısı çarpılarak başka bir atama işlemi gerçekleştirilmektedir.
