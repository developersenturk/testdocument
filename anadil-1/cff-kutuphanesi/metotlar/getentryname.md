# GetEntryName

Bu metod bir entry'nin kayıt ismini vermektedir.\
\
**Kullanımı**

```
CFFObject.GetEntryName() As String
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri öğrenmek istediğimiz entry isim bilgisi olan string bir ifadedir.\
\
**Dikkat Edilecek Hususlar**\
Bu metodun kullanımı ile o andaki current entry göstericisinin bize sağladığı entry değerinin isim bilgisini alabilmekteyiz. Bu işlemin de başarılı olması için daha önceden current gösterici değerinin doğru bir şekilde ayarlanmış olması gerekmektedir.\
\
Bu metodun da kullanımı daha çok sequential olarak yapılan bir tarama işlemi ile bütün CFF içeriğinin sahip olduğu entry isimlerinin dökümü şeklinde olabilir.
