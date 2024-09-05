# Dirty

Bu property formun, Always® altında kullanılırken, o anda kirlenmiş olması ile ilgili bilgiyi tutar.\
\
**Uygulandığı Nesneler**\
Form nesneleri.\
\
**Uygulama Biçimi**\
Sadece okunabilir bir özelliktir.\
\
**Kullanımı**

```
FormObject.Dirty As Bool
```

\
**Dikkat Edilecek Noktalar**

Her form kullanım aşamasında sahip olduğu Windows kontrolleri açısından, "Dirty" şeklinde ifade edilmekte olan bir property'e sahiptir. Bu property değeri Always® tarafından kontrol edildiğinden sadece okunabilir niteliğe sahiptir.

Bir formun kirlenmesi ise üzerinde barındırdığı Windows kontrollerinden, en az birinde mesela bir edit-box'da meydana gelen değişim ile olabilmektedir. Her bir kontrolün de kendi "Dirty" property'si bulunmaktadır. Yani aslında olay kontrollerde meydana gelen değişimin sonucudur ki, bu değişim gösterilen form ile ilgili ya bir insert(yeni kayıt) veya update(güncelleme) işlemi halinde meydana gelmektedir.

Formun kirlenmesi durumunda, ayrıca formun sol üst köşesinde küçük bir kalem işareti de görsel açıdan, o anki form kullanıcısına bilgi vermektedir.
