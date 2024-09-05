# GetCaption

Bu fonksiyon verilen resource a karşılık Caption.DLL kütüphanesinde tanımlı ilgili dildeki string karşılığını geri döndürür. Control paneldeki input locale degisikligi veya taskbarda bulunan locale dil değişikliği, modüllerde bulunan CaptionRefresh eventini çalıştırır. CaptionRefresh fonksiyonu içinde bulunan GetCaption fonksiyonları LoadString sistem fonksiyonu aracılığı ile Caption kütüphanesinden aktif dildeki resource stringleri field captionlara güncellenmesini sağlar.\
\
Kullanımı

```
Function GetCaption(
  FieldResourceId As Number  
  DefaultValue As String  
)As String
```

Parametreler\
_FieldResourceId_\
Number data tipindeki Resource numarasıdır.\
_DefaultString_\
Caption.DLL kütüphanesinde verilen ResourceId nin resource u bulunmuyorsa, DefaultValue string geri döner.\
Geri Dönüş Değeri\
İlgili resourceid nin, aktif dildeki string değeri geri döner. ResourceId tanımsız ise verilen DefaultString geri döner.\
\
Dikkat Edilecek Hususlar\
GetCaption fonksiyonunda kullanılacak FieldResourceId ler sayısal ifadeleri ile direkt olarak kullanılmamalı MOD\_FORM\_FIELD benzeri isim formatlarında constant olarak tanımlanmalı ve bu constant ifadeler kullanılmalıdır. Önerilen isim formatlar : MOD\_SUBMOD\_FORM\_FIELD or MOD\_FORM\_FIELD or MOD\_FORM\_SUBFORM\_FIELD\
\
Örnek

```
const  IDS_WRK_MUHFIS_ACIKLAMA := 2100000  'örnek olarak resource numarası 2100000 olsun

Function wrk_muhfis_CaptionRefresh(f As Object) As Bool
 'This is called when user Locale Language is changed from taskbar
 'Form.Fis.aciklama.caption := GetCaption(ControlId, DefaultCaptionString)

     f.aciklama.caption  := GetCaption(IDS_WRK_MUHFIS_ACIKLAMA, "Açıklama")

 wrk_muhfis_CaptionRefresh:=True
EndFunction
```
