# CompileStm

Bu metod oluşturulan bir SQL statement ifadenin compile edilmesini sağlamaktadır.\
\
**Kullanımı**

```
RSObject.CompileStm()
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
RS kütüphanesi boyunca anlatılan bütün SQL statement oluşturma işlemlerinde, ortaya çıkan ifadenin EXECUTE ile SQL Server tarafından işletiminden önce mutlaka compile işleminden geçirilmesi gerekmektedir. Aksi taktirde oluşturulmuş olan ifadenin EXECUTE edilmesi imkansızdır.\
\
Compile işleminin tek kullanılmadığı uygulama şekli vardır, o da ExecuteStmDirect() fonksiyonu ile direkt yazılmakta olan statement şeklidir.\
\
Compile ile yazılmış olan SQL satement ifadeler EXECUTE öncesi SQL Server'e gönderilmeye hazırlanmakta olup, ifade aynı zamanda son bir kontrolden de geçmektedir. Ayrıca eğer diğer bir Always® uygulaması olan Debug Terminal de açık ise; oluşturulmuş olan RS statement ifadenin ANSI SQL olarak karşılığı burada geliştiriciye sunulmaktadır. Bu sayede geliştirici Anadil® kodu ile yazdığı ifadenin tam SQL karşılığını kontrol edebilmektedir.
