# MoveToCol

Bu metod grid üzerinde bilgi girişinde kullanılan aktif hücrenin bulunduğu sütunu değiştirmektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.MoveToCol(
  ColName As String  ' hedeflenen sütun ismi
)
```

**Parametreler**\
\
_ColName_\
Aktif satır üzerinde, hangi sütuna gidileceğini belirlemektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Metodun kullanımı ile aktif sütun dediğimiz, kullanıcının vereceği giriş bilgisini alacak olan grid hücresinin bulunduğu sütun değiştirilmektedir. Burada verilen sütun isminin doğru olmaması durumunda bu işlem gerçekleşemeyecektir.
