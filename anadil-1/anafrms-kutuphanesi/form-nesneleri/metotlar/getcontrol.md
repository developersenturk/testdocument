# GetControl

Bu method ismi verilen kontrol nesnesini döndürür.\
\
**Kullanımı**

```
FormObject.GetControl(
  name  'kontrol ismi
)
```

\
**Parametreler**\
_name_\
Kontrol nesnesinin ismidir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
GetControl Methodu ismi verilen bir kontrol nesnesini döndürür.\
Kullanım alanına bir örnek verecek olursak;\
Bir formun üzerindeki kontrollerin değerlerini bir array'e atalım ve form üzerindeki kontrollere 1,2,3... gibi isimler verelim.

```
Dim i As Number
Dim S[100] As String
Do 
  i:= i + 1
  S[i] := f.GetControl(Str(i)).ValueStr
Loop
```

Yukarıdaki örnekte de görüldüğü gibi GetControl methodu ile form üzerindeki kontrollere kolayca erişilebilmektedir.
