# UNCName

Bu property, kontrol nesnelerinin UNC (Universal Naming Convention : Evrensel İsim Yapısı) bilgisini elde etmemizi sağlar.\
\
**Uygulandığı Nesneler**\
Bütün kontrol nesneleri.\
\
**Uygulama Biçimi**\
Sadece okunabilir bir özelliktir.\
\
**Kullanımı**

```
ControlObject.UNCName As String

örnek:
Dim szUNCName As String

'f formunda bulunan aciklama alanının UNC ifadesini elde edelim
szUNCName:=f.aciklama.UNCName
outm("UNC:" & szUNCName)

Terminal output:
UNC: Document.wrk_Muhfis.wrk_muhfis:muhfis@aciklama

```

**Dikkat Edilecek Noktalar**\
Bu özellik sayesinde tüm kontrollerin hiyerarşik tanımlarını elde etmek mümkündür.
