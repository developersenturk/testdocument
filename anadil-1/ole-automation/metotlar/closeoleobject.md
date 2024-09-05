# CloseOleObject

Bu method, bir ole kontrol üzerinde yaratılmış OLE nesnesini close eder.\
\
**Kullanımı**

```
ControlObject.CloseOleObject(
  bSave As Bool  
)
```

**Parametreler**\
_bSave_\
bSave TRUE olduğunda OLE nesnesi saklanarak kapatılır.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlem başarılı ise TRUE, değilse FALSE ifadedir.\
\
**Dikkat Edilecek Noktalar**\
Bu method, bir ole kontrol üzerinde yaratılan OLE nesnesini close eder.

```
  ControlObject.CloseOleObject(TRUE)
```
