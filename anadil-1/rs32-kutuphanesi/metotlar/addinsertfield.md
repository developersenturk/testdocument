# AddInsertField

Bu metod ile yazılan bir INSERT query statement için kayıt değerleri verilmektedir.\
\
**Kullanımı**

```
RSObject.AddInsertField(
  ColName As String	        ' table column ismi
  Value As <Variant>  ' kaydı yapılacak row değeri
)
```

**Parametreler**\
_ColName_\
Table içersine kayıt yapılırken verilecek column ismidir.\
_Value_\
Verilen column ismine karşılık gelen row değeridir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Bu metod ile BuildInsertStm() fonksiyonunun kullanımı ile ortaya konulan RS nesnesinde, INSERT statement içersindeki yeni table row değerleri verilmektedir. Verilen row değerleri SQL Server tarafıından ilgili table içersine kayıt edilecektir.\
\
Bu işlemde sadece bir column ismi verilmekte olup sonuçta INSERT işlemi ile table içersine yeni bir row eklenmesi gerçekleşmektedir.\
\
Ayrıca value değerinin variant olması, bu değerin string, number veya date olabileceğini hatta NULL içeriğe sahip olabileceği anlamına gelmektedir.
