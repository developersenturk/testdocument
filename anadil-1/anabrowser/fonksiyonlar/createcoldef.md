# CreateColDef

Bu fonksiyon bir Browser Kolon Tanım Nesnesi oluşturulmasını sağlamaktadır.\
\
**Kullanımı**

```
Function CreateColDef(
)As Object
```

**Parametreler**\
Parametre bulunmamaktadır.\
\
**Geri Dönüş Değeri**\
Browser Kolonu Always® dahilinde nesne olarak ele alınmakta ve geri dönüş değeri olan nesne de bu nesnenin kendisi olmaktadır.

**İlişkili başlıklar:**\
[AddBrowseFolderExLang](addbrowsefolderexlang.md)\
[CreateColDef](createcoldef.md)\
[AddFolderAlias](addfolderalias.md)\
[GetFolderFromStructuredName](getfolderfromstructuredname.md)\
\
**Örnek**\
Kolon nesneleri Object olarak tanımlandıktan sonra CreateColDef fonksiyonu tarafından yaratılmaktadırlar. Aynı fonksiyon içinde tekrarlı kullanımlardan önce, hafızadan temizlenmesi için, Close methodu ile yokedilmesi gerekmektedir.\


```
''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''
' BDEF_MALZEMEYONETIMI.SER  
' Bu Service Klasör İş-bitirici tarafından oluşturulmuştur...
' Versiyon: 1.0                                     
' Tarih: 28/6/1996   
' Yazan: MODEL/CemT  
''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''
Function ServiceMain(Service As Object) As Bool
  Service.AddDependency("fknt")
  '
  'CreateBrowsers fonksiyonunun burada expose edilmesinin nedeni: Firma değiştirme ve benzeri durumlarda
  'browser ağaç yapılarının ilgili firma tanımlarına göre yeniden yaratılması gerekmektedir.
  '
  Service.ExposeServiceCall("CreateBrowsers", "")

  ServiceMain := TRUE
EndFunction
  
Function StartService(Service As Object, Cci As Object) As Bool
'Yeniden çağırılabilecek browser fonksiyonlarını içeren servisler, ilk çalıştırma sonrasında durdurulmazlar.
'  Service.End()
  CreateBrowsers()
  StartService:=TRUE
EndFunction

'Ilgili tarayıcı ağaç bölümünü yaratan fonksiyon                    
Function CreateBrowsers()
  Dim  cd As  Object
  Dim  Srv As  Object
  Dim view As Bool  
  ' BWIZARDSTART: Malzeme Yonetimi
  ' Browser wizard generated code. Do not modify!
  
    cd:=CreateColDef() 
    AddBrowseFolderExLang(GetFolderFromStructuredName(""),#
                    "Malzeme Yönetimi",#
                    "",#
                    "",cd,FALSE,"12.00", 22000200)
  
  ' BWIZARDEND: Malzeme Yonetimi
 
  ' BWIZARDSTART: /Malzeme Yonetimi/Parti Tanimlari
  ' Browser wizard generated code. Do not modify!
  
    cd:=CreateColDef()
    cd.Name:="Malzeme Kodu"
    cd.SQL:="Select mlz.r_sayac rs,mlz.malzeme_kodu rs2,p.malzeme_adi from mlz_ana_parti_tanimi mlz,mlz_tanimi p where p.malzeme_kodu=mlz.malzeme_kodu and p.cid=mlz.cid and mlz.cid = (?) order by mlz.malzeme_kodu"
    cd.SearchSQL:="Select mlz.r_sayac rs,mlz.malzeme_kodu rs2,p.malzeme_adi from mlz_ana_parti_tanimi mlz,mlz_tanimi p  where p.malzeme_kodu=mlz.malzeme_kodu  and mlz.malzeme_kodu>=(?) and  p.cid=mlz.cid and mlz.cid = (?) order by mlz.malzeme_kodu" 
    cd.Field:="rs2"
    cd.Sortable:=True
    cd.Format:="s"
    cd.CounterField:="rs"
    cd.Type:=VARTYPE_TEXT
    cd.DisjunctService1:="fknt"
    cd.DisjunctServiceCall1:="GetCurrentCompany"
    cd.DisjunctServiceParam1:="CompanyId"
    cd.AddTitle()
 
    cd.Name:="Malzeme Adı"
    cd.SQL:="Select mlz.r_sayac rs,mlz.malzeme_kodu rs2,p.malzeme_adi from mlz_ana_parti_tanimi mlz,mlz_tanimi p where p.malzeme_kodu=mlz.malzeme_kodu and  p.cid=mlz.cid and mlz.cid = (?) order by p.malzeme_adi"
    cd.SearchSQL:="Select mlz.r_sayac rs,mlz.malzeme_kodu rs2,p.malzeme_adi from mlz_ana_parti_tanimi mlz,mlz_tanimi p  where mlz.malzeme_kodu=p.malzeme_kodu and p.malzeme_adi>=(?) and  p.cid=mlz.cid and mlz.cid = (?) order by p.malzeme_adi" 
    cd.Field:="malzeme_adi"
    cd.Sortable:=True
    cd.Format:="s"
    cd.CounterField:="rs"
    cd.Type:=VARTYPE_TEXT
    cd.DisjunctService1:="fknt"
    cd.DisjunctServiceCall1:="GetCurrentCompany"
    cd.DisjunctServiceParam1:="CompanyId"
    cd.AddTitle()
    View:=False
    srv:=CreateServiceCall("utl_security_manager","CheckAccess",2)
    srv.execid:="MAL_Ana_Parti_Tanimi"
    srv.rightname:="Load"
    If Not Srv.CallService() Then
      View:=True
    EndIf
    srv.Close()
    AddFolderAlias(AddBrowseFolderExLang(GetFolderFromStructuredName("/Malzeme Yönetimi/"),#
                    "Parti Tanımları",#
                    "MAL_Ana_Parti_Tanimi",#    
                    "MAL_Ana_Parti_Tanimi",cd,View,"1.10",22000201),"Parti Tanımları")
   
  ' BWIZARDEND: /Malzeme Yonetimi/Parti Tanimlari

  ' BWIZARDSTART: /Malzeme Yönetimi/Malzeme Sınıfları
  ' Browser wizard generated code. Do not modify!
  
    cd:=CreateColDef()
    cd.Name:="Malzeme Sınıfı No"
    cd.SQL:="select r_sayac,malzeme_sinifi_id,malzeme_sinifi_adi from mlz_siniflari_satir Where  cid =(?) Order by malzeme_sinifi_id"
    cd.SearchSQL:="select r_sayac,malzeme_sinifi_id,malzeme_sinifi_adi from mlz_siniflari_satir Where malzeme_sinifi_id>=(?) and cid =(?) Order by malzeme_sinifi_id"
    cd.Field:="malzeme_sinifi_id"
    cd.Sortable:=True
    cd.Format:="LEFT;s"
    cd.CounterField:="r_sayac"
    cd.Type:=VARTYPE_TEXT
    cd.DisjunctService1:="fknt"
    cd.DisjunctServiceCall1:="GetCurrentCompany"
    cd.DisjunctServiceParam1 :="CompanyId"
    cd.AddTitle()
  
    cd.Name:="Malzeme Sınıfı Adı"
    cd.SQL:="select r_sayac,malzeme_sinifi_id,malzeme_sinifi_adi from mlz_siniflari_satir Where  cid =(?) Order by malzeme_sinifi_adi"
    cd.SearchSQL:="select r_sayac,malzeme_sinifi_id,malzeme_sinifi_adi from mlz_siniflari_satir Where malzeme_sinifi_adi>=(?) and cid =(?) Order by malzeme_sinifi_adi"
    cd.Field:="malzeme_sinifi_adi"
    cd.Sortable:=True
    cd.Format:="LEFT;s"
    cd.CounterField:="r_sayac"
    cd.Type:=VARTYPE_TEXT
    cd.DisjunctService1:="fknt"
    cd.DisjunctServiceCall1:="GetCurrentCompany"
    cd.DisjunctServiceParam1 :="CompanyId"
    cd.AddTitle()
  
    AddFolderAlias(AddBrowseFolderExLang(GetFolderFromStructuredName("/Malzeme Yönetimi/"),#
                    "Malzeme Sınıfları",#
                    "",#
                    "",cd,TRUE, "1.11",22000202),"Malzeme Sınıfları")
  
  ' BWIZARDEND: /Malzeme Yönetimi/Malzeme Sınıfları
  cd.Close()    
 EndFunction
```
