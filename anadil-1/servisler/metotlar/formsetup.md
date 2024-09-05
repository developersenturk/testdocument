# FormSetup

FormSetup Methodu, bir Basılı Formun column ve satır ve karakter genişliklerini ayarlayabilmek için Setup penceresini açar.\
\
**Kullanımı**

```
AlwaysCallObject.FormSetup(
  FormName As String  ' Basılı Form adı
) As Bool
```

**Parametreler**\
_FormSetup_\
Setup ayarlarının geçerli olması istenen Basılı Form adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
FormSetup Methodu, bir Basılı Formun column ve satır ve karakter genişliklerini ayarlayabilmek için Setup penceresini açar.\
\
**Örnek**

```
Dim alw As Object
  alw:=GetAlwaysCallObject()
  alw.FormSetup("banka_listesi")
  alw.FormPreview("banka_listesi")
```
