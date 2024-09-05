# Date2Serial

Bu fonksiyon tarih olarak aldığı bir değişkeni, sayısal bir ifadeye dönüştürmektedir.\
\
Kullanımı

```
Function Date2Serial(
  D As Date  ' işlem görecek ifade
)As Number
```

Parametreler\
D\
Sayısal olarak ifade edilecek tarih bilgisi.\
\
Geri Dönüş Değeri\
Geri dönüş değeri fonksiyondan çıkış olarak beklediğimiz bir sayıdır.\
\
Dikkat Edilecek Hususlar\
Bu fonksiyonun kullanımı ile herhangi bir tarih bilgisini sayısal bir ifadeye dönüştürebilmekteyiz. Bunun sonucunda 2 tarih arasındaki farkları hesaplama veya belli bir gün sonraki tarihi belirleme gibi uygulamaları gerçekleştirebiliriz.\
\
Eğer tarih değişkenini yanlış verirseniz fonksiyon geri dönüş değeri olarak 0 (sıfır) sayısını geri döndürecektir.\
\
Başka bir nokta da 1 Ocak 1980 tarihi sayısal olarak başlangıç 1 değerine sahiptir, bu yüzden bundan önceki tarihlerin sayısal olarak karşılıkları 1 olarak gelecektir. Üst limit olarak ise 31 Aralık 2049 tarihi en büyük elde edilebilecek sayısal değere sahiptir.\
\
Örnek\


```
  Dim d As Date
  d:= Serial2Date(Date2Serial(Str2Date("19/02/1996")) + 50)
  MessageBox(Date2Str(d),"19 Şubat'tan 50 gün sonrası",MB_OK)
```

Örnek Açıklaması\
"19/02/1996" karakter ifadesi, bu fonksiyonla tarih tipine dönüştürüldükten sonra, bu tarih tipi Date2Serial() fonksiyonu ile sayısal hale getirilmektedir. Daha sonra 50 gün sonrası için toplama işlemi gerçekleştirilmekte ve sonuçta elde edilen sayı tekrar tarihsel şekle dönüştürülmektedir. Elde edilen tarih değişkeni MessageBox ile ekranda gösterilmektedir.
