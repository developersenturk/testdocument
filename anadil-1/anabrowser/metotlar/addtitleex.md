# AddTitleEx

Kolon nesnesine ResourceId ile birlikte yeni bir başlık ekler.\
\
**Kullanımı**

```
ColDefObject.AddTitleEx(
)As Bool
```

**Parametreler**\
Parametresi bulunmamaktadır.\
\
**Geri Dönüş Değeri**\
TRUE/FALSE şeklindedir.\
\
**İlişkili başlıklar:**\
[AddBrowseFolderExLang](../fonksiyonlar/addbrowsefolderexlang.md)\
[CreateColDef](../fonksiyonlar/createcoldef.md)\
[AddFolderAlias](../fonksiyonlar/addfolderalias.md)\
[GetFolderFromStructuredName](../fonksiyonlar/getfolderfromstructuredname.md)\
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
    cd.Format:="s"
    cd.ResourceId:=22000434
    cd.CounterField:="rs"
    cd.Type:=VARTYPE_TEXT
    cd.DisjunctService1:="fknt"
    cd.DisjunctServiceCall1:="GetCurrentCompany"
    cd.DisjunctServiceParam1:="CompanyId"
    cd.AddTitleEx()
```
