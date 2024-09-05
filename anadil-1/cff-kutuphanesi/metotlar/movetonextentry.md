# MoveToNextEntry

Bu metod aktif entry göstericisinin değerini bir sonraki entry'yi gösterecek şekilde düzenlemektedir.\
\
**Kullanımı**

```
CFFObject.MoveToNextEntry() As Bool
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlemin başarılı olması halinde DOĞRU, aksi durumda ise YANLIŞ olarak gerçekleşmekte olan bir Boolean değerdir.\
\
**Dikkat Edilecek Hususlar**\
Current(aktif) entry göstericisi değerinin doğru bir şekilde çalişabilmesi için daha önceden mutlaka bir kere MoveToFirstEntry ile gösterici değerinin bir şekilde ayarlanmış olması gerekmektedir.\
\
Ayrıca daha önceden de aktif satır göstericisinin değerinden de emin olunması başka bir önemli noktadır.\
\
Geliştirilmekte olan uygulamanın başarısı açısından da metodun geri dönüş parametresinin de göz önünde tutulması ve buna göre Anadil kodu yazılması çok önemlidir.
