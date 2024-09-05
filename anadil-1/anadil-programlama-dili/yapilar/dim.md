# DIM

Değişken tanımlanması işlemini gerçekleşten bir yapıdır.\
Görevi\
Değişkenleri Anadil®'e tanıtarak, onlarla ilgili gereken hafızayı temin etmektir.

\
**Kulanımı**

\
`Dim Örnek_Değişken As <Type>`

\
**Açıklama**\
Değişkenler genel olarak Anadil'de 2 türlü tanımlanabilmektedir:

* Local(yerel) olarak,
* Global(küresel) olarak.

Local değişkenler "Function...EndFunction" sınırları arasında tanımlanan yani fonksiyon sınırları dahilinde geçerli olan değişkenlerdir. Fonksiyondan çıkış işlemi sonucunda, değişken de Anadil® tarafından yok edilecek ve o değişkenle ilgili daha başka işlem yapılamayacaktır. Ayrıca local değişkenler memory(hafıza)'nın daha etkin kullanımını sağlamakta gereksiz memory kullanımını önlediğinden daha verimli uygulama işletimi sağlamaktadırlar.

Global yani küresel değişkenler ise herhangi bir Anadil programı geliştirirken bütün fonksiyonların dışında, en üstte tanımlananan değişkenlerdir. Bu değişkenlerin etkinlikleri bütün Anadil kodu dahilinde olmakta, istenildiği an bu değişkenle ilgili bir işlem yapılabilmektedir.

Etkilerinin bütün program dahilinde olması bazı durumlarda sakıncalar doğurabilmekte, gereksiz kaynak kullanımı, ulaşımda denetimsizlik gibi sorunlara yol açabilmektedir. İşte bu yüzden çok fazla mecbur kalmadıkça Global değişken kullanımından kaçınılması gerekmektedir.

Ama bazı durumlarda global değişkenlerin işleri oldukça kolaylaştırdığı da gerçektir; örneğin bir dökümana ait context işlemlerinde kullanılan nesnelerin global olarak kullanılması gibi.
