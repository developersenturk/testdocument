# AddCustomAccelerator

Bu metod herhangi bir Always® uygulamasında accelerator kullanımını gerçekleştirmektedir.\
\
**Kullanımı**

```
CCIObject.AddCmdAcceleratorKey(
  AccName As String		' accelerator ismi
)
```

**Parametreler**\
_AccName_\
Oluşturulmak istenilen accelerator için verilecek isim.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Accelerator'lar veya Türkçe anlamıyla hızlandırıcılar, herhangi bir Windows uygulamasında yapılabilecek işlemleri daha kısa zamanda gerçekleştirebilmek amacıyla uygulanan kısayol tuşlarıdır. Mesela bir belgenin saklanmasına ilişkin işlemi herhangi bir menüden gerçekleştirebildiğimiz gibi aynı anda bir hızlandırıcı üzerinden yürütebiliriz.\
\
Uygulama son kullanıcısı da seri halde iş yaparken bu hızlandırıcı tuşlar yardımıyla daha verimli olarak çalışabilmektedir.\
\
Hızlandırıcılar tuş kombinasyonlarından oluşmakta ve SHIFT, CONTROL ve ALT tuşları ile birlikte uygulanmaktadırlar.\
\
Hızlandırıcı uygularken dikkat edilmesi gereken başka bir nokta da, Windows'un kendi kullandığı bazı hızlandırıcı tuş kombinasyonlarının, Anadil® ile geliştirilen uygulamaya yerleştirilmesinin mümkün olmamasıdır.
