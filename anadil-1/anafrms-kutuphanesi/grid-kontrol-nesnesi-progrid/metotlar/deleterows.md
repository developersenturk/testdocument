# DeleteRows

Bu metod grid kontrol nesnesinde verilen satırları siler.\
\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
MyGridObject.DeleteRows(
  StartRow As String,  ' başlangıç grid satır numarası
  EndRow As Number     ' son grid satır numarası
)
```

**Parametreler**\
_StartRow_\
Grid kontrol nesnesinde içeriği temizlenecek olan grid satır aralığının ilk elemanı.\
_EndRow_\
Grid kontrol nesnesinde içeriği temizlenecek olan grid satır aralığının son elemanı.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Metod yardımıyla grid kontrol nesnesi dahilinde, belli bir aralık dahilindeki satır bilgileri silinmektedir. Grid nesnesinde aralık olarak verilmekte olan grid satırları arasındaki bilgiler veritabanına kayıt anında da yok edilecek artık bu bilgilere ulaşım mümkün olmayacaktır.\
\
Silme aralığı verilirken ilk sayı başlangıç grid satırı olmakta, verilen ikinci sayı ise aralığı meydana getirmekte olan son grid satır numarası olmaktadır. Başka bir deyişle verilen son sayı da dahil olmak üzere aradaki tüm grid satırlarının silinmesi gerçekleştirilmektedir.
