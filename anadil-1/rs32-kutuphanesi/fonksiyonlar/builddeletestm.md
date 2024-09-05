# BuildDeleteStm

Bu fonksiyon bir DELETE statement oluşturulmasını sağlamaktadır.\
\
**Kullanımı**

```
Function BuildDeleteStm(
  TableName As String  ' table ismi
)As RSObject
```

**Parametreler**\
_TableName_\
DELETE işleminin uygulanacağı, içersinde var olan bir kaydın silineceği table ismidir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, ilerde kullanacağımız, içeriği DELETE statement olan bir RS nesnedir.\
\
**Dikkat Edilecek Hususlar**\
Burada yapılan aslında herhangi bir DELETE statement oluşturabilmek için atılan ilk adımdır.\
\
Geri dönüş değerinin nesne olması, Always®'in, RS kütüphanesindeki statement kavramını nesneler içersinde yönetim getirmesindendir. Ayrıca oluşturulan UPDATE statement ile ilgili gerekli işlemler, ortaya konulan bu nesnenin metod ve property'leri olarak uygulanacaktır.\
\
DELETE statement oluşturulurken, table içersindeki hangi kaydın silineceğinin çok iyi belirlenmesi gerekir. Bunu da SQL uygulamasında WHERE clause kullanarak başarabilmekteyiz. Yoksa SQL statement içersinde parametresiz olarak direkt uygulanan bir DELETE statement, ilgili table içersindeki bütün kayıtları silmektedir.
