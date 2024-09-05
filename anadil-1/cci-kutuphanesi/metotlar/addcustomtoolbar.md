# AddCustomToolbar

Bu metod geliştirilen bir uygulamada, toolbar kullanımını gerçekleştirmektedir.\
\
**Kullanımı**

```
CCIObject.AddCustomToolbar(
  ToolbarName As String  ' toolbar ismi
  Title As String        ' toolbar başlık bilgisi
  GDIObject As Object    ' bitmap resmi içeren nesne
)
```

**Parametreler**\
_ToolbarName_\
Toolbar için verilen referans ismidir.\
_Title_\
Toolbar'ın Always® terminalinde bağımsız görüntüsünde son kullanıcının gördüğü en üstteki başlık bilgisidir.\
_GDIObject_\
Dahilinde bitmap resmin olduğu GDI nesnesidir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Herhangi bir Always® uygulamasında Toolbar uygulaması için atılacak ilk adım, Anadil® koduyla bu metodu kullanarak toolbar tanımlama işleminin gerçekleştirilmesidir.\
\
Toolbar için GDI nesnesi verilmeden önce, nesnenin daha önceden oluşturulmuş olması ve dahiline de bitmap resminin eklenmiş olması gerekmektedir.\
\
Verilen toolbar referans ismi de, bu toolbar'a ilişkin daha sonraki uygulanacak işlemlerde, ayırt edici isim olacak ve bu isim sayesinde toolbar işlemleri gerçekleştirilecektir.
