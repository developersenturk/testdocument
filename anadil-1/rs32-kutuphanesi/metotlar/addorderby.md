# AddOrderBy

Bu metod oluşturulan bir SELECT statement içersinde ORDER BY ifadesinin uygulanabilmesini sağlamaktadır.\
\
**Kullanımı**

```
RSObject.AddOrderBy(
  OrderByCol As String  'table column ismi
)
```

**Parametreler**\
_OrderByCol_\
Query ile uygulanan ORDER BY ile belirtilecek, table'da yer alan column ismidir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
ORDER BY yapılan bir query işleminde SQL Server tarafından ortaya konulan sonuç bilgilerini sıralama için kullanılmaktadır. Bu özelliğin kullanımı ile SQL Server tarafından ortaya konulan recordset üzerindeki bilgiler verilen column ismine göre sıralanmaktadır. Always® platformunda çalışmakta olan bir kimse de yaptığı query işlemlerinde ORDER BY kullanımını bu metod ile gerçekleştirmektedir.\
\
Always® tarafından ortaya konulan sıralama büyükten küçüğe olarak gerçekleşmektedir.\
\
Unutulmaması gereken husus burada verilen parametrenin table'ın sahip olduğu bir column ismi olmasıdır. Yapılan query işleminde eğer bir hata olursa, mesela hatalı bir SELECT statement; oluşan hata SQL Server tarafından işletim esnasında son kullanıcının karşısına gelmektedir.
