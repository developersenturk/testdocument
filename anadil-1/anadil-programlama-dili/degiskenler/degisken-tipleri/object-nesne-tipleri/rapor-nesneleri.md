# Rapor Nesneleri

Modül ve servis nesnelerinin ardından gelen 3.Executable nesne de raporlardır. Diğer nesneler gibi Always® altında dizinlerde file şeklinde saklanmaktadır. Oluşturulması ve değiştirilmesi Imagine® yardımıyla yapılmaktadır.Veritabanında saklanmakta olan belge şeklindeki bilgilerin, genel olarak saklanma amacı belli bir süre sonunda raporlar halinde sonuç bilgileri alabilmektir. Raporlar da sonuçta belge verilerinin sahibi olan işletmenin belli bir dönemdeki faaliyetleri hakkında bilgiler verecektir. Rapor nesnelerinin görevi de raporlama işlemine yönelik bilgilerin veritabanından, kullanıcının bulunduğu workstation sisteme getirilmesini sağlamaktır.

Always® altında, Browser uygulamasına benzeyen hiyerarşik gösterime sahip bir rapor penceresi vardır. Bu pencerede bütün raporlar belli bir ağaç yapısında sunulmaktadır. Aktif hale geçirilen raporlar çıktılarını ekrandan kullanıcıya sunabildiği gibi, ortaya konulan bu çıktının yazıcıdan alınması da mümkündür.

Rapor nesneleri, Always® altında özel thread(kanal) 'larında çalışmakta olduğundan, aktif çalışma anında örneğin veritabanından istenilen verinin uzun bir sürede gelmesi gibi bir durumda; Always®'in başka bir işlem yapabilmesi mümkün olabilmektedir. Bu sayede kullanıcı raporlar ile daha verimli bir şekilde çalışabilmektedir.
