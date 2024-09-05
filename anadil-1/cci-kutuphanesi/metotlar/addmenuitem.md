# AddMenuItem

Bu metod bir popup menü altındaki, seçenek ifadeleri yerleştirmektedir.\
\
**Kullanımı**

```
CCIObject.AddMenuItem(
  MenuName As String,  ' Menü ismi
  ItemText As String,  ' Eklenen menü text ifadesi
  CmdNum As Number     ' menü seçeneği referans no
)
```

**Parametreler**\
_MenuName_\
Hangi menü altında yer alacağını belirtir. AddCustomMenu() metodu ile daha önceden verilmiş, popup menünün genel referans ismidir.\
_ItemText_\
Menü seçeneğine ait, Always® terminalinde görünen isim bilgisidir.\
_CmdNum_\
Menü seçeneğine ait, event yazarken kullanılacak olan command index numarasıdır. Bu index menü seçenekleri arasında ayırıcı olmaktadır.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
ItemText verilirken ise aynen .AddCustomMenu() metodunda olduğu gibi "&" sembolü kullanarak, menü seçeneği text ifadesinde bir karakterin altı çizilmesi sağlanabilmektedir. Bunun sonucunda, menü aktif olduktan sonra, klavyeden altı çizili olan karaktere basılması ile menü elemanı seçilebilmektedir.\
\
Ayrıca ItemText verilirken "-"(eksi işareti) şeklindeki kullanım ise, menü seçenekleri arasında ayırıcı bir çizgi çizecektir. Bu da birçok seçeneğin gruplanmasında kullanılabilen bir özelliktir.\
\
CmdNum ile verilen command numarası ise daha sonra bu menü seçeneği ile ilgili yapılan referanslarda ve Anadil® ile bu seçeneğe ilişkin event driven kod yazılırken kullanılacaktır.
