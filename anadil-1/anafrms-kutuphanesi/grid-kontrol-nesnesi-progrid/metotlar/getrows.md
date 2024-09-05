# GetRows

Bu metod grid nesnesinden CFF nesnesine bilgi taşınmasını sağlamaktadır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.GetRows(
  DestCFF As Object	' hedef CFF nesnesi
)
```

**Parametreler**\
_DestCFF_\
Grid üzerindeki değişimlerin, taşınacağı hedef CFF nesnesi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Form ile işlemlerini tamamlayan kullanıcının grid üzerinde yapmış olduğu etkilerin belli bir şekilde veritabanına yansıtılması gerekmektedir. İşte bu noktada bu metod grid-cff bilgi transferi işlemlerini oldukça kolaylaştıran bir yöntem sunmaktadır.\
\
Grid üzerindeki kullanıcının yaptığı değişimleri, geliştirici 2 şekilde veritabanına taşıyabilmektedir. Bunlardan ilki geliştiricinin, grid hücre içeriklerini tek tek ele alıp CFF'e taşıması ve daha sonra da veritabanına aktarmasıdır. Diğer yöntem ise direkt olarak grid değişikliklerini, CFF nesnesine bu metod ile tek adımda taşımasıdır.\
\
Grid ile CFF arasında bu metodu kullanarak, direkt tek adımda veri transferi yapabilmek için geliştiricinin bazı kurallara dikkat etmesi gerekmektedir. Bunlardan ilki grid sütun isimlerinin (Grid.ColName property değeri), CFF üzerindeki entry isimleri ile tam olarak uyuşması gerekliliğidir. İkinci olarak ise, grid'in davranış olarak; CFF nesnesine gönderdiği her grid satırı bilgisine karşılık bir de row\_id entry name altında table kayıtlarını ayıran bilgiyi sunmasıdır. Bunun anlamı ise daha önceden yapılmış table dizaynlarında, grid satırlarının her birine karşılık gelen, unique kayıt ayırımı, row\_id değerleri ile sağlanmaktadır. Geliştirici tüm bunlara dikkat ederse daha sağlıklı ve kısa zamanda grid uygulaması geliştirebilecektir.\
\
Metodun kullanımıyla grid kontrolünde kullanıcının verdiği girdiler, parametre ile verilen CFF altında, alt CFF nesneleri dahilinde saklamaktadır. Bu alt CFF nesneleri "Inserted", "Updated" ve "Deleted" adları ile organize edilmektedir.\
\
İsimlerinden de anlaşılacağı gibi "Inserted" alt CFF nesnesi altında, kullanıcının grid üzerinde vermiş olduğu yani satır bilgileri yer almaktadır. Tabi ki bu yeni satır bilgileri, grid'in sütun isimleri altında saklanmaktadır. Bu bilgiler veritabanında ilk kez kayıt edilecek bilgiler olup, geliştiricinin bunları RS nesnesi altında, SQL anlamıyla INSERT işlemi şeklinde veritabanına taşıması gerekmektedir.\
\
Diğer bir alt CFF ismi de "Updated" olup, burada kullanıcının var olan bazı grid satırlarında değişiklikler yapması durumundaki, yeni grid satır bilgileri yer almaktadır.\
\
Güncelleme işleminin yapılabilmesi için, daha önceden var olan bir kaydın değişikliğe uğramasından dolayı ek bir bilgiye ihtiyaç bulunmaktadır. Bu da var olan grid satırı kayıtlarını table içerisinde birbirinden ayıran unique counter(r\_sayac) bilgisi olmaktadır. Ayırıcı olan bu bilgi ise CFF altında .row\_id isimli ekstra bir entry altında saklanmakta ve grid tarafından sunulmaktadır. Verilen bu ayırıcı bilgiyi kullanarak, "Updated" isimli alt CFF nesnesi içeriğinin, geliştirici tarafından, RS nesnesi ile, SQL anlamıyla UPDATE işlemi şeklinde veritabanına gönderilmesi gerekmektedir.\
\
Kullanıcının grid ile yaptığı işlemler yeni kayıt ve güncelleme dışında, grid üzerinde var olan bir satır bilgisinin silinmesi şeklinde olabilmektedir. Böyle bir grid satırı silme işleminde "Deleted" isimli alt CFF nesnesi altında, silinen satıra ait .row\_id bilgisi grid nesnesi tarafından transfer edilecektir. Daha sonra geliştirici .row\_id bilgisini kullanarak ilgili kaydın veritabanından silinmesini gerçekleştirecektir. Bu işlem ise RS nesnesi yardımıyla, SQL anlamıyla bir DELETE işletiminden başka uygulama değildir.
