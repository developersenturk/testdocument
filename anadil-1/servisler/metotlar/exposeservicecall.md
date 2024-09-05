# ExposeServiceCall

ExposeServiceCall Methodu, serviste bulunan fonksiyonları, diğer executable'ların kullanımına açar.\
\
**Kullanımı**

```
ServiceObject.ExposeServiceCall(
  FunctionName  As String  ' Fonksiyon adı
  Params As String         ' Fonksiyonun parametreleri
) As Bool
```

**Parametreler**\
\
_FunctionName_\
Servisin, diğer executable'ların kullanımına açtığı fonksiyon ismi\
\
_Params_\
Fonksiyonun parametreleri\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
Servis, ExposeServiceCall methodu ile kendi içinde barındırdığı fonksiyonlarını diğer executable'ların kullanımına açar.\
ServiceCall'un maximun 6 tane parametresi olabilir.\
Fonksiyonun parametreleri, birden fazla ise parametre aralarına ";" koymak yoluyla parametre isimleri birbirinden ayırılır.\
\
Örnek

```
Function ServiceMain(Service As Object) As Bool
  Service.ExposeServiceCall("GetPartOfDate","Tarih;PartName;Part")
EndFunction
```
