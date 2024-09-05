# GetDayCount

Bir ayın kaç gün çektiğini belirtir.\
\
Kullanımı

```
Function GetDayCount(
  Year As Number    ' yıl
  Month As Number   ' ay
)As Number
```

Parametreler\
_Year_\
Bir ayındaki gün sayısı istenen yıl\
_Month_\
Gün sayısı istenen ay\
\
Geri Dönüş Değeri\
Geri dönüş değeri, istenen ayın kaç gün çektiğini belirten sayıdır.\
\
Dikkat Edilecek Hususlar\
Bu fonksiyon ile ay ve yılı verilen, bir ayın kaç günden oluştuğu şeklindeki bilgi, sayı şeklinde elde edilmektedir.

```
Dim Result As Number
 
 result := GetDayCount(1997,2)
 result = 28
```
