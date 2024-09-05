# RunWizard

RunWizard Methodu, bir servisi çalıştırır.\
\
**Kullanımı**

```
AlwaysCallObject.RunWizard(
  ServiceName As String  ' servis adı
) As Bool
```

**Parametreler**\
_ServiceName_\
Çalıştırılmak istenen servis adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
RunWizard Methodu, bir servisi çalıştırır.\
\
**Örnek**

```
Function form_button1_Click(f As Object)
Dim alw As Object
  alw:=GetAlwaysCallObject()
  alw.RunWizard("Test_Service")
EndFunction
```
