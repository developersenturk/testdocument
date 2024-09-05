# SetDynamicParamsFirst

Bu property ilgili tarayıcı kolonunun SearchSQL tümcesinin çalıştırılması sırasında, öncelikle hangi parametrelerin elde edileceğini belirler: Eğer SetDynamicParamsFirst özelliği TRUE ise, öncelikle DisjunctService(n), DisjunctServiceCall(n) ve DisjunctServiceParam(n) komutları ile dinamik parametreler elde edilir, daha sonra Arama alanına girilen değer (ve/veya SearchSQL tümcesinde bulunan diğer parametreler elde edilir).\
\
**Kullanımı**

```
ColDefObject.<SetDynamicParamsFirst> As <Bool>
```

**Uygulandığı Nesneler**\
Bu özellik Tarayıcı Kolon nesnelerinde uygulanmaktadır.\
\
**Property Tipi**\
WriteOnly yani salt yazılabilir bir özelliktir.\
\
**Property Değeri**\
Boolean değer içermelidir.\
\
**İlişkili başlıklar:**\
[DisjunctService](disjunctservice-n.md)\
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
    cd.ResourceId:=22000433
    cd.SetDynamicParamsFirst:=TRUE
    cd.Hidden:=FALSE
    cd.DisjunctService1:="fknt"
    cd.DisjunctServiceCall1:="GetCurrentCompany"
    cd.DisjunctServiceParam1:="CompanyId"

```
