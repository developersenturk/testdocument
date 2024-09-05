# DialogBox

Bu fonksiyon modal bir diyalog kutusu oluşturulmasını sağlamaktadır.\
\
**Kullanımı**

```
Function DialogBox(
  FormName As String,  ' form ismi
  xpos As Number,      ' yatay koordinat değeri
  ypos As Number       ' dikey koordinat değeri
)As Number
```

\
**Parametreler**\
_FormName_\
Imagine® içinde yaratılan dialog kutusu formunun ismi,\
_xpos_\
Dialog kutusu koordinatlarının yatay değeri,\
_ypos_\
Dialog kutusu koordinatlarının dikey değeri.\
\
**Geri Dönüş Değeri**\
Fonksiyon çağrıldıktan sonra geri dönen sayı dialog kutusunun açılması ile ilgili bilgi vermektedir. Sayının değeri -1 olduğunda başarısız bir işlem gerçekleştiği anlaşılmalıdır.\
Başarısızlığın nedeni form isminin yanlış olmasından veya ilgili formun bulunamamasından olabilir. Geri dönüş değeri 0 ise diyalog kutusu başarılı bir şekilde oluşturulmuş demektir.\
\
**Dikkat Edilecek Noktalar**\
Bu fonksiyon yardımıyla modal bir diyalog kutusu oluşturulabilmektedir. Modal diyalog kutuları kullanıcıdan mutlaka bir giriş değeri beklemekte olan kutulardır. Yani Always® bu kutunun sonucunu almadan başka bir işlem yapamayacaktır. Hatta mouse ile diyalog kutusunun sınırları dışına tıklamanız bile etkisiz olacaktır.\
Örnek vermek gerekirse herhangi bir Windows uygulamasının DosyaAç bölümü bir modal diyalog kutusu uygulamasıdır.\
Dialog kutusu ekrana geldiğinde koordinat olarak pozisyonu belirlenirken, koordinat değerleri (0,0) olan koordinat ekseninin başlangıç noktası tüm ekranın sol üst köşesidir. Kutunun hesaplanan pozisyon değerleri yine sol üst köşesine göre belirlenmektedir.
