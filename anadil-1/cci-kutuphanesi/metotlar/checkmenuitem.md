# CheckMenuItem

Bu metod popup menü sisteminde, menü seçeneklerini işaretlemekte veya işareti yok etmektedir.\
**Kullanımı**

```
CCIObject.CheckMenuItem(
  MenuName As String,  ' Popup menü referans ismi
  CmdNum As Number,    ' Menü seçeneği referans num	
  CheckEnable As Bool  ' Check işlemi bilgisi
)
```

**Parametreler**\
_MenuName_\
Burada verilen menünün genel referans ismi olup, Anadil® içersinde daha önceden menü oluşturulurken. AddCustomMenu() ile verilen isimdir.\
_CmdNum_\
Menü seçeneğine ait referans numarasıdır.\
_CheckEnable_\
İşaretleme bilgisi True verildiğinde gerçekleşmektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Windows uygulamalarında sıklıkla kullanılmakta olan menü seçeneklerinin işaretlenmesi yoluyla, o an uygulama ile ilgili yapılan bir işlem hakkında bilgi verilebilmektedir. Menü seçeneğinin işaretlenmesi ise sol yanına "" sembolü yerleştirilmesi şeklinde Always® tarafından uygulanmaktadır.\
\
Menü seçeneklerinin işaretlenmek istendiğinde CheckEnable BOOL parametresi True olarak verilmekte; eğer işaretleme iptal edilmek isteniyorsa yine aynı parametre False olarak verilmektedir.
