# EQV Operatörü

Bu operatör iki mantıksal ifadenin denk olmasını test etmektedir.\
**Kullanımı**\
sonuç\_ifade := \<ifade1> EQV \<ifade2>\
**Açıklama**\
Bu operatörün kullanımı ile mantıksal ifadelerin karşılaştırılması sonucunda aşağıdaki tablodaki kriterlere göre sonuç mantıksal ifadesi oluşmaktadır.\
\
Ayrıca karşılaştırma işleminde number(sayısal) veya string(karakter dizisi) olan ifadeler EQV ile test edilebilir.\
\
Örnek

| ifade1 | ifade2 | sonuç\_ifade |
| ------ | ------ | ------------ |
| True   | True   | True         |
| True   | False  | False        |
| False  | True   | False        |
| False  | False  | True         |

```
Function F()
  Dim sayı1 As Number
  Dim sayı2 As Number
  Dim sayı3 As Number
  sayı1:= 10
  sayı2:= 8
  sayı3:= 6
  If sayı1>sayı2 EQV sayı2>sayı3 Then
    MessageBox("İfadeler birbirine denk.","",MB_OK)
  Else
    MessageBox("İki ifade denk değil.","",MB_OK)
  EndIf
EndFunction
```

\
**Örnek Açıklaması**\
Yukardaki örnek uygulamada sayı1, sayı2, sayı3 değişkenlerine sıra ile 10, 8 ve 6 değerleri atanmakta ve EQV operatörü ile karşılaştırma işlemlerinin denkliği test edilmektedir. Her iki ifade de doğru olduğu için sonuç True olarak oluşmakta ve sonuçla ilgili bilgi mesajı Always® terminalinde görüntülenmektedir.
