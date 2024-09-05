# AddRow

Bu metod bir CFF nesnesine row(satır) eklemektedir.\
\
**Kullanımı**

```
CFFObject.AddRow()
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Bir CFF nesnesi içerdiği bilgileri row(satır) lar dahilindeki entry değerleri içersinde tutabilmektedir. En minimum koşulda bile bir root satır bulunmaktadır. Ayrıca satırlar başka satırları da içerebilmektedir. Yani istediğimnizde bir satır altında başka bir satır açabilirsiniz.\
\
Fakat bir entry altında bir satır açamazsınız.\
\
Bilgileri bu şekilde satırlar şekinde organize etmek bir sürü aynı türden bilginin yönetimini kolaylaştırarak, yapısal programlamada döngü yapılarının kurulmasıyla işlemleri uygulama geliştirici açısından oldukça basitleştirmektedir.\
\
Entry'lerin isim bilgileri olduğu halde satırların isimleri olmamaktadır.
