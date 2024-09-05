# MoveToFirstRow

Bu metod bir CFF nesnesinde ilk satıra gitmektedir.\
\
**Kullanımı**

```
CFFObject.MoveToFirstRow() As Bool
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlemin başarılı olması halinde DOĞRU, aksi durumda ise YANLIŞ olarak gerçekleşmekte olan bir Boolean değerdir.\
\
**Dikkat Edilecek Hususlar**\
CFF nesnelerinde bir sıra dahilinde oluşturulmuş olan satırlar arasında ilk yaratılmış olan satıra bu metod sayesinde gidebilmekteyiz. Özellikle önceden yazılmış olan entry bilgilerin okunması işleminde oldukça sık kullanılmaktadır.\
\
Satırlar arasında gezme işlemi bilgi akışının sağlıklı gerçekleşmesi bağlamında çok önemli olduğundan, oluşturulan döngülerde azami dikkat sarfedilmesi gerekmektedir. Bu işlemde uygulanan, aslında current satır gösterici değerinin ilk satırı işaret edecek şekilde değiştirilmesidir.\
\
Yeni bir satıra gitme işleminde current entry, yani aktif entry değeri kaybolmaktadır, sonuç olarak mutlaka current entry ifadesinin ayrıca belirlenmesi gerekmektedir.
