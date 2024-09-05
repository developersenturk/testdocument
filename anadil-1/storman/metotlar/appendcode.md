# AppendCode

Bu metod Always projesine program satırı ekler.\
\
**Uygulandığı Nesneler**\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.AppendCode(
  AnadilKodSatırı As String	' Anadil program kod satırı
)
```

**Parametreler**\
_AnadilKodSatırı_\
Anadil program kod satırı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri boolean ifadedir.\
\
**Örnek**

```
  Exec.AppendCode("''''''''''''''''''''''''''''''''''''''''''''''''''''")
  Exec.AppendCode("' Bu Modül iş-bitirici tarafından oluşturulmuştur...")
  Exec.AppendCode("' Versiyon: 1.0                                     ")
  Exec.AppendCode("' Tarih: " & Date2Str(GetSystemDate())               )
  Exec.AppendCode("' Yazan: " & GetEnvVar("USERDOMAIN") & "/" & GetEnvVar("USERNAME") )
  Exec.AppendCode("''''''''''''''''''''''''''''''''''''''''''''''''''''")
  Exec.AppendCode("")
```
