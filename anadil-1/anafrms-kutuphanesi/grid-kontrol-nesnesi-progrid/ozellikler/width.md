# Width

Bu property grid sütunlarının Always® altında çalışma anındaki, görünür genişliğini belirlemektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir ve yazılabilir bir özelliktir.\
\
**Kullanımı**

```
GridColObject.Width As Number
```

**Dikkat Edilecek Noktalar**\
Grid sütunlarının nesne olarak alınması sonucunda, Always® altındaki çalışma anındaki davranışına ilişkin bazı bilgiler property şeklinde Anadil® kodu ile belirlenmektedir. Bu property bilgilerden birisi de sütun çalışma genişliğidir.\
\
Bu genişlik sayı cinsinden pixel olarak verilmekte olup, yanlış bir değer ile set edilmek istenmesi durumunda, Always® tarafından default bir değer ile belirlenmektedir.\
\
Grid sütunlarının genişlikleri, Always® altında çalışma anında da, kullanıcının isteği ile mouse yardımıyla basit bir dragging(sürükleme) şeklinde ayarlanabilmektedir.
