# LockRow

Bu metod grid satırlarını kullanıcı etkilerinden soyutlamak manasında kilitlemekte veya önceden kilitlenmiş olan satırlarda kilit olayını kaldırmaktadır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.LockRow(
  RowNum As Number	' hedeflenen satır numarası
  KilitInfo As Bool	' kilitleme bilgisi
)
```

**Parametreler**\
_RowNum_\
Üzerinde kilit kontrolü uygulanacak olan satır numarasıdır.\
_KilitInfo_\
Kilitleme veya kilit olayı kaldırılmasına ilişkin bilgi içermektedir. "DOĞRU" şeklinde verildiğinde ilgili satır kilitlenmiş olacaktır.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Grid kontrol nesnesi kullanımı, özellikle birden fazla table bilgisinin söz konusu olduğu durumlarda uygulanmaktadır. İlişkisel verilerin bütünlüğü açısından ve de business details denilen ticari detay işletimi özel kuralları gerçekleştirilirken, grid üzerinde yer alan bazı bilgilerin sabit kalması taleb edilebilmektedir.\
\
Bu gibi durumlarda grid satırlarının bazıları kullanıcıdan soyutlanması, metod ile gerçekleştirilmektedir. Metod kullanımında geçen 2. parametre True olarak verildiğinde, hedeflenen satır kilitlenmektedir. Eğer kilit olayı ortadan kaldırılmak isteniyorsa metod ile parametreyi False şeklinde vermek yeterli olmaktadır.
