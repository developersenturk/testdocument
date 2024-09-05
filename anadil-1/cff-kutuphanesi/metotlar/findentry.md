# FindEntry

Bu metod bir entry ifadenin aranması işlemini gerçekleştirmektedir.\
\
**Kullanımı**

```
CFFObject.FindEntry(
  EntryName As String  ' aranılan entry ismi
)As Bool
```

**Parametreler**\
_EntryName:_\
Bulunmak istenilen entry ifadenin isim bilgisi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlemin başarılı olması halinde DOĞRU, aksi durumda ise YANLIŞ olarak gerçekleşmekte olan bir Boolean değerdir.

**Dikkat Edilecek Hususlar**\
Burada CFF içersinde daha önce kaydı yapılmış olan entry ifadeye ilişkin bir arama işlemi uygulanmaktadır. Arama işlemi o anki mevcut current satır göstericisinin içersinde gerçekleşmekte olduğundan, current satır göstericisi değerinin doğru şekilde ayarlanmış olması gerekmektedir.\
\
İşlemin başarılı olması halinde current entry göstericisi değeri bulunan entry'yi gösterecektir.\
\
Bu işlem sonucunda bulunan ifadelerin değerini, variant olarak, GetEntry ile alınmaktadır. Burada önemli olan nokta FinEntry ile GetEntry metodlarının beraberce kullanılacak olmasıdır.\
\
CFF içersinde entry taraması yaparken 2 yol vardır: bunlardan ilkini yukarıda verilen metodla arama ve değerini alma şeklindedir. Diğer yol ise MoveToFirstEntry ve MoveToNextEntry metodlarının kullanımı ile yapılan taramadır. Bu iki yolun kesinlikle kesişecek şekilde kullanılmaması gerekmektedir.
