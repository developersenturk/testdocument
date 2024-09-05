# GetUserStringEx

Bu fonksiyon Registry veri tabanında HKEY\_CURRENT\_USER altındaki bir anahtar saha içersindeki entry dahilindeki karakter bilginin değerini vermektedir.

\
**Kullanımı**

```
Function GetUserString(
  Path As String,		' entry yol bilgisi
  Default As String		' default değer
) As String
```

**Parametreler**\
_Path_\
HKEY\_CURRENT\_USER altında saklanan entry bilgisinin yol ifadesi\
_Default_\
HKEY\_CURRENT\_USER altında saklanan entry bilgisinin bulunaması durumunda geri dönüş değeri olarak elde edilecek değerdir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri öğrenmek istediğimiz entry bilginin içeriğidir.\
\
**Dikkat Edilecek Hususlar**\
Fonksiyon kullanımı ile ilgili olarak GetUserString() fonksiyonu ile aynı kısıtlar geçerlidir.\
\
Bilindiği üzere GetUserString() fonksiyonu kullanımında HKEY\_CURRENT\_USER altında istenilen entry ifade bulunamadığında fonksiyon geri dönüş değeri olarak "" (boş string) vermekteydi. Bu fonksiyon ise bu tür bir durumda geri dönüş değerini Default parametresi ile verilen string olarak vermektedir.
