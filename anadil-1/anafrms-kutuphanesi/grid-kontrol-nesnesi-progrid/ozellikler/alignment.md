# Alignment

Bu property grid sütunu hücrelerinde yer alan bilgilerin, yerleşimi ile ilgili düzenlemeyi gerçekleştirmektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir ve yazılabilir bir özelliktir.\
\
**Kullanımı**

```
GridColObject.Alignment As Number
```

\
**Dikkat Edilecek Noktalar**\
Grid sütununda yer alan hücreler ister bilgi girişi olarak kullanılsın veya kullanıcıya bilgi gösterimi için kullanılsın, sahip olduğu bilginin hücre içersinde yerleşimi bulunmaktadır. Bu yerleşim ise bu property değeri ile belirlenmekte olup, grid hücresinin genişliğine bağlı olarak bilgi hücrede görünmektedir.\
\
Bilgilerin yerleşimi ise sola yanaşık, sağa yanaşık veya ortalanmış şeklinde üç şekilde olabilmektedir. İstenen yerleşim ise sabit sayıların bu property değeri olarak verilmesiyle ayarlanmaktadır:\
\


* PG\_LEFTALIGN (sola yanaşık),
* PG\_RIGHTALIGN (sağa yanaşık),
* PG\_CENTERALIGN (ortalanmış).

Property değeri olarak yanlış bir sayı değeri verilmek istenmesi durumunda, Always® default olarak property değerini PG\_LEFTALIGN şeklinde algılamakta ve uygulamaktadır.
