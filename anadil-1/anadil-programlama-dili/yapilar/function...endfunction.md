# FUNCTION...ENDFUNCTION

Bu yapı Anadil®'de fonksiyon sınırlarını belirlemektedir.\
**Görevi**\
Anadil® kodunda yapısal program yapısını temin etmek ve event-driven programlamayı gerçekleştirmektir.\
**Kullanımı**

\
Açıklama

```
Function Name_Func() As <VarType> ' fonksiyon başlangıcı 
.
.<deyim> ler ' fonksiyon kodu 
.
Name_Func:=Return_Value ' geri dönüş değeri 
EndFunction
```

Anadil® 'de geliştirilmekte olan uygulamalar fonksiyonlar dahilinde yazılmaktadır. En basit biçimde kod yazılması bile fonksiyonlar dahilinde gerçekleştirilmektedir.

Bir fonksiyon ise Function deyimi ardından gelen isim ile adlandırılmaktadır. İsmin ardından verilen parantezler arasında ise parametreler belirlenmektedir. Parantez kapatıldıktan sonra istenilirse geri dönüş değeri belirlenebilmektedir. Geri dönüş değeri ise "As \<VarType>" ifadesi ile belirlenmektedir. Fonksiyon isimlendirilmesi ve parametreler de belirlendikten sonra alt satırdan itibaren fonksiyon kodu başlamaktadır.

Geri dönüş değeri ise aynen değişken kullanımında olduğu gibi fonksiyon ismine karşılık gelen basit bir atama ile gerçekleştirilmektedir. Geri dönüş değerinin fonksiyon ismi ile aynı satırda yer almasına dikkat edilmelidir. Aksi durumda Anadil® compile hatası verecektir. Birbirini izleyen satırları tek satır şeklinde kullanabilmek için satır devam etme sembolü olan "#" işaretinden yararlanılabilir.

Fonksiyon kodu bittikten sonra "EndFunction" ile sonlandırma işlemi gerçekleştirilmektedir. Sonlandırılması yapılmamış bir fonksiyonun, Anadil ile compile edilmesi mümkün olmadığından, işletilmesi de imkansızdır.

Herhangi bir fonksiyondan istenildiği an ayrılınması ise Return yardımcı kelimesi ile mümkün olabilmektedir.

Anadil® 'de bütün fonksiyonlar yukardan aşağıya doğru, yazıldığı sırada işletilmektedir. Fakat event fonksiyonları için bu durum böyle değildir. Event'ler oluştuğu anda işletildiğinden, yazım sıraları önemli değildir.\
\
**Örnek**

```
Function RGB(Red As Number, Green As Number,#
         Blue As Number) As Number
  If ( Red < 0 VEYA Green < 0 VEYA Blue < 0 ) Then
    RGB:=0
    Return
  EndIf
  RGB:=Red + (Green * 16) + (Blue * 16 * 16)
EndFunction
```
