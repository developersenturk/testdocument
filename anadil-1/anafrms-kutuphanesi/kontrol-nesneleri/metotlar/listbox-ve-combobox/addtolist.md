# AddToList

Bu metod çoktan seçimli kontrol nesneleri için içerik ifadelerini yerleştirmektedir.

**Uygulandığı Nesneler**\
Combo-Box ve List-Box kontrolleri.\
\
**Kullanımı**

```
ControlObject.AddToList(
  Text As String  ' eklenecek ifade
)
```

**Parametreler**\
_Text_\
Çoktan seçimli olarak düzenlenmekte olan combo veya list box dahiline katılacak olan seçenek ifadelerdir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
List-box ve combo-box şeklinde düzenlenmek istenilen kullanıcıya çoktan seçim olanağı veren özel Windows kontrollerinde, seçim listesine yeni string alternatiflerinin eklenmesini sağlayan bir metoddur.\
\
ControlObject ile gelen Imagine® ile form üzerine yerleştirmiş olduğunuz, list-box veya combo-box nesnesidir. İstenildiği zaman kullanılabilen bir özelliktir yani aktif olarak da list veya combo box'ların içeriklerine eklemeler her zaman yapılabilir.
