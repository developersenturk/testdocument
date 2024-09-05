# BuildInsertStm

Bu fonksiyon bir INSERT statement oluşturulmasını sağlamaktadır.\
\
**Kullanımı**

```
Function BuildInsertStm(
  TableName As String  ' table ismi
)As RSObject
```

**Parametreler**\
_TableName_\
INSERT işleminin uygulanacağı, içerisine kayıt yapılan table ismidir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, içeriği INSERT statement olan bir RS nesnedir.\
\
**Dikkat Edilecek Hususlar**\
Burada yapılan aslında herhangi bir INSERT statement oluşturabilmek için atılan ilk adımdır.\
\
Geri dönüş değerinin nesne olması, Always®'in, RS kütüphanesindeki statement kavramını nesneler içersinde yönetim getirmesindendir. Ayrıca oluşturulan statement ile ilgili gerekli işlemler, ortaya konulan bu nesnenin metod ve property'leri olarak uygulanacaktır.\
\
Bir INSERT statement'in üzerinde işlem yapacağı table belli olduğu için burada mutlaka table ismini vermemiz gerekmektedir. Sonuçta INSERT şeklinde oluşturduğumuz bu SQL statement, parametre olarak verdiğimiz table içersine kayıt yapacaktır.
