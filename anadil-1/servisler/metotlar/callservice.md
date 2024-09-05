# CallService

CallService Methodu ile service\_call nesnesi çağırılır.\
\
**Kullanımı**

```
ServiceObject.CallService() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
CallService Methodu ile Service Call nesnesi çağırılır.\
\
**Örnek**

```
Dim srv As Object
Dim ay_name As String
  srv := CreateServiceCall("GetServerDate","GetMonthName",2)
  srv.MonthNumber:= 1
  srv.Name := ay_name
  srv.CallService()
  ay_name:=Srv.name
```

Yukarıdaki örnekte Servis Call'da hangi parametrenin input ya da output olduğu belli olmadığı için tüm parametrelere bir değer gönderilmiş ve Servis'teki fonksiyonun döndürdüğü sonucu alabilmek için CallService methodu çalıştırılmıştır.
