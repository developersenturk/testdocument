# Format

Bu property kontrol nesnelerinin kullanıcıya bilgi sunarken, bilginin hangi şekilde gösterileceğini belirlemektedir.\
\
**Uygulandığı Nesneler**\
Edit-box ve Static kontrol nesneleri.\
\
**Uygulama Biçimi**\
Hem okunabilir hem de yazılabilir bir property'dir.\
\
**Kullanımı**

```
ControlObject.Format As String
```

\
**Dikkat Edilecek Noktalar**\
Verilerin kullanıcı karşısına gelirken bazı ön düzenlemelerden geçirilip sunulması, bilginin sayılar için yuvarlanması, para ile ilgili işlemlerde okumayı kolaylaştırması, string ile yapılan işlemlerde de kısaltmalar sunması gibi faydaları vardır.\
\
Format spesifikasyonu verilirken, _"Harf;Sayı"_ şeklinde string ifade kullanılmaktadır. Yani "format" property'si için veri tipini belirten ilgili harf ardından, noktalı virgül gelmekte ve daha sonra format tipi hakkında diğer sayı bilgisi olarak yazılmaktadır.\
\
Farklı veri tipleri için "format" property aşağıda sunulan şekillerde uygulanmaktadır:\
\


* String(karakter dizisi) için "s;x" ,
* Number(sayı) için "n;x" ,
* Money(para birimi) "m;x" ,
* Date(tarih) için "d".
* Maske(string, sayı, para birimi, date) için "x;0(###) ### ## ##" benzeri yapılar kullanılmaktadır.
* String formatı kullanılmak istenildiğinde; s harfinin ardından gelen sayı bilgisi, string'in alabileceği max uzunluk değeridir. Yani sonuç ifade max bu uzunlukta olacak, fazlası kesilecektir.

Örneğin "s;20" format şekli, giriş variant bilgisini string olarak max 20 uzunlukta olacak şekilde dönüştürecektir. Eğer sadece "s" şeklinde, karakter sayısı olmadan verilirse max limit değeri 255 olacaktır.\
\
Number(sayı) formatı kullanılırken; n harfinin ardından verilen sayı değeri ondalık kısımdan sonraki istenilen basamak sayısını belirtmektedir. Ondalık kısım tamsayı kısmından nokta ile ayrılmaktadır. Ayrıca ondalık kısımdan atma işlemi yapılırken yuvarlama işlemi de gerçekleşmektedir.\
\
Örneğin "n;3" şeklindeki format bilgisi sayının noktadan sonra 3 basamak olacak şekilde gösterileceğini belirtmektedir. Sayının ondalık kısmı arzu edilen basamak sayısından küçükse, diğer basamaklar 0 olarak gösterilecektir.\
\
Eğer "n" veya "n;x" şeklinde format belirtilirse sayı gerektiği kadar ondalık basamak sayısı ile gösterilecek ancak ondalık kısımdaki en sağdaki sıfırlar atılacaktır. Bilindiği üzere Always® sayı tipindeki değişkenleri, öndeğer olarak, noktadan sonra 6 tane sıfır olacak şekilde ele almaktadır.\
\
Ondalık basamak sayısı en fazla 6 olmasına reğmen eğer 6'dan büyük bir sayı formatlama parametresi olarak verilirse, parametrenin değeri 6 şeklinde değerlendirilecektir.\
\
Money formatlama şekli kullanılmak istenildiğinde ise yukarda sıralanan Number(sayı) için geçerli kurallar uygulanmaktadır. Sadece uygulamadaki farkı sayının tam sayı kısmında her 3 basamak virgüller ile ayrılmaktadır.\
\
Örnek olarak 132455.987 sayısı "m;2" ile formatlanacak olursa 132,455.99 şeklinde sonuç değeri elde edilebilmektedir.\
\
Son olarak date(tarih) şeklindeki bir variant bilgisini string bir değere formatlarken, sadece "d" şeklinde format spesifikasyonu yeterli olmakta, başka bir parametresi bulunmamaktadır.\
\
**Maske kullanım örnekleri**\
Format ifadesi x veya X karakteri ile başlıyorsa maske olduğu anlaşılmaktadır. Maske kullanımı Editbox kontrollerinde geçerlidir. Grid hücrelerinde kullanıma açılmamıştır. Maske ifadesinde sayısal karakter için #, her türlü harf için ? ve sabit herhangi bir rakam veya harf kullanabiliriz.

```
# : Nümerik karakter girilebilir
? : Alfanümerik (Hem alfabetik hem de nümerik) karakter girilebilir.
_ : PlaceHolder : Silinen karakterlerin yerine Always bu karakteri yerleştirecektir.
	      Format belirleme sırasında öndeğer olarak "_" karakteri atanır.
	      f.mut_no.PlaceHolder:='%' methodu ile değiştirilebilir.

Telefon bilgisi girişi maske örneği : 0 (###) ### ## ##

 'form üzerinde mut_no alanının formatı maske olarak ifade ediliyor
  f.mut_no.format:="x;(0###) ### ## ##"
 
  'Maske üzerine atama yapılıyor ekranda ve terminalde (0123) 456 78 __ olarak görülecektir. 
  f.mut_no.ValueStr:="12345678"

  'Terminale yazdırılıyor
  outm(" ******  f.mut_no.ValueStr : " & f.mut_no.ValueStr)

 örnek2 : (A###) (B???) (C445)
 (A___) (B___) (C445) şeklinde giriş yapılabilir ve (A213) (B567) (C445) giriş örneği olabilir.

IP Maske örneği:
f.mut_no.format:="x;###.###.###.###"

Date Time maske örneği:
"x;##/##/200# ##:##:##.##"
Bu maske örneğinde girilen değer  "10/10/2005 23:59:59.30" şeklinde olabilir. 
Girilen bölümlerin doğruluk testi Anadil bölümünde yapılmalı. 
Örneğin Ay alanına girilen değerin 1-12 arasında olduğunu garanti etmek size düşmektedir.
```

**İlgili komutlar: PlaceHolder Property Format fonksiyonu**
