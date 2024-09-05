# FormText

Bu property formun Always® altında kullanılırken, başlık bilgisini değiştirmektedir.\
\
**Uygulandığı Nesneler**\
Form nesneleri.\
\
**Uygulama Biçimi**\
Sadece yazılabilir bir özelliktir.\
\
**Kullanımı**

```
FormObject.FormText As String
```

**Dikkat Edilecek Noktalar**

Açılan bir formun başlık bilgisini bu property yardımıyla değiştirebilmekteyiz. Başlık bilgisi verilirken, string bir ifade şeklinde olmalıdır.

Anadil® ile kod geliştirilirken bir belge event'i olan \_FormatTitle, aslında bu property'nin uygulamasıdır. Ama geliştirici bu event dışında da istediği zaman, bu property ile form\_caption bilgisini değiştirebilmektedir.
