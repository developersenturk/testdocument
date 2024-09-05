# MoveToPrevRow

Bu metod CFF nesnesinde bir önceki satıra gidilmesini sağlamaktadır.\
\
**Kullanımı**

```
CFFObject.MoveToPrevRow() As Bool
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlemin başarılı olması halinde DOĞRU, aksi durumda ise YANLIŞ olarak gerçekleşmekte olan bir Boolean değerdir.\
\
**Dikkat Edilecek Hususlar**\
Kullanımı oldukça basit olan bu metod ile bir CFF nesnesinde current dediğimiz aktif satır değerini bir önceki satıra değiştirmekteyiz. Bu işlem de current satır gösterici değerinin bir önceki satırı işaret edecek şekilde ayarlanması şeklinde gereçekleşmektedir.\
\
Üzerinde gezmekte olduğumuz CFF nesnesinin bir root CFF veya alt CFF olması önemli değildir.\
\
Yeni bir satıra gitme işleminde current entry, yani aktif entry değeri kaybolmaktadır, sonuç olarak mutlaka current entry göstericisinin ayrıca belirlenmesi gerekmektedir.\
\
Özellikle önceden içeriği belirlenmiş olan CFF nesnelerinde daha çok okuma işleminin uygulanmasında kullanılan bu metoddur. Geri dönüş değeri işlemin başarılı gereçekleşmesi açısından ve de doğru bilgiye ulaşımı garantilemek açısından oldukça önemlidir.\
\
Unutulmaması gereken başka bir nokta da bilgiyi satırların değil, entry'lerin saklamasıdır.
