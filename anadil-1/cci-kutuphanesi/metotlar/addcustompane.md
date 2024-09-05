# AddCustomPane

Bu metod Always® statusbarindaki pane sistemi kullanımını sağlamaktadır.\
\
**Kullanımı**

```
CCIObject.AddCustomPane(
  PaneName As String  ' pane ismi
  Pos As Number       ' diğer pane'ler arasındaki sırası
  Len As Number       ' oluşturulan pane genişliği
)
```

**Parametreler**\
_PaneName_\
Yerleştirilen pane için verilen referans ismi.\
_Pos_\
Always® terminalindeki diğer pane'ler arasındaki yeri.\
_Len_\
Yerleştirilen pane için verilen genişlik.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Pane sisitemi Windows uygulamalarında özellikle MDI uygulamalarında daha çok karşımıza çıkmakta olan, pencerenin en altında yer alan bilgi sistemi sahasıdır. Pane statü bilgileri ve genel bilgiler verebildiği gibi, üzerinde çalışılan belge ile ilgili de özel bilgiler sunabilmektedir.\
\
Örnek olarak genel bilgiler arasında, zaman ile ilgili bilgileri, özel olarak da o anki aktif belge ile ilgili detay bilgileri verebiliriz.\
\
Bu metod kullanımı ile, Always® terminalinde yer alan pane sisteminde bir saha taleb edilmektedir. Bu sahanın sıra numarası ise soldan itibaren diğer pane'ler arasında kaçıncı sırada olacağını belirlemektedir. Bu parametrenin 1 olarak verilmesi, oluşturulan pane'in, diğerleri arasında en solda yer alacağına karşılık gelmektedir.\
\
Pane uzunluğu olarak verilen sayı ise "dialog unit" denilen Windows özel birimi cinsinden olup, herhangi bir özel pixel'den veya ekran çözünürlüğünden bağımsız bir değer olmaktadır.
