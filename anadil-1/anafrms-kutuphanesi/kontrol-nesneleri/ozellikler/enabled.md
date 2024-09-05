# Enabled

Bu property, kontrol nesnelerinin Always® altında çalışma anında, form üzerinde görünmesine rağmen kullanılabilir olması ile ilgili düzenlemeyi gerçekleştirir.\
\
**Uygulandığı Nesneler**\
Bütün kontrol nesneleri.\
\
**Uygulama Biçimi**\
Hem okunabilir hem de yazılabilir bir property'dir.\
\
**Kullanımı**

```
ControlObject.Enabled As Bool
```

\
**Dikkat Edilecek Noktalar**\
Kontrol nesnelerinin bazı durumlarda görünebilir olmalarına rağmen kullanıcıdan gelen değişiklik isteğine tepkisiz kalmaları istenilebilir. İşte bu tür durumlarda kontroller disable edilmek, başka bir deyişle devre dışı bırakılmak suretiyle son kullanıcının input etkisi iptal edilebilmektedir.\
\
Bu özellik form ilk yaratıldığında True olarak ilkdeğer almakta daha sonra istenildiğinde Anadil® kodu yardımıyla False değerine eşitlenmek suretiyle, kontrolün kullanıcı ile bağlantısı kesilebilmektedir.
