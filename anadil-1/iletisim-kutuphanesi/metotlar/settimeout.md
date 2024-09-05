# SetTimeout

Bu method ile port okuma işleminde uygulanacak salise cinsinden timeout değeri set edilir.\
\
**Kullanımı**

```
DeviceObject.SetTimeout(
nTimeout As Number
) As Bool
```

**Parametreler**

```
nTimeout 
1000 : 1 saniye
Okuma işleminde cihazdan yollanan bir veri olmadığında, okuma işleminin ne kadar zaman sonra 
iptal edileceği bu parametre ile belirlenir.


```

**Geri Dönüş Değeri**\
Geri dönüş değeri, işlem başarılı ise TRUE, değilse FALSE ifadedir.\
\
**Örnek program için:** [**CreateDevice**](../fonksiyonlar/createdevice.md)
