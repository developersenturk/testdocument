# Format

Bu property grid sütunlarında yer alan hücrelerde yer alan bilgilerin genel görünüm formatını belirlemektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Sadece yazılabilir bir özelliktir.\
\
**Kullanımı**

```
GridColObject.Format As String
```

\
**Dikkat Edilecek Noktalar**\
Verilerin kullanıcı karşısına gelirken bazı ön düzenlemelerden geçirilip sunulması, bilginin sayılar için yuvarlanması, para ile ilgili işlemlerde okumayı kolaylaştırması, string ile yapılan işlemlerde de kısaltmalar sunması gibi faydaları vardır.\
\
Format spesifikasyonu verilirken, _"Harf;Sayı"_ şeklinde string ifade kullanılmaktadır. Yani property değeri için veri tipini belirten ilgili harf ardından, noktalı virgül gelmekte ve daha sonra format tipi hakkında diğer sayı bilgisi olarak yazılmaktadır.\
\
Farklı veri tipleri için "format" property değeri aşağıda sunulan şekillerde uygulanmaktadır:\
\


* String(karakter dizisi) için "s;x" ,
* Number(sayı) için "n;x" ,
* Money(para birimi) "m;x" ,
* Date(tarih) için "d".
* String formatı kullanılmak istenildiğinde; s harfinin ardından gelen sayı bilgisi, string'in alabileceği max uzunluk değeridir. Yani sonuç ifade max bu uzunlukta olacak, fazlası kesilecektir.

Örneğin "s;20" format şekli, giriş variant bilgisini string olarak max 20 uzunlukta olacak şekilde dönüştürecektir. Eğer sadece "s" şeklinde, karakter sayısı olmadan verilirse limit değeri, string uzunluğu için max değer olan 255 olacaktır.\
\
Number(sayı) formatı kullanılırken; n harfinin ardından verilen sayı değeri ondalık kısımdan sonraki istenilen basamak sayısını belirtmektedir. Ondalık kısım tam sayı kısmından nokta ile ayrılmaktadır. Ayrıca ondalık kısımdan atma işlemi yapılırken yuvarlama işlemi de gerçekleşmektedir.\
\
Örneğin "n;3" şeklindeki format bilgisi sayının noktadan sonra 3 basamak olacak şekilde gösterileceğini belirtmektedir. Sayının ondalık kısmı arzu edilen basamak sayısından küçükse, diğer basamaklar 0 olarak gösterilecektir.\
\
Eğer "n" veya "n;x" şeklinde format belirtilirse sayı gerektiği kadar ondalık basamak sayısı ile gösterilecek ancak ondalık kısımdaki en sağdaki sıfırlar atılacaktır. Normalde Always® sayı tipindeki değişkenleri, default olarak, noktadan sonra 6 tane sıfır olacak şekilde ele almaktadır.\
\
Ondalık basamak sayısı en fazla 6 olmasına reğmen eğer 6'dan büyük bir sayı formatlama parametresi olarak verilirse, parametrenin değeri 6 şeklinde değerlendirilecektir.\
\
Money formatlama şekli kullanılmak istenildiğinde ise yukarıda sıralanan Number(sayı) için geçerli kurallar uygulanmaktadır. Sadece uygulamadaki farkı sayının tamsayı kısmında, her 3 basamak virgüller ile ayrılmaktadır.\
\
Örnek olarak 132455.987 sayısı "m;2" ile formatlanacak olursa 132,455.99 şeklinde sonuç değeri elde edilebilmektedir.\
\
Son olarak Date(tarih) şeklindeki bir variant bilgisini string bir değere formatlarken, sadece "d" şeklinde format spesifikasyonu yeterli olmakta, izleyen ikinci bir sayı değeri bulunmamaktadır.
