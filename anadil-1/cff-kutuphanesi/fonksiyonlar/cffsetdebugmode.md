# CFFSetDebugMode

PROCFF'i debug etmek icin kullanılır ve hata takibi yapılabilir.\
\
**Kullanımı**

```
Function CFFSetDebugMode( Mode As Boolean ) As Boolean
```

**Parametreler**\
_Mode_\
\--------\
\
**Geri Dönüş Değeri**\
TRUE/FALSE şeklindedir.\
\
Örnek

`CFFSetDebugMode(True)`

Bunu herhangi bir yerde yukarıdaki sekilde cagirirsaniz CFF operasyonlari PROCFF.DLL tarafindan titizlikle takip edilecek ve hata olan yerler terminale yazilarak hatayi duzeltmek konusunda yonlendirecektir.Hata duzeltme isiniz bittikten sonra yukaridaki cagriyi kaldiriniz. Zira ekstra takip isleri normalden yavas olacaktir.
