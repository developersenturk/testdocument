# MoneyToText

Bu fonksiyon verilen sayıyı, yazıyla yazmaya yarar. Always Rel394 ile birlikte bu fonksiyon verilen rakamın tam sayı bölümünü YTL olarak, ondalık bölümünü ise Kuruş olarak geri vermektedir. Ondalık bölümde digit sayısı 2 dir. 3. digit 5 veya daha büyük ise 2. digit yukarıya yuvarlanır.\
\
Kullanımı

```
Function MoneyToText(
  Money  'money formatında bir sayı
)As String
```

Parametreler\
_Money_\
Yazıyla yazılacak para değeri

```
12345678.125  rakamı için geri dönen örnek:
OnİkiMilyonÜçYüzKırkBeşBinAltıYüzYetmişSekiz YTL OnÜçKrş.
```

\
Dikkat Edilecek Hususlar\
Bu fonksiyon verilen sayıyı, yazıyla yazmaya yarar. Dili Türkçedir.
