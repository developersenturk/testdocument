# Enabled

Bu property, form nesnelerinin Always® altında çalışma anında, formun üzerindeki (alt tabsheet kontrolleri dahil) tüm kontrollerin Enable/Disable yapılabilmesini sağlar. Özellikle iptal edilmiş belgelerin gösteriminde kullanılabilir.\
\
**Uygulandığı Nesneler**\
Bütün Form nesneleri.\
\
**Uygulama Biçimi**\
Yazılabilir bir property'dir.\
\
**Kullanımı**

```
FormObject.Enabled As Bool

örnek:
FormObject.Enabled:=TRUE
FormObject.Enabled:=FALSE

```

\
**Dikkat Edilecek Noktalar**\
Bu özellik sayesinde güncellenmesini istemediğimiz belgelerin alanlarının tümünü kullanıcıya gösterirken, düzeltme şansı verilmemiş olur.\
\
Form sahip olduğu bu property'sinde True değere sahipse, ilgili kontroller normale döner, aksi durumda ise form üzerinde edit edilemez şekilde görünürler.\
\
