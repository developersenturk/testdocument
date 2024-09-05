# Like

Bu operatör iki string(karakter dizisi) ifade arasında karşılaştırma işlemi uygulamaktadır.\
**Kullanımı**\
sonuç := \<karakter\_ifade> LIKE \<model> veya\
sonuç := \<model> LIKE \<karakter\_ifade>\
**Açıklama**\
Bu işlem sonucunda mantıksal bir sonuç ifade oluşmaktadır. Karşılaştırılan iki dizin birbirlerine eş ise sonuç True, değilse False olarak oluşmaktadır.\
Karşılaştırılan ifadelerin mutlaka string olmaları gerekmektedir ve modelin veya karakter ifadenin hangisinin önce yazıldığı önemli değildir.\
Başka önemli bir nokta ise benzerlik kontrolünde (? , \*) joker sembolleri kullanılabilir. Bilindiği üzere, "?" sembolü herhangi bir tek karakter yerine geçebilen; "\*" ise bir veya birden fazla karakter yerine geçebilen sembollerdir.\
\
**Örnek**

| model     | karakter\_ifadesi | mantıksal\_sonuç |
| --------- | ----------------- | ---------------- |
| "abcdefg" | "abcdefg"         | True             |
| "abcdefg" | "a\*"             | True             |
| "abcdefg" | "abcd??g"         | True             |

```
  Dim model As String
	Dim test As String
	model:= "abcdefg"
	test:= "a*"
	If model LIKE test Then
		MessageBox("Verilen ifadeler birbirine eş.", #
                   "Örnek Uygulama",MB_OK)
	Else
		MessageBox("İfadeler birbirine DENK DEĞİL.", #
                   "Örnek Uygulama",MB_OK)
	EndIf
```

**Örnek Açıklaması**\
Yukarıdaki örnek uygulamada iki stirng ifade karşılaştırılmış ve denk olmalarına göre oluşan sonuç mantıksal ifadesi ile Always® terminalinde MessageBox fonksiyonu ile bilgi mesajı görüntülenmiştir.
