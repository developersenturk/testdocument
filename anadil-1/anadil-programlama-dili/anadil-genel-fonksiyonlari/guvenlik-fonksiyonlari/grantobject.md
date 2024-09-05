# GrantObject

Bu fonksiyon ile bir kullanıcıya veya gruba yetki verilebilir. Bu fonksiyon Admin ile yapılabilen işlemlerin, Admin olmayan fakat Admin ile aynı yetkiye sahip kullanıcılar tarafından da yapılabilmesi icin kullanılabilir.\
\
**Kullanımı**

```
Function GrantObject(
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
Kullanıcıya verilecek yetki nesnesidir.\
\
\
_Right_\


```
Kullanıcıya verilecek yetki sabitidir:

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
Kullanıcıya yetki verildiğinde TRUE, edilemezse FALSE değeri döner.\
\
\
_Örnek_\


```
if GrantObject( "Model", "Admin", R_FULLREAD) then
     outm("Model isimli kullanıcıya, Admin nesnesi (kullanıcısı) üzerinde FULLREAD yetkisi verilmiştir...")
else
    outm("Yetki verme işlemi başarısız...")
endif
```
