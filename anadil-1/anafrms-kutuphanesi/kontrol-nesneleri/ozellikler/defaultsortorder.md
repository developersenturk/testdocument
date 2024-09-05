# DefaultSortOrder

Bu property yardımıyla, kontrol nesnesine ilişkin Browser ile yapılan arama işlemi öncesi, burada verilen değere göre sıralanmaktadır.\
\
**Uygulandığı Nesneler**\
Edit-box kontrol nesnesi.\
\
**Uygulama Biçimi**\
Sadece yazılabilir bir property'dir.\
\
**Kullanımı**

```
ControlObject.DefaultSortOrder As String
```

\
**Dikkat Edilecek Noktalar**\
Anadil® bünyesinde Browser uygulaması olan, kontrol nesnesi içeriğinin veritabanından getirilmesine ilişkin .Search() isimli bir metod bulunmaktadır. Bu metod ise opsiyonel olarak 0, 1 ve 2 parametre sayısı ile uygulanabilmektedir. Yapılan bu uygulamalarda, geliştirici eğer 0 parametre kullanması,yani hiç parametre vermemesi durumunda kontrol nesnesinin .DefaultSortOrder property içeriği devreye girmektedir.\
\
Daha önceden geliştirilmiş olan Browser kodunda, Folder'larda yer alan sütunlar bulunmaktadır. Bu sütunlar ise veritabanında yer alan table bilgilerinin, SQL kodu yardımıyla, organize edilmesi sonucunda oluşturulmuştur.\
\
Browser içeriğinin 0 parametre verilerek gösterimi sırasında, kullanıcı karşısına gelen kayıtlar, son bir sıralama işleminden geçirilmektedir. Sıralamanın baz alınacağı, Browser Folder'da yer alan sütun ismi ise, bu property değeri ile belirlenmektedir.\
\
.Search() metoduna ilişkin 1 ve 2 parametre ile uygulama sırasında ise, bu property içeriği devre dışı kalmaktadır.\
\
Bu property değerini belirlemek için en uygun yer ise formun \_Open event'i olmaktadır.
