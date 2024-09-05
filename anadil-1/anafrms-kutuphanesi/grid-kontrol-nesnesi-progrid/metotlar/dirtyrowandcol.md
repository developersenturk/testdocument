# DirtyRowAndCol

Bu metod tek bir grid hücresinin yapay olarak kirlenmesini temin etmektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.DirtyRowAndCol(
  RowNum As Number   ' hücrenin yer aldığı satır
  ColName As String  ' hücrenin dahil olduğu sütun
)
```

**Parametreler**\
_RowNum_\
Kirletilmesi istenen hücrenin yer aldığı satır numarası.\
_ColName_\
Kirletilmesi istenen hücrenin yer aldığı sütun ismi.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Grid kontrol nesnesinin ve Anafrms kapsamında bulunan kullanıcıdan belli bir input bilgisi alınmasına yönelik kontrollerin, kullanıcının yaptığı etki ile set olmakta olan "Dirty" özellikleri bulunmaktadır. Kirlenme olayı sayesinde etki görmüş kontrol içerikleri veritabanına taşınmaktadır.\
\
Grid nesnesi kendi bünyesinde, kullanıcıdan gelen etkiler sonucu gerçekleşen kirlilik olayını, geliştiriciden bağımsız olarak uygulamaktadır. Fakat bazı özel veri transferi uygulamalarında; mesela Browser üzerinden veri getirilmesi gibi, hücreler kirlenme olayını algılayamamaktadır. Bu gibi durumlarda geliştirici bu metod ile söz konusu hücrenin kirlilik özelliğini set etmelidir.\
\
Bir satır nesnesinin sahip olduğu bir hücrenin kirlenmesi durumunda ilgili satır nesnesinin kirlenmesi olayı gerçekleşecektir. Bu sayede \_FormToCFF event'i yardımıyla ilgili satır nesnesi içeriği CFF dahiline aktarılacaktır. Bunu izleyen \_CFFToDatabase event ise değişiklikleri veri tabanına taşıyacaktır.
