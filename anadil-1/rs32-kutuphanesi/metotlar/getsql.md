# GetSQL

Bu method, olusturulan rs SQL tümcesini, varsa parametre değerleri ile birlikte, string object olarak geri döndürür. Internal mode terminalde SQL string görülebilir. Excel e SQL Server dan direkt raporlama (tablereport) amacıyla kullanılabilir.

**Kullanımı**

```
RSObject.GetSQL(
)As Bool
```

\
**Geri Dönüş Değeri**\
SQL tümcesi 255 karakterden daha büyük olabileceği için, XML object yaratılır ve SQL string içeren XML object geri döner.\
\
**Dikkat Edilecek Konular**\
Date tipindeki alanların değerleri, _Ay/Gün/Yıl_ formatında yer alır.

**Örnek**

```

  Dim  Rs as object
  Dim tar as Date
  Dim str as String
  Dim num as Number

  tar:=Str2Date("30/10/2003")
  str:="StringParameter"  
  num:=123456789
  
  Rs:=PrepareStmDirect("Select kod from wrk_hesap_plani Where r_sayac = (?) and tarih = (?)  param = (?)")
  Rs.SetParam(num)
  Rs.SetParam(tar)
  Rs.SetParam(str)
  oXML:=Rs.GetSql()
  oXML.Dump("c:\Always\sql.txt", 0)
```
