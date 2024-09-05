# IsConnected

Bu fonksiyon verilen internet adresine baglanti olup olmadigini kontrol eder. Internet erisimi ve ilgili adrese erisim varsa TRUE, yoksa FALSE döner.\
\
Kullanımı

```
Function IsConnected(
  InternetAddress As String   '  http://www.mbi.com.tr
)As Bool
```

Parametreler\
_InternetAddress_\
Ilgili internet adresi.\
\
Örnek

```
if ( IsConnected("http://www.mbi.com.tr") ) then
   outm("OK")
else
  outm("Baglanti yok")
endif
```
