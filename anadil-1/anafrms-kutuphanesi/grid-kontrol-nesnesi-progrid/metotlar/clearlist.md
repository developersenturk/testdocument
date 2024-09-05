# ClearList

Bu metod grid sütunlarında combo-box ve list-box tipindeki alanlardaki listeyi yok eder.\
\
**Uygulandığı Nesneler**\
Grid sütunu nesneleri.\
\
**Kullanımı**

```
GridColObject.ClearList(
) As Bool
```

**Geri Dönüş Değeri**\
Geri dönüş değeri başarılı ise TRUE değilse FALSE döner.\
\
**Dikkat Edilecek Noktalar** \
Bu method grid combo-box listesinde yer alacak bilgilerin, bir başka hücredeki seçime göre belirlendiği durumlarda kullanılabilir. Örneğin seçilen malzeme sınıfı veya koduna göre uygulanacak fiyat veya indirim seçeneklerinin combo-box listesine doldurulabilmesi için, her bir seçim sonrası, ilgili liste sıfırlanır ve uygun liste AddToColList metodu ile baştan oluşturulur.
