# EntryName

Bu property CFF nesnesi dahilinde, database ile document arasında taşınan variant ifadeleri tutmaktadır.\
\
**Kullanımı**

```
CFFObject.<EntryName> As <Variant>
```

**Uygulandığı Nesneler**\
Bu özellik CFF nesnelerinde uygulanmaktadır.\
\
**Property Tipi**\
Read-Write yani hem okunur hem de yazılabilir bir özelliktir.\
\
**Property Değeri**\
Değer olarak variant ifadeleri saklayabilen bu property, sonuçta; _String, Number, Date_ olan değerler içerebilmektedir. Hatta variant ifadeler NULL içeriğe de sahip olabildiğinden bu property NULL içerik de taşıyabilmektedir.\
\
**Dikkat Edilecek Hususlar**\
Bir CFF nesnesinin sahip olduğu yegane property'dir. Bütün entry ifadelerin property şeklinde saklanması CFF dahilinde satırlar altında gerçekleşmektedir.
