# AutoDirty

Bu property formun, aktif kullanım anında kirlenebilme özelliğini kontrol etmektedir.\
\
**Uygulandığı Nesneler**\
Form nesneleri.\
\
**Uygulama Biçimi**\
Sadece yazılabilir bir özelliktir.\
\
**Kullanımı**

```
FormObject.AutoDirty As Bool
```

\
**Dikkat Edilecek Noktalar**

AutoDirty özelliği, her formun sahip olduğu "Dirty" mekanizmasının kullanımını sağlamaktadır. Eğer değeri "set" edilmememişse ilgili form üzerinde "Dirty" yani kirlenme mekanizması kullanılamaz.

Bu property değerinin belirleneceği Anadil® kodu ise formun myform\_Open event olmaktadır. Burada yapılan atama ile, form kendi kendine kirlenme ile hareket edebilmekte, örneğin hiç kirlenmemiş bir formun sahip olduğu bilgilerin, veritabanına gönderilmesi imkansız hale gelmektedir. Kirlenme mekanizmasının çalışması, Anadil®'in event-driven yapısından kaynaklanmaktadır.

Form ilk açıldığında property içerik değeri False olduğundan, "Dirty" özelliğinin kullanılabilmesi için mutlaka True şeklinde set edilmesi gerekmektedir.
