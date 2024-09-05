# AddWhereConjunct

Bu metod yapılan query işlemlerinde equi-join uygulanmasını sağlamaktadır.\
\
**Kullanımı**

```
RSObject.AddWhereConjunct(
  ColName As String  'table column ismi
  Value As Variant   'join değeri
)
```

**Parametreler**\
_ColName_\
Oluşturulan query ifadedeki join'de yer alan table column ismidir. Join ifadenin sol tarafına karşılık gelmektedir.\
_Value_\
Oluşturulan join ifadede yer alan column değerinin alabileceği değerdir. Bir nevi eşitliğin sağ tarafına karşılık gelmektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Anadil® kodu ile şimdiye kadar vermiş olduğumuz fonksiyonlar ile temelde 4 çeşit statement oluşturabilmekteyiz. Bunlar SELECT, INSERT, UPDATE ve DELETE statement'lerdir. İşte bu yapılan query işlemlerinde join uygulamasını bu metod ile yapabilmekteyiz.\
\
SQL ile yazım esnasında WHERE clause ile belirtilmekte olan join uygulamasında, bilindiği üzere, join ifadenin sol kısmı ve sağ kısmı bulunmaktadır. Bu ifadelerin sağ kısmının aldığı değere göre sonuç ifadenin satır sayısı değişmektedir. Ama biz Anadil® ile yalnızca "equi join" uygulamaktayız. Query işletimi sonucunda sadece 1 row değeri etkilenmektedir.\
\
Bu metod ile tek bir join işlemi uygulanmaktadır. Sonuç olarak oluşturulan query ifadede ise metodun her kullanımı ile ortaya konulan join'ler, aralarına AND mantıksal bağlayıcısı gelecek şekilde birleştirilecektir.\
\
Ayrıca value değerinin variant olması, bu değerin string,number veya date olabileceğini hatta NULL içeriğe sahip olabileceği anlamına gelmektedir.
