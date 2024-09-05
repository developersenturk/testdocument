# GetStatus

Bu method ile herhangi bir hata sonrası device status elde edilebilir.\
\
**Kullanımı**

```
DeviceObject.GetStatus() As Number
```

**Parametreler**

```
Parametresi bulunmamaktadır.


Geri Dönüş Değeri


Geri dönüş değeri, device status değeridir: 
      1: CreateFile FAILED (OpenDevice) 
      2: CreatePipe FAILED (OpenDevice)
      3: Create Communication watch thread FAILED (OpenDevice)
      6: ReadPipe FAILED (ReadDevice)
     12: Timeout (ReadDevice)
 others: GetLastError()   (OpenDevice--> SetupDevice FAILED)
```

\
Örnek program için: [CreateDevice](../fonksiyonlar/createdevice.md)
