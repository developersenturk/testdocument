# FindLine

Bu metod Anadil programında verilen satır numarasından itibaren, verilen string ifadeye eşit olan program satırını arar.\
\
**Uygulandığı Nesneler**\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.FindLine(
  nSatirNo As Number		' Anadil program satır numarası
  szProgramSatiri As String	' Aranan satırın string ifadesi
) As Number
```

**Parametreler**\
_nSatirNo_\
Anadil program satır numarası\
_szProgramSatiri_\
Aranan satırın string ifadesi

**Geri Dönüş Değeri**\
Geri dönüş değeri bulunan satır numarasıdır.\
\
**Örnek**

{% code overflow="wrap" fullWidth="false" %}
```
  Dim nKodSatiri As Number
  Dim szArananSatir As String

  szArananSatir:="Exec.CreateExecutable(" & CHR(34) & "C:\Always\Muhasebe\Servisler\Test.SER" & CHR(34) & ,"PROJECT_SERVICE)"
  nKodSatiri:=Exec.FindLine(15, szArananSatir )  '15. satırdan itibaren Exec.CreateExecutable satırı aranmaktadır.
```
{% endcode %}
