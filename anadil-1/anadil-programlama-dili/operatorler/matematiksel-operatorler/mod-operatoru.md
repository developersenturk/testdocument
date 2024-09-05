# MOD Operatörü

Bu operatör bir sayısal ifadenin belli bir sayıya göre modunu almaktadır.\
**Kullanımı**\
\<atanacak\_değer> := \<sayısal\_ifade1> MOD \<sayısal\_ifade2>\
**Açıklama**\
Mod alma işleminde elde edilen sonuç ifade, birinci sayısal ifadenin ikinci sayısal ifadeye tam bölünmesiyle ortaya çıkan kalan değeridir.\
İşlemde mutlaka sayısal ifadeler kullanılmalıdır ve işlem sonucunda elde edilen sonuç değeri yine sayısal bir ifadedir.\
Başka önemli bir nokta ise verilen ikinci sayısal ifade mutlaka 0'dan farklı olmalıdır.\
\
**Örnek**

```
Function F()
  Dim sayı1 As Number
  Dim sayı2 As Number
  Dim sonuç As Number
  sayı1:= 50
  sayı2:= 7
  sonuç:= sayı1 MOD sayı2
  MessageBox(Str(sonuç), "Sonuç Değeri", MB_OK)
EndFunction
```

**Örnek Açıklaması**\
Yukarıdaki örnek uygulamada ilk etapta sayı1 değişkenine 50, sayı2 değişkenine de 7 değeri atanmaktadır. Daha sonra ise 50 sayısının 7 sayısına göre MOD değeri elde edilmektedir. Son olarak ise elde edilen sonuç değeri MessageBox fonksiyonu ile Always® terminalinde görüntülenmektedir.
