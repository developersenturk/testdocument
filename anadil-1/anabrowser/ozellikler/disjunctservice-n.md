# DisjunctService(n)

Bu property SQL ve SearchSQL tümcelerinde bulunan parametrelerin alınacağı servisi belirtir. Örneğin (CompanyId) cid bilgisi fknt.ser dosyasında bulunan GetCurrentCompany adlı fonksiyondan, CompanyId parametre adıyla alınır ve SQL tümcelerine yerleştirilirler. Birden fazla servis-fonksiyon-parametre kullanılabilir. Bu nedenle DisjunctService(n) formatı kullanılır. İkinci parametre için DisjunctService2:="test" şeklinde kullanım mümkündür.\
\
**Kullanımı**

```
ColDefObject.<DisjunctService> As <String>
```

**Uygulandığı Nesneler**\
Bu özellik Tarayıcı Kolon nesnelerinde uygulanmaktadır.\
\
**Property Tipi**\
WriteOnly yani salt yazılabilir bir özelliktir.\
\
**Property Değeri**\
String değer içermelidir.\
\
**İlişkili başlıklar:**\
[DisjunctServiceCall](disjunctservicecall-n.md)\
[DisjunctServiceParam](disjunctserviceparam-n.md)\
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
    cd.DisjunctService1:="fknt"
    cd.DisjunctServiceCall1:="GetCurrentCompany"
    cd.DisjunctServiceParam1:="CompanyId"

```
