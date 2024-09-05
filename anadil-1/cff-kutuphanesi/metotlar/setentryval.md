# SetEntryVal

Bu metod bir entry içeriğini değiştirmek için kullanılmaktadır.

**Kullanımı**

```
CFFObject.SetEntryVal(
  Value As <Variant>  ' yeni entry içeriği
)
```

**Parametreler**\
_Value_\
Herhangi bir variant olabilen, entry içersine yazmak istediğimiz değer.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Bir entry içersine yazma işlemi özellikle update işleminde gerçekleşebilmektedir. Bu işlem için daha önceden current entry göstericisi değerinin doğru bir şekilde ayarlanmış olması gerekmektedir.\
\
Bu metod da eğer tam olarak entry ifadenin satır içersindeki yerini tam bilemiyorsak ve de current göstericisinin değerini doğru bir şekilde ayarlayabilmek için, FindEntry metodu ile birlikte kullanmak en etkin yoldur.\
\
Entry değerlerini verirken NULL desteği de tam olarak sağlanmaktadır.
