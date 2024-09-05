# CopyDocument

CopyDocument Methodu, ilgili modülü boş olarak açar, r\_sayac'ı verilen varolan bir dökümanın içeriğini, yeni açılan dökümana kopyalar. Yeni dökümanın statusu kirli, grid satırları inserted durumundadır.\
\
**Kullanımı**

```
AlwaysCallObject.CopyDocument(
  DocName As String  ' Döküman adı
  r_sayac As Number  ' Kopyalanacak Dökümanın sayacı
) As Bool
```

**Parametreler**\
_DocName_\
Kopyalanacak dökümanın adı\
\
_r\_sayac_\
Kopyalanacak dökümanın sayacı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
CopyDocument Methodu, varolan bir dökümanın kopyasını yeni döküman olarak açar.\
\
Örnek

```
Dim alw As Object
  alw:=GetAlwaysCallObject()
  alw.CopyDocument("muhfis",1)
```
