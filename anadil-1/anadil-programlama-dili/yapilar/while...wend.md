# WHILE...WEND

Koşullu döngü işletimini sağlayan bir yapıdır.\
Görevi\
Belirli işlem grubunu mantıksal bir koşula bağlı olarak tekrarlı olarak işlem görmesini sağlamaktır. Sonuçta mantıksal koşul True olduğu sürece döngü devam edecek, koşul False olduğunda döngüden çıkılacaktır.\
\
**Kullanımı**

```
WHILE <koşul> ' döngü başlangıcı 
<işlem_grup> ları ' işlemler . 
WEND ' döngü sonu 

OLDUKÇA <koşul> ' döngü başlangıcı 
<işlem_grup> ları ' işlemler . 
SON ' döngü sonu 

```

\
**Açıklama**\
Bu yapıda belirtilen mantıksal koşul sağlandığı sürece döngü devam eder. Yapı itibarıyla, mantıksal koşul işlem yapılmadan test edilmektedir. Bu tür yapılara ise "Test at First" yapıları denilmektedir.\
Ayrıca bu yapılar iç içe geçebilmektedir. Exit yardımcı kelimesi ile de istenildiği an döngüden ayrılmak mümkündür.\
\
**Örnek**

```
Function Test()	
  Dim sayı1 As Number
  Dim sayı2 As Number
  Dim toplam As Number
 
  WHILE sayı1 < 100
      sayı1:=sayı1+5
      toplam:= toplam + sayı1
  WEND
  MessageBox(Str(toplam),"Örnek",MB_OK)

  OLDUKÇA  sayı2 < 100
      sayı2:=sayı2+5
      toplam:= toplam + sayı2
  SON
  MessageBox(Str(toplam),"Örnek",MB_OK)
EndFunction
```

**Örnek Açıklaması**\
Sayı1 değişkeni 100 değerini alıncaya kadar 5' er 5' er artarak artım değerleri toplanır ve toplam değişkenine atanır. Sayı1 değişkeninin değeri 100 olduğunda döngüden çıkılmaktadır. Sonuçta toplamın değeri 1050 olmakta ve Always® terminalinde bir mesaj kutusu yardımıyla görülmektedir.
