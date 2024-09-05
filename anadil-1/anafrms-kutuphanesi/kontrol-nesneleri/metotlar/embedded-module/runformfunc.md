# RunFormFunc

Embed edilmiş modül formlarına ait fonksiyonların çalıştırılabilmesini sağlar. (Fonksiyon listesinden çıkarılacaktır. RunFunc methodunu form object ile birlikte kullanabilirsiniz)

**Uygulandığı Nesneler**\
Embedded Modül\
\
**Kullanımı**

```
ControlObject.RunFormFunc(
       FullFormFunctionName As String  'Embed edilmiş modülde bulunan form fonksiyonunun tam adı. 
  ) As BOOL
```

\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri boolean: TRUE/FALSE şeklindedir. Call edilen fonksiyonun return tipi BOOL ise return edilen deger dondurulur, return tipi yok ise TRUE doner.\
\
**Dikkat Edilecek Noktalar**\
İlgili fonksiyona form object parametresi, method tarafından eklenmektedir.\
\
**Örnek**

```
wrk_mahsup.mod:

Function muhfis_belge_ac_Click(f As Object) As Bool
  Dim srv AS ServiceCAll 

  Srv:=CreateServiceCall("utl_iliskili_belge_ac","GetRelatedDocumetsMuh",2)
  Srv.r_sayac:=doc_rsayac
  srv.doc_id:="wrk_mahsup"
  srv.CallService()
  muhfis_belge_ac_Click:=TRUE  
EndFunction

-----------------------------------------------------------------------------------------------------------
Embed.ser: Bu service wrk_mahsup.mod u embed olarak kullanır

Function f_TestEmbedFcn_Click(f As Object)

  if (f.em.RunFormFunc("muhfis_belge_ac_Click")) then
     outm("Embedded RunFunc OK")
  else
     outm("Embedded RunFunc FALSE")
  endif

EndFunction

Function f_LoadEm_Click(f As Object)
 'Ornek olarak r_sayaci 1000 olan muhasebe fisi, em isimli embed kontrole yüklenir.
   f.em.DocId:="wrk_muhfis"
   f.em.LoadDoc(1000)
EndFunction

Function f_UnLoad_Click(f As Object)
 'Embed modül kapatılır.
 f.em.CloseDoc()
EndFunction

```
