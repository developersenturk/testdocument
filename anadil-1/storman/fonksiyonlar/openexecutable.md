# OpenExecutable

Bu fonksiyon mevcut bir Imagine projesini açar.\
\
**Kullanımı**

```
Function OpenExecutable(
  ProjectName	' Açılacak Always programının adı
) As Object
```

**Parametreler**\
_ProjectName_\


```
Açılacak Always programının adı
örnek :	 c:\Always\Malzeme\mlz_giris.ser,  
	 c:\Always\Muhasebe\wrk_rapor.rep
```

**Geri Dönüş Değeri**\
Geri dönüş değeri açılan Always executable nesnesidir.\
\
**Dikkat Edilecek Noktalar**\
Bu fonksiyon mevcut bir Always executable (Imagine projesi) açar.

```
 Dim Exec As Executable
 
 Exec:=OpenExecutable("c:\Always\Muhasebe\test.rep")
 if Not Exec Then
  OutputResult("Hedef dosya açılamadı")
 EndIf
```
