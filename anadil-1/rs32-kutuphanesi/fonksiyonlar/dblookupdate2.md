# DBLookUpDate2

Bu fonksiyon içeriği date(tarih) olan bir sahaya ilişkin sorgulama işlemi uygulamaktadır.\
\
**Kullanımı**

```
Function DbLookUpDate2(
  Table As String,     ' table ismi
  Field As String,     ' table column ismi
  KeyField1 As String,  ' anahtar saha1
  KeyValue1 As Variant  ' anahtar saha değeri1
  KeyField2 As String,  ' anahtar saha2
  KeyValue2 As Variant  ' anahtar saha değeri2
)As Date
```

**Parametreler**\
_Table_\
Sorgulama işleminin uygulanacağı table ismidir.\
_Field_\
Table içersinde aranılan column ismidir.\
_KeyField1_\
Sorgulama işleminde uygulanacak kriter column ismidir.\
_KeyValue1_\
Sorgulama işleminde KeyField değeridir. Variant olmasından dolayı number, string, veya date olabilmektedir.\
_KeyField2_\
Sorgulama işleminde uygulanacak 2. kriter column ismidir.\
_KeyValue2_\
Sorgulama işleminde 2. KeyField değeridir. Variant olmasından dolayı number, string, veya date olabilmektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, sorgulamada değeri alınmak istenilen, table column ismine karşılık gelen tarih bilgisidir.\
\
**Dikkat Edilecek Hususlar**\
Bu fonksiyon ile yapılan işlem, SQL ile SELECT statement uygulamasıdır. Query işletimi ile sonuçta içeriği tarih olan bir sahanın değeri elde edilmektedir.\
\
İşletilen SQL statement ise\
SELECT field FROM table WHERE KeyField1 = KeyValue1 and KeyField2 = KeyValue2\
şeklindedir. Burada gereçekleştirilen işlem normal yoldan uygulanabilecek SELECT statement işleminin daha kısa zamanda gerçekleştirilmesidir.
