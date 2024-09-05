# InitWorkspaceEx

Bu fonksiyon ile workspace initialize edilmekte, mevcut veritabanı ve firma ile bağlantı kesilir, parametreler ile verilen veritabanı, firma, username ve şifre bilgileriyle, yeni bir bağlantı kurulur.\
\
**Kullanımı**

```
Function InitWorkspaceEx(
  ODBCDriver As String,   ' ODBCDriver string ifadesi : "SQL Server", "Oracle ODBC Driver"
  Server As String,       ' Server makina adı
  Username As String,     ' Kullanici adı
  Password As String,     ' Şifresi
  Database As String,     ' Veritabanı
) As Bool
```

**Parametreler**\
_ODBCDriver_\
ODBCDriver string ifade : "SQL Server", "Oracle ODBC Driver"\
_Server_\
SQL Server makina adı.\
_Username_\
Veritabanı kullanıcısı.\
_Password_\
Veritabanı kullanıcısı şifresi.\
_Database_\
Bağlanılacak olan veritabanı.

**Geri Dönüş Değeri**\
Geri dönüş değeri, işlem başarılı ise TRUE değilse FALSE ifadedir.\
\
**Dikkat Edilecek Hususlar**\
