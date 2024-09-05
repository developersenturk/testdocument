# PressToolbarButton

Bu metod bir toolbar buttonu üzerinde basılmasını sağlamaktadır.\
\
**Kullanımı**

```
CCIObject.PressToolbarButton(
  ToolbarName As String  ' toolbar ismi
  CmdNum As Number       ' button referans ismi
  Pressed As Bool        ' basılı olma bilgisi
)
```

**Parametreler**\
_ToolbarName_\
Toolbar için kullanılan referans ismidir.\
_CmdNum_\
Toolbar üzerindeki button'ları birbirinden ayıran referans numarasıdır.\
_Pressed_\
Toolbar button'una basılı olarak görünebilmesi için verilen Bool ifadedir. True olarak verildiğinde işlem gerçekleşmektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Windows uygulamalarında bazı durumlarda toolbar button'ları ekranda daha önceden basılmış şekilde görülebilmektedir. Bu duruma örnek olarak bir seçimi ifade eden grup halinde yan yana yer alan toolbar button'larını verebiliriz. Böyle bir anda grup arasındaki sadece bir button basılı olarak gözükmektedir.\
\
Bu metodla toolbar basılma işlemleri gerçekleştirilebilmekte, basılan bir toolbar button'unun tekrar eski haline dönmesi ise metod parametresinin False olarak verilmesi ile gerçekleştirilmektedir.
