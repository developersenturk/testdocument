# InsertCode

Bu metod Always projesinde program satırını araya (verilen satır numarasına) ekler.\
\
**Uygulandığı Nesneler**\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.InsertCode(
  nSatirNo As Number	' Anadil program satır numarası
  szKodSatırı As String	' Anadil program kod satırı
)
```

**Parametreler**\
_nSatirNo_\
Anadil program satır numarası\
_szKodSatırı_\
Anadil program kod satırı

**Geri Dönüş Değeri**\
Geri dönüş değeri boolean ifadedir.\
\
**Örnek**

```
  Exec.InsertCode(45, "Dim bCancelled As Bool")  '45. satıra kod ekleniyor
```
