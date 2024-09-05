# SetObjectValue

Bu method ile OLE Automation nesnesi içerisindeki bir nesneye değer gönderilir.\
\
**Kullanımı**

```
OLEObject.SetObjectValue(
  ObjectName As String  ' Nesne adı 
  Value As Bool         ' Property değeri
) As Object
```

\
**Parametreler**\
_ObjectName_\
OLE Automation nesnesi altında yer alan nesne adı\
_Value_\
Nesneye geçirilmek istenen değerdir.\
Kullanılan property'e göre Value değişkeninin tipi Boolean, Anavariant veya Object olabilir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemli değildir.\
\
**Dikkat Edilecek Noktalar**\
