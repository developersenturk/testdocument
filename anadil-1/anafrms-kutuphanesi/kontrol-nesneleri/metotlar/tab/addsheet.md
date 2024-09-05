# AddSheet

Bu metod tab sistemine, tab sayfalarını eklemektedir.\
\
**Uygulandığı Nesneler**\
TAB kontrol nesnesi.\
\
**Kullanımı**

```
TabControlObject.AddSheet(
  TabFormName As String,  ' tab formunun ismi
  TabName As String       ' tab başlık bilgisi
)
```

**Parametreler**\
_TabFormName_\
Imagine® içinde yaratılan tab sayfası formunun ismi\
_TabName_\
Tab sayfasının üstünde yer alan başlık bilgisi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
TAB sisteminde her TAB sayfası form olarak ayrı ayrı yaratılmakta ve bu ayrı sayfalar bu metodla birleştirilmekte kullanıcının karşısına da üst üste bindirilmiş şekilde çıkmaktadır.\
\
TabControlObject olarak verdiğimiz nesne ilk başta TAB sisteminin hepsini üzerinde barındırmakta olan bir formun sahip olduğu, Imagine® ile yerleştirdiğimiz TAB kontrolüdür. Birinci parametre ile tab sayfalarının olduğu formlar verilmekte ikinci parametre ile bu tab sayfalarının son kullanıcı karşısına çıkarken görünen başlık bilgisi verilmektedir.
