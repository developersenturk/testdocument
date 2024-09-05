# AllowNull

Bu property grid sütunu hücrelerinde NULL şeklinde veri girişi yapılabilmesini düzenlemektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir ve yazılabilir bir özelliktir.\
\
**Kullanımı**

```
MyGridColObject.AllowNull As Bool
```

\
**Dikkat Edilecek Noktalar**\
NULL yönetimi, Always® tarafından, bilgi girişlerinde sorunsuz bir şekilde gerçekleştirilebilmektedir. Bunun sayesinde grid hücrelerinde, edit uygulaması şeklinde yapılan bilgi girişlerinde, eğer hiçbir karakter verilmemişse, hücre bilgi içeriği NULL olarak algılanmaktadır.\
\
Grid hücrelerinde NULL bilgi iºlemleri uygulanabilmesi içinse, bu property değerinin True değeri ile set edilmiş olması gerekmektedir. NULL olarak algılanan bu bilgiler CFF ve RS geçişini de NULL şeklinde yapacak ve eğer SQL Server da ilgili table field dahilinde izin veriyorsa NULL olarak veritabanına kayıt edilecektir.
