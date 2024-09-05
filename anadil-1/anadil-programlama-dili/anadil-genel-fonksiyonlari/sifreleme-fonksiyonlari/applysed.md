# ApplySED

Bu fonksiyon verilen key ile daha önce şifrelenmiş string i, yine aynı key ile, Data Encryption Standart algoritmasına göre deşifre eder .\
\
**Kullanımı**

```
Function ApplySED(
  CipherText      As String,     ' Input string
  Len             As Number,     ' CipherText Length
  Key             As String      ' Key string
) As String                      ' Decrypted output string
```

**Parametreler**\
\
_CipherText_\
Deşifrelenecek olan input string. Uzunluğu 8 karakter veya katları olmalıdır.\
\
_Len_\
Deşifrelenecek olan input string uzunluğudur. Maksimum uzunluk 512 karakterdir.\
\
_Key_\
Deşifrelemede kullanılacak anahtar kelimedir. Uzunluğu 8 karakter olmalıdır.\
\
\
**Geri Dönüş Değeri**\
Deşifrelenmiş string geri döner.\
\
**Dikkat Edilecek Hususlar**\
Daha önce hexadecimal e çevirilmiş CipherText HexToBin fonksiyonu ile original haline çevirilmelidir.\
\
**Örnek**

```
Dim Cipher As String
Dim CipherText As String
Dim PlainText  As String
Dim Key  As String

PlainText  := "12345678"
Key := "COKGIZLI"

Cipher := ApplyDES (  PlainText, 8, Key )          'DES algorithması ile encryption
CipherText := BinToHex( Cipher, 8 )                'Cipher hexadecimal e çeviriliyor
MessageBox (CipherText, "CipherText is : ", MB_OK) 'E2E918C1DEAC3E9501       01 CRC dir

Cipher := HexToBin( CipherText, 8 )                'Cipher binarye çeviriliyor
PlainText := ApplySED (  Cipher, 8, Key )          'DES algorithması ile decryption
MessageBox (PlainText, "PlainText is : ", MB_OK)   '12345678


PlainText  := "AAAAAAAAAAAAAAAA"
Key := "AAAAAAAA"

Cipher := ApplyDES (  PlainText, 16, Key  )        'DES algorithması ile encryption
CipherText := BinToHex( Cipher, 16 )               'Cipher hexadecimal e çeviriliyor
MessageBox (CipherText, "CipherText is : ", MB_OK) '19DF84AC9555100319DF84AC955510034A  4A CRC dir

Cipher := HexToBin( CipherText, 16 )               'Cipher binary e çeviriliyor
PlainText := ApplySED (  Cipher, 16, Key )         'DES algorithması ile decryption
MessageBox (PlainText, "PlainText is : ", MB_OK)   'AAAAAAAAAAAAAAAA


```

**Örnek Açıklaması**\
Yukarıda önce 8 karakter uzunluğundaki Plaintext COKGIZLI anahtarı ile ApplyDES fonksiyonuna veriliyor. Elde edilen Cipher yine 8 karakter uzunluğunda nonprintable karakterlerden oluşuyor. Bu nedenle BinToHex ile 16 + 2 uzunluğundaki hexadecimal ifadesi elde ediliyor. Daha sonra CipherText HexToBin fonksiyonu ile Cipher a (binary) dönüştürülüyor. Ve bu ifade yine aynı key (AAAAAAAA) ile deşifrelenerek PlainText elde ediliyor.
