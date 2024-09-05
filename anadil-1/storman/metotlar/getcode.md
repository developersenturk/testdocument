# GetCode

Bu metod Anadil programının ilgili satırına ulaşmamızı sağlar.\
\
Uygulandığı Nesneler\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.GetCode(
  nSatirNo As Number	' Anadil program satır numarası
)
```

**Parametreler**\
_nSatirNo_\
Anadil program satır numarası\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri string ifadedir. Program satırı mevcut ise ilgili satırın string ifadesi, mevcut değilse NULL string ifade geri döner.\
\
**Örnek**

```
  Dim KodSatiri As String

  KodSatiri:=Exec.GetCode(15)
```
