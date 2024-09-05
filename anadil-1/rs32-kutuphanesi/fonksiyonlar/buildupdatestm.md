# BuildUpdateStm

Bu fonksiyon bir UPDATE statement oluşturulmasını sağlamaktadır.\
\
**Kullanımı**

```
Function BuildUpdateStm(
  TableName As String  ' table ismi
)As RSObject
```

**Parametreler**\
_TableName_\
UPDATE işleminin uygulanacağı, içersinde var olan bir kaydın değiştirileceği table ismidir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, içeriği UPDATE statement olan bir RS nesnedir.\
\
**Dikkat Edilecek Hususlar**\
Burada yapılan aslında herhangi bir UPDATE statement oluşturabilmek için atılan ilk adımdır.\
\
UPDATE statement ile ilgili hangi kaydın güncelleneceğine dair diğer table column ismi bilgileri ve row bilgileri daha sonra RS nesnesinin metodları ile belirlenecektir.\
\
Geri dönüş değerinin nesne olması, Always®'in, RS kütüphanesindeki statement kavramını nesneler içersinde yönetim getirmesindendir. Ayrıca oluşturulan UPDATE statement ile ilgili gerekli işlemler, ortaya konulan bu nesnenin metod ve property'leri olarak uygulanacaktır.
