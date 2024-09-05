# Commit

Bu metod ile Anadil projesi diske kaydedilir.\
\
**Uygulandığı Nesneler**\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.Commit(
)
```

**Parametreler**\
Parametresi bulunmamaktadır.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri boolean ifadedir.\
\
**Örnek**

```
  if Not Exec.Commit() Then
    OutputResult("Hedef dosya yaratılamadı")
    goto ex:
  Endif
  Exec.Close()
  OutputResult("success")
```
