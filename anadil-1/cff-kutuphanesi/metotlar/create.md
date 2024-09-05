# Create

Bu metod var olan bir CFF altında bir alt CFF oluşturmak için kullanılmaktadır.\
**Kullanımı**

```
CFFObject.Create(
  CFFName As String  ' alt CFF nesnesi ismi
)As Object
```

**Parametreler**\
_CFFName_\
Oluşturulacak olan alt CFF için verilen isim.\
**Geri Dönüş Değeri**\
Geri dönüş değeri oluşturulan alt CFF'in kendisi anlamına gelen nesnedir.\
**Dikkat Edilecek Hususlar**\
Bu özellik var olan bir CFF altında bir alt CFF oluşturmaktadır.\
\
CFF yapı itibarıyla çok esnek olduğundan, dilediğimiz kadar sub CFF'leri bünyesi dahilinde tutabilmektedir. İşte bu sub CFF'lerin oluşturulmaları ve ana CFF'e bağlantıları bu metod ile yerine getirilmektedir.\
\
Alt CFF nesnelerine isim verirken aynı ismi tekrar kullanmamalı, yani unique isimlendirme yapmamız gerekmektedir.
