# LastError

Programların çalışması sırasında(Run-Time) meydana gelebilecek hataların kontrol edilmesini sağlayan bir fonksiyondur.\
\
Kullanımı

```
Function LastError() As Number
```

Parametreler\
Herhangi bir parametresi yoktur.\
\
Geri Dönüş Değeri\
Geri dönüş değeri hatanın oluşması durumunda, ilgili hataya karşılık gelen sayısal bir değerdir.\
\
Dikkat Edilecek Hususlar\
Dönüş değeri sayısal olan bu fonksiyon, herhangi bir Run-Time hatası oluştuğu taktirde yapılacak işlemler için tanımlanabilir.\
\
Aşağıdaki tabloda ise hatalar ve karşılık gelen hata kodları verilmiştir:\
\


| Bilinmeyen Metod                     | 1  |
| ------------------------------------ | -- |
| Bilinmeyen Özellik                   | 2  |
| Hatalı \<Metod / Özellik> dönüş tipi | 3  |
| Hatalı Özellik tipi                  | 4  |
| Yeterli Hafıza Yok                   | 5  |
| Salt Okunabilir Özellik              | 6  |
| Metodun Parametre Sayısı Yanlış      | 7  |
| Metodun Parametresinin Tipi Yanlış   | 8  |
| Salt Yazılabilir Özellik             | 9  |
| Nesneye İlk Değer Verilmemiş         | 10 |
| Dizinin Sınırları Aşıldı             | 11 |
| Bilinmeyen Hata                      | 99 |

\
Örnek

```
  Dim hata As Number
  Dim a As Object
  a.hesapla()
  hata:= LastError()
  If hata <> 0 Then
    MessageBox("Hata Oluştu.",     "UYARI",MB_OK+MB_ICONEXCLAMATION)
  EndIf
```

Örnek Açıklaması\
Burada a nesnesinin "hesapla" şeklinde bir metodu kullanılmaya çalışılıyor. Fakat böyle bir metod daha önceden tanımlı olmadığından hata değişkeninin değeri "1" olur. Sonuç olarak ise "0" dan farklı bir değer için ekrana "Hata Oluştu" uyarı mesajı gelmektedir.
