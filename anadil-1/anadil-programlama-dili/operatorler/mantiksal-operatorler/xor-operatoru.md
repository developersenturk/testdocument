# XOR Operatörü

Bu operatör iki mantıksal ifade arasında mantıksal XOR işlemini uygulamaktadır.\
**Kullanımı**\
sonuç\_ifade := \<mantıksal\_ifade1> XOR \<mantıksal\_ifade2>\
**Açıklama**\
XOR operatörü mantıksal ifadelerde ve kontrol deyimlerinde kullanılan bir operatördür. Aşağıdaki tabloda işlem sonunda oluşan sonuç ifadenin değişimi gösterilmiştir:\


| ifade1 | ifade2 | sonuç\_ifade |
| ------ | ------ | ------------ |
| True   | True   | False        |
| True   | False  | True         |
| False  | True   | True         |
| False  | False  | False        |

\
Tablodan da görüldüğü gibi işlem sonucunun True olarak oluşabilmesi için ifadelerden mutlaka birbirinden farklı olması gerekmektedir.\
\
**Örnek**

```
Function F()
 Dim sayı1 As Number
 Dim sayı2 As Number
 Dim sayı3 As Number
  sayı1:= 6
  sayı2:= 8
  sayı3:= 10
  If sayı1<sayı2 XOR sayı2>sayı3 Then
    MessageBox("Bir tanesi DOĞRU","",MB_OK)
  Else
    MessageBox("İkisi de DOĞRU veya ikisi de YANLIŞ","",MB_OK)
  EndIf
EndFunction
```

**Örnek Açıklaması**\
Yukardaki örnek uygulamada ilk etapta sayı1, sayı2, sayı3 değişkenlerine sıra ile 6, 8, 10 değerleri atanır. Daha sonra bir karşılaştırma işlemi uygulanmakta ve karşılaştırmaların sonuçları XOR operatörü ile birleştirilmektedir. Son olarak ise işlemin sonucuna ilişkin bilgi mesajı Always® terminalinde görüntülenmektedir.
