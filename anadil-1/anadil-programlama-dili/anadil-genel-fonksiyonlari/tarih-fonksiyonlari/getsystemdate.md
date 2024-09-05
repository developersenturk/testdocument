# GetSystemDate

Bu fonksiyon sistemden o andaki tarih bilgisini almaktadır.\
\
Kullanımı

```
Function GetSystemDate()As Date
```

Parametreler\
Fonksiyonun parametresi yoktur.\
\
Geri Dönüş Değeri\
Geri dönüş değeri sistemden alınmakta ve date olarak yani tarih şeklinde olmaktadır.\
\
Dikkat Edilecek Hususlar\
GetSystemDate herhangi bir andaki günün tarihini öğrenmek için kullanılabilir. Fakat kullanılan bilgisayar sisteminin tarih bilgisi yanlış ayarlanmış ise günün tarihi sistem tarihine göre dönecek eğer Always® ile yapılan işlem tarih içeren bir işlem ise bu yanlış bilgiye göre gerçekleştirilecektir.\
\
Geri dönüşte elde edilen tarih bilgisi ise GG/AA/YYYY şeklinde formata sahip olacaktır. Bu format Always®'in genel olarak, default tarih format şeklidir.\
\
Örnek

```
Function F()
  Dim current As Date
  current:= GetSystemDate()
  MessageBox(Format(current,"d"), 
	"Örnek Uygulama", MB_OK+MB_ICONINFORMATION)
EndFunction
```

Örnek Açıklaması\
Buradaki örnek uygulamada önce sistemden tarih bilgisi alınmakta daha sonra da bu bilgi, Mesaj kutusu ile ekranda gösterilmektedir.
