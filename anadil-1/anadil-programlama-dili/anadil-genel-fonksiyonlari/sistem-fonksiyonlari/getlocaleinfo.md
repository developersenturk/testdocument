# GetLocaleInfo

Sistem veya kullanıcı bazında geçerli olan, Ondalık (Genellikle nokta kullanılır) ve binlik ayıraç (Genellikle virgül kullanılır) karakterini sistemden almak için kullanılır.\
\
Kullanımı

```
Function GetLocaleInfo(
LocaleSys  As Number   'System veya User seçimi
LocaleItem As Number   'Alınmak istenen item kodu
) As String
```

Parametreler\
_LocaleSys_ : LOCALE\_SYSTEM\_DEFAULT veya LOCALE\_USER\_DEFAULT sabitleri kullanılabilir. _LocaleItem_ :

LOCALE\_SDECIMAL veya LOCALE\_STHOUSAND sabitleri veya Anadilde henüz tanımlanmamış, string ifade döndüren, item kodları (Bknz : MSDN GetLocaleInfo fcn help) kullanılabilir.

\
\
Geri Dönüş Değeri\


```
Geri dönüş değeri 
LOCALE_SDECIMAL için ondalık karakteri içeren string ifadedir.
LOCALE_STHOUSAND  için binlik ayıraç karakterini içeren string ifadedir.. 
```

\
\
Dikkat Edilecek Hususlar\


'GetLocaleInfo fonksiyonu Excel e bir sayı yazdırırken o sayının formatını ayarlamak için kullanılabilir.

\
\
\
Örnek

```
Dim decChar  as string

decChar := GetLocaleInfo(LOCALE_USER_DEFAULT, LOCALE_STHOUSAND)
decChar := "#" & decChar & "##"
O.SetProp("NumberFormat", decChar)

'Böylece formatı sabit olarak #.##  veya  #,## olarak belirtmeye gerek kalmıyor.
```

Örnek Açıklaması\


Burada aktif kullanıcının binlik ayıraç karakteri sistemden alınmakta ve Excel hücresine yazdırılacak rakamın formatı parametrik olarak belirtilmektedir. Kullanıcıların Regional Settings DECIMAL ve THOUSAND karakter tanımları farklılık gösterebilmektedir.
