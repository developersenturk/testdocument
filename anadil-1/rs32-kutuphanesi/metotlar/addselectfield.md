# AddSelectField

Bu metod bir SELECT statement içerisine, field parametrelerini eklemektedir.\
\
**Kullanımı**

```
RSObject.AddSelectField(
  Field As String  ' table içerisindeki column ismi
)
```

**Parametreler**\
_Field_\
Yapılan query işleminde SELECT statement'da kullanılan table'da yer alan column ismi.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
SQL ile bir SELECT statement oluştururken mutlaka vermemiz gereken parametreler arasında, sorgulama işleminden öğrenilmek istenilen table field isimleri bulunmaktadır. İşte SELECT statement oluşturulurken, statement içersinde kullandığımız bütün table column isimlerini bu metod ile belirtebilmekteyiz.\
\
Unutulmaması gereken husus oluşturduğumuz SELECT statement işletimi sonrasında, SQL Server'dan alınacak query sonucunda, verdiğimiz field parametreleri, RS nesnesinin property'leri olarak, variant ifadeleri bize getirmesidir.\
\
Verilen table column isimleri her zaman sadece çıplak column ismi olmak zorunda değildir; mesela SQL dili ile heading, veya aggregate fonksiyonları uygulanacak şekilde column ismi olarak verdiğimiz parametre olarak da yazmak mümkündür.\
\
Örnek olarak bu metod ile field parametresini\
SUM(ay\_toplam) yıl\_toplamı\
şeklinde verirsek yıl\_toplamı property name olarak RS nesnesinde yerleşecek; variant olarak değeri de bize bütün değerlerin toplamını getirebilecektir.
