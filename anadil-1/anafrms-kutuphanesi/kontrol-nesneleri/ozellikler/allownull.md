# AllowNull

Bu property kontrol nesnelerinin NULL bir içeriğe sahip olabilmelerini kontrol etmektedir.\
\
**Uygulandığı Nesneler**\
Edit-box kontrol nesnesi.\
\
**Uygulama Biçimi**\
Hem okunabilir hem de yazılabilir bir property'dir.\
\
**Kullanımı**

```
ControlObject.AllowNull As Bool
```

\
**Dikkat Edilecek Noktalar**\
Anadil® altında veritabanı ile yapılan işlemlerde NULL yönetimi büyük bir önem arz etmektedir. Özellikle kullanıcının veri girişi veya değiştirme işlemi uygulamakta olduğu sırada, Always® altında, form üzerindeki kontrollerde, bazı alanları boş bırakması durumunda; bu kontrollerin içeriği NULL olarak algılanacaktır.\
\
NULL içeriğe sahip olarak algılanan bu kontroller tabi ki daha sonraki CFF ve RS işlemlerinde de NULL olarak transfer edilecektir. Veritabanına kayıt anında ise, eğer bu bilgilerin table içersinde NULL olmasına izin verilmiyorsa; son ana kadar belgeyi veritabanına göndermektense, kullanıcıyı daha önceden uyarmak daha faydalıdır.\
\
True içeriğe sahip olması durumunda NULL değerlere izin vermekte olan bu property aynı zamanda Imagine® altında da bir check-box sayesinde aktif yapılabilmekte, sonuçta Anadil® kodu yazmadan da kullanılabilmektedir.
