# OutM

Bu fonksiyon Debug penceresine verilen bir string ifadeyi yazmaktadır.\
\
Kullanımı

```
Function OutM(
  Mesaj As String  ' Debug penceresine yazılacak ifade
)
```

Parametreler\
_Mesaj_\
Debug penceresine yazılmak istenilen ifadedir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri önemsizdir.\
\
Dikkat Edilecek Hususlar\
Bazı durumlarda Always altında geliştirilen uygulamalarda test etmek amacıyla veya yazılan uygulamanın işleyişini izlemek amacıyla bazı mesajlarla denetim sağlanmak istendiğinde bu fonksiyon yardımıyla istenilen mesajlar Debug penceresine yazılabilmektedir.\
\
Ayrıca Debug penceresinin Always® alt yapısına sahip başka bilgisayar sistemlerine de yönlendirebilmesi sayesinde, istenilen mesajlar aynen karşı sistemdeki Debug penceresinde de gözükmeye devam edecektir.\
Örnek

```
Function F()
  OutM("Merhaba Dünya, bu benim deneme mesajım.")
EndFunction
```

Örnek Açıklaması\
Burada test amacıyla Debug penceresine normal bir mesaj yazımı gösterilmektedir.
