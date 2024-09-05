# Init

Bu metod grid nesnesi kullanımında ilk basamağı teşkil etmektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.Init(
  TotalColNum As Number,    ' sütun sayısı
  InitRowNumber As Number,  ' başlangıç satır sayısı
  ExpandBy As Number        ' eklenecek satır sayısı
)
```

**Parametreler**\
_TotalColNumber_\
Grid'de yer alacak olan toplam sütun sayısıdır.\
_InitRowNumber_\
Grid ilk oluşturulduğunda, sahip olacağı satır sayısını belirlemektedir.\
_ExpandBy_\
Kullanım anında verilen satır sayısı bittiğinde, grid'in kendi bünyesine ekleyeceği satır sayısına karşılık gelmektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Grid ilk olarak form üzerine yerleştirildiğinde sadece bir resimden ibarettir. Asıl kullanım amacını gerçekleştirebilmek için bazı önişlemlere ihtiyaç duymaktadır. Bu işlemler ise bu metod sayesinde gerçekleştirilmektedir.\
\
Grid uygulaması açısından uygulanabilecek olan ilk metod da Init() metodu olmaktadır. Çünkü diğer grid metodları ancak bu metodla teşkil edilen yapı üzerinde çalışmaktadırlar. Init uygulanmamış grid de, Always® altında çerçeve şeklinde garip bir biçimde gözükecek, bu da geliştiriciyi uyaracaktır.\
\
Grid'in kullanım aşamasında genişlemesine dair, son parametre ile, verilebilecek minimum değer 1 olmaktadır. Eğer bu değer yanlış bir sayı, mesela negatif bir sayı olarak verilirse, Anadil® bunu düzeltir ve uyarı mesajını da verir.
