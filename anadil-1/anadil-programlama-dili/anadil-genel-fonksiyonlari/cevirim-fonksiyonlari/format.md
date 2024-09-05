# Format

Bu fonksiyon herhangi bir variant için string şeklinde bir format belirlemektedir.\
\
Kullanımı

```
Function Format(
  Var As Variant        ' işlem görecek variant
  FormatSpec As String  ' istenilen format bilgisi
)As String
```

Parametreler\
_Var_\
Formatı belirlenecek olan variantdır.\
_FormatSpec_\
Variant için istenilen format şeklidir. Genel olarak 4 çeşit format şekli vardır:\


* String için "s;x",
* Number(sayı) için "n;x",
* Money(para birimi) "m;x",
* Date(tarih) için "d;x" kullanılmaktadır.
* Maske(string, sayı, para birimi, date) için "x;0(###) ### ## ##" benzeri yapılar kullanılmaktadır.
* Geri Dönüş Değeri

Geri dönüş değeri fonksiyondan string olarak istediğimiz format şeklindedir.\
\
Dikkat Edilecek Hususlar\
Always variant'lar ile çalışırken içeriklerinin ne olduğu ile ilgilenmemektedir. Genel anlamda bir variant 3 çeşit değişken saklayabilmektedir. Bunlar string, number(sayı) ve date tipindedir. Bir variant'ın içeriğinin Null olması ise tamamen run-time ile ilgili bir işlemdir.\
\
Format spesifikasyonu belirtilirken genel olarak _Harf;Sayı_ şeklinde string olarak verilmelidir. Yani Format tipi için ilgili harf ardından noktalı virgül ve izleyen format tipi hakkında diğer sayı bilgisi olarak yazılmalıdır.\
\
String formatı kullanılmak istenildiğinde; s harfinin ardından gelen sayı bilgisi, string'in alabileceği max uzunluk değeridir. Yani sonuç ifade max bu uzunlukta olacak fazlası kesilecektir.\
\
Örneğin "s;20" format şekli, giriş variant bilgisini string olarak max 20 uzunlukta olacak şekilde dönüştürecektir. Eğer sadece "s" şeklinde karakter sayısı olmadan verilirse max limit değeri 255 olacaktır.\
\
Number(sayı) formatı kullanılırken; n harfinin ardından verilen sayı değeri ondalık kısımdan sonraki istenilen basamak sayısını belirtmektedir. Ondalık kısım tam sayı kısmından nokta ile ayrılmaktadır. Ayrıca ondalık kısımdan atma işlemi yapılırken yuvarlama işlemi de gerçekleşmektedir.\
\
Örneğin "n;3" şeklindeki format bilgisi sayının noktadan sonra 3 basamak olacak şekilde gösterileceğini belirtmektedir. Sayının ondalık kısmı arzu edilen basamak sayısından küçükse, diğer basamaklar 0 olarak gösterilecektir.\
\
Eğer "n" veya "n;x" şeklinde format belirtilirse sayı gerektiği kadar ondalık basamak sayısı ile gösterilecek ancak ondalık kısımdaki en sağdaki sıfırlar atılacaktır. Bilindiği üzere Always® sayı tipindeki değişkenleri, default olarak, noktadan sonra 6 tane sıfır olacak şekilde ele almaktadır.\
