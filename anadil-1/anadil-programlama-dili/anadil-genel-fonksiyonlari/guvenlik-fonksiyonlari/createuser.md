# CreateUser

Bu fonksiyon Security Server veritabanında kullanıcı yaratır. Kullanıcılar AlwSSMan programı ile de yaratılabilir veya programa Admin olarak girmiş olan yetkili kullanıcılar, güvenlik yönetimi servislerinden bu fonksiyon sayesinde kullanıcı tanımı yaratabilirler.\
\
Kullanımı

```
Function CreateUser(
Username As String
) As Bool
```

\
Parametreler\
_Username_\
Kullanıcın adı\
\
Geri Dönüş Değeri\
Kullanıcı yaratıldığında TRUE,yaratılamazsa FALSE değeri döner.
