# CreateMDI

Bu fonksiyon MDI child window oluşturulmasını sağlamaktadır.\
\
**Kullanımı**

```
Function CreateMDI(
  FormName As String,  ' form ismi
)As Object
```

\
**Parametreler**\
_FormName_\
Imagine® içinde yaratılan MDI child window ismi,\
\
**Geri Dönüş Değeri**\
Geri dönüş nesnesi bir form nesnesidir, ve form nesneleri ile ilgili yapılan işlemlerde kullanılmaktadır.\
\
**Dikkat Edilecek Noktalar**\
MDI(Multiple Document Interface) windowlar bir uygulamada standart bir arayüzle birden fazla dökümanla çalışabilme özelliği sağlamaktadır. Always'in kendi window'u MDI olduğu için CreateMDI ile yaratılacak formlar birer MDI child olacaktır.MDI Child'lar parentlarına bağlı olmak zorundadır.
