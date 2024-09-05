# MaxLine

MaxLine property'si bir sayfadaki maximum satır sayısını gösterir.\
\
**Kullanımı**

```
ReportObject.MaxLine As Number
```

**Geri Dönüş Değeri**\
Geri dönüş değeri sayfadaki maximum satır sayısıdır.\
\
**Dikkat Edilecek Noktalar**\
MaxLine property'si bir sayfadaki maximum satır sayısını gösterir.\
\
**Örnek**

```
Const Sayfa_Sonu_Yükseklik := 2
Function SayfaSonuKontrol(r As Report)
  If r.Curline=(r.MaxLine-Sayfa_Sonu_Yükseklik) Then
    SayfaNo:=SayfaNo+1
    SayfaSonu(r)
    r.NextPage()
  EndIf
EndFunction
```
