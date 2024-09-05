# SetDescriptor

Bu metod Always projesinin tanımlayıcı bilgilerini projeye ekler.\
\
**Uygulandığı Nesneler**\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.SetDescriptor(
  DecObjectCFF As Object	' Proje tanım bilgilerini içeren CFF nesnesi
)
```

**Parametreler**\
_DescObjectCFF_\
Proje tanım bilgilerini içeren CFF nesnesi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri boolean ifadedir.\
\
**Dikkat Edilecek Noktalar**

```
Tanımlayıcı CFF entry leri proje tipine göre değişir:

PROJECT_REPORT
	TargetDevice
	ID
	name
	reppath
	target

PROJECT_PRINTEDFORM
	TargetDevice
	ID
	name
	target

PROJECT_SERVICE
	ID
	name
	AutoStart
	StopAnahtar96

PROJECT_MODULE
	ID
	name
	comments

```

**Örnek**

```
  ' Write the desc.
  desccff:=CFFCreate("CFF")
  desccff.Add("ID", sht1.id.ValueStr)
  desccff.Add("Name", sht1.name.ValueStr)
  desccff.Add("Comments", sht1.comments.ValueStr)
  Exec.SetDescriptor(desccff)
```
