# ShowImmediateParams

\-------\
\
**Kullanımı**

```
Function ShowImmediateParams(r_sayac As Number) As Bool
 'Report Parameters DialogBox is displayed.
 Dim srv As Object
 
 Srv:=CreateServiceCall("utl_security_manager","CheckAccessMsg",2)
 Srv.Execid:=""
 Srv.Rightname:="Load"
 If not Srv.CallService() Then
   Outm(">>>Bu İşlemi yapmaya hakkınız yok! Lütfen sistem yöneticinize başvurunuz...")
   bcancelled:=True
   Return
 Endif
 Srv.Close()
 DialogBox("savedparams",0,0)
 ShowImmediateParams:= NOT bcancelled
EndFunction
```

**Parametreler**\
_r\_sayac As Number_\
\
**Geri Dönüş Değeri**\
Bool\
\
**Dikkat Edilecek Hususlar**\
\-----\
\
**Örnek**

```
-----
```

**Örnek Açıklaması**\
\-----
