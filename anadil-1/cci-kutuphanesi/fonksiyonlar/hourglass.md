# HourGlass

Bu fonksiyon uzun süren işlemlerde kullanılabilecek kum saati özelliğini sağlamaktadır.\
\
**Kullanımı**

```
Function HourGlass(
  bOpen As Bool  ' başlama veya bitirme bilgisi
)
```

**Parametreler**\
_bOpen_\
HourGlass özelliğini başlatmayı veya bitirmeyi sağlayan parametredir. True olarak verildiğinde işlem başlamaktadır.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Bu fonksiyonun kullanımı ile, geliştirilmekte olan uygulamanın Always® terminalindeki işletimi esnasında, uzun sürebilecek işlemlerde kullanılmaktadır. Böyle bir işlemde cursor da şeklini kum saatine dönüştürmek suretiyle kullanıcıya bir süre için beklemesi gerektiği mesajını vermektedir.\
\
Bekleme anında son kullanıcının, karşısındaki uygulamayla bağlantısı geçici olarak askıya alınmakta, sonuçta son kullanıcı uygulamayla ilgili hiçbir işlem yapamamaktadır.\
\
HourGlass işlemini sonlandırmak içinse yine bu fonksiyon parametresi ile False değeri vermek yeterli olmaktadır.
