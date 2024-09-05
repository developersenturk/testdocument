# RunFunc

Embed edilmiş modüle ait fonksiyonların çalıştırılabilmesini sağlar.

**Uygulandığı Nesneler**\
Embedded Modül\
\
**Kullanımı**

```
ControlObject.RunFunc(
       FullFunctionName As String,    'Embed edilmiş modülde bulunan fonksiyonunun tam adı. 
       Parametre1 As [String veya Number veya Date veya Object],    
       Parametre2 As [String veya Number veya Date veya Object],    
       Parametre3 As [String veya Number veya Date veya Object],    

       ParametreN As [String veya Number veya Date veya Object],    
  ) As [String veya Number veya Date veya Bool]
```

\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri \[String veya Number veya Date veya Bool] olabilir. Object olamaz.\
\
**Dikkat Edilecek Noktalar**\
İlk parametre fonksiyon ismi, diğerleri fonksiyonun parametreleridir. Boolean tipinde parametre geçirilemez ve object return edemez.\
\
**Örnek**

```
wrk_mahsup.mod:

Function TestNum(s1 as string, s2 as string, n as number) As Number
  TestNum:=n*2
EndFunction

Function TestStr(s1 as string, s2 as string, n as number) As String
  TestStr:=" Sonuc str  : " & s1  & " " & s2
EndFunction

Function TestDate(s1 as string, s2 as string, n as number) As Date
 Dim current As Date
 
  current:= GetSystemDate()
  TestDate:=current
EndFunction

Function TestObjPar(cff as Object, s1 As String, n1 As Number) As Bool

 outm("    TestObjPar  cff.text : "& cff.text)
 outm("    s1                   : "& s1)
 outm("    n1                   : "& str(n1))
 cff.Add("returntext","RETURN STRING1111111")

 TestObjPar:=True
EndFunction

-------------------------------------------------------------------------
Embed.ser: Bu service wrk_mahsup.mod u embed olarak kullanır

Function f_TestEmbedFcn_Click(f As Object)
Dim n   As Number
Dim s   As String
Dim d   As Date
Dim o   As Object

  n:=f.em.RunFunc("TestNum", "s111111111", "s2222", 123456)
  outm("TestNum Result : "& str(n))

  s:=f.em.RunFunc("TestStr", "s111111111", "s2222", 123456)
  outm("TestStr Result : "& s)

  d:=f.em.RunFunc("TestDate", "s111111111", "s2222", 123456)
  outm("TestDate Result : "& Format(d,"d"))

  cff:=CffCreate("TestCff")
  cff.Add("text","bu string parametre olarak gecti")
 
  b:=f.em.RunFunc("TestObjPar", cff,  "s111111", 123456789)
  if (b) then
      outm("TestObjPar OK")
  else
      outm("TestObjPar FALSE")
  endif

  outm(" ---------cff1.returntext : "& cff.returntext & "--------------")


EndFunction

Function f_LoadEm_Click(f As Object)
 'Ornek olarak r_sayaci 1000 olan muhasebe fisi, em isimli embed kontrole yüklenir.
   f.em.DocId:="wrk_muhfis"
   f.em.LoadDoc(1000)
EndFunction

Function f_UnLoad_Click(f As Object)
 'Embed modül kapatılır.
 f.em.CloseDoc()
EndFunction
```
