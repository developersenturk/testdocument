# AND Operatörü

Bu operatör iki mantıksal ifade arasında, mantıksal AND işlemi uygulamaktadır.\
**Kullanımı**\
sonuç\_ifade := \<mantıksal\_ifade1> AND \<mantıksal\_ifade2>\
**Açıklama**&#x20;

VE operatörü mantıksal ifadelerde ve kontrol deyimlerinde kullanılan bir operatördür. Aşağıdaki tabloda işlem sonunda oluşan sonuç ifadenin değişimi gösterilmiştir:\
\
Tablodan da görüldüğü gibi sonucun True olarak oluşabilmesi için her iki ifadenin de True içeriğe sahip olması gerekmektedir.\
\
**Örnek**

```
Function F()
  Dim sayı1 As Number
  Dim sayı2 As Number
  Dim sonuç As Boolean
  sayı1:= 3
  sayı2:= 8
  sonuç:= sayı1=5 AND sayı2<10
  

  If sonuç Then
    MessageBox("Karşılaştırmaların ikisi de DOĞRU","",MB_OK)
  Else
    MessageBox("En az biri YANLIŞ","",MB_OK)
  EndIf
EndFunction
```

**Örnek Açıklaması**\
Yukarıdaki örnek uygulamada sayı1, sayı2 değişkenlerine sıra ile 3 ve 8 değerleri atanarak bir karşılaştırma işlemi uygulanmaktadır. Daha sonra ise AND operatörü ile karşılaştırmaların sonuçları mantıksal çarpma işlemine tabi tutulmaktadır. Son olarak ise işlemin sonucuna ilişkin bilgi mesajı Always® terminalinde görüntülenmektedir.
