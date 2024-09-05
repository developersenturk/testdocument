# DeleteEntry

Bu metod herhangi bir CFF içersindeki entry ifadeyi silmektedir.\
\
**Kullanımı**

```
CFFObject.DeleteEntry(
  EntryName As String  ' silinecek entry ismi
)As Bool
```

**Parametreler**\
_EntryName_\
Kendisini silmek istediğimiz entry ifadenin isim bilgisi.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlemin başarılı olması halinde DOĞRU, aksi durumda ise YANLIŞ olarak gerçekleşmekte olan bir Boolean değerdir.\
\
**Dikkat Edilecek Hususlar**\
Bir entry ifadenin silinmesi sadece onun içeriğinin silinmesi değil, kendisinin tamamen bulunduğu satırdan yok edilmesi şeklinde gerçekleşmektedir.\
\
Yapılan işlemin başarısının geliştirilen uygulama içersinde, mutlaka Bool olan geri dönüş ifadesi ile teyit edilmesi gerekmektedir.
