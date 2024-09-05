# EmulateSearch

Bu method, embed edilmiş bir modülün içerisindeki find eventlerini embed edildiği yerden çalıştırmaya yarar.\
\
**Uygulandığı Nesneler**\
Edit-Box kontrol nesnesi.\
\
**Kullanımı**

```
ControlObject.EmulateSearch( 
	UniqueID  ' Browser Search'den dönen r_sayac 
)
```

**Parametreler**\
Parametre sayısı sabittir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Bu method, başka bir yerden embed edilen bir modülün içerisindeki find eventleri çalıştırılmak istendiğinde kullanılır.\
\
Kullanıcının herhangi bir belge ile ilgili veri girişi esnasında,ilişkisel yapıya sahip olan bazı önemli bilgiler, Browser yardımıyla veritabanından aranabilmektedir. Bu işlem sayesinde bu tür önemli bilgilerde giriş hatası önlenmektedir.\
\
Metodun esas görevi embed edilmiş bir modülde, \_Find event'in kodu içerisinde yapılmış olabilecek özel bir takım şeylerin embed edildiği yerde de geçerli olmasını sağlamaktır.
