# SetCode

Bu metod ile Anadil programının ilgili satırı güncellenebilir.\
\
**Uygulandığı Nesneler**\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.SetCode(
  nSatirNo As Number	' Güncellenecek Anadil program satır numarası
  szYeniSatir As String	' Yeni Anadil program satırı
)
```

**Parametreler**\
_nSatirNo_\
Anadil program satır numarası\
_szYeniSatir_\
Anadil program satır string ifadesi

**Geri Dönüş Değeri**\
Geri dönüş değeri boolean ifadedir. Verilen satır güncellenirse TRUE ifade döner.\
\
**Örnek**

```
  Exec.SetCode(15, "Exec.AddForm(form, " & CHR(34) & "f"  & CHR(34) & ") ")
```
