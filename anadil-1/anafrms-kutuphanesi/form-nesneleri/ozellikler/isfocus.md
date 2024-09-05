# IsFocus

Bu property formun, "Focus" özelliği açısından test edilmesini sağlamaktadır.\
\
**Uygulandığı Nesneler**\
Form nesneleri.\
\
**Uygulama Biçimi**\
Sadece okunabilir bir özelliktir.\
\
**Kullanımı**

```
FormObject.IsFocus As Bool
```

**Dikkat Edilecek Noktalar**

Anadil® form tabanlı uygulamalarında, Always® işletimi sırasında run-time anında sadece bir kontrol "Focus" flag değeri aktif olacaktır. Birden fazla Always® uygulamasının aynı anda çalıştığını da düşünürsek, Windows sadece bir kontrolün "Focus" özelliğini aktif yapacak, sonuçta ise sadece bir form aktif "Focus" değerine sahip olmuş olacaktır.

Geliştirici herhangi bir formun sahip olduğu kontrole "Focus" özelliğini aktif hale geçirmek istediğinde, öncelikle formun gerçekten aktif olduğunu test etmek için bu property değerine başvurmalıdır. Bu property değerinin True olması durumunda, söz konusu form aktif demektir. Aktif form sayesinde geliştirici, kontrollere ilişkin yanlış yapılabilecek işlemleri önleyebilmekte ve sonuçta daha sağlıklı uygulamalar ortaya çıkmaktadır.
