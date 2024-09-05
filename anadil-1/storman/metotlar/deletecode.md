# DeleteCode

Bu metod ile Anadil programının ilgili satırı silinir.\
\
**Uygulandığı Nesneler**\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.DeleteCode(
  nSatirNo As Number	' Silinecek Anadil program satır numarası
)
```

**Parametreler**\
_nSatirNo_\
Silinecek Anadil program satır numarası\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri boolean ifadedir. Verilen satır silinebilirse TRUE ifade döner.\
\
**Örnek**

```
  Exec.DeleteCode(15)  '15. satır programdan silinmektedir
```
