# AddToColList

Bu metod grid sütunlarında combo-box tipindeki alanlarda listeye yeni bir satır ekler.\
\
**Uygulandığı Nesneler**\
Grid sütunu nesneleri.\
\
**Kullanımı**

```
GridColObject.AddToColList(
  Text As String 	' liste elemanı
) As Bool
```

**Parametreler**\
_Text_\
Combo-box içeriğini oluşturacak olan liste elemanı.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri başarılı ise TRUE değilse FALSE döner.\
\
**Dikkat Edilecek Noktalar** \
Metod yardımıyla grid kontrol nesnesi dahilinde, belli bir sütun için çoktan seçimli bir kullanım uygulanmaktadır.
