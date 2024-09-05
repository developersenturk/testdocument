# OR Operatörü

Bu operatör iki mantıksal ifade arasında mantıksal OR işlemini uygulamaktadır.\
**Kullanımı**\
sonuç\_ifade := \<mantıksal\_ifade1> OR \<mantıksal\_ifade2>\
**Açıklama**\
OR operatörü mantıksal ifadelerde ve kontrol deyimlerinde kullanılan bir operatördür. Aşağıdaki tabloda işlem sonunda oluşan sonuç ifadenin değişimi gösterilmiştir:

| ifade1 | ifade2 | sonuç\_ifade |
| ------ | ------ | ------------ |
| True   | True   | True         |
| True   | False  | True         |
| False  | True   | True         |
| False  | False  | True         |

\
Tablodan da görüldüğü gibi işlem sonucunun True olarak oluşabilmesi için ifadelerden en az birisinin True içeriğe sahip olması yeterlidir.\
\
**Örnek**

```
Function F()
 Dim sayı1 As Number
 Dim sayı2 As Number
 Dim sonuç As Boolean
  sayı1:= 3
  sayı2:= 8
  sonuç:= sayı1=5 VEYA sayı2<10
  If sonuç Then
    MessageBox("Karşılaştırmalardan en az biri DOĞRU", 
    		  "",MB_OK)
  Else
    MessageBox("İkisi de YANLIŞ","",MB_OK)
  EndIf
EndFunction
```

**Örnek Açıklaması**\
Yukarıdaki örnek uygulamada sayı1, sayı2 değişkenlerine sıra ile 3 ve 8 değerleri atanarak bir karşılaştırma işlemi uygulanmaktadır. Daha sonra ise OR operatörü ile karşılaştırmaların sonuçları mantıksal toplama işlemine tabi tutulmaktadır. Son olarak ise işlemin sonucuna ilişkin bilgi mesajı Always® terminalinde görüntülenmektedir.
