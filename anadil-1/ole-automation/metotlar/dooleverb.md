# DoOLEVerb

Bu method, bir ole nesnesini execute eder.\
\
**Kullanımı**

```
ControlObject.DoOLEVerb(
  Verb As String
) As Bool
```

**Parametreler**\
_Verb_

**Geri Dönüş Değeri**\
Geri dönüş değeri OLE nesnesidir.\
\
**Dikkat Edilecek Noktalar**\
Bu method, bir ole kontrol üzerinde yaratılan OLE nesnesini aktif hale getirir.

```
  ControlObject.OLEActivate(TRUE)
```
