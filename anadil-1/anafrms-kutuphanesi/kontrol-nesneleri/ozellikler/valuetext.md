# ValueText

Bu property kontrol nesnelerine, 255 karakterden daha uzun büyük stringleri set edebilmemizi sağlar.\
\
**Uygulandığı Nesneler**\
Edit-box ve Static kontrol nesneleri.\
\
**Uygulama Biçimi**\
Hem okunabilir hem de yazılabilir bir property'dir.\
\
**Kullanımı**

```
ControlObject.ValueText As String
```

**Dikkat Edilecek Noktalar**\
String uzunluğu sınırı bulunmamaktadır. Her set etmede veya eklemede gerekli olan hafıza allocate edilmektedir.\
