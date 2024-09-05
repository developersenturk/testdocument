# AddGroupBy

Bu metod oluşturulan bir SELECT statement içersinde GROUP BY ifadesinin uygulanabilmesini sağlamaktadır.\
\
**Kullanımı**

```
RSObject.AddGroupBy(
  GroupBy As String  ' table column ismi
)
```

**Parametreler**\
_GroupBy_\
Query ile uygulanan GROUP BY ile belirtilecek table'da yer alan column ismidir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
GROUP BY kullanımı SQL ile yapılan query işlemlerinde çok etkili olan bir uygulama şeklidir. GROUP BY ile yapılmaya çalışılan aynı türden ifadeleri, gruplamak suretiyle her grup için bir tek sonuç ortaya konacak şekilde sonuç kümesi ortaya koymaktır. Özellikle aggregate fonksiyonları ile birlikte çok sık kullanılabilmektedir.\
\
GROUP BY ifadesini doğru olarak uygulamak için yazılan query ifadenin daha önceden test edilmiş olmasında büyük fayda vardır.
