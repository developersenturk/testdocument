# SetDebug

Bu metod, okuma işlemlerinde, okunan değerlerin, Terminal penceresine yazılmasını sağlar.\
Bu sayede, program akışında oluşan hataların nedenini bulmak kolaylaşır.\
\
**Kullanımı**

```
DeviceObject.SetDebug(
	bDebugPrint As Boolean       
							)As Boolean
```

**Parametreler**\
_bDebugPrint_\
TRUE - FALSE As Boolean\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
\-----\
\
**Örnek**

```
oDev.SetDebug(True)
```

**Örnek Açıklaması**\
\-----
