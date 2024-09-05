# MoneyToTextEx

Bu fonksiyon verilen sayıyı ve ondalık bölümünü, yazıyla yazmaya yarar. YTL-TRL değişikliklerinde kodları değiştirmemek için, YTL ve Kuruş gibi string ifadeleri firma tanımdan almalısınız.\
\
Kullanımı

```
Function MoneyToTextEx(
  Money  As Number 'money formatında bir sayı
  nDigit  As Number   'ondalık hane sayısı
  @szOndalik  'ondalık bölümün geri dönen string ifadesi
)As String
```

Parametreler\
_Money_\
Yazıyla yazılacak para değeri\
\
_nDigit_\


```
Ondalık hane sayısı. Örneğin 426.345 rakamı için .345 .35 olarak yuvarlanır ve 426.35 olarak ifade edilir.
Hane sayısı 1 ise, 1-  9 arası rakamlar string olarak ifade edilir
Hane sayısı 2 ise, 1- 99 arası rakamlar string olarak ifade edilir
Hane sayısı 3 ise, 1-999 arası rakamlar string olarak ifade edilir
```

\
_szOndalik_\
Ondalık bölümün string ifadesi döner. Yukarıdaki örnekte "OtuzBeş" ifadesi bu değişken ile geri döner.\
\
Geri Dönüş Değeri\
Verilen rakamın integer bölümünün string ifadesi geri döner. Örnek:

```
 Dim n as Number
 Dim n1 as Number
 Dim o as Number
 Dim str as String
 Dim szKurus as String

 n:=12345678.1235
 str:=MoneyToText(n)
 outm(str(n)&" str : "&str)
12345678.1235 str : OnİkiMilyonÜçYüzKırkBeşBinAltıYüzYetmişSekiz YTL OnİkiKrş.

 szKurus:=""
 str:=MoneyToTextEx(n, 2, @szKurus)
 outm(str(n)&" str : "&str&" YTL "&szKurus&"Kuruş")
12345678.1235 str : OnİkiMilyonÜçYüzKırkBeşBinAltıYüzYetmişSekiz YTL OnİkiKuruş

 n:=12345678.125
 str:=MoneyToText(n)
 outm(str(n)&" str : "&str)
12345678.125 str : OnİkiMilyonÜçYüzKırkBeşBinAltıYüzYetmişSekiz YTL OnÜçKrş

 szKurus:=""
 str:=MoneyToTextEx(n, 2, @szKurus)
 outm(str(n)&" str : "&str&" YTL "&szKurus&"Kuruş")
12345678.125 str : OnİkiMilyonÜçYüzKırkBeşBinAltıYüzYetmişSekiz YTL OnÜçKuruş
```

\
\
Dikkat Edilecek Hususlar\
Bu fonksiyon verilen sayıyı, yazıyla yazmaya yarar. Dili Türkçedir. YTL ile birlikte sisteme eklenmiştir. YTL ve Kuruş veya Krş ifadelerinin firma tanımlarından alınarak kullanılması tavsiye edilir.\
