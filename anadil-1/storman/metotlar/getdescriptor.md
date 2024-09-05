# GetDescriptor

Bu metod Always projesinin tanımlayıcı bilgilerini verir.\
\
**Uygulandığı Nesneler**\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.GetDescriptor(
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
  'Get the desc.
  desccff:=CFFCreate("CFF")
  Exec.GetDescriptor(desccff)
```
