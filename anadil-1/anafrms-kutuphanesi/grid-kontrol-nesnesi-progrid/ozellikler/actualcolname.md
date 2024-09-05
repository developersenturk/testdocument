# ActualColName

Bu property, uygulandığı nesneye göre sütun nesnesini veya hücre nesnesini sunmaktadır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Sadece okunabilir bir özelliktir.\
\
**Kullanımı**

```
GridObject.<ActualColName> As GridColObject
veya
GridRowObject.<ActualColName> As GridCellObject
```

**Dikkat Edilecek Noktalar**\
Birinci durumda bu property yardımıyla grid nesnesinin sahip olduğu sütun nesnelerine doğrudan erişim sağlanmaktadır. Grid sütun nesnelerine bu şekilde ulaşıp onları küresel değişkenlerde saklayabilmekteyiz. Daha sonra sütun nesnelerinin kendine özgü metod ve property işlemleri bu küresel nesne değişkenleri üzerinde uygulanabilmektedir.\
\
Property uygulamasında geçen .ActualColName ifadesi ise grid üzerinde ilk uygulanan .SetColName() metodu uygulanması ile verilen isim olmaktadır. Örnek olarak eğer grid sütunları belirlenirken,

```
...
form.g.SetColName(2,"miktar")  ' örnek sütun isimlendirmesi
...
Anadil® kodu yardımıyla "miktar" ismi bir sütuna verilmişse; 
...
my_object := form.g.miktar     ' örnek sütun nesnesi ulaşımı
...
```

referansı ile bu sütun nesnesine ulaşılabilir veya başka bir nesneye atanabilir.\
\
İkinci durumda ise property grid row nesneleri yani satır nesneleri üzerinde uygulandığında hücre nesnelerini geliştiriciye sunmaktadır. Hücre nesnelerine ulaşım sağlandıktan sonra, hücre ile ilgili her türlü metod ve property'ler bu nesne üzerinde uygulanabilmektedir.\
\
Grid satır nesneleri event'ler dahilinde geliştiriciye sunulmakta olan nesneler olduğundan bir bakıma sanal nesneler olmaktadırlar. Sanal nesnelerin ise küresel olarak atanmaları ve kullanımları mümkün olmamaktadır.\
\
Örnek olarak eğer grid sütunları belirlenirken,

```
...
form.g.SetColName(4,"fiyat")       ' örnek sütun isimlendirmesi
...
Anadil® kodu yardımıyla "miktar" ismi bir sütuna verilmişse; 
...
fiyat:=InsertedRow.fiyat.ValueNum  ' hücre nesnesi ulaşımı
...
```

referansı ile satır nesnesi dahilindeki hücre nesnesine ulaşılabilir veya başka bir nesneye atanabilir.
