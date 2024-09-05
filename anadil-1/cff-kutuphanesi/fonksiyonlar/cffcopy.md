# CFFCopy

Bu fonksiyon kaynak CFF i hedef CFF e kopyalar.\
\
**Kullanımı**

```
Function CFFCopy(
  HedefCFF As Object  'Hedef CFF nesnesi
  KaynakCFF As Object  'Kaynak CFF nesnesi
)As Boolean
```

**Parametreler**\
_HedefCFF_\
Üzerine kopyalama yapılacak hedef CFF nesnesidir.\
\
_KaynakCFF_\
Kopyası alınacak kaynak CFF nesnesidir.\
\
**Geri Dönüş Değeri**\
TRUE/FALSE şeklindedir.\
\
**Örnek**

```
Dim hCFF as Object
Dim kCFF as Object

kCFF:=CFFCreate("KaynakCFF")
kCFF.Add("Entry1", "Entry1")
kCFF.Add("Entry2", 123456)
.
.
.
'Hedef CFF yaratılıyor
hCFF:=CFFCreate("HedefCFF")

'Kopyalama işlemi yapılıyor
CFFCopy(hCFF, kCFF)

'Hedef CFF dump ediliyor
hCFF.DumpCFF() 'c:\Always\cff.txt ye bakiniz 
```

\
**İlgili Konular: CFFCreate cff.Clear**\
