# GetUserNumberEx

Bu fonksiyon Registry veri tabanında HKEY\_CURRENT\_USER altındaki bir anahtar saha içersindeki entry sayı bilgisinin değerini vermektedir.\
\
**Kullanımı**

```
Function GetUserNumber(
  Path As String,		' entry yol bilgisi
  Default As Number		' default değer
)As Number
```

**Parametreler**\
_Path_\
HKEY\_CURRENT\_USER altında saklanan entry bilgisinin yol ifadesi\
_Default_\
HKEY\_CURRENT\_USER altında saklanan entry bilgisinin bulunamaması durumunda elde edilecek geri dönüş değeridir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri öğrenmek istediğimiz entry bilginin içeriğidir.\
\
**Dikkat Edilecek Hususlar**\
Fonksiyon kullanımı ile ilgili olarak GetUserNumber() fonksiyonu ile aynı kısıtlar geçerlidir.\
Bilindiği üzere GetUserNumber() fonksiyonu kullanımında HKEY\_CURRENT\_USER altında istenilen entry ifade bulunamadığında fonksiyon geri dönüş değeri olarak 0(sıfır) vermekteydi. Bu fonksiyon ise bu tür bir durumda geri dönüş değerini Default parametresi ile verilen sayı olarak vermektedir.
