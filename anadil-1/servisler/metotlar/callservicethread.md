# CallServiceThread

CallServiceThread Methodu ile service\_call nesnesi ayrı bir thread olarak çağırılır.\
\
**Kullanımı**

```
ServiceObject.CallServiceThread() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
CallServiceThread Methodu ile Service Call nesnesi ayrı bir thread ortamında çağırılır. Bu nedenle call edilen servis fonksiyonu bağımsız çalışmaya başlar ve bu fonksiyon sonuçlanmadan, kontrol, call eden servise döner.\
\
**Örnek**

```
Dim srv As Object
Dim ay_name As String
  srv := CreateServiceCall("GetServerDate","GetMonthName",2)
  srv.MonthNumber:= 1
  srv.Name := ay_name
  srv.CallServiceThread()
  ay_name:=Srv.name 'Bu satır execute ederken "GetServerDate" fonksiyonu return etmemiş olabilir.
```

Yukarıdaki örnekte Servis Call'da hangi parametrenin input ya da output olduğu belli olmadığı için tüm parametrelere bir değer gönderilmiş ve Servis'teki fonksiyonun döndürdüğü sonucu alabilmek için CallServiceThread methodu çalıştırılmıştır.
