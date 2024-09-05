# AddDependency

AddDependency methodu, bir Servisin başlayabilmek için başka bir servise ihtiyacı varsa, çalışmasının o servisin çalışmasına bağlı olduğunu belirtir .\
\
**Kullanımı**

```
ServiceObject.AddDependency(
  ServiceName  ' Servis kimliği
) As Bool
```

**Parametreler**\
\
_ServiceName_\
Kendisinden önce başlatılması istenen servisin id'si\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
AddDependency methodu, bir Servisin başlayabilmek için başka bir servise ihtiyacı varsa, çalışmasının o servisin çalışmasına bağlı olduğunu belirtir .\
Servis başlamak için, bağımlı olduğu servisin çalışıp çalışmadığını kontrol eder. Eğer bağımlı olduğu servis başlamamışsa o servisi başlatır. Bu şekilde her servis, önce kendisine bağımlı olan servisi zincirleme bir şekilde başlatır. Eğer servisin bağımlı olduğu servislerden biri başlatılamazsa, kendi servisimizde başlamayacaktır.
