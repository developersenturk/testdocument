# EnableSheet

Bu metod Tab Sheetin Enable yada disable olmasını sağlar.\
\
**Uygulandığı Nesneler**\
TAB kontrol nesnesi.\
\
**Kullanımı**

```
TabControlObject.EnableSheet(
  TabFormName As String,  ' tab formunun ismi
  bEnable As Bool         ' Sheet'in Enable veya disable olmasını belirler
)
```

**Parametreler**\
_TabFormName_\
Imagine® içinde yaratılan tab sayfası formunun ismi\
_bEnable_\
Tab Sheet'in enable veya disable olmasını belirler\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Bu method TabSheet'in Enable veya disable olmasını sağlar. 1. parametre Tabformunun ismini, 2. parametre ise kendisine verilen TRUE yada FALSE değeri ile Tab Sheet'in enable veya disable olmasını sağlar.
