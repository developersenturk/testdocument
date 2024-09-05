# CreateDevice

Bu fonksiyon bir Communication Device nesnesi elde edilebilmesini sağlamaktadır.\
\
**Kullanımı**

```
Function CreateDevice() As Object
```

**Parametreler**\
Fonksiyonun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, içeriği Communication Device nesnesi olan nesnedir.\
\
Bu fonksiyon, Always Framework'ün çalıştığı bilgisayardaki COM portları üzerinden, çeşitli cihazlar ile iletişim kurulabilmesi için, bir iletişim nesnesi yaratmaktadır. Örnek : POS cihazları.\
\
\
**Örnek Program**\


```
Function ComRead()
  Dim oDev as Object
  Dim sWord As String
  Dim sLine As String
  Dim s1    As String
  Dim STX As String
  Dim ETX As String
  Dim ACK As String
  Dim NAK As String
    
  STX:=chr(2)
  ETX:=chr(3)
  ACK:=chr(6)
  NAK:=chr(21)

  oDev:=CreateDevice()
  
  oDev.SetPort(1) ' COM1
  oDev.SetBaudRate(9600)
  oDev.SetTimeout(8000) '8 saniye
  
  oDev.OpenDevice()
  
 'Kredi kartı pos cihazından geçiriliyor ve porttan gelen bilgiler okunuyor.
  sWord:=oDev.ReadDevice()

  outm(sWord)
  sLine:=sLine & sWord
  outm("sLine 1 st --- >>>>>>>>>>>>>>>>> " & sLine)
  If length(sWord) > 0 then
      outm("Length > 0 OK  sWord   : " & sWord)
 
   'Timeout 1 saniyeye düşürülüyor   
    oDev.SetTimeout(1000)
    
    do
      sWord:=oDev.ReadDevice()
      outm("sWord >>>>>>>>>>>>>>>>>>>    : " & sWord)
      sLine:=sLine & sWord
    loop while (Length(sWord) > 0)
    
    outm("sLine --- >>>>>>>>>>>>>>>>>>> " & sLine)

    'Send NAK
    'oDev.WriteDevice(NAK)
    
    'Send ACK
    oDev.WriteDevice(ACK)
    
    Sleep(200)
    
   'Pos cihazına slip basması için bilgiler yollanıyor
    'Send STX
    oDev.WriteDevice(STX)
    
    'Merchant_no  15 bytes
    oDev.WriteDevice("123456789012345")
    
    'date_time    14 bytes
    oDev.WriteDevice("20020820230500")
    
    'trans_seq     4 bytes
    oDev.WriteDevice("4444")
    
    'response_code 3 bytes
    oDev.WriteDevice("000")
    
    'approval code 6 bytes
    oDev.WriteDevice("666666")
    
    'merchant name 30 bytes
    oDev.WriteDevice("CetinlerAŞCetinlerAŞCetinlerAŞ")
    
    'tutar 12 bytes
    oDev.WriteDevice("123456789012")
    
    'ETX            1 byte
    oDev.WriteDevice(ETX)
    
    'LRC            1 byte
    oDev.WriteDevice(">")
    
    'Read ACK
    sWord:=oDev.ReadDevice() 

  EndIf
    
  'ParseInput(sLine)

 'Device close ediliyor.
  oDev.CloseDevice()

EndFunction
```
