# CaptionRefresh

\-------\
\
**Kullanımı**

```
Function Form_CaptionRefresh(f As Object) As Bool
 'This is called when user Locale Language is changed from taskbar
 Form_CaptionRefresh:=True
EndFunction

```

**Parametreler**\
_f As Object_\
**Geri Dönüş Değeri**\
Bool\
\
**Dikkat Edilecek Hususlar**\
\-----\
\
**Örnek**

```
'Example : Form.Fis.aciklama.caption := GetCaption(ControlId, DefaultCaptionString)
'Example : f.explanation.caption     := GetCaption(IDS_Work_Order_Str, DefaultCaptionString)
```

**Örnek Açıklaması**\
\-----
