# GetLanguage

Bu fonksiyon aktif thread locale id değerini döndürür.\
\
Kullanımı

```
Function GetLanguage(
) As Number
```

Parametreler\
Parametresi bulunmamaktadır.\


```
Geri Dönüş Değeri
Aktif locale id değeri döner. Geri dönen değeri aşağıdaki Anadil sabitleri ile karşılaştırabilirsiniz.
LANG_TURKISH
LANG_ENGLISH
LANG_JAPANESE
LANG_CHINESE
LANG_SPANISH
LANG_GERMAN

Örnek
Function wrk_muhfis_CaptionRefresh(f As Object) As Bool
 'This is called when user Locale Language is changed from taskbar
 'Form.Fis.aciklama.caption := GetCaption(ControlId, DefaultCaptionString)

    if (GetLanguage()=LANG_ENGLISH)
       f.aciklama.caption  := "Explanation"
    else
       f.aciklama.caption  := "Açıklama"
   endif

 wrk_muhfis_CaptionRefresh:=True
EndFunction
```
