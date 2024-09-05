# FieldName

Bu property RS nesnesi dahilinde, database ile document arasında taşınan variant ifadeleri tutmaktadır.\
\
**Kullanımı**

```
RSObject.<FieldName> As <variant>
```

**Uygulandığı Nesneler**\
Bu özellik RS nesnelerinde uygulanmaktadır.\
\
**Property Tipi**\
Read-Only yani sadece okunur bir özelliktir.\
\
**Property Değeri**\
Değer olarak variant ifadeleri saklayabilen bu property, sonuçta; string, number, date olan değerler içerebilmektedir. Hatta variant ifadeler NULL içeriğe de sahip olabildiğinden bu property de NULL içerik taşıyabilmektedir.\
\
**Dikkat Edilecek Hususlar**\
Bilindiği üzere herhangi bir SQL SELECT statement oluşturulurken, RS nesnesinde, .AddInsertField() metodu ile table column isimleri eklenmektedir. Oluşturulan SQL statement ifadenin diğer parametreleri de diğer metodlar ile belirlendikten sonra .CompileStm() ve .ExecuteStm() metodları ile SQL Server işletimi gerçekleştirilmektedir.\
\
RS nesnesinde kullandığımız table column isimleri property uygulaması şeklinde, RS nesnesi dahilinde, variant ifadeleri saklamakta; daha sonra variant ifadelere tekrar ulaşmak istenildiğinde yine aynı table column isimleri kullanılmaktadır.
