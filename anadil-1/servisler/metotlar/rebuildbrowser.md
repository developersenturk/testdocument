# ReBuildBrowser

ReBuildBrowser Methodu, yeniden yaratılan browser tree nin görüntülenmesini sağlar.\
\
**Kullanımı**

```
AlwaysCallObject.ReBuildBrowser() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**

ReBuildBrowser Methodu, switch edilen firmanın bilgilerine göre yeniden oluşturulmuş browser tree nin görüntülenmesini sağlar.

**Örnek**

```
Function GetBdefServices() As Number
  Dim serid As String
  Dim enum As Number
  Dim i As Number
    
  GetBdefServices := -1
  enum:=alwrun.OpenEnumExecs(2)  'services, 2 is service 
  
  if enum=0 Then ' We are now running in alwrun
    Return
  EndIf
  
  i := 0
  While TRUE
    serid:=alwrun.GetNextExec(enum)
    If serid="" Then
      Exit
    EndIf 
    If Mid(serid,1,4)="bdef" Then
      OutM(">>>>>>>>>>>>>>>>>>>>>>>>>> "&Str(i)&" : "&serid)
      i := i+ 1
      BdefServisleri[i] := serid
    EndIf  
  Wend
   alwrun.CloseEnumExecs(enum)
   GetBdefServices := i
EndFunction

  .
  .
  .
  BdefServicesCount:=GetBdefServices()
  AlwRun := GetAlwaysCallObject()
  AlwRun.ReCreateBrowser()

  For i := 1 To BdefServicesCount
    objDummy := CreateServiceCall(BdefServisleri[i], "CreateBrowsers", 0)
    if objDummy Then
      objDummy.CallService()
    EndIf
    objDummy.Close()
  Next
  
  AlwRun := GetAlwaysCallObject()
  AlwRun.ReBuildBrowser()

  AlwRun := GetAlwaysCallObject()
  AlwRun.RefreshAllBrowsers()
```

\
**İlgili komutlar:** [**ReCreateBrowser**](recreatebrowser.md)
