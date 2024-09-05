# MoveToFirstEntry

Bu metod current entry göstericisinin değerini ilk entry ifadeye eşitlemektedir.\
\
**Kullanımı**

```
CFFObject.MoveToFirstEntry() As Bool
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri işlemin başarılı olması halinde DOĞRU, aksi durumda ise YANLIŞ olarak gerçekleşmekte olan bir Boolean değerdir.\
\
**Dikkat Edilecek Hususlar**\
CFF ile işlem yapılırken o an hangi satır ile işlem yapıldığını göstermekte olan current satır göstericisinin yanında; aktif olan entry ifadeyi göstermekte olan current entry göstericisi bulunmaktadır. İşte bu metod current(aktif) entry göstericisini ilk entry'yi gösterecek şekilde ayarlamaktadır.\
\
Aktif entry göstericisinin değeri o anki aktif olan satır içersindeki değeri göstermektedir. Yeni satırlara gidilmesi durumunda, her satır için aktif entry göstericisinin değerinin ayrıca set edilmesi, işlemin sağlıklı olarak yapılabilmesi açısından daha güvenilirdir.
