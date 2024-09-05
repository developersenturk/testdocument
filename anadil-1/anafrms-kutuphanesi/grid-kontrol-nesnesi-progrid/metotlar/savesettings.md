# SaveSettings

Bu metod ile grid'in form üzerindeki görünüm ayarlarının saklanması gerçekleştirilmektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi.\
\
**Kullanımı**

```
GridObject.SaveSettings() As Bool
```

\
**Parametreler** \
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri yapılan işlemin başarılı olması durumunda True, aksi durumda ise False olarak gerçekleşmekte olan boolean değerdir.\
\
**Dikkat Edilecek Noktalar**\
Grid'in görünüm ayarları arasında sütunların sıralamaları, genişlikleri, satır yükseklikleri gibi kullanıcı tarafından mouse ile her zaman değiştirilebilen ayarlar bulunmaktadır. Bu ayarların Registry ile saklanması ve yüklenmesi sayesinde, daha kullanışlı bir grid uygulaması sağlanmaktadır.\
\
Grid ayarlarının saklanabilmesi için öncelikle Imagine™ altında form geliştirilmesi sırasında grid'e ait "Özellikler" bölümünde "Use Registry for Settings" adlı check-box'ın seçili olması gerekmektedir. Bu işlemler sonucunda aynı bölümde yer alan "User Popup Menu Enabled" check-box da otomatik olarak seçilmekte olup; bunun sayesinde de grid'e ait kullanım işlemlerinin yapılabileceği menu kullanımı da grid tarafından kullanıcıya sağlanmaktadır. Bu menüyü kullanmak isteyen Always™ kullanıcısı, mouse göstericisinin grid üzerinde olduğu herhangi bir anda mouse sağ tuşuna basmalıdır.\
\
Herhangi bir anda grid kullanıcı ayarlarının saklanması için bu metodun programcı tarafından çağrılması yeterli olmaktadır. Grid menusu sayesinde de kullanıcının direkt olarak kendisinin bu ayarları saklaması mümkündür. Bu işlem için menüden "Ayarları Kaydet" isimli ifade mouse ile seçilmelidir.\
\
Saklanmış olan ayarların grid üzerinde tekrar uygulanması ise grid menusu yardımıyla olabileceği gibi, grid metodu olarak da .LoadSettings() ile yapılabilmektedir.
