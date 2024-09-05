# IsDate

Bu fonksiyon verilen tarih in geçerli tarih ifadesi olup olmadığını kontrol eder.

\
Kullanımı

```
Function IsDate(
  D As Date  ' Kontrol edilecek date ifade
)As Bool
```

Parametreler\
_D_\
Doğruluğu kontrol edilecek olan tarih ifadesi.\
\
Geri Dönüş Değeri\
Geçerli ifade ise TRUE değilse FALSE döner.\
\
Örnek

```
  Dim d As Date
  Dim s As String
  d:=Str2Date("15/08/1974")
  if ( IsDate (d) ) then
     outm("Geçerli tarih ifadesi")
else
     outm("Geçersiz tarih ifadesi")
endif
```
