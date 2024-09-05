# SetColName

Bu metod grid kontrol nesnesi bünyesindeki sütunları isimlendirmektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.SetColName(
  ColNumber As Number,  ' sütun numarası
  Name As String        ' sütuna verilecek isim
)
```

Parametreler\
_ColNumber_\
İsimlendirme işleminin uygulanacağı sütun numarasıdır.\
_ColName_\
Verilen sütun numarasına verilecek isim.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Grid nesnesi .Init() ile gerekli önişlemler sonucu oluşturulduktan sonra sahip olduğu sütunların isimlendirilmesi gerekmektedir. Bütün sütunların isimlendirilmesi mecbur değildir ama isimlendirilmemiş sütunlara sahip olan bir grid, daha yavaş çalışacaktır.\
\
İsimlendirme işlemi 1 den itibaren başlayarak sırasıyla bütün sütunlara uygulanmalıdır. Daha önceden ismi verilmemiş olan sütuna, herhangi bir işlem için, geliştiricinin sütun nesnesi olarak ulaşması da mümkün değildir.\
\
Sütunlara bu metodla verilen isimlerin ilerde uygulanacak olan grid-CFF işlemlerinde, kullanılan table sütun isimleri ile aynı olması, geliştiricinin işlerini oldukça hafifletecektir. Aksi halde geliştiricinin CFF bilgi geçişleri için ayrıca Anadil® kodu yazması gerekmektedir.
