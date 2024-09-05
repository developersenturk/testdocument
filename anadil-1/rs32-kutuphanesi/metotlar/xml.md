# xml

Bu method Database BLO TEXT Object datasını XML objectine dönüştürür.

**Kullanımı**

```
BLOObject.xml(
) As Object
```

\
**Geri Dönüş Değeri**\
Geri dönüş değeri, XML objectidir.\
\
**Örnek**

```

Text kolonu bilgisinin okunması

  rs:=PrepareStmDirect("Select text from wrk_hesap_plani where r_sayac=36056")
  if  Rs.ExecuteStm() Then
      oBlo:=CreateBlo()
      oBlo.Load(rs, "text")
      oXML:=CreateXML()
      
      'BLO Text object, XML Text object e donusturuluyor
      oXML:=oBlo.xml()
      oXML.Dump("c:\Always\text1.txt",0)
  Endif

```
