# Normal

Bu method raporda yazdırılan yazı tipinin normal olmasını sağlar.\
\
**Kullanımı**

```
ReportObject.Normal() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Normal methodu raporda yazdırılan yazı tipinin o satır için normal boyutlarda olmasını sağlar. Yazının tipi default olarak Normal'dir. Ancak bir satırda DoubleWidth veya Condensed methodları kullanıldıktan sonra, yazı tipinin o satır içinde Normal olması isteniyorsa belirtilmelidir.\
\
**Örnek**

```
Dim r As report
  r.DoubleWidth()
  r.Write("Konu Başlığı",20,TTYALIGN_LEFT)
  r.Space(20)
	r.Normal()
  r.Write("Tarih",20,TTYALIGN_LEFT)
  .
  .
```
