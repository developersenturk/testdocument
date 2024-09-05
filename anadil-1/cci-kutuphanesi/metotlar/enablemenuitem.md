# EnableMenuItem

Bu metod popup menü sisteminde, menü seçeneklerinden birini devre dışı veya tekrar kullanılabilir kılmaktadır.\
\
**Kullanımı**

```
CCIObject.EnableMenuItem(
  MenuName As String,  ' Popup menü referans ismi
  CmdNum As Number,    ' Menü seçeneği referans numarası
  ItemEnable As Bool   ' Aktif edilme bilgisi
)
```

**Parametreler**\
_MenuName_\
Burada verilen menünün genel referans ismi olup, Anadil® içersinde daha önceden menü oluşturulurken .AddCustomMenu ile verilen isimdir.\
_CmdNum_\
Menü seçeneğine ait referans numarasıdır.\
_ItemEnable_\
Bool olan bu ifade False olduğunda menü seçeneği devre dışı olacak, son kullanıcı bu menü seçeneğini seçemeyecektir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Bu metod kullanımı ile CCI dahilinde geliştirilmiş olan menü sisteminde, menü seçeneklerinden herhangi birinin geçici olarak devre dışı bırakılması sağlanmaktadır. Devre dışı kalan menü seçeneği Always terminalinde, diğer menü seçenekleri arasında farklı bir renkte görünecektir.\
\
Devre dışı kalan menü seçeneği yine bu metodun kullanımı ile ItemEnable parametresinin True şeklinde verilmesi ile tekrar seçilebilir hale getirilebilmektedir.
