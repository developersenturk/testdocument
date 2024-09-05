# AddCustomMenu

Bu metod geliştirilen bir uygulamada popup menü sistemini oluşturmaktadır.\
\
**Kullanımı**

```
CCIObject.AddCustomMenu(
  MenuName As String    ' menü referans ismi
  PopupTitle As String  ' uygulamada görülen pop-up isim
  MenuPos As Number     ' menünün pozisyon index değeri
)
```

**Parametreler**\
_MenuName_\
Oluşturulan menü sisteminin Anadil kodu için referans ismi.\
_PopupTitle_\
Menünün, uygulama esnasında Always® terminalinden görünen ismi\
_Menupos_\
Menünün Always® terminalinde diğer menüler arasındaki yerini belirler.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
MenuName parametresi ile verilen isim bilgisi menüden yapılan işlemlerde event dahilinde gerçekleşen seçimlerde ve menü seçeneklerinin belirlenmesinde kullanılacaktır.\
\
PopupTitle ise uygulamanın son kullanıcı karşısına Always® terminalinde geldiğinde karşısına gelen menü başlık ismidir. Bu ismi verirken herhangi bir harften önce yazılan "&" işareti ile, o karakterin altının çizilmesi sağlanmaktadır. Bunun anlamı ise mouse kullanmadan, klavyeden ALT ile beraber o harfe basılması ile menü'den seçim yapabilecek şekilde menünün açılmasını sağlayabilmesidir.\
\
Menülere bu şekilde kısayol tuşları atarken Always® terminalindeki diğer kısayol tuşları ile çakışmamasına dikkat edilmesi gerekmektedir.\
\
Pozisyon indexleme numarası ise 0(sıfır) dan itibaren başlamaktadır. Yani Always® terminalindeki ilk popup menü olan "Dosya", 0. Index numarasına sahiptir. Ancak 0 ve 1 index numaraları Always tarafından reserved edilmiştir. Yani eklenecek menünün index numarası 3 ten başlamalıdır.
