# CFFVarType

Bu property grid sütunlarındaki bilgilerin, CFF veri geçişlerinde kullanılmak üzere, veritipini belirlemektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Sadece yazılabilir bir özelliktir.\
\
**Kullanımı**

```
GridColObject.CFFVarType As Number
```

\
**Dikkat Edilecek Noktalar**\
Grid üzerindeki bilgiler CFF dahiline transferi 2 ayrı yöntemle gerçekleştirilebilmektedir. Bu yöntemler hücre içeriklerinin tek tek ele alınması veya blok olarak tüm grid içeriğinin, CFF'e aktarılması şeklindedir.\
\
Blok transfer olayında kullanıcının grid üzerindeki yaptığı etkiler 3 ayrı alt CFF altında transfer edilmektedir. Bunlar etkilerin de çeşidini belirlemekte olan "Inserted", "Updated", ve "Deleted" alt CFF isimleri altında grid değişimlerini içermektedir.\
\
Grid - CFF veri geçişlerinin tam olarak gerçekleştirilebilmesi için grid sütunlarındaki hücre bilgilerinin, veritipi olarak ne olduklarının bu property ile belirtilmesi gerekmektedir. Bu değerler CFF-RS bilgi geçişlerinde kullanılacak ve grid içeriği sonuçta doğru bir şekilde SQL Server'a yansıtılabilecektir. Burada yapılan yanlışlık durumunda, veritipi uyuşmazlığı SQL Server tarafından algılanacaktır ve büyük ihtimalle de SQL Server veri transferini gerçekleştirmeyecektir.\
\
Property değeri, veritiplerine göre sabit sayılar şeklinde verilmekte olup bu sayılar Anadil® altında daha önceden tanımlanmıştır.
