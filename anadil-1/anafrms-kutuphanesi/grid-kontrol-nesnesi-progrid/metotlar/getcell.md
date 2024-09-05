# GetCell

Bu metod grid sütun nesnesinden, hücre nesnesine ulaşımı temin etmektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid sütun nesneleri.\
\
**Kullanımı**

```
GridColObject.GetCell(
  RowNum As Number  ' hücrenin yer aldığı satır numarası
)As GridCellObject
```

**Parametreler**\
_RowNum_\
Sütun nesnesinin bünyesinde yer alan hücre nesnesinin grid üzerinde yer aldığı satır numarası.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri ulaşılmak istenilen Grid Hücre nesnesi olmaktadır.\
\
**Dikkat Edilecek Noktalar**\
Grid yapısında kullanılan nesne şeklindeki organizasyon, nesneler arasındaki geçişleri oldukça kolaylaştırmaktadır. Bu içiçe geçmiş yapı sayesinde bir grid nesnesinden yola çıkılarak başka bir grid nesnesine metod ve property uygulamaları ile ulaşım mümkün olmaktadır.\
\
Herhangi bir hücre nesnesine ulaşırken, grid kontrol nesnesinden yola çıkılarak önce bir sütun nesnesine ulaşılmaktadır. Daha sonra ise, sütun nesnesi bünyesinde birçok hücreyi barındırdığından, istenilen hücre için bir belirleyici karakteristik bilgi gerekmektedir. Bu karakteristik bilgi ise ilgili hücrenin yer aldığı grid satır numarasından başkası değildir.\
\
Sonuçta metod kullanımı ile grid satır numarası yardımıyla grid sütun nesnesinden hücre nesnesine ulaşılmış olmaktadır. Bu tür ulaşım özellikle grid event'lerinde parametre olarak gelen nesnelerden hücre nesnelerine ulaşımda kullanılabilmektedir.
