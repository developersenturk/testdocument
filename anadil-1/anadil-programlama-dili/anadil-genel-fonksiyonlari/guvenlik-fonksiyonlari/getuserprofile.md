# GetUserProfile

Bu fonksiyon aktif kullanıcı profile bilgilerini verilen CFF e kaydeder.\
\
Kullanımı

```
Function GetUserProfile(
  CFF As Object
) As Bool                      
```

\
\
Parametreler\
_CFF_\
Kullanıcı bilgilerinin yazılacağı CFF object\
\
Geri Dönüş Değeri\
Aktif kullanıcı bilgileri CFF parametresine kaydedildiğinde TRUE değeri geri döner. Kaydedilemediğinde FALSE döner.\
\
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

\
GetUserProfile User subcff yapısını CFF parametresine kaydeder.
