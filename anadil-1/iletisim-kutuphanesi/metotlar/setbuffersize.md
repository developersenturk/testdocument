# SetBufferSize

Bu metod ile port okuma işlemlerinin belirli bir maksimum uzunlukta yapılmasını sağlayabiliriz.\
Değiştirilmediği takdirde maksimum 255 karakter ile okuma yapılır.\
\
**Kullanımı**

```
DeviceObject.SetBufferSize(
	nMaxBufferSize As Number   ' AÇIKLAMA : Dizi Uzunluğu     
							)As Boolean
```

**Parametreler**\
_nMaxBufferSize_\
Maksimum Dizi Uzunluğu (Maximum Buffer Size) As Number\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
\-----\
\
**Örnek**

```
oDev.SetBufferSize(20) 
```

Örnek Açıklaması\
\-----
