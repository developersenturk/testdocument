# FOR...NEXT

Bu yapı aynı işlem grubunun tekrarlı olarak işletilmesini sağlamaktadır.

```
<for_next> ::= FOR <id>[<dimensions>] = <b_Expr> TO <b_Expr> [<step>] <cr>
                  [<statements>] NEXT 
   <say_devamet> ::= SAY <id>[<boyutlar>] = <b_Expr> DEN <b_Expr> [<ADIM>] <cr>
                  [<satırlar>] DEVAMET 
   <say_devamet> ::= SAY <id>[<boyutlar>] = <b_Expr> DAN <b_Expr> [<ADIM>] <cr>
                  [<satırlar>] DEVAMET 
```

**Görevi**\
Belirli işlem grubunun koşul ileri sürmeksizin belirlenmiş sayıda tekrarlanmasını sağlamaktır. Sonuçta koşulsuz döngü işlemleri bu deyimle yapılmaktadır.\
**Kullanımı**\
FOR kontrol\_değişkeni=değişken/sabit ' alt limit\
To değişken/sabit ' üst limit\
\[STEP değişken/sabit] ' artış veya azalış\
. ' miktarı\
.\
\<işlem\_(grup)ları>\
.\
.\
NEXT\
**Açıklama**\
Bu yapıda kontrol değişkeni anahtar bir görev üstlenerek belirli değerler alarak işlem grubunun belirli sayıda işlem görmesini sağlamaktadır. Buna göre genel yazılışındaki işleyiş şu şekilde olmaktadır:\
Kontrol değişkeni önce eşitliğin sağındaki değişken ya da sabit değerini alarak işlem grubundaki işlemleri 1 kez yapacaktır. NEXT deyimine geldikten sonra, bu kez kontrol değişkeni STEP değiminde verilen değişkendeki veya sabit sayıdaki değer kadar arttırılarak işlem grubundaki işlemler 2. kez yapılacaktır.\
İşleyiş bu şekilde devam edecek ve kontrol değişkeni TO deyiminden sonra belirlenen değişken ya da sabite eşit olduğunda da sonuncu kez işlem grubunu uygulayarak döngüden çıkacaktır. STEP deyimi belirtilmemiş ise artım miktarı 1 olacaktır.\
Alt limit değeri üst limitten büyük olarak verilebilir ve STEP sayısı negatif olarak kullanılmak suretiyle yapının uygulanması da mümkündür. Ayrıca FOR...NEXT yapılarının iç içe uygulanması da başka bir alternatif kullanımdır.\
Son olarak "EXIT" kullanımı ile FOR...NEXT yapısından istenildiği anda ayrılınması da mümkündür.\
\
**Örnek**\


```
Function Test()
  Dim sayı1 As Number
  Dim toplam As Number
	FOR sayı1 = 0 TO 100  STEP 5
		toplam:= toplam + sayı1
	NEXT
	MessageBox(Str(toplam),"Örnek",MB_OK)	


	SAY sayı1 = 0 DEN 100  ADIM 5
		toplam:= toplam + sayı1
	DEVAMET
	MessageBox(Str(toplam),"Örnek",MB_OK)	


EndFunction
```

**Örnek Açıklaması**\
Sayı1 değişkeni 0 değerini alır. Daha sonra 5' er 5' er artarak artım değerleri toplanır ve toplam değişkenine atanır. Sayı1 değişkeninin değeri 105 olduğunda döngüden çıkılır. Sonuçta en son olarak toplamın değeri 1050 olmakta ve mesaj kutusu ile Always® terminalinde görüntülenmektedir.
