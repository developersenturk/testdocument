# Color

Bu property grid sütunu başlık bilgisinin görünme rengini belirlemektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir ve yazılabilir bir özelliktir.\
\
**Kullanımı**

```
GridColObject.Color As Number
```

\
**Dikkat Edilecek Noktalar**\
Grid sütunlarının kullanıcıya göre görünümlerini düzenlemek daha görsel uygulamalar geliştirilmesini sağlayabilecektir. İşte bu anlamda bazı sütun başlıklarını farklı renklerde göstermek kullanıcının daha fazla dikkatini çekecektir. Bu bir anlamda monoton uygulamalardan da uzaklaştırabilecek bir kullanım şeklidir.\
\
Property değerini belirleyebilmek için başka bir fonksiyondan yararlanılmaktadır. Bu fonksiyon ise RGB ismindedir, ve 3 parametreye sahiptir. Ayrıca sayı şeklinde geri dönüş değerine bulunmaktadır ve bu değer bu property değeri olarak verilmektedir.

```
Function RGB(
  RedValue As Number,    ' kırmızı etkisi değeri
  GreenValue As Number,  ' yeşil etkisi değeri
  BlueValue As Number    ' mavi etkisi değeri
)As Number
```

RGB fonksiyonunda verilen parametre değerleri 0 ile 255 arasında değişmekte ve bu değer 3 ayrı rengin ağırlığını temin etmektedir. Mesela her üç parametre 255 olarak verilirse beyaz rengi veya her üçü de 0 olarak verilirse siyah rengi elde edilecektir. Eğer 255, 0 ,0 şeklinde parametre değerleri verilecek olursa kırmızı renginde başlık bilgisi Always® altında kullanıcı tarafından görülebilecektir.
