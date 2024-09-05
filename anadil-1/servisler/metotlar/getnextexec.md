# GetNextExec

GetNextExec Methodu, bir sonraki executable'ı getirir.\
\
**Kullanımı**

```
AlwaysCallObject.GetNextExec(
  EnumID As Number  ' Executable Id no	
) As String
```

**Parametreler**\
_EnumID_\
Kapatılmak istenen Executable'ın Id numarasıdır.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri String'dir.\
\
**Dikkat Edilecek Noktalar**\
CloseEnumExecs Methodu, executable numarası verilen excutable'ı kapatır\
\
**Örnek**

```
Dim alw As Object
Dim enum As Number
Dim serid As String
Dim servids[100] As String
Dim nser As Number
  alw:=GetAlwaysCallObject()
  enum:=alw.OpenEnumExecs(2)  'services
  
  While TRUE
    serid := alw.GetNextExec(enum)
    if left(serid,4)="tnm_" Then
      nser:=nser+1
      servids[nser]:=serid
    Endif
  Wend
  alw.CloseEnumExecs(enum)
```

Yukarıdaki örnekte, Servis Id'leri "tnm\_" ile başlayan servisler teker teker bir diziye atanıyor.
