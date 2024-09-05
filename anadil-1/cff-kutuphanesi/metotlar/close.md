# Close

Bu metod bir root CFF nesnesini ortadan kaldırmak için kullanılmaktadır. Root CFF destroy listesine eklenir. Eğer verilen CFF bir alt CFF ise derhal yok edilir.

Kullanımı

```
CFFObject.Close()
```

Parametreler

Metodun parametresi yoktur.

Geri Dönüş Değeri

Geri dönüş değeri önemsizdir.

Dikkat Edilecek Hususlar

Bu metod kullanımı ile bir CFF nesnesi silinmekte sonuç olarak CFF nesnesinin kullandığı memory sisteme geri kazanılmaktadır. Bir CFF nesnesini ortadan kaldırmadan önce onunla ilgili işlemlerin bitmiş olduğundan emin olmamız gerekmektedir.

Bu metod bir root CFF nesnesini ortadan kaldırdığı için dolaylı olarak bu CFF nesnesinin sahip olabileceği alt CFF’ler de yok olmaktadır.

Döküman işlemlerinde kullanılan event dahilinde parametre olarak gelen CFF nesnelerinin silinmesi işlemi otomatik olarak Always® tarafından yapılmaktadır.

**İlgili Konular:** [**Destroy**](destroy.md)\
