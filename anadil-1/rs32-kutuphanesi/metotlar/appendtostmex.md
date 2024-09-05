# AppendToStmEx

Bu metod PrepareStmDirect() fonksiyonu ile oluşturulmakta olan başlangıç SQL statement ifadeye, araya boşluk eklemeden, yeni SQL statement parçalar eklenmesini sağlamaktadır.\
\
**Kullanımı**

```
RSObject.AppendToStmEx(
  Ekİfade As String	' SQL statement parçası
)
```

**Parametreler**\
_Ekİfade_\
256 karakteri geçmemekte olan SQL statement parçası.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
SQL Server üzerinde zaman zaman 256 karakteri geçebilmekte olan SQL dilindeki ifadelerin işletimi gerekmektedir. Bu tür durumlarda PrepareStmDirect() ile başlangıç olarak bir RS nesnesi oluşturulabilmektedir. Fakat .AppendToStmEx() sadece 256 karakterlik SQL ifadeye izin vermektedir. Bu durumda uzun olan statement ifade 256 karakteri geçmeyen ayrı ayrı parçalara ayrılıp bu metod ile ilgili RS nesnesine eklenebilir.\
AppendToStmEx() methodu verilen string ifadeyi, başına boşluk koymadan, ekler.\
Metodun kullanımında sayı olarak limit bulunmamaktadır. Her kullanım sırasında ortaya çıkan toplam SQL ifade, Anadil® tarafından otomatik olarak Compile edilecek, sonuçta geliştirici en son statement parçasını ekledikten sonra RS nesnesi üzerinde sadece .ExecuteStm() metodunu uygulayarak SQL işletimini gerçekleştirecektir.
