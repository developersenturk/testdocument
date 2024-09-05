# AddTable

Bu metod bir SELECT statement içersine, table parametrelerini eklemektedir.\
\
**Kullanımı**

```
RSObject.AddTable(
  TableName As String  ' table ismi
)
```

**Parametreler**\
_TableName_\
Yapılan query işleminde SELECT statement içersinde kullanılan table ismi.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
SQL ile oluşturulan SELECT statement içersinde mutlaka verilmesi gereken parametreler arasında yapılan query sonucunda row değerleri okunmakta olan table ismi yer almaktadır. İşte query işleminin üzerinde uygulandığı table bu metod kullanımı ile belirlenmektedir.\
\
Table ismi verilirken genel Anadil® string limitlerine uyulmalı ve table'ın SQL Server'daki ismi ile aynı olmalıdır.
