# ColObject

Bu property, grid hücre nesnesinden, kendisinin ait olduğu grid sütun nesnesine ulaşımı temin etmektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Hücre nesneleri.\
\
**Uygulama Biçimi**\
Sadece okunabilir bir özelliktir.\
\
**Kullanımı**

```
MyGridCellObject.ColObject As GridColObject
```

\
**Dikkat Edilecek Noktalar**\
Grid kontrol nesnesi ile ilgili işlemlerde geliştiricinin işlerini daha da kolaylaştırmak amacıyla, farklı grid öğelerini ayrı ayrı nesnelerde organize etmektedir. Bu farklı nesneler ise kendi aralarındaki geçişlerini metod ve property'ler yardımıyla gerçekleştirmektedir.\
\
Bilindiği üzere bir grid hücresi başka bir grid sütun nesnesinin bünyesinde yer almaktadır. Grid yapısının sonucu olarak ise, bir hücre sadece bir sütun nesnesi dahilinde yer almaktadır. Grid hücresinden, kendisinin ait olduğu Grid Sütunu nesnesine bu property yardımıyla ulaşılabilmektedir. Ulaşım sonunda gerçek bir sütun nesnesi elde edilmekte ve sütun nesnesine ait diğer metod ve property uygulamaları da gerçekleştirilebilmektedir.
