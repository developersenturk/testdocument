# ChangePassword

Bu fonksiyon Security Server veritabanında yaratılmış kullanıcının sifresini degistirir. Kullanı şifreleri AlwSSMan programı ile veya programa Admin olarak girmiş olan yetkili kullanıcılar, güvenlik yönetimi servislerinden bu fonksiyon sayesinde güncellenebilir.\
\
Kullanımı

```
Function ChangePassword(
Username As String
OldPassword As String
NewPassword As String
) As Bool
```

\
Parametreler\
_Username_\
Kullanıcının adı\
\
_OldPassword_\
Kullanıcının eski şifresi. Admin kullanıcının eski şifresini vermeyebilir.\
\
_NewPassword_\
Kullanıcının yeni şifresi\
Geri Dönüş Değeri\
Kullanıcı şifresi güncellendiğinde TRUE, güncellenemezse FALSE değeri döner.
