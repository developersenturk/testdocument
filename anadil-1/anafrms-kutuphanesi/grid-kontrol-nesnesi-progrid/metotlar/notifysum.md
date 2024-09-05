# NotifySum

Bu metod sütun nesneleri üzerinde toplam değeri kontrolüne ilişkin event kullanımını mümküm kılmaktadır.

**Uygulandığı Nesneler** \
Grid kontrol nesnesi bünyesinde yer alan Grid sütun nesneleri.&#x20;

**Kullanımı**&#x20;

`GridColObject.NotifySum()`

**Parametreler** \
Metodun parametresi yoktur.

**Geri Dönüş Değeri** \
Geri dönüş değeri önemsizdir.

**Dikkat Edilecek Noktalar** \
Metod kullanımı ile grid üzerinde yer alan sütunlara ilişkin toplam kontrolüne ilişkin bir event devreye girmektedir. Bilindiği üzere grid kontrolünün kullanılma amaçlarından biri de sütunlara ilişkin toplamların elde edilme gereğidir.

Sütun toplamları ise kullanıcının sütunda yer alan hücrelerden herhangi bir anda yaptığı değişikliğe bağlı olarak değişebilmektedir. Geliştiricinin bu toplam değere ihtiyacı olduğunda \_ColSumChange event yardımıyla, bu değere ulaşabilmesi mümkündür. Grid sütun toplamı ise bu event dahilinde parametre olarak geliştiriciye gelmektedir.

Bu metodun içeriği number değişken tipinden farklı sütun nesneleri üzerinde uygulanması da anlamsız olmaktadır.
