# UpdateProgress

Bu fonksiyon, uzun süreli işlemlerin aşamalarını, progress bar bölümünde görsel ve yüzdesel olarak gösterebilmek için, progress bar güncellemesi amacıyla kullanılır.\
\
Kullanımı

```
Function UpdateProgress(
  Explanation As String,    ' Progress bar işlem açıklaması
  Count       As Number     ' İlgili işlemin hangi adımda olduğu veya yüzdesi
)As Boolean
```

Parametreler\
_Explanation_\
Progress bar başında yer alan işlem açıklamasıdır.\
_Count_\
Progress bar işlem adım sayısı veya yüzdesidir.\
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
