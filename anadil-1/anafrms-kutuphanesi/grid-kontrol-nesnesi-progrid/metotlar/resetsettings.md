# ResetSettings

Bu metod ile grid'in form üzerindeki görünüm ayarlarının Default değerler ile yüklenmesi sağlanmaktadır.

**Uygulandığı Nesneler**\
Grid kontrol nesnesi.

**Kullanımı**&#x20;

`GridObject.ResetSettings() As Bool`

**Parametreler** \
Metodun parametresi yoktur.

**Geri Dönüş Değeri** \
Geri dönüş değeri yapılan işlemin başarılı olması durumunda True, aksi durumda ise False olarak gerçekleşmekte olan boolean değerdir.

**Dikkat Edilecek Noktalar** \
Grid'in görünüm ayarları arasında sütunların sıralamaları, genişlikleri, satır yükseklikleri gibi kullanıcı tarafından mouse ile her zaman değiştirilebilen ayarlar bulunmaktadır. Bu ayarların Registry ile saklanması ve yüklenmesi sayesinde, daha kullanışlı bir grid uygulaması sağlanmaktadır.

Grid'in Anadil® kodu ile sütun değerlerinin belirlenmesi sırasında ortaya çıkan görünüm ayar değerleri bulunmaktadır. İşte bu ayarlar "Default değerler" olarak adlandırılmaktadır.

Herhangi bir anda grid Default ayarlarının yüklenmesi için bu metodun, programcı tarafından çağrılması yeterli olmaktadır. Grid menusu sayesinde de kullanıcının direkt olarak kendisinin bu hazır ayarları yükleyip grid'e uygulaması mümkündür. Bu işlem için, menüden "Hazır Ayarlar" isimli ifade mouse ile seçilmelidir.
