# SelectItemInList

Bu metod combo kontrolünden Anadil kodu yardımıyla seçimi sağlamaktadır.\
\
**Uygulandığı Nesneler**\
Combo-Box ve List-Box kontrol nesneleri.\
\
**Kullanımı**

```
ControlObject.SelectItemInList( 
  ItemNum As Number  ' ifade index numarası
)
```

**Parametreler**\
_ItemNum_\
Control içersinden seçilmek istenilen ifade.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Listeden yapılan seçimlerde, çoktan seçim içeriğinden index numarasını vermek suretiyle istediğimiz seçeneğin aktif olmasını temin eden metoddur. Parametre olarak verilen numara 0(sıfırdan) itibaren başlamak üzere, arzulanan ifadenin seçilmiş olmasını sağlar.\
\
Index numarasına dayalı seçim uygulama, geliştirme açısından, seçeneklerin kendi aralarında sort(sıralama) işleminden geçtiklerinden sonra yanlış sonuçlar üretebilmektedir. Bu yüzden kesin sonuç açısından text olarak seçim yapmak daha uygundur.
