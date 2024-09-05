# DefaultSortOrder

Bu property, grid sütunu event'i olan \_Search uygulanmasında, sıralama parametresini belirlemektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir ve yazılabilir bir özelliktir.\
\
**Kullanımı**

```
MyGridColObject.DefaultSortOrder As String
```

**Dikkat Edilecek Noktalar**\
Anadil® bünyesinde yer alan Browser uygulaması olan, kontrol nesnesi içeriğinin veritabanından getirilmesine ilişkin .Search() isimli bir grid sütunu metodu bulunmaktadır. Bu metod ise opsiyonel olarak 0, 1 veya 2 parametre sayısı ile uygulanabilmektedir. Yapılan bu uygulamalarda, geliştirici eğer 0 parametre kullanması, yani hiç parametre vermemesi durumunda grid sütunu nesnesinin .DefaultSortOrder property içeriği devreye girmektedir.\
\
Daha önceden geliştirilmiş olan Browser kodunda, Folder'larda yer alan sütunlar bulunmaktadır. Bu sütunlar ise veritabanında yer alan table bilgilerinin, SQL kodu yardımıyla, organize edilmesi sonucunda oluşturulmuştur.\
\
Browser içeriğinin 0 parametre sayısı verilerek gösterimi sırasında, kullanıcı karşısına gelen kayıtlar, son bir sıralama işleminden geçirilebilmektedir. Sıralamanın baz alınacağı, Browser Folder'da yer alan sütun ismi ise, bu property değeri ile belirlenmektedir.\
\
.Search() metoduna ilişkin 1 veya 2 parametre ile uygulama sırasında ise, bu property içeriği devre dışı kalmaktadır.
