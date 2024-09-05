# RunWizardThread

RunWizardThread Methodu, bir servisi ayrı bir Thread ortamında, düşük priority ile çalıştırır. Bu sayede bu servis çalıştığı sürece mainthread yani kullanıcı bloke olmaz.\
\
**Kullanımı**

```
AlwaysCallObject.RunWizardThread(
  ParentServiceName As String  ' Call eden servis adı
  ServiceName As String        ' servis adı
  CallBackFcnName As String    ' Parent servis callback fonksiyonu adı
) As Bool
```

**Parametreler**\
_ParentServiceName_\
Call eden servis adı\
\
_ServiceName_\
Çalıştırılmak istenen servis adı\
\
_CallBackFcnName_\
Call eden serviste bulunan callback fonksiyon adıdır. Call edilen servisin çalışması sonuçlanınca, parent servisteki callback fonksiyonu tetiklenir. Bu sayede call eden serviste gerekli aksiyonlar alınabilir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
RunWizardThread Methodu, ilgili servisi başlattıktan hemen sonra çalışmasına devam eder.\
\
**Örnek**

```
Function form_button1_Click(f As Object)
Dim alw As Object
  alw:=GetAlwaysCallObject()
  alw.RunWizardThread("ParentServiceName",  "Test_Service", "KontrolFcn")
  outm("Test_Service.SER çalışmaya başladı. ParentService (bu servis) de çalışmasına devam etmektedir...")
EndFunction

Function KontrolFcn(f As Object)
  outm("Test_Service.SER çalışmasını tamamladı...")
EndFunction

```
