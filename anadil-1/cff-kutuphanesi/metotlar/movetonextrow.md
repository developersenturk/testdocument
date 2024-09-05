# MoveToNextRow

Bu metod bir CFF nesnesinde bir sonraki satıra gidilmesini sağlamaktadır.\
\
**Kullanımı**

```
CFFObject.MoveToNextRow() As Bool
```

**Parametreler**\
Metodun parametresi yoktur.\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlemin başarılı olması halinde DOĞRU, aksi durumda ise YANLIŞ olarak gerçekleşmekte olan bir Boolean değerdir.\
\
**Dikkat Edilecek Hususlar**\
Bir CFF nesnesinde current dediğimiz aktif satır değerini bir sonraki satıra değiştiren bu metod kullanımı oldukça basittir.\
\
Navigating(gezme) metodları dediğimiz bu metodların kullanımı ile oluşturulan döngülerde geri dönüş değerinin de göz önünde tutulması işlemin sağlıklı gerçekleşmesi ve doğru bilgiye ulaşım açısından oldukça önemlidir.\
\
Yeni bir satıra gitme işleminde current satır gösterici değerinin, bir sonraki satırı işaret edecek şekilde ayarlanması uygulanan yöntemdir.\
\
Unutulmaması gereken başka bir nokta da bilgiyi satırların değil, entry'lerin saklamasıdır.
