# CloseDocument

CloseDocument Methodu, açık bir dökümanı kapatır.\
\
**Kullanımı**

```
AlwaysCallObject.CloseDocument(
  DocName As String  ' Döküman adı
  r_sayac As Number  ' Kapatılacak Dökümanın sayacı
) As Bool
```

**Parametreler**\
_DocName_\
Kapatılacak dökümanın adı\
\
_r\_sayac_\
Kapatılacak dökümanın sayacı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
CloseDocument Methodu, açık bir dökümanı kapatır.\
\
**Örnek**

```
Dim alw As Object
  alw:=GetAlwaysCallObject()
  alw.OpenDocument("muhfis",2)
  if alw.OpenDocument("muhfis",1) Then
    alw.CloseDocument("muhfis",2)
  Endif
```
