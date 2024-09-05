# DeleteSubCFF

Bu metod bir alt CFF nesnesini ortadan kaldırmaktadır.\
\
**Kullanımı**

```
CFFObject.DeleteSubCFF(
  SubCFFName As String  'alt CFF nesnesi ismi
)
```

**Parametreler**\
_AltCFFName_\
Silinmek istenilen altCFF nesnesinin ismi.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Parametre olarak verdiğimiz alt CFF nesnesinin ismi, root CFF nesnesinin birden fazla alt CFF içerebilmesinden dolayıdır. Ancak bu ayırıcı isim sayesinde hangi alt CFF nesnesini sileceğimizi belirtmekteyiz. Bu yüzden alt CFF isimleri, oluşturma esnasında ilk verilirken unique olmalıdır.
