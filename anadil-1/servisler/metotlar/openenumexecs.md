# OpenEnumExecs

OpenEnumExecs Methodu, tipi verilen excutable'ı açar ve executable'ın id'sini döndürür.\
\
**Kullanımı**

```
AlwaysCallObject.OpenEnumExecs(
  ExecType As Number  ' Executable tipi 
) As Number
```

**Parametreler**\
_ExecType_\
Executable'ın tipidir. Always'de executable'ların sabit numaraları aşağıdaki gibidir.\


* 0\. Rapor
* 1\. Basılı Form
* 2\. Servis
* 3\. Modül

\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri Number'dır.\
\
**Dikkat Edilecek Noktalar**\
OpenEnumExecs Methodu, tipi verilen excutable'ı açar ve executable'ın id'sini döndürür.\
\
**Örnek**

```
Dim alw As Object
Dim enum As Number
  alw:=GetAlwaysCallObject()
  enum:=alw.OpenEnumExecs(2)  'services
```
