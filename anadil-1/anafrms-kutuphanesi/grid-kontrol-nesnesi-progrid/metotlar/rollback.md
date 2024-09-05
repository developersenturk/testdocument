# RollBack

Bu metod grid ile ilgili yapılan işlemlerde, belli bir sürede yapılmış olunan işlemleri iptal etmektedir.

**Uygulandığı Nesneler** \
Grid kontrol nesnesi.

**Kullanımı**&#x20;

`GridObject.RollBack()`

**Parametreler** \
Metodun parametresi yoktur.

**Geri Dönüş Değeri** \
Geri dönüş değeri önemsizdir.

**Dikkat Edilecek Noktalar** \
Rollback işlemi, veritabanı sistemlerindeki transaction kullanımına banzeyen bir uygulama biçimidir. Buna göre grid üzerinde belli bir ana kadar yürütülmüş olan işlemler, istenildiğinde geliştiricinin bu metod kullanımı sayesinde iptal edilebilmektedir.

Mesela kullanıcı belli bir bilgiyi girdi şeklinde verdiğinde, eğer geliştirici bilginin yanlış verilmesinden dolayı, o ana kadar yapılmış olan bazı işlemler de varsa bu metod ile tüm bu işlemler iptal edilmektedir.

Grid Rollback işleminde, veritabanı sistemlerindeki transaction uygulamasından farkı, transaction başlatımının ve sonlandırılmasının Always® tarafından yürütülmesidir. Yani grid işlemlerinde "Begin" veya "Commit" şeklinde bir uygulama yoktur. Geliştirici sadece gelinen noktada, belli bir grup grid işlemini iptal edebilmektedir.

Ayrıca geliştiricinin Rollback işlemini uygulaması durumunda, uygulama kullanıcısını da belli bir biçimde uyarması, yanlış giden bir olayla ilgili bilgi vermesi, uygulamayı daha kullanıcı-dostu kılacaktır.
