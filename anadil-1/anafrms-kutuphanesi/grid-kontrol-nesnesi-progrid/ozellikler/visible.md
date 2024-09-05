# Visible

Bu property grid sütunlarının görünür olması ile ilgili düzenlemeyi gerçekleştirmektedir.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi bünyesinde yer alan Grid Sütunu nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir ve yazılabilir bir özelliktir.\
\
**Kullanımı**

```
GridColObject.Visible As Bool
```

**Dikkat Edilecek Noktalar**\
Grid sütunları belirlendikten sonra, sütun dahilindeki hücreler için geçerli olacak olan bazı bilgileri bulunmaktadır. Bu bilgiler grup halinde verilmekte olup, sütun property değerleri şeklinde Anadil® kodu ile set edilmektedir.\
\
Sütunlar için verilen bilgilerden biri de görünür olmasına ilişkin verilen bu property değeridir. Property değerinin True olarak belirlenmesi durumunda, sütun görünür olmaktadır. Aynı zamanda bu değer default olarak uygulanmakta olan property bilgisidir.\
\
Grid sütunlarını, bilgi saklama amacıyla geçici olarak kullanmak bazı durumlarda uygulanan bir yöntemdir. İşte bu durumlarda bu sütunları görünmez kılarak, kullanıcıdan ayırmak oldukça mantıklıdır. Görünmez sütunlar, uygulama olarak sanal sütunlar olduğundan, Always® çalışma anında grid görüntüsünde kapladıkları genişlik değeri de 0(sıfır) olmaktadır.
