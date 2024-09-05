# SetTimer

Servis'e kronometre set eder.\
\
**Kullanımı**

```
ServiceObject.SetTimer(
  TimerId As Number  ' Timer'a verilen belirteç
  TimeOut As Number  ' millisecond 
) As Bool
```

**Parametreler**\
\
_TimerId_\
Timer'a verilen belirteç.\
\
_TimeOut_\
Millisecond biriminden Time out süresi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Konular**\
SetTimer Methodu millisecond cinsinden belirtilen sürede bir OnTimer eventini generate edecektir.
