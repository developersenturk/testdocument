# RemoveUser

Bu fonksiyon Security Server veritabanında yaratılmış kullanıcı kaydını siler. Kullanıcılar AlwSSMan programı ile de silinebilir veya programa Admin olarak girmiş olan yetkili kullanıcılar, güvenlik yönetimi servislerinden bu fonksiyon sayesinde kullanıcı tanımını silebilir.\
\
**Kullanımı**

```
Function RemoveUser(
Username As String
) As Bool
```

\
**Parametreler**\
_Username_\
Kullanıcının adı\
\
**Geri Dönüş Değeri**\
Kullanıcı silindiğinde TRUE,yaratılamazsa FALSE değeri döner.\
