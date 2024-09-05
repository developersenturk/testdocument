# LoadBitmap

Bu metod GDI nesnesine BITMAP resmi eklenmektedir.\
**Kullanımı**

```
GDIObject.LoadBitmap(
  BitmapName As String  ' Anadil projesi icinde bulunan bitmap ismi veya bitmap dosya ismi
)
```

**Parametreler**\
_BitmapName_\
Imagine® ile görülebilen, geliştirilen uygulama içersinde, "Grafikler" grubunda "Bit Eşlem" adı altında yer alan BITMAP ismidir. Eğer Anadil projesi içinde verilen isimde bitmap bulunamazsa verilen isim, bitmap dosya ismi olarak değerlendirilir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Metodun kullanımı ile harhangi bir GDI nesnesi dahilinde bir bitmap resmi eklenmektedir ki bu da daha sonra CCI kütüphanesi kullanımında gerekebilecek olan bir resim bilgisidir.\
\
CCI kütüphanesi kullanımında özellikle Toolbar uygulamasında gereken, toolbar'ın üzerinde yer alan button resimleri de aslında birer küçük bitmap resmi olup, bu resimler de bu metod yardımıyla Anadil® içersinde yerleştirilmektedir.\
\
Unutulmaması gereken başka bir husus da her toolbar button resminin 16x16 pixel olduğudur. Bir toolbar'a ilişkin bütün button resimleri grup halinde ele alındığından, gereken resmin boyutları yan yana gelen 16x16'lık ebatların toplamı kadar olacaktır.\
\
Sonuç olarak resmin yüksekliği 16 pixel olacak, genişliği ise 16'nın katları şeklinde toolbar'daki button sayısına bağlı olarak gerçekleşecektir.\
**Örnek**\
gdiobj.LoadBitmap("tus.bmp") ' Anadil projesine alinmis Bit Eşlem yükleniyor gdiobj.LoadBitmap("c:\Always\resim.bmp") 'Diskte bulunan bir bitmap yükleniyor Yüksek çözünürlüğe sahip bitmapleri de yükleyebilirsiniz. Bu tip bitmapleri, projeleri gereksiz olarak büyüteceğinden, Anadil projelerinin içine saklamayıp direkt yükleyip kullanmanız önerilir.
