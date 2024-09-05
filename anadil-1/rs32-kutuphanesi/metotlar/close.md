# Close

Bu metod uygulanarak RS nesnesinin kullanımı sonlandırılmaktadır.\
\
**Kullanımı**

```
RSObject.Close()
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
RS nesnesi ile yaptığımız bilgi alışverişini tamamladıktan sonra, nesnenin kullanımını sonlandırmak amacıyla bu metodun uygulanması gerekmekteddir. Metodun kullanılmasından sonra RS nesnesi ile bir daha işlem yapılamayacaktır.\
\
Bu metod kullanımı ile nesne tamamen ortadan kaldırılmakta olup, nesnenin kullandığı sistem kaynakları da, sisteme geri dönmektedir.
