# CreateServiceCall

Bu fonksiyon, bir Service Call nesnesi yaratır.\
\
**Kullanımı**

```
Function CreateServiceCall(
  ServiceName  ' Çağırılacak servis'in identifier'ı
  FuncName     ' Servisin kullanılmak istenen fonksiyonu
  NumParams    ' Fonksiyonun parametre sayısı
) As Object
```

\
**Parametreler**\
\
_ServiceName_\
Çağırılacak servisin id'si\
\
_FuncName_\
Serviste bulunan ve kullanılmak istenen fonksiyon adı\
\
_NumParams_\
Serviste bulunan ve kullanılmak istenen fonksiyonun parametre sayısı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri servis nesnesidir.\
\
**Dikkat Edilecek Noktalar**\
Bu fonksiyon, bir Service Call nesnesi yaratır.\
Bu tür uygulamaya örnek olarak bir belge nesnesinin, Servis\_Call nesnesini uzaktan çağırmak suretiyle onun verdiği hizmetten yararlanmasını verebiliriz. Servis\_Call nesnelerinin parametreleri sayesinde iki uygulama veri alış-verişinde de bulunabilmektedir.
