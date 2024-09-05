# Search

Bu metod kullanıldığı kontrol içeriği için Browser yardımıyla arama işlemi uygulamaktadır.\
\
Uygulandığı Nesneler\
Edit-Box kontrol nesnesi.\
\
**Kullanımı**

```
ControlObject.Search( 
	' Not: Metod parametrelerinin kullanımı opsiyoneldir,
	' kullanıma göre parametre sayısı 0, 1, veya 2
	' olabilmektedir.
	SortOrderColName As String,	' Browser sıralama bilgisi
	ControlValue:Property		' kontrolün değeri
)
```

**Parametreler**\
Parametre sayısı değişken olabilen bir metoddur. Bunun sonucu olarak 0, 1, veya 2 parametre sayısı ile bu metod uygulanabilmektedir.\
\
_SortOrderColName_\
Browser üzerinden uygulanacak arama işlemi yapılırken, gelen kayıtların sıralanacağı sütun bilgisi.\
\
_ControlValue_\
Arama işleminde verilebilecek öndeğer olan kontrolün içeriğidir. Property olarak kontrol bünyesinde yer alan bu değer, aramanın yapıldığı sütun isminin değişken tipine göre:\
\


* form\_edit.ValueNum
* form\_edit.ValueStr
* form\_edit.ValueDate

Şekillerinden biri ile ifade edilmektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Sadece edit-box kontrol nesnelerinde uygulanmakta olan bir metoddur. Bu metod yardımıyla, kullanıcının herhangi bir belge ile ilgili veri girişi esnasında, ilişkisel yapıya sahip olan bazı önemli bilgiler, Browser yardımıyla veritabanından aranılabilmektedir. Bu işlem sayesinde bu tür önemli bilgilerde giriş hatası önlenmektedir.\
\
Bu metod ile kullanılan parametreler ise tamamen opsiyonel olup, geliştirici isterse bu parametre sayısı 0, 1, veya 2 şeklinde verilebilmektedir. 0 parametre verilmesi durumunda, Browser üzerinden yapılacak arama işleminde, kontrol nesnesinin .SearchFolder property değeri ile daha önce verilmiş olan, FOLDER içersinde arama işlemi gerçekleşecektir. Fakat gelen Browser kayıtları, kontrol nesnesine ait .DefaultSearchFolder property değeri ile verilen BrowserColumnName bilgisine göre sort edilmiş yani sıralanmış olacaktır.\
Metodun sadece 1 parametre ile uygulanmasında verilen tek parametre SortOrderColName değeri şeklinde işlem görecektir. Bu şekildeki uygulama da .DefaultSearchFolder property değerini etkisiz kılacak; geliştirici, aramanın yapılacağı Browser kayıtlarını, bu parametre ile vereceği BrowserColumnName bilgisine göre, kullanıcının karşısına gelirken sıralı bir şekilde olmasını sağlayacaktır.\
