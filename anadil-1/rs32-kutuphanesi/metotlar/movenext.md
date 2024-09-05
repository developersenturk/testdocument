# MoveNext

Bu metod RS nesnesinden SQL Server işletimi sonrasında, row değerlerinin alınmasında kullanılmaktadır.\
\
**Kullanımı**

```
RSObject.MoveNext() As Bool
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri yapılan bir sonraki satıra geçme işleminde başarı durumunda True, işletimin başarısız olması durumda ise içeriği False olan Bool değerdir.\
\
**Dikkat Edilecek Hususlar**\
Bu metod tamamen server'dan client'a yapılan bilgi transferinde kullanılmakta olup; esasen SQL Server'dan taleb edilen query sonucunda table row bilgilerinin, RS nesnesinde satırlar halinde yerleştirilmesine dayanmaktadır. Uygulama esnasında eğer biz server'dan birden fazla sayıdaki table row bilgisi talep edersek, gelen her row bilgisi, RS nesnesinde de ayrı ayrı row'larda yer alacaktır.\
\
RS recordset kümesinde client tarafından istenen bilgi 0 satır da olabildiği gibi binlerce satır da olabilir. İşte burada client tarafında, 1 satırlık bilginin ve 1,000,000 satırlık bilginin RS tarafından alınması arasında hiçbir fark bulunmamaktadır. İşlem esnasında her zaman birer satır olarak bilgi alınması RS nesnesinin çalışma şeklidir.\
\
Alınmak istenilen bilginin tamamı sequential olarak yani düz bir sırada RS nesnesinden property'lerin okunması sonucunda elde edilmektedir. Bu işlem sırasında bir LOOP döngüsü kurulabilir ve RS nesnesinde hiç satır kalmadığında da, bu metodun geri dönüş değeri False olacağından döngü işletimi o esnada sonlandırılabilir.
