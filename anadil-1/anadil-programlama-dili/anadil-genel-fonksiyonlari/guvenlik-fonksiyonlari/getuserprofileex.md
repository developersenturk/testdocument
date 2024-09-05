# GetUserProfileEx

Bu fonksiyon kullanıcı ismi verilen kullanıcının profile bilgilerini CFF olarak geri döndürür.\
\
**Kullanımı**

```
Function GetUserProfileEx(
  KullanıcıAdı As String
) As Object                      
```

\
\
**Parametreler**\
_KullanıcıAdı_\
Kullanıcı adının verildiği String ifade\
\
**Geri Dönüş Değeri**\
Verilen kullanıcının güvenlik bilgileri CFF olarak geri döner. Kullanıcının güvenlik bilgileri alınamazsa NULL CFF döner. Bu fonksiyon Admin veya Admin yetkisine sahip kullanıcılar tarafından kullanılabilir.\
\
**CFF Yapısı**\


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


Program örneği

 Dim cff As Object
 Dim ucff As Object
 Dim rscff As Object
  
 cff :=CffCreate("test")
 cff:=GetUserProfileEx(  "t20"  )
 cff.DumpCFF()

 rscff:=cff.OpenSubCFF("RS32")
 ucff:=cff.OpenSubCFF("User")
 
 Outm("Kullanici: "  ucff.UserName)
 Outm("Database: "  rscff.Database)


CFF Dump örneği

CFF: No name Entries
 UserName : t20 
	Sub CFFs
                      CFF:       RS32             Entries       
                             ServerName : .                             
                             OdbcDriver : SQL Server                               
                             Database : Always                                   
                             User : sa       
                      CFF:       User             Entries       
                            BaseCompany : RBD                       
                            AllowedCompanies : RBD                        
                            ReportCompanies : RBD
```
