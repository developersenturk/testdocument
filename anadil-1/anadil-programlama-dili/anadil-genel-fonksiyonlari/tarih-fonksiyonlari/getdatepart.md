# GetDatePart

Bu fonksiyon verilen tarihin içinden, yıl, ay, gün, hafta no, hafta gün sayısı gibi, istenilen tarih bölümünü rakam olarak geri döndürür. yapmaktadır.\
\
Kullanımı

```
Function GetDatePart(
  D As Date         ' tarih bilgisi
  Option As Number  ' istenilen tarih detay bilgisi
)As Number
```

Parametreler\
D\
Fonksiyona input olarak verilen tarih bilgisidir.\
_Option_\
Öğrenilmek istenilen, tarihe ait özel bilgi çeşidini belirleyen sabit sayıdır. Bu parametre:

* yıl bilgisi için DP\_YEAR,
* ay bilgisi için DP\_MONTH,
* gün bilgisi için DP\_DAY,
* hafta bilgisi için DP\_WEEK,
* haftanın günü bilgisi için DP\_DAYOFWEEK

şeklinde verilmelidir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri, giriş tarih değişkeninin detay bilgisidir. Bu bilginin çeşidi yıl bilgisi, ay bilgisi, gün bilgisi veya haftanın hangi günü olduğuna dair bilgidir.\
\
Dikkat Edilecek Hususlar\
Bu fonksiyon ile verilen bir tarihin, ayrı ayrı parçaları olan yıl bilgisi, ay bilgisi, gün bilgisi veya haftanın hangi gününe ait olduğu şeklindeki bilgi, sayı şeklinde elde edilmektedir.\
\
Haftanın gününe ait olarak bilgi istenmesi durumunda ise, fonksiyon geri dönüş değeri olarak, 0 ile 6 arasında bir sayı elde edilmektedir. 0 sayısı ise Pazar gününe; 1 sayısı Pazartesi gününe, 2 sayısı Salı gününe v.b. denk gelmek üzere, hafta günü bilgisi oluşturulmaktadır.
