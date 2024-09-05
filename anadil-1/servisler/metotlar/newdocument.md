# NewDocument

NewDocument Methodu, Always executable'larına ait yeni bir döküman yaratır.\
\
**Kullanımı**

```
AlwaysCallObject.NewDocument(
  DocName As String  ' Döküman adı
) As Bool
```

**Parametreler**\
_DocName_\
Yaratılacak dökümanın adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
NewDocument Methodu, Always executable'larına ait yeni bir döküman yaratır.\
\
**Örnek**

```
Dim alw As Object
  alw:=GetAlwaysCallObject()
  alw.NewDocument("muhfis")
```

\
Training Card Denemesi için örnek tuş:\
