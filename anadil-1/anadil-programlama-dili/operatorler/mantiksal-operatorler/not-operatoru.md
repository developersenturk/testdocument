# NOT Operatörü

Bu operatör mantıksal ifadelerle yapılan işlemlerde ifadenin değerini ters çevirmektedir.\
**Kullanımı**\
\<atanacak\_değer> := NOT \<ifade>\
**Açıklama**\
Eğer mantıksal ifadelerin değeri True ise NOT operatörü sayesinde False olarak çevrime uğramaktadır. Aksi durumda ise içeriği False olan mantıksal ifadeler True şeklinde işlem görmektedir.\
Bazı durumlarda, özellikle IF yapılarında veya DÖNGÜ'lerle yapılan işlemlerde, olumsuzluğa dayalı program işleyişi oldukça etkili olabilmektedir.\
\
**Örnek**

```
Function F()
  Dim sayı1 As Number
  Dim sayı2 As Number
  sayı1:= 10
  sayı2:= 20
  If NOT sayı1 = sayı2 Then
    MessageBox("Sayı1 ile sayı2 eşit değil","",MB_OK)
  Else
    MessageBox("Sayı1 ile sayı2 eşit","",MB_OK)
  EndIf
EndFunction
```

**Örnek Açıklaması**\
Yukardaki örnek uygulamada sayı1, sayı2 değişkenlerine sıra ile 10 ve 20 değerleri atanmakta ve bir karşılaştırma işlemi uygulanmaktadır. İşlem sırasında ise NOT operatörü ile sonuç mantıksal ifadesinin değeri tersine çevrilmektedir. Burada gerçek sonuç mantıksal False olmasına rağmen True olarak işlem görmektedir.
