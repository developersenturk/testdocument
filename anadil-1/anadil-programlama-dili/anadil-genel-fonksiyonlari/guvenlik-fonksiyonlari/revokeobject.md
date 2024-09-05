# RevokeObject

Bu fonksiyon ile kullanıcıya verilmiş yetki geri alınır.\
\
**Kullanımı**

```
Function RevokeObject(
User/Group As String
Object As String
Right As String
) As Bool
```

\
**Parametreler**\
_User/Group_\
Kullanıcı adı veya grup adı.\
\
\
_Object_\
Kullanıcıdan alınacak yetki nesnesidir.\
\
\
_Right_\


```
Kullanıcıdan alınacak yetki sabitidir:

R_VIEWOBJECT : Object  e erişim yetkisi
R_OPENOBJECT : Object açabilme yetkisi
R_GETOBJECTDATA : Object verisini alabilme yetkisi
R_CHANGEOWNPASS : Kendi şifresini veya object şifresini değiştirebilme yetkisi
R_FULLREAD : Object üzerinde tam okuma yetkisi
R_SETOBJECTDATA : Object verisini set edebilme yetkisi
R_CHANGEOBJECTSEC : Object in güvenlik özelliklerini değiştirebilme yetkisi
R_DELETEOBJECT : Object i silme yetkisi
R_FULLWRITE : Object üzerinde tam yazma yetkisi 

Not : Her yetki yukarısındaki tüm yetkileri kapsar.

```

\
\
**Geri Dönüş Değeri**\
Kullanıcıdan yetki alındığında TRUE, alınamazsa FALSE değeri döner.\
\
\
_Örnek_\


```
if RevokeObject( "Model", "Admin", R_FULLREAD) then
     outm("Model isimli kullanıcıdan, Admin nesnesi (kullanıcısı) üzerinde FULLREAD yetkisi geri alınmıştır...")
else
    outm("Yetki geri alma işlemi başarısız...")
endif
```
