# VisibleListRows

Bu property grid sütunlarıda combo-box uygulanması durumunda, combo-box tarafından kullanıcıya gösterilecek olan satır sayısını belirlemektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir ve yazılabilir bir özelliktir.\
\
**Kullanımı**

```
GridColObject.VisibleListRows As Number
```

**Dikkat Edilecek Noktalar**\
Property sadece grid sütunlarında combo-box şeklinde çoktan seçim olanağı sunan hücrelerde geçerli olmaktadır. Görevi ise kullanıcının combo seçimi yapmak istediğinde karşısına gelecek listede kaç tane liste elemanı yer almasını belirlemektedir.\
\
Combo-box satır sayısını belirlemek, onun sadece belirlenen satır sayısında elemana sahip olacağı değil sadece ilk etapta kullanıcıya kaç tane seçim elemanı göstereceğini belirlemektedir.\
\
Değerinin yanlış bir sayı ile belirlenmek istenmesi durumunda, Always® tarafından default değer olan 5 şeklinde algılanmakta ve uygulanmaktadır.
