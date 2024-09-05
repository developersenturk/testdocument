# OpenDocument

OpenDocument Methodu, varolan bir dökümanı açar.\
\
**Kullanımı**

```
AlwaysCallObject.OpenDocument(
  DocName As String  ' Döküman adı
  r_sayac As Number  ' Açılacak Dökümanın sayacı
) As Bool
```

**Parametreler**\
_DocName_\
Açılacak dökümanın adı\
\
_r\_sayac_\
Açılacak dökümanın sayacı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
OpenDocument Methodu, varolan bir dökümanı açar.\
\
**Örnek**

```
Dim alw As Object
  alw:=GetAlwaysCallObject()
  alw.OpenDocument("muhfis",1)
```

\
