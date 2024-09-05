# IsRowLocked

Bu metod grid satırlarının kilitli olup olmaması hakkında bilgi vermektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.IsRowLocked(
  RowNum As Number ' grid satır numarası
)As Bool
```

**Parametreler**\
_RowNum_\
Grid satırına karşılık gelen sayı değeridir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri ilgili grid satırının kilitli olması hakkındaki bilgiyi içermektedir.\
\
**Dikkat Edilecek Noktalar**\
Grid satırlarının kilitli olup olmadığına ilişkin bilgiyi bu metod ile alabilmekteyiz. Eğer metod geri dönüş değeri True şeklinde elde edilirse, söz konusu satır önceden kilitlenmiş demektir.
