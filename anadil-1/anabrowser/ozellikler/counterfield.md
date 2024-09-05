# CounterField

Bu property ilgili SQL tümcesinde bulunan sayaç kolonunun adını içermelidir. Genellikle "r\_sayac" kolonu sayaç kolonudur. Tarayıcıda kullanıcı ilgili belgeyi çift tıkladığında, belge, burada verilen sayaç alanı (counterfield) bilgisi kullanılarak açılmaktadır.\
\
**Kullanımı**

```
ColDefObject.<CounterField> As <String>
```

**Uygulandığı Nesneler**\
Bu özellik Tarayıcı Kolon nesnelerinde uygulanmaktadır.\
\
**Property Tipi**\
WriteOnly yani salt yazılabilir bir özelliktir.\
\
**Property Değeri**\
String değer içermelidir..\
\
**İlişkili başlıklar:**\
[Name](name.md)\
[SQL](sql.md)\
[SearchSQL](searchsql.md)\
[AddTitleEx](../metotlar/addtitleex.md)\
[CreateColDef](../fonksiyonlar/createcoldef.md)\
\
**Örnek**

```
    Dim cd As Object

    cd:=CreateColDef()
    cd.Name:="Malzeme Kodu"
    cd.SQL:="Select mlz.r_sayac rs,mlz.malzeme_kodu rs2,p.malzeme_adi from mlz_ana_parti_tanimi mlz,mlz_tanimi p  where p.malzeme_kodu=mlz.malzeme_kodu and p.cid=mlz.cid and mlz.cid = (?) order by mlz.malzeme_kodu"
    cd.SearchSQL:="Select mlz.r_sayac rs,mlz.malzeme_kodu rs2,p.malzeme_adi from mlz_ana_parti_tanimi mlz,mlz_tanimi p  where p.malzeme_kodu=mlz.malzeme_kodu  and mlz.malzeme_kodu>=(?) and  p.cid=mlz.cid and mlz.cid = (?) order by mlz.malzeme_kodu" 
    cd.Field:="rs2"
    cd.Sortable:=True
    cd.Format:="n;0"
    cd.CounterField:="r_sayac"
```
