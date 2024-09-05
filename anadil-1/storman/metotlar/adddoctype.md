# AddDocType

Bu metod Always projesinin doküman tipini belirlememizi sağlar.\
\
**Uygulandığı Nesneler**\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.AddDocType(
  DocTypeCFF As Object	' Dokuman tipi bilgilerini içeren CFF nesnesi
)
```

**Parametreler**\
_DocTypeCFF_\
Dokuman tipi bilgilerini içeren CFF nesnesi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri boolean ifadedir.\
\
**Dikkat Edilecek Noktalar**

```
DocTypeCFF entryleri şunlardır:
	DocType
	Name
	NewName  : ReadableName
	StartingForm
	PrintedForm
```

**Örnek**

```
  Dim desccff As CFF
  Dim doctycff As CFF
  Dim Exec As Object 'Executable
  Dim i as Number

  Hourglass(True)
  OutputResult("Hedef dosya yaratılamadı")
  bNormalClose:=True
  Exec:=CreateExecutable(GetEnvVar("PROJECT_DEST"),3)

  if Not Exec Then
    OutputResult("Hedef dosya yaratılamadı")
    goto ex:
  EndIf

  ' Write the desc.
  desccff:=CFFCreate("CFF")
  doctycff:=CFFCreate("CFF")
  desccff.Add("ID",sht1.id.ValueStr)
  desccff.Add("Name",sht1.name.ValueStr)
  Exec.SetDescriptor(desccff)
 
  doctycff.Add("Doctype",sht1.doctype.ValueStr)
  doctycff.Add("Name",sht1.name.ValueStr)
  doctycff.Add("NewName",sht1.readname.ValueStr)
  doctycff.Add("StartingForm","f")
  Exec.AddDocType(doctycff)
 
  desccff.Close()
  doctycff.Close()

```
