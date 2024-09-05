# ColName

Bu property grid hücre nesnesinin, ait olduğu grid sütun nesnesinin ismini geliştiriciye sunmaktadır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Hücre nesneleri.\
\
**Uygulama Biçimi**\
Sadece okunabilir bir özelliktir.\
\
**Kullanımı**

```
MyGridCellObject.ColName As String
```

\
**Dikkat Edilecek Noktalar**\
Grid hücre nesnelerinin, başka bir grid sütunu bünyesinde yer almasının sonucu olarak, hücreden yola çıkarak sütun nesnesine ulaşım mümkün olabilmektedir. Sütun nesnesinin kendisine ulaşım mümkün olduğu için, sütun referans ismi de bu property ile ulaşılabilmektedir.\
\
Örnek vermek gerekirse, grid kontrol nesnesine ilişkin grid sütunları belirlenirken; .SetColName() metodu uygulanması ile eğer,

```
...
form.g.SetColName(2,"miktar")       ' sütun isimlendirmesi
...
Anadil® kodu yardımıyla "miktar" ismi bir sütuna verilmişse; 
başka herhangi bir anda,
...
Dim sütun_name As String
...
sütun_name := ExCellObject.ColName  ' sütun ismi ulaşımı
...
```

referansı ile hücrenin ait olduğu sütun nesnesinin ismi elde edilebilir. Burada elde edilecek string değer .SetColName() metodu ile ilgili hücreye verilmiş olan referans ismi bilgisi olmaktadır.\
