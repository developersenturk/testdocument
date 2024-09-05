# AddWhereConjunctEx

Bu metod yapılan query işlemlerinde join uygulamasını sağlamaktadır.\
\
**Kullanımı**

```
RSObject.AddWhereConjunct(
  ColName As String  ' table column ismi
  Value As Variant   ' join değeri
  Type As Number     ' join şekli
)
```

**Parametreler**\
_ColName_\
Oluşturulan query ifadedeki join'de yer alan table column ismidir. Join ifadenin sol tarafına karşılık gelmektedir.\
_Value_\
Oluşturulan join ifadede yer alan column değerinin alabileceği değerdir. Bir nevi eşitliğin sağ tarafına karşılık gelmektedir.\
_Type_\
Join uygulamasında, join tipini belirlemektedir. Sabit sayı olarak alabileceği değerler ise COMP\_EQUAL, COMP\_LESS, COMP\_GREATER, COMP\_NOTEQUAL, COMP\_LESSEQUAL, COMP\_GREATEREQUAL şeklindedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Metodun uygulamasındaki kurallar .AddWhereConjunct() ile aynıdır. Ama bu metod join uygulamasında daha geniş bir karşılaştırma sonuç kümesi oluşturabilmektedir.\
\
Join uygulamasında getirdiği esneklik sayesinde, query işletimi ile sadece 1 row değil, daha fazla sayıda row etkilenebilmektedir.\
\
Bu metod ile tek bir join işlemi uygulanmaktadır. Sonuç olarak oluşturulan query ifadede ise metodun her kullanımı ile ortaya konulan join'ler aralarına AND mantıksal bağlayıcısı gelecek şekilde birleştirilecektir.\
\
Join tipine ilişkin sabit sayılar için bu bölümdeki "Constants" konusuna bakabilirsiniz.
