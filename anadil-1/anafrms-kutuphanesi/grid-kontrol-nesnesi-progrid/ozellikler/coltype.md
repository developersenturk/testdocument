# ColType

Bu property grid sütunlarının kullanım amacını belirlemektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir ve yazılabilir bir özelliktir.\
\
**Kullanımı**

```
GridColObject.ColType As Number
```

\
**Dikkat Edilecek Noktalar**\
Grid sütunları dahilindeki hücrelerin bir kullanım amacı bulunmaktadır. Bu amaç özellikle kullanıcının bilgi girişi yapması durumunda önem kazanmakta ve bilgi girişini kolaylaştırmaktadır. Sayı cinsinden verilmekte olan bu property bilgisi sabit sayılar şeklinde Anadil® kodu ile belirlenmektedir:\


* PG\_EDIT\_TEXT
* PG\_SELECTOR
* PG\_EDIT\_SELECTOR
* PG\_CHECKBOX

Default olarak grid sütunları PG\_EDIT\_TEXT property değerine sahip bulunmaktadır. Bu değer ile normal anlamdaki kullanıcının bilgi girişini gerçekleştirdiği hücre kullanımı uygulanmaktadır. Kullanıcı bilgileri klavye ile karakterleri tek tek yazmak suretiyle verdiği bu hücre kullanımında number, string, veya date şeklindeki bilgiler hücrelerden alınabilmektedir.\
PG\_SELECTOR property değeri ile sütun dahilindeki hücrelerde kullanıcıya çoktan seçimli kullanım olanağı sunulmaktadır. Listeden yapılan bu seçimde bilgi girişi hatası 0(sıfır) olabilmektedir. Combo-box uygulanması şeklinde gerçekleşen hücre kullanımında, geliştricinin hücre değerine ulaşımı ise ValueStr veya ValueNum property değerlerinin okunması ile başarılmaktadır. ValueStr ile combo-box seçiminin okunabildiği gibi ValueNum ile de seçimin index numarası alınabilmektedir. İndexleme ile combo-box uygulanması sırasında ise 0 şeklindeki değer, seçim yapılmamış olmasına karşılık gelmektedir.\
\
Grid hücrelerinin üçüncü bir kullanım şekli de PG\_EDIT\_SELECTOR ile çoktan şeçimli uygulama şeklidir. Bu yöntemin normal combo-box uygulamasını gerçekleştirmesinin yanında, kullanıcı bu hücre üzerinde normal edit typing şeklinde bilgi girişi yapabilmektedir. Kullanıcının normal edit girişinde verdiği bilginin, seçim listesindeki ifadelerden birinin olması zorunluğu bulunmaktadır.\
\
Son olarak property ile PG\_CHECKBOX şeklinde bir değer verilmesi sayesinde 2 alternatifli kullanıcıdan bilgi girişi yapması istenebilmektedir. Yine ValueNum property bilgisi yoluyla geliştirici grid hücrelerindeki bilgileri okuyabilmektedir. Eğer kullanıcı check-box seçimini yapmamışsa 0(sıfır) şeklinde bir içeriğe sahip olacaktır. Sonuç olarak böyle bir hücre uygulanması durumunda, kullanıcının NULL şeklinde bilgi girişi yapması mümkün değildir.
