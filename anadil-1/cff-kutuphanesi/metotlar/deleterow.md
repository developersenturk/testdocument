# DeleteRow

Bu metod bir CFF nesnesinde bir satırı silmektedir.\
\
**Kullanımı**

```
CFFObject.DeleteRow() As Bool
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlemin başarılı olması halinde DOĞRU, aksi durumda ise YANLIŞ olarak gerçekleşmekte olan bir Boolean değerdir.\
\
**Dikkat Edilecek Hususlar**\
Bir CFF nesnesinin sahip olduğu satır silinecek olursa bu satırın içerdiği entry değerleri de yok olmaktadır. Aktif olarak bulunan pozisyon ise satırdan bir önceki seviyedir.\
\
Özellikle döküman işlemlerinde Always® satır silme işlemlerini internal olarak çözmektedir. Bu yüzden uygulama geliştirici çok fazla satır silme işlemi kullanmamaktadır.
