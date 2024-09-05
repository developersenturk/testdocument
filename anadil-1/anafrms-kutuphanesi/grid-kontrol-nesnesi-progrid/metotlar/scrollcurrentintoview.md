# ScrollCurrentIntoView

Bu metod aktif hücrenin, Always® altında görülebilir olmasını sağlamaktadır.

**Uygulandığı Nesneler** \
Grid kontrol nesnesi.

**Kullanımı**&#x20;

`GridObject.ScrollCurrentIntoView()`

**Parametreler** \
Metodun parametresi yoktur.

**Geri Dönüş Değeri** \
Geri dönüş değeri önemsizdir

**Dikkat Edilecek Noktalar** \
Aktif hücre dediğimiz, kullanıcının herhangi bir klavye bilgi girişini alabilen hücreyi, geliştirici uygun metodlar ile başarabilmektedir. Bu işlem ise verilen sütun üzerinde veya satır numarası ile gerçekleştirilebilmektedir.

Aktif hücrenin değiştirilmesi sonucunda, kullanıcının kullandığı pencere sınırları dahilinde göremeyeceği bir grid hücresine de gidilmiş olunabilir. Bu durumda bu metod ile aktif hücre kullanıcının formu üzerindeki grid'de, görünebilecek şekilde karşısına gelmektedir.
