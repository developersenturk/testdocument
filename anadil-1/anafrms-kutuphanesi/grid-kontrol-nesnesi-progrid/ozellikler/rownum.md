# RowNum

Bu property, grid hücresinin, ait olduğu grid kontrol nesnesinde kaçıncı satırda yer aldığını içermektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Satır nesneleri ve Grid Hücre nesneleri.\
\
**Uygulama Biçimi**\
Sadece okunabilir bir özelliktir.\
\
**Kullanımı**

```
GridRowObject.RowNum As Number
veya
GridCellObject.RowNum As Number
```

\
**Dikkat Edilecek Noktalar**\
Grid hücre nesneleri yapı itibarıyla grid kontrol nesnesinin bünyesinde yer almaktadır. Bir hücrenin ise kaçıncı satıra ait olduğu, bazı durumlarda gereken bir özellik olabilmektedir. Bu property bize hücrenin yer aldığı satır numarasını vermektedir. Aynı zamanda herhangi bir satır nesnesinin de gerçek anlamda kaçıncı satırda yer aldığı bu property bünyesinde yer almaktadır.\
\
Grid kontrol nesneleri satır olarak 65535 limit değerine sahip olduğundan, bu property içeriği de 1 ile 65535 arasındaki herhangi bir sayı değeri olabilmektedir.
