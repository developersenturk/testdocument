# FlushEvents

Bu fonksiyon birden fazla uygulamanın aynı anda işletimi esnasında, bir uygulamadan diğerlerine işletim zamanı sağlamaktadır.\
\
**Kullanımı**

```
Function FlushEvents()
```

**Parametreler**\
Fonksiyonun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Windows 3.x sürümü ile karşımıza çıkan multitasking dediğimiz çokgörevlilik özelliği sayesinde, aynı anda birden fazla uygulama çalıştırılabilmektedir. Bu fonksiyon aynı anda ayrı pencerelerde çalışmakta olan uygulamalarda çalışma zamanı tahsisi ile ilgili düzenleme yapmaktadır.\
\
Always® terminalinde de birden fazla uygulamanın aynı anda ayrı pencerelerde çalıştığını düşünelim. Aktif uygulamanın oldukça zaman alıcı bir döngüde iş yaparken, son kullanıcı, başka bir Always® uygulaması penceresini kullanmak istediğinde, pencereler arası geçişi sağlıklı olması için bu fonksiyonun kullanımına ihtiyaç bulunmaktadır. Çünkü bazı durumlarda aktif uygulama, diğer uygulamaya geçişte pencere oluşumunu bloke edebilmekte, oluşumunu tamamlamamış pencere dahilindeki uygulamanın kullanımı da imkansız olmaktadır.\
\
Çok fazla gerekmediği takdirde kullanılmaması gereken bir fonksiyondur.\
\
**Örnek**\
Aşağıdaki örnek c:\Always\UserReportDevices\devusr\_xl.ser (Excel için kullanıcı tanımlı device driver servisi) dosyasından alınmıştır. Bu örnekte, "ReceiveData" fonksiyonu ile Excel'e, OLE kanalından, bir döngü içerisinde yoğun veri iletildiğini varsayarsak, bu arada, sisteme ve kullanıcıya, Always® in kilitlenmediği hissini vermek için, FlushEvents komutu kullanılmaktadır.

```
Function ReceiveData(Instance As Number, Command As String, Params As String) As Bool
' The only method of passing data from the report to the driver service is to 
' use this function.
' Repsrv32 and devusr32 hand-in-hand handle the data passing mechanism.
' The report runs the method SendToDevice, Repsrv32 and devusr32 maps this 
' request to the Device Instance associated with the report.
' Command and Params contents and format is negotiated between the user device
' writer and the report writer. It is a good idea to clearly document these 
' commands and params.

Dim cell As Object
Dim r As Number
Dim c As Number
Dim cmd As String
Dim pos As Number


pos:=FindStr(Command, ";")

if pos=0 Then
 Return
EndIf

cmd:=Mid(Command,1,pos-1)
Command:=Erase(Command, 1, pos)
' We currently have one command
  if cmd="WriteToCell" Then
    c:=Val(Command)
    pos:=FindStr(Command, ";")
    Command:=Erase(Command, 1, pos)
    r:=Val(Command)
    cell:=xlo[Instance].GetProp("Cells",r,c)
    cell.SetProp("Value", Params)
    cell.Close()
    

    frms[Instance].rc.valuestr:=Format(r,"n;0") & ", " & Format(c,"n;0")
    ' Flush events is used to give the impression that
    ' Always is not crashed but running
    FlushEvents()
  EndIf
  ReceiveData:= TRUE
EndFunction
```
