# EnableToolbarButton

Bu metod bir toolbar button'unu kullanım dışı bırakmaktadır.\
\
**Kullanımı**

```
CCIObject.EnableToolbarButton(
  ToolbarName As String  ' toolbar ismi
  CmdNum As Number       ' button referans numarası
  ButtonEnable As Bool   ' aktif olma bilgisi
)
```

**Parametreler**\
_ToolbarName_\
Toolbar için kullanılan referans ismidir.\
_CmdNum_\
Toolbar üzerindeki button'ları birbirinden ayıran referans numarasıdır.\
_ButtonEnable_\
Devre dışı bırakılacak veya tekrar aktif olmasını sağlayan Bool ifadedir. Eğer False olarak verilirse button geçici olarak devre dışı kalacaktır.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Bütün button'lar ilk toolbar içersinde yerleştirildiklerinde aktif edilme bilgileri ilk değer olarak True değere sahiptir. İstenildiğinde bu metod kullanımı ile bu bilginin değeri False şeklinde değiştirilerek button geçici olarak devre dışı kalabilmektedir.\
\
Toolbar buttonları devre dışı kaldıklarında Always® terminalinde diğer buttonlar arasında soluk olarak gözükmekte ve son kullanıcı bu button'a ilişkin herhangi bir işlem yapamamaktadır.\
\
Tekrar button kullanımını aktif hale getirmek için yine bu metodla, aktif olma bilgisi True şeklinde parametre olarak verilmesi yeterlidir.
