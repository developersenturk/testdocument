# BulkCopy

Bu metod CFF nesnesinden, grid nesnesi dahiline satır bilgilerinin ayrı bir thread tarafından aktarımını sağlamaktadır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.BulkCopy(
  SourceCFF As Object ' kaynak CFF nesnesi
  bWait As Bool 'Opsiyonel WaitForBulkCopy parametresi
)As Bool
```

**Parametreler**\
\
_SourceCFF_\
Bilgi taşıma işleminin yapılacağı kaynak CFF nesnesidir.\
\
_bWait_\
True değeri verildiğinde BulkCopy işleminin bitmesi beklenir.\
Bu parametre verilmediğinde veya FALSE değer verildiğinde BulkCopy işlemi tetiklenir ve kontrol\
bir sonraki satıra döner.

\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
BulkCopy ayrı bir thread (alt proses) tarafından çalıştırıldığından,\
BulkCopy işlemi devam ederken, BulkCopy satırının altındaki\
satırlar paralel olarak çalışmaya devam ederler. BulkCopy\
metodunu çağıran Anadil kodu, BulkCopy nin bitmesini beklemez.\
Bu nedenle BulkCopy parametresi olan CFF hemen kullanılmaya çalışılırsa,\
"CFF is locked for updates" mesajı alınır. Bunun nedeni,\
BulkCopy cff i lock etmiş henüz unlock etmemiştir.

```

GridObject.BulkCopy(SourceCFF)

SourceCFF.Add("YeniEntry", "Degeri")  'Bu satırda "CFF is locked for updates" mesajı alınabilir


Önerilen kullanım:

GridObject.BulkCopy(SourceCFF, True) 'BulkCopy işlemi bitinceye kadar kontrol bu satırda kalır

SourceCFF.Add("YeniEntry", "Degeri")  'Bu satırda "CFF is locked for updates" mesajı alma şanşınız yoktur.
```

Metod yardımıyla özellikle belge işlemlerinde CFF nesnesinden, grid nesnesine doğrudan bilgi aktarımı gerçekleştirilmektedir. \_DatabaseToCFF event uygulanması ile veritabanından RS nesnesi yardımıyla bilgiler alındıktan sonra, gelen bilgilerin \_CFFToForm event'i dahilinde CFF nesnesinden, form üzerindeki grid kontrolü içeriğine taşınması tek adımda gerçekleştirilmektedir.\
\
Metod parametresi ile verilen CFF nesnesi bilgi kaynağı olmaktadır. Bilgi aktarımının tam olarak uygulanabilmesi için CFF nesnesi ve grid kontrolünün birbiri arasında, veri saklama biçimi açısından uyumluluk olması gerekmektedir. Bu uyumluluk ise grid kontrolünün sahip olduğu column(sütun) nesnelerinin gerçek isimlerinin, CFF altında tutulan alt CFF dahilindeki bilgi kaynağı olan entry isimleri ile aynı olması gerekmektedir. Grid sütun nesne adları, alt CFF nesnesi entry isimleri ile aynı olmazsa bilgi transferi gerçekleşemeyecektir.\
\
Bilgi kaynağı olan alt CFF nesnesinin teşkili ise tamamen \_DatabaseToCFF event dahilinde geliştirici tarafından gerçekleştirilecek olan bir olaydır. Belge parametreleri ile gelen CFF nesnesinin altında yer alan bu alt CFF nesnesi, grid bilgilerini tutacaktır. Ayrıca RS nesnesinden, bu alt CFF nesnesine bilgi aktarımı sırasında her grid satırına karşılık gelen ayırıcı uniqe sayaç bilgisinin de alt CFF nesnesinin dahilinde saklanması gerekmetedir. Bu bilgi "row\_id" isimli entry dahilinde saklanacaktır.\
\
Alt CFF nesnesi dahilinde tutulan adlarında başka alt CFF nesneleri oluşturulacaktır. Değişikliği tutan bu alt CFF nesnelerinin oluşturulması ise Always® tarafından tamamen otomatik olarak gerçekleştirilmektedir.\
\
Geliştirici grid değişikliklerini tutan alt CFF nesnelerindeki bilgileri row\_id bilgisi yardımıyla veritabanına taşıyacak olan SQL statement uygulamasını RS nesneleri dahilinde Anadil® ile yazacaktır. Burada sadece Inserted isimli alt CFF nesnesi .row\_id entry bilgisine sahip değildir çünkü buradaki grid satırı bilgilerinin henüz veritabanına kaydı yapılmamamıştır. Fakat kayıt işlemi gerçekleştikten sonra buradaki grid satırları bilgilerinin .row\_id değerleri olacaktır.
