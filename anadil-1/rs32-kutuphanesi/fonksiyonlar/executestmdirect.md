# ExecuteStmDirect

Bu fonksiyon doğrudan bir SQL statement yazılabilmesini ve işletimini sağlamaktadır.\
\
**Kullanımı**

```
Function ExecuteStmDirect(
  Statement As String  ' SQL statement
)
```

**Parametreler**\
_Statement_\
SQL Server üzerinde doğrudan işletilecek olan SQL ifadedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Burada uygulanmakta olan, direkt olarak herhangi bir SQL statement yazılması ve doğrudan yazılan SQL dilindeki query ifadenin SQL Server üzerinde işletiminin gerçekleştirilmesidir. Bu işletimin doğrudan olmasından dolayı yazılan ifade Compile ve Execute işlemlerinden geçmemektedir.\
\
Bu fonksiyonun hedeflerinden biri herhangi bir kalıba sığmayan özel SQL statement işletimini Anadil® kodu yardımıyla gerçekleştirilebilmesini sağlayabilmektedir.\
\
Bu fonksiyon ile yazılabilecek olan string formatındaki SQL statement ifadenin uzunluğu max. 255 karakter olabilmektedir. Bu da tabi ki genel Anadil® string limit değerinden kaynaklanmaktadır.
