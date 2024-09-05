# StartDeviceNotification

Bu metodu, Com portuna bağlı kart okuyucuya, kart takıldığında ve kart çıkarıldığında,\
Anadil tarafında haberdar olmak istediğimizde kullanırız. Kart takılınca, ilgili personel\
kartının Id si okunur ve belirtilen fonksiyon (aşağıdaki örnekte : StartFuncKart) kart id\
parametresi ile birlikte tetiklenir. Kart okuyucuda durduğu sürece her hangi bir tetikleme\
gerçekleşmez. Personel kartı okuyucudan çıkardığında, belirtilen Stop Fonksiyonu\
(örnekte : StopFunc) tetiklenir.\
\
**Kullanımı**

```
DeviceObject.StartDeviceNotification(
	Service As String   ' AÇIKLAMA : Servis   
	StartFunction As String   ' AÇIKLAMA : Fonksiyon ismi
	StopFunction As String   ' AÇIKLAMA : Fonksiyon ismi  
							)As Boolean
```

**Parametreler**\
_Service_\
Tetiklenecek fonksiyonların yer aldığı Servisin ismi. (Bu metodun çağırıldığı servis) As String\
_StartFunction_\
Kart takıldığında tetiklenecek fonksiyonun ismi. (StartFunction) As String\
_StopFunction_\
Kart çıkarıldığında tetiklenecek fonksionun ismi. (StopFunction) As String\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri TRUE/FALSE.\
\
**Dikkat Edilecek Hususlar**\
\-----\
\
**Örnek**

```
Function OpenComPort() As Bool
Dim sCom as String
 
  '+
  '  Kart okuyucunun Registry de USBSER000 entry si ile yer aldığını varsayalım.
  '  USBSER000        Com5        gibi
  ' -                        
  sCom:=GetMachineString("/Hardware/Devicemap/SerialComm/\\Device\\USBSER000")
  outm("\Device\USBSER000 = " & sCom)
  
  if (sCom = "") Then 'Kart Okuyucu Takılı Değil
    outm("Kart Okuyucu Takılı Değil...Lütfen sistem yöneticinize bildiriniz")
    OpenComPort:=False
    return
  EndIf

  ' Com portu için Device nesnesi yaratılıyor
  oDev:=CreateDevice()

  oDev.SetPort(val(Right(sCom,1))) ' COM5 --> 5  
  oDev.SetBaudRate(9600) ' Hız 9600 olarak belirleniyor
  oDev.SetTimeout(500) '0.5 saniye
  outm("Set Timeout 500 mseconds (0.5 saniye)")   

  'Com portundan 20 şer karakter okunması sağlanıyor
  oDev.SetBufferSize(20) 
  outm("Set Buffer Size : 20")   

  '+
  ' Debug mesajlar Internal mesajlar halinde Terminale yazılırlar
  ' SetDebug metodu, yeni bir cihaz ile ilgili okuma, yazma akışını izleyebilmek
  ' ve varsa hatları bulabilmek için fayda sağlar.
  '-
  oDev.SetDebug(True) 
  outm("Set Debug TRUE...")   
  
  oDev.OpenDevice() 
  outm("Device Opened...")   

  bPortOpen:=True

  ' +
  '  Com portuna bağlı kart okuyucuya, kart takıldığında, StartFuncKart fonksiyonunun,
  '  kart çıkarıldığında ise StopFunc fonksiyonunun çağırılması isteniyor
  ' -  
  oDev.StartDeviceNotification("urt_isemri_takibi_dokunmatik", "StartFuncKart", "StopFunc")  
  
  OpenComPort:=True
EndFunction

Function StopReadingComPort()  

    'Okuyucuya kart takıldığında ve çıkarıldığında çalışan tetikleme yapısı durduruluyor
    oDev.StopDeviceNotification()  

    CloseComPort()
    bPortOpen:=False
  EndIf  

EndFunction             

Function CloseComPort() 
  oDev.CloseDevice()     
  outm("Device Closed...")  
EndFunction
```

**Örnek Açıklaması**\
Com portundan veri okundugunda, ilgili Anadil servisi tetiklenir.\
_Kullanım Alanı :_\
Üretim ortamları, dokunmatik veri toplama bilgisayarlarına monte edilmiş kart okuyucuları.
