# IsGroupStart

Bu method gruplanmak istenen field'a göre gruplama yapılıp yapılmadığını kontrol eder. Raporlar da kullanılır.

**Kullanımı**

```
RSObject.IsGroupStart(
  FieldName  'SQL statement'tan alınan column adı
)As Bool
```

**Parametreler**\
_FieldName_\
SQL statement'tan alınan column adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, gruplama yapildiysa TRUE döner.\
\
**Dikkat Edilecek Konular**\
Raporlarda kullanılır. Select statement'ta istenen field'a göre orderlanmış olan datanın, raporlarda o field'ın içeriğinin değişmesi durumunda, grup başlarını ve sonlarını bulmak için kullanılır.
