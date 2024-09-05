# ApplyDES

Bu fonksiyon verilen string i verilen key ile Data Encryption Standart algoritmasına göre şifreler.\
\
**Kullanımı**

```
Function ApplyDES(
  PlainText       As String,     ' Input string
  Len             As Number,     ' PlainText Length
  Key             As String      ' Key string
) As String                      ' Encrypted output string
```

**Parametreler**\
\
_PlainText_\
Şifrelenecek olan input string. Uzunluğu 8 karakter veya katları olmalıdır.\
\
_Len_\
Şifrelenecek olan input string uzunluğudur. Maksimum uzunluk 512 karakterdir.\
\
_Key_\
Şifrelemede kullanılacak anahtar kelimedir. Uzunluğu 8 karakter olmalıdır.\
\
\
**Geri Dönüş Değeri**\
Şifrelenmiş string geri döner. Cipher PlainText ile aynı uzunluktadır.\
\
**Dikkat Edilecek Hususlar**\
Geri dönen string okunabilir string olmayabilir. BinToHex fonksiyonu ile Hexadecimal ifadeye dönüştürülmesi gerekir.\
\
**Örnek**

```
Dim Cipher As String
Dim PlainText  As String
Dim Key  As String

PlainText  := "12345678"
Key := "COKGIZLI"

Cipher := ApplyDES (  PlainText, 8, Key )         'DES algorithması ile encryption
Cipher := BinToHex( Cipher, 8 )                   'Cipher hexadecimal e çeviriliyor
MessageBox (Cipher, "Cipher is : ", MB_OK)        'E2E918C1DEAC3E9501       01 CRC dir

PlainText  := "AAAAAAAAAAAAAAAA"
Key := "AAAAAAAA"

Cipher := ApplyDES (  PlainText, 16, Key  )       'DES algorithması ile encryption
Cipher := BinToHex( Cipher, 16 )                  'Cipher hexadecimal e çeviriliyor
MessageBox (Cipher, "Cipher is : ", MB_OK)        '19DF84AC9555100319DF84AC955510034A  4A CRC dir

```

**Örnek Açıklaması**\
Yukarıda önce 8 karakter uzunluğundaki Plaintext COKGIZLI anahtarı ile ApplyDES fonksiyonuna veriliyor. Elde edilen Cipher yine 8 karakter uzunluğunda nonprintable karakterlerden oluşuyor. Bu nedenle BinToHex ile 16 + 2 uzunluğundaki hexadecimal ifadesi elde ediliyor. Daha sonra 16 karakter uzunluğundaki PlainText yine 8 karakterlik AAAAAAAA anahtarı ile şifreleniyor. Elde edilen 16 karakterlik Cipher BinToHex ile 32 + 2 uzunluğundaki hexadecimal string e çeviriliyor.
