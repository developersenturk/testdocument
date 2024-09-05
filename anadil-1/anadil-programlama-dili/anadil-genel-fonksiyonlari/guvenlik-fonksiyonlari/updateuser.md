# UpdateUser

Bu fonksiyon Security Server veritabanında yaratılmış kullanıcı bilgilerini günceller. Kullanıcılar AlwSSMan programı ile de güncellenebilir veya programa Admin olarak girmiş olan yetkili kullanıcılar, güvenlik yönetimi servislerinden bu fonksiyon sayesinde kullanıcı tanımı güncellenebilir.\
\
**Kullanımı**

```
Function UpdateUser(
Username As String
CFF As Object
) As Bool
```

\
**Parametreler**\
_Username_\
Kullanıcının adı\
_CFF_\
Kullanıcın bilgilerinin bulunduğu CFF değişkeni\
**Geri Dönüş Değeri**\
Kullanıcı bilgileri güncellendiğinde TRUE, güncellenemezse FALSE değeri döner.\
