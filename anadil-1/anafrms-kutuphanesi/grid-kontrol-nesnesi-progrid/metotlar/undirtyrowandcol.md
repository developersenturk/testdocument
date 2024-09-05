# UnDirtyRowAndCol

Bu metod önceden kirlenmiş bir grid hücresinde, yapay olarak kirlilik durumunu ortadan kaldırmaktadır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.UnDirtyRowAndCol(
  RowNum As Number   ' hücrenin yer aldığı satır
  ColName As String	 ' hedeflenen dahil olduğu sütun
)
```

**Parametreler**\
_RowNum_\
Kirletilmesi istenen hücrenin yer aldığı satır numarası.\
_ColName_\
Kirletilmesi istenen hücrenin yer aldığı sütun ismi.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Metod kullanımı ile daha önceden kirlenmiş olan bir hücrenin, yapay olarak tekrar kirlenmemiş durumuna dönmesi temin edilmektedir. Eğer bir satırın sahip olduğu hücrelerin hepsinin kirlilik özelliği yok edilmiş ise söz konusu satır da kirlenmemiş olacaktır. Kirlenmemiş olan bir satırın veritabanına taşınması, Always® tarafından gerçekleştirilmeyen bir olaydır.
