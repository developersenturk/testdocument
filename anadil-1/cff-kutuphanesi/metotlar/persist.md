# Persist

Bu method CFF'in memoryde kapladığı alanı hexadecimal string row lara dönüştürür. Elde edilen yeni cff yaklaşık olarak iki kat fazla yer tutar. Uygulamalar arası paylaşılan veya veritabanı tablolarında saklanan string cff ten, CFFCreateFromStringRows methodu ile yeniden original CFF elde edilir.\
\
**Kullanımı**

```
CFFObject.Persist(
  CFF As Object  ' CFF nesnesi
)As Object
```

**Parametreler**\
_CFF_\
......CFF nesnesi.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**

Bu fonksiyon bir CFF'i String rowlar haline getirir. Bir örnekle açıklanacak olursa; database'den satır satır alınan  bilgi bir CFF'e atılıp, daha sonra da bu CFF'i, string rowlar halinde tutulacak bir başka CFF'e atama işlemini yapar.

**İlgili Konular:** [**CFFCreateFromStringRows**](../fonksiyonlar/cffcreatefromstringrows.md)
