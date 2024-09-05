# CreateDialog

Bu fonksiyon modeless bir diyalog kutusu oluşturulmasını sağlamaktadır.\
\
**Kullanımı**

```
Function CreateDialog(
  FormName As String,  ' form ismi
  xpos As Number,      ' yatay koordinat değeri
  ypos As Number       ' dikey koordinat değeri
)As Object
```

\
**Parametreler**\
_FormName_\
Imagine® içinde yaratılan diyalog kutusu formunun ismi,\
_xpos_\
Diyalog kutusu koordinatlarının yatay değeri,\
_ypos_\
Diyalog kutusu koordinatlarının dikey değeri.\
\
**Geri Dönüş Değeri**\
Geri dönüş nesnesi bir form nesnesidir, ve form nesneleri ile ilgili yapılan işlemlerde kullanılmaktadır.\
\
**Dikkat Edilecek Noktalar**\
Modal diyalog kutusuna alternatif olarak da modeless bir diyalog kutusu bu fonksiyon ile oluşturulabilmektedir. Modeless diyalog kutuları kendilerine ait formu olan ve üzerinde normal kontrolleri olan kutulardır, ancak farkları bu kutular giriş işlemini arka planda bekleyebilmektedir, ve de window sınırları vardır. Bir kere açıldıklarında kritik bir şekilde ön planda değillerdir.\
Ayrıca açık oldukları sürece ait oldukları MDI uygulamanın sahip olduğu 'açık pencereler' listesinde görülmezler. Aslında MDI window'a da ait değillerdir çünkü 'Maximize' seçeneği ile MDI window sınırlarını aşmaktadırlar. Son kullanıcı açısından da bu tür dezavantajları nedeniyle kullanım açısından pratik değillerdir. Uygulama geliştirilen kimseler tarafından da bu sakıncalarından dolayı kullanımı fazla tercih edilmeyen diyalog kutularındandır.
