# Search

Bu metod kullanıldığı grid sütunu dahilindeki hücrelerde Browser yardımıyla arama işlemi uygulamaktadır.\
\
Uygulandığı Nesneler\
Grid sütunu nesneleri.\
\
**Kullanımı**

```
GridColObject.Search(
  ' Not: Metod parametrelerinin kullanımı opsiyoneldir,
  ' kullanıma göre parametre sayısı 0, 1 veya 2
  ' olabilmektedir.
  SortOrderColName As String,  ' Browser sıralama bilgisi
  CellObject.Value*            ' hücre içerik değeri
)
```

**Parametreler**\
Parametre sayısı değişken olabilen bir metoddur. Bunun sonucu olarak 0, 1, 2 parametre sayısı ile bu metod uygulanabilmektedir.\
_SortOrderColName_\
Browser üzerinden uygulanacak arama işlemi yapılırken, gelen kayıtların sıralanacağı sütun bilgisi.\
_CellObject.Value\*_\
Arama işleminde verilebilecek öndeğer olan kontrolün içeriğidir. Property olarak hücre bünyesinde yer alan bu değer, aramanın yapıldığı sütun isminin değişken tipine göre:\


* CellObject.ValueNum
* CellObject.ValueStr
* CellObject.ValueDate

şekillerinden biri ile ifade edilmektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Metod yardımıyla, kullanıcının herhangi bir belge ile ilgili veri girişi esnasında, ilişkisel yapıya sahip olan bazı önemli bilgiler, Browser yardımıyla veritabanından aranılabilmektedir. Bu işlem sayesinde bu tür önemli bilgilerde giriş hatası önlenmektedir.\
\
Bu metod ile kullanılan parametreler ise tamamen opsiyonel olup, geliştirici isterse bu parametre sayısı 0, 1, ve 2 şeklinde verilebilmektedir. 0 parametre verilmesi durumunda, Browser üzerinden yapılacak arama işleminde, kontrol nesnesinin .SearchFolder property değeri ile daha önce verilmiş olan, FOLDER içerisinde arama işlemi gerçekleşecektir. Fakat gelen Browser kayıtları, kontrol nesnesine ait .DefaultSearchFolder property değeri ile verilen BrowserColumnName bilgisine göre sort edilmiş yani sıralanmış olacaktır.\
\
Metodun sadece 1 parametre ile uygulanmasında verilen tek parametre .SortOrderColName değeri şeklinde işlem görecektir. Bu şekildeki uygulama da .DefaultSearchFolder property değerini etkisiz kılacak; geliştirici, aramanın yapılacağı Browser kayıtlarını, bu parametre ile vereceği Browser\_ColumnName bilgisine göre, kullanıcının karşısına gelirken sıralı bir şekilde olmasını sağlayacaktır.\
\
Eğer geliştirici 2 parametreyi de verirse, bu durumda 1 parametreli durumun yanısıra, verilen diğer parametre değeri ile kontrol nesnesine ait değerin ön okuması gerçekleşecektir. Okunan bu öndeğer baz alınarak, Browser ile gösterilen, aramanın yapılacağı kayıtlar sıralamaya tabi tutulacaktır. Sıralama sonucunda ise verilen bu öndeğerden büyük kayıtlar, kullanıcının karşısına gelecektir. Örneğin kontrol nesnesi içeriğine "K" harfi verilmesi durumunda, aramanın yapılacağı Browser penceresi ile sadece "K" harfi ile başlamakta olan kayıtlar kullanıcının karşısına, seçim yapmak üzere gelecektir.\
\
Metodun asli görevi ise tamamen Browser uygulamasını kullanıcının karşısına getirmektir. Gelen Browser ise içerik olarak daha önceden verilen .SearchFolder bilgisine göre gözükecektir. Eğer bir ön limit de verilmişse, o limitten sonraki belgelerin detaylarını kullanıcıya gösterecektir.\
\
Gelen Browser penceresinden eğer kullanıcı bir seçim yaparsa, grid nesnesinin \_Find event'i, Always® tarafından işletilecek ve asıl istenilen bilgiye bu event sayesinde ulaşılacaktır. Bu event'in diğer bir görevi de Browser üzerinden, kontrol üzerine uygulanan drag-drop(sürükle-bırak) uygulamasıdır.\
\
\_Find event'in kodu yardımıyla istenilen bilgi kullanıcının karşısına getirilecektir. Burada da aslında yapılan, gelen parametre ile, istenilen bilginin veritabanından getirilmesidir. Tüm bunlar geliştiricinin yazmak zorunda olduğu diğer kodlara karşılık gelecektir.
