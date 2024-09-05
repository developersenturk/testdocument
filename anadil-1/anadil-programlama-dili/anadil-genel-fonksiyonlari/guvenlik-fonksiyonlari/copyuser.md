# CopyUser

Bu fonksiyon Security Server veritabanında tanımlı bir kullanıcının özelliklerini bir başka bir kullanıcıya kopyalar.\
\
Kullanımı

```
Function CopyUser(
FromUsername As String
ToUsername As String
) As Bool
```

\
Parametreler\
_FromUsername_\
Özellikleri kopyalanacak olan kullanıcının adı\
_ToUsername_\
FromUsername özelliklerinin saklanacağı kullanıcının adı\
\
Geri Dönüş Değeri\
Kullanıcı bilgileri kopyalama başarılı ise TRUE, başarısız ise FALSE değeri döner.\
CFF Yapısı\


```
	User
		Username
		BaseCompany
		AllowedCompanies
		ReportCompanies
	RS32
		ServerName
		OdbcDriver
		Database
		User
```
