# R\_STATE\_TERMINATED

Başarılı bir şekilde durdurulan raporun status değeridir.\
\
**Kullanımı**

```
Function OnReportFinish(rState As Number) As Bool
 'This is called when the report is finished.
 'rState : R_STATE_ENDOFREPORT

 if (rState=R_STATE_ENDOFREPORT) Then
    outm("Rapor basariyla sonuclanmistir")
 EndIf

 OnReportFinish:=True
EndFunction

Function OnReportCancelled(rState As Number) As Bool
 'This is called when the report is cancelled.
 'rState : R_STATE_TERMINATED  R_STATE_TERMINATEDABNORMAL

 if (rState=R_STATE_TERMINATED) Then
    outm("Rapor basariyla durdurulmuştur")
 else
 if (rState=R_STATE_TERMINATEDABNORMAL) Then
    outm("Rapor durduruldu! Sistem kararsız duruma gelmiş olabilir. Lütfen programdan çıkınız!")
 EndIf

 OnReportCancelled:=True
EndFunction

```

\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
