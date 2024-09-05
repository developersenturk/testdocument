# Add

Bu metod bir CFF nesnesine variant ifadeleri yerleştirmektedir.\
**Kullanımı**

```
CFFObject.Add(
  FieldName As String,      ' kayıt edilen alan ismi
  Value As <Variant>  ' yeni alanın değeri
)
```

**Parametreler**\
_FieldName_\
CFF içersine kaydı yapılan ifadeye verilecek isim.\
_Value_\
CFF içersine kaydı yapılan ifadenin değeri.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Bu metod CFF'in asli görevi olan bilgi kaybının uygulanma yoludur. CFF içersine yerleştirilen bu ifade herhangi bir variant olabilir ki bunlar string, number veya date tiplerinden biri olabilir demektir.\
\
Bilinmesi gereken başka bir önemli nokta da CFF içersine yerleştirilen variant ifadelerin, nesne altında bizim verdiğimiz isimler ile property şeklinde yer almasıdır. Bu yerleşim sonucunda variant ifadelere daha sonra nesnenin property'si şeklinde ulaşacağız.\
\
Bilgi kayıt işlemi o anki current satır altında gerçekleşmekte olmasından dolayı, uygulama geliştiricinin hangi satırda kayıt yapmakta olduğunu iyi bilmesi daha sonraki o bilgiye tekrar ulaşmasında kolaylık sağlayacaktır.\
\
CFF içersine yazdığımız bu variant ifadelerin isim değerlerini kendimiz tayin etmekteyiz. Ama bu isimlerin özellikle grid'le CFF arasındaki etkileşimlerde, grid'in column isimleri ie aynı olması bazı grid işlemlerini oldukça kolaylaştırmaktadır.\
\
Özellikle database'ten dökümana ve dökümandan database'e yapılan bilgi akışında bu metod NULL yönetimini desteklemekte, bu sayede kullanıcı NULL değerler ile işlem yaparken zorluk çekmemektedir.
