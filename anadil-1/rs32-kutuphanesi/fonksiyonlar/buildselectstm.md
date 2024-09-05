# BuildSelectStm

Bu fonksiyon bir SELECT statement oluşturulmasını sağlamaktadır.\
\
**Kullanımı**

```
Function BuildSelectStm()As RSObject
```

**Parametreler**\
Fonksiyonun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, içeriği SELECT statement olan bir RS nesnesidir.\
\
**Dikkat Edilecek Hususlar**\
Bu fonksiyon ile yapılan işlem, SQL ile SELECT statement yazılması için atılan ilk adımdır.\
\
Geri dönüş değerinin nesne olması, Always®'in, RS kütüphanesindeki statement kavramını nesneler içersinde yönetim getirmesindendir. Ayrıca oluşturulan statement ile ilgili gerekli işlemler, ortaya konulan bu nesnenin metod ve property'leri olarak uygulanacaktır.\
\
Bir SELECT statement'in içerebileceği table sayısı belli olmadığı için burada herhangi bir table parametresi bulunmamaktadır. Gereken table bilgilerini ilerde RS nesnesinin metodları ile belirleyeceğiz.
