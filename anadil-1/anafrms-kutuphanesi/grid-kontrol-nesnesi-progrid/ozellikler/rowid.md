# RowId

Bu property grid satırlarının saklandığı veritabanındaki, saklanma bilgisine ilişkin unique kayıt numarasını vermektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Hücre nesneleri ve Grid Satır nesneleri.\
\
**Uygulama Biçimi**\
Sadece okunabilir bir özelliktir.\
\
**Kullanımı**

```
GridCellObject.RowId As Number
veya
GridRowObject.RowId As Number
```

\
**Dikkat Edilecek Noktalar**\
Grid kontrol nesnesi veritabanında birden fazla table içersinde saklanan verilerin organize edilmesi görevini yerine getirmektedir. Grid bünyesinde yer alan satırlar da veritabanında bir table içersinde saklanmakta ve her satıra karşılık da unique bir kayıt numarası yer almaktadır. Always® dahilinde r\_sayac field ismi sayesinde unique kayıt numaraları saklanmaktadır.\
\
Grid satırlarının veya hücrelerinin .RowID property değerleri, ilgili satıra karşılık gelen r\_sayac bilgisini içermektedir. .RowID içeriği grid satırlarına ilişkin her türlü veritabanı ile ilgili işlemde kullanılmakta olan bilgi olmaktadır.
