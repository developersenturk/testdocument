# MoveToRow

Bu metod grid üzerinde bilgi girişinde kullanılan aktif hücrenin bulunduğu satırı değiştirmektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.MoveToRow(
  RowNum As Number  ' hedeflenen satır numarası
)
```

**Parametreler**\
_RowNum_\
Aktif sütun üzerinde hangi satıra gidileceğini belirlemektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Metodun kullanımı ile aktif satır dediğimiz, kullanıcının vereceği giriş bilgisini alacak olan grid hücresinin bulunduğu satır değiştirilmektedir. Burada verilen grid satır numarasının doğru olmaması durumunda bu işlem gerçekleşemeyecektir.
