# AddWhereCond

Bu metod yapılmakta olan query işleminde SELECT statement içersinde WHERE clause uygulanmasını sağlamaktadır.\
\
**Kullanımı**

```
RSObject.AddWhereCond(
  Cond As String  'where clause olarak verilen ifade
)
```

**Parametreler**\
_Cond_\
WHERE clause olarak verilen SELECT statement string ifadesi.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Genel olarak WHERE clause ile SQL ile yazılabilecek query ifadelerde, ortaya konulacak sonuç setinde sınırlama işlemi, ve limitler uygulanmaktadır. Bu limitler verilirken NOT, LIKE, EXISTS, IN, BETWEEN gibi yardımcı kelimeler kullanılmaktadır. Bunların yanında AND, OR gibi mantıksal bağlayıcılar da WHERE clause ile birden fazla sınırlayıcıyı birleştirebilmektedir. Bütün sayılan yardımcı ifadelerin kullanımına ilişkin gerekli detaylar için lütfen SQL Server dökümanlarına bakınız.\
\
Bu metodun birden fazla kullanımı ile ayrı ayrı verilen ifadeler, oluşturulan statement içersinde AND mantıksal bağlayıcısı ile birleştirilmektedir.\
\
WHERE ifadesinin başka bir uygulama alanı da yazılan query'lerde joinler oluşturabilmemizi sağlamaktır. Bu join'ler sayesinde table'lar arasında veri entegrasyonu temin edilmekte ve SQL Server'ün yapmak zorunda olduğu işlemler de azaltılabilmektedir.
