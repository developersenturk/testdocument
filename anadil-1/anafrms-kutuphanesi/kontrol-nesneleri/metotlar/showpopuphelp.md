# ShowPopupHelp

Bu metod Anadil'den herhangi bir kontrole ait balon yardim gosterilmesini sağlar. Methodun string parametresi boş string olarak verildiğinde, ilgili kontrolün daha önce kaydedilmiş balonyardim metni ekrana gelir. Methodun parametresi boşluk değilse, verilen string parametre balon yardim metni olarak gösterilir.\
\
**Uygulandığı Nesneler**\
Bütün kontrol nesneleri.\
\
**Kullanımı**

```
ControlObject.ShowPopupHelp(  Text  ' Gösterilecek balon yardım metni)
ControlObject.ShowPopupHelp("Örnek balon yardım metni")  
ControlObject.ShowPopupHelp("")  'ControlObject için varsa daha önce girilmiş balon yardım gösterilir.
 
```

\
**Parametreler**\
Text : Metodun parametresi boş string veya dolu help stringtir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Anadil programından ardarda farklı alanlar için method çağırıldığında, balon yardımlar aynı anda ekrana gelmez. İlk ekrana gelen balon yardım formuna tıklandığında varsa sonraki balon yardım formu ekrana gelir.\
\
String parametre olarak verilen yardım metninin satır satır görünmesi için satır aralarına RETURN (chr 13) karakterinin yerleştirilmesi gerekmektedir.\
\
Örnek **Kullanım**:

```
Dim Msg As String
Msg:="Balon yardım birinci satır" & chr(13) & "Balon yardım ikinci satır" & chr(13) &
"Balon yardım üçüncü satır" & chr(13)& "Balon yardım dördüncü satır"

f.mut_no.ShowPopupHelp(Msg) ' Msg stringi balon yardım olarak gösterilir
f.aciklama.ShowPopupHelp("" ) ' f formundaki aciklama alanı için daha önce girilmiş yardım metni ekrana gelir.
```

<figure><img src="../../../../.gitbook/assets/Ekran görüntüsü 2024-09-03 222124.png" alt=""><figcaption></figcaption></figure>
