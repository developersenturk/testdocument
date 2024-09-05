# StartProgress

Bu fonksiyon, uzun süreli işlemlerin aşamalarını, progress bar bölümünde görsel ve yüzdesel olarak gösterebilmek için kullanılır.\
\
Kullanımı

```
Function StartProgress(
  Explanation As String,    ' Progress bar kelimesi
  Limit       As Number     ' Genellikle 100 olarak verilir
)As Boolean
```

Parametreler\
_Explanation_\
Progress bar başında yer alan açıklamadır.\
_Limit_\
Progress bar maximum count limitidir.\
\
Geri Dönüş Değeri\
Geri dönüş değeri önemsizdir.\
\
Örnek

```
StartProgress("Belge Tarama ",100)
for i := 1 to 100 
          ...
          ...
    UpdateProgress("Belgeler Taranıyor ",i)
next 
EndProgress()
```

Örnek Açıklaması\
StartProgress fonksiyonu ile progress bar, max limit 100 ile hazirlaniyor. For döngüsü içinde herbir işlem sonrası progress bar güncelleniyor. Döngüden çıktıktan sonra progress bar iptal ediliyor.
