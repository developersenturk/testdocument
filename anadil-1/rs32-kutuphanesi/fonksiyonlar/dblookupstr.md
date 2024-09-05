# DBLookUpStr

Bu fonksiyon içeriği string olan bir sahaya ilişkin sorgulama işlemi uygulamaktadır.\
\
**Kullanımı**

```
Function DbLookUpStr(
  Table As String,     ' table ismi
  Field As String,     ' table column ismi
  KeyField As String,  ' anahtar saha 
  KeyValue As Variant  ' anahtar saha değeri
)As String
```

**Parametreler**\
_Table_\
Sorgulama işleminin uygulanacağı table ismidir.\
_Field_\
Table içersinde aranılan column ismidir.\
_KeyField_\
Sorgulama işleminde uygulanacak kriter column ismidir. Çoğunlukla primary key olarak uygulanmaktadır.\
_KeyValue_\
Sorgulama işleminde KeyField değeridir. Variant olmasından dolayı number, string, veya date olabilmektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, sorgulamada değeri alınmak istenilen, table column ismine karşılık gelen string değerdir.\
\
**Dikkat Edilecek Hususlar**\
Bu fonksiyon ile yapılan işlem, SQL ile SELECT statement uygulamasıdır. Query işletimi ile sonuçta içeriği String olan bir sahanın değeri elde edilmektedir.\
\
İşletilen SQL statement ise\
SELECT field FROM table WHERE KeyField = KeyValue\
şeklindedir. Burada gereçekleştirilen işlem normal yoldan uygulanabilecek SELECT statement işleminin daha kısa zamanda gerçekleştirilmesidir.
