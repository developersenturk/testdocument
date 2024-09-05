# GetAllRows

Bu metod grid nesnesinde bulunan tüm (mevcut, inserted, updated) satirlari CFF nesnesine taşır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.GetAllRows(
  DestCFF As Object	' hedef CFF nesnesi
)
```

**Parametreler**\
_DestCFF_\
Grid üzerindeki satırların, taşınacağı hedef CFF nesnesi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Grid üzerinde bulunan mevcut satirlar, yeni eklenmiş satırlar ve değişiklik görmüş satırlar GetAllRows ile birlikte verilen cff nesnesine aktarılır.\
\
