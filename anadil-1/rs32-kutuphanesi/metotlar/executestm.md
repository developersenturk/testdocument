# ExecuteStm

Bu metod ile oluşturulmuş olan SQL statement ifadeler işletilmektedir.

**Kullanımı**

```
RSObject.ExecuteStm()As Bool
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri yapılan query işleminin gerçekleşmesi durumunda True, işletimin başarısız olması durumda ise içeriği False olan Bool değerdir.\
\
**Dikkat Edilecek Hususlar**\
RS kütüphanesi anlatımı boyunca verilen ve belli bir plan dahilinde gerçekleştirilen statement oluşturulmasında, gerçekleştirilen en son işlem, ifadenin bu metod ile işletimidir. İşletim sonrasında yapılan query'e bağlı olmak üzere, yapmak istediğimiz işlem SQL Server tarafından gerçekleştirilmektedir.\
\
Yapılan işlem sonucunda eğer bilgi SQL Server'dan talep edilmişse, yani SELECT statement, bilgiyi RS nesnesinin property'leri şeklinde elde etmekteyiz.\
\
Execute ile client/server uygulamadaki, client isteğini server'e iletmekte; server da gerekli işletimi gerçekleştirmekte; ve sonuçtan da daha sonra client'ı haberdar etmektedir.\
\
Execute işlemin başarılı bir şekilde gerçekleştiğini garantilemek için geri dönüş değerinin test edilerek, kontrol edilmesi gerekmektedir.
