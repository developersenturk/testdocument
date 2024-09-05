# DO...LOOP

Belli bir koşula bağlı olarak bir işlem grubunu tekrarlı yapan yapıdır.\
Görevi\
Mantıksal koşul sağlandığı sürece belirli bir işlem grubunun sürekli olarak işlem görmesini sağlamaktır.

\
**Kullanımı**\
**WHILE uygulaması**

```
DO WHILE <koşul> 
<işlem_grup>ları VEYA <işlem_grup>ları 
LOOP 

DO 
<işlem_grup>ları VEYA <işlem_grup>ları 
LOOP WHILE <koşul> 
```

**UNTIL uygulaması**

```
DO UNTIL <koşul> 
<işlem_grup>ları VEYA<işlem_grup>ları 
LOOP 

DO 
<işlem_grup>ları VEYA<işlem_grup>ları 
LOOP UNTIL <koşul> 
```

**Açıklama**\
Bu yapıda genel olarak 2 şekilde uygulama vardır. Bunlar WHILE ve UNTIL yardımcı kelimeleri sayesinde belirlenmektedir.\
WHILE yapısında test koşulu olan mantıksal ifade True olduğu sürece döngü devam etmekte, ne zamanki False değerini aldığında döngü işletimi sona ermektedir. UNTIL yapısında ise verilen bir koşul bir hedef değere sahip olana dek işletim sürdürülmektedir.\
Her iki yapının da ayrıca, mantıksal koşulun test edilmesi bakımından başlangıçta test ve sonda test şeklinde iki ayrı uygulama şekli bulunmaktadır. Aradaki fark ise sonda test şeklinde olan uygulamada döngü mutlaka en az bir kez işletilmektedir.\
Örnek.1

```
Function Test1()
  Dim sayı1 As Number
  Dim toplam As Number
  DO WHILE sayı1 < 100
    sayı1=sayı1+5
    toplam:= toplam + sayı1
  LOOP
  MessageBox(Str(toplam),"Örnek","",MB_OK)
EndFunction
```

Örnek.1 Açıklaması\
Sayı1 değişkeni 100 değerinden küçük olduğu sürece 5' er 5' er artarak artım değerleri toplanmakta ve toplam değişkenine atanmaktadır. Sayı1 değişkeninin değeri 100 olduğunda döngüden çıkılır.\
Unutulmaması gereken nokta sayıların ilk tanımlandıklarında 0 (sıfır) değerini sahip olmalarıdır.\
Sonuçta toplamın değeri 1050 olmakta ve Mesaj Kutusu ile Always® terminalinde görüntülenmektedir. Örnek.2

```
Function Test2()
  Dim sayı1 As Number
  Dim toplam As Number
  DO UNTIL sayı1 = 100
    sayı1=sayı1+5
    toplam:= toplam + sayı1
  LOOP
  MessageBox(Str(toplam),"Örnek","",MB_OK)
EndFunction
```

Örnek.2 Açıklaması\
Sayı1 değişkeni 100 değerine eşit oluncaya kadar 5' er 5' er artarak artım değerleri toplanmakta ve toplam değişkenine atanmaktadır. Sayı1 değişkeninin değeri 100 olduğunda döngü işletimi sona ermektedir.\
Sonuçta toplamın değeri 1050 olmakta ve Mesaj Kutusu ile Always® terminalinde görüntülenmektedir.
