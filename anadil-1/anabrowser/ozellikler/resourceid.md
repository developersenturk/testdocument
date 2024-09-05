# ResourceId

Bu property ilgili tarayıcı kolon adının diğer dillerdeki karşılığının bulunabilmesi için kullanılan Kaynak Numarası bilgisini belirler. Always çalışırken, taskbarda bulunan Locale dil değişikliğini algılamakta ve varsa tüm kaynakların ifadeleri, ResourceId leri kullanılarak ilgili dildeki karşılıkları ile yer değiştirmektedir.\
\
**Kullanımı**

```
ColDefObject.<ResourceId> As <Number>
```

**Uygulandığı Nesneler**\
Bu özellik Tarayıcı Kolon nesnelerinde uygulanmaktadır.\
\
**Property Tipi**\
WriteOnly yani salt yazılabilir bir özelliktir.\
\
**Property Değeri**\
Nümerik değer içermelidir.\
\
**İlişkili başlıklar:**\
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
    cd.Type:=VARTYPE_NUM
    cd.ResourceId:=22000433
    cd.DisjunctService1:="fknt"
    cd.DisjunctServiceCall1:="GetCurrentCompany"
    cd.DisjunctServiceParam1:="CompanyId"
```
