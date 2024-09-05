# IF...THEN...ELSE...ENDIF

Anadil® ile yazılan uygulamalarda dallanma yapan bir yapıdır.\
**Görevi**\
Mantıksal ifadeler arasındaki her türden kıyaslama işlemini gerçekleştirip farklı işlem gruplarını uygulamaktır.\
**Kullanımı**

\
**Açıklama**

```
IF <koşul> THEN 
<deyim> ler 

[ ELSE 

<deyim> ler 

] 

ENDIF
```

Bu yapının uygulanmasıyla önce ilk koşul deyimi ele alınır. Koşulda ele alınan mantıksal operatör-aritmetik operatör karışımı karşılaştırma deyimleri aracılığı ile koşul deyiminin sağlanıp True; sağlanmadığı False saptanmakta ve THEN deyiminin altındaki deyim(ler) ya da ELSE deyiminin altındaki deyim(ler) uygulanmaktadır.

İstenilirse ELSE yardımcı kelimesi kullanılmayabilir. Koşulun durumuna göre ikisinden birine sapan uygulama ENDIF deyiminden sonraki deyimleri işleterek normal işleyişini sürdürür. Ayrıca deyimler içerisinde başka durumları kontrol etmek için ELSE ardından açılabilecek başka IF yapılarıyla başka karşılaştırma işlemleri de uygulanılabilmektedir.

Bu yapıda yapılan karşılaştırmalar sayısal veya mantıksal şekilde olabilmektedir ve birden fazla karşılaştırma da mantıksal operatörler yardımıyla birleştirilebilmektedir. Birleştirilen ifadeler parantezler arasında verilirse, geliştirici ve compiler açısından yapılabilecek mantıksal hataların önüne geçilmiş olunabilir.\
\
Örnek

```
	Dim sayı1 As Number
	Dim sayı2 As Number
	Dim sayı3 As Boolean
	sayı1:= 3
	sayı2:= 8
	sayı3:= (sayı1=5) VEYA (sayı2<10)
	If sayı3 Then
		MessageBox("en az biri DOĞRU","Örnek",MB_OK)
	Else
		MessageBox("ikisi de YANLIŞ","Örnek",MB_OK)
	EndIf
```

**Örnek Açıklaması**\
Sayı1, sayı2 değişkenlerine sıra ile 3 ve 8 değerleri atanmakta ve ardından VEYA operatörü kullanılarak yapılan karşılaştırılmalar birleştirilmektedir. Sonuç mantıksal True ise, Always® terminalinde mesaj kutusu yardımıyla "en az biri DOĞRU"; False ise mesaj kutusu yardımıyla "ikisi de YANLIŞ" yazmaktadır.\
Yine aynı örnekte mantıksal ifadenin sayı3 değişkenine atılması yerine, bu mantıksal ifade If yapısının içinde direkt olarak da kullanılabilir.
