# FormParams

FormParams Methodu, bir Basılı Formun parametrelerini belirleyebilmek için Basılı Forma ait parametreler penceresinin açılmasını sağlar.\
\
**Kullanımı**

```
AlwaysCallObject.FormParams(
  FormName As String  ' Basılı Form adı
) As Bool
```

**Parametreler**\
_FormName_\
Parametre penceresi açılması istenen Basılı Form adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
FormParams Methodu, bir Basılı Formun parametrelerini belirleyebilmek için Basılı Forma ait parametreler penceresinin açılmasını sağlar.\
\
**Örnek**

```
Dim alw As Object
  alw:=GetAlwaysCallObject()
  alw.FormParams("banka_listesi")
  alw.FormPreview("banka_listesi")
```

Yukarıdaki örnekte Banka Listesi Basılı Formunun parametre penceresi açılmakta ve Parametre değerleri girildikten sonra Form öngörmeye alınmaktadır.
