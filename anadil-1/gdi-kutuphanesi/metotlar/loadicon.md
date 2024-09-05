# LoadIcon

Bu metod GDI nesnesine ICON eklenmektedir.\
\
**Kullanımı**

```
GDIObject.LoadIcon(
  IconName As String  ' Icon ismi
)
```

**Parametreler**\
_IconName_\
Imagine® altında uygulamanın parçası olan, geliştirilen uygulama içerisinde, "Grafikler" grubunda "Simge" adı altında yer alan ICON ismidir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Metodun kullanımı ile form tabanlı çalışmakta olan Always® uygulamalarında, son kullanıcının Always® terminalinde uygulamayı MINIMIZE ile küçülttüğünde karşısına gelen ICON şekli belirlenmektedir. ICON'un daha önceden Imagine® altında grafikler bölümünde simge adı altında kayıtlı olması gerekmektedir.\
\
Metodun kullanımı yani ICON yükleme işlemi myform\_GetIcon() event'i içerisinde gerçekleştirilmektedir. Burada GDI nesnesi de parametre olarak event dahilinde geldiğinden ayrıca GDI nesnesi oluşturulmamaktadır.
