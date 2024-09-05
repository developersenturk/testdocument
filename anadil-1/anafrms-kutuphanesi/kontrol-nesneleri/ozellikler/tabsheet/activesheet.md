# ActiveSheet

Bu property TAB kontrol nesnesinde aktif tab sayfasını belirlemektedir.\
\
**Uygulandığı Nesneler**\
TAB kontrol nesnesi.\
\
**Uygulama Biçimi**\
Hem okunabilir hem de yazılabilir bir property'dir.\
\
**Kullanımı**

```
TabControlObject.ActiveSheet As String
```

\
**Dikkat Edilecek Noktalar**\
Oluşturulmuş olan bir TAB sisteminin sadece bir sayfası aktif olabilmektedir, işte bu metod tabformu ismi verilmiş olan TAB sisteminin hangisinin aktif olacağını, örneğin kullanıcının karşısına ilk çıktığında, belirlemektedir.\
\
Başka bir kolaylık da; tab sayfalarını belli bir sırada eklediğimizi farz edersek, tabformunun ismini vermeden de "#" karakterinin ardından tab sayfasının numarasını vermek suretiyle de istediğimiz tab sayfasının aktif olmasını sağlayabilmekteyiz. Dikkat etmemiz gereken nokta index numaralarının 1'den itibaren başlamasıdır.
