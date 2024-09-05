# GetFocus

Bu property formun, "Focus" özelliği aktif olan kontrolünü içermektedir.\
\
**Uygulandığı Nesneler**\
Form nesneleri.\
\
**Uygulama Biçimi**\
Sadece okunabilir bir özelliktir.\
\
**Kullanımı**

```
FormObject.GetFocus As Object
```

**Dikkat Edilecek Noktalar**

Always® altında geliştirilen form tabanlı uygulamalarda, söz konusu form aktif olması durumunda, sahip olduğu kontrollerden bir tanesinin "Focus" özelliği aktif olacaktır. Kullanıcıdan gelen input etkilerini alacak olan bu aktif kontrol nesnesi, bu metod yardımıyla elde edilebilmektedir.

Bu property değerinin okunmasından önce, formun gerçekten aktif olmasının test edilmesi gerekmektedir. Bu işlemse formun .IsFocus property değerinin öğrenilmesi ile mümkündür. Eğer bu kontrol yapılmazsa, bu metodun uygulanması ile, Always® altında, o anda aktif olan başka bir formun, aktif olan kontrol nesnesi elde edilecektir.
