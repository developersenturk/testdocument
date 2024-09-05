# Locked

Bu property grid nesnesi sütunlarında kilitleme işlemini uygulamaktadır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir ve yazılabilir bir özelliktir.\
\
**Kullanımı**

```
GridColObject.Locked As Bool
```

\
**Dikkat Edilecek Noktalar**\
Kilitleme işlemi özellikle grid sütunlarının kullanıcı ile bağlantısını kesmek amacıyla kullanılmaktadır. Uygulanması ile ilgili sütuna kullanıcının yapacağı, hücre içeriğini değiştirmeye yönelik edit etkisi önlenmektedir. Kilitlenmiş sütun nesneleri içeriğini ise sadece geliştiricinin yazdığı Anadil® kodu belirleyebilmektedir.\
\
İşlemin gerçekleşebilmesi için, yani bir sütunu kilitlleyebilmek için property değerinin True şeklinde set edilmesi gerekmektedir. Kilit olayını kaldırmak için ise property değeri olarak False değeri vermek yeterli olmaktadır.
