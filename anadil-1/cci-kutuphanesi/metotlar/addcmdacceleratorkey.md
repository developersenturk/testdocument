# AddCmdAcceleratorKey

Bu metod accelerator altında uygulanacak tuş kombinasyonlarını belirlemektedir.\
\
**Kullanımı**

```
CCIObject.AddCmdAcceleratorKey(
  AccName As String  ' accelerator ismi
  CmdName As String  ' menü veya toolbar ismi
  CmdNum As Number   ' atanan tuş referans numarası
  KeyAsc As Number   ' tuş ASCII değeri
)
```

**Parametreler**\
_AccName_\
Accelerator için kullanılan referans ismi.\
_CmdName_\
Eğer accelerator bir menü'ye veya toolbar sistemine atanmak isteniyorsa, gereken referans ismidir, veya sade accelerator uygulamasında boş string olmaktadır.\
_CmdNum_\
Accelerator için verilen referans numarası veya menü veya toolbar dahilindeki kontrollere ait olan referans numarasıdır.\
_KeyAsc_\
Accelerator olarak verilecek olan tuş bilgisidir. Tuş ile beraber kullanılan tamamlayıcı diğer kontrol sayısı FALT, FCONTROL, FSHIFT şeklinde sabit sayılarla belirlenmektedir. Bu kontrol sayısı sayesinde ALT, CONTROL ve SHIFT tuşları ile beraber accelerator uygulanmaktadır. Bu değer + ile gerçek tuş değerine eklenmekte ve sonuç sayısı fonksiyon tarafından kullanılmaktadır.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Burada parametre olarak verilen CmdNum ile hızlandırıcılar arasında ayırım işlemi gerçekleşmektedir. Verilen bu değer daha sonra event programlama yaparken, hızlandırıcı için kullanılacak olan numaradır.\
\
Accelerator uygulaması tek başına yapıldığı gibi, daha önceden CCI dahilinde geliştirilmiş olan menü veya toolbar sistemine atama da yapılabilmektedir. Tek başına kullanımda CmdName parametresi boş string yani "" şeklinde verilmelidir.\
\
Eğer menü veya toolbar sistemine bağlanmak isteniyorsa, CmdName parametesi olarak, menüye veya toolbar'a ait olan referans ismi verilmelidir. Menü veya toolbar sistemine atama yapıldığında, accelerator için çalışan event çalışmayacak onun yerine menü veya toolbar event devreye girecektir.\
\
Menü veya toolbar sistemine yapılan yönlendirmede, hangi menü item veya toolbar button'u için atama yapılmakta olduğu, bu kontrollere ait olan daha önceden belirlenmiş olan referans numaraları CmdNum parametresi ile verilmektedir.\
\
Hızlandırıcı tuş kullanırken, büyük ve küçük harfler aynı şekilde değerlendirilmektedir. Yani bir harfin, büyük ve küçük hallerinin ASCII kodlarının değişik olması sayesinde ayrı ayrı hızlandırıcılar uygulayamazsınız.
