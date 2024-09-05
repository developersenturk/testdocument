# PrepareStmDirect

Bu fonksiyon ile ExecuteStmDirect() fonksiyonun kullanımı sırasında ortaya çıkan 256 karakter limiti sorunu aşılmaktadır.\
\
**Kullanımı**

```
Function PrepareStmDirect(
  Statement As String  ' SQL ifade
)As RSObject
```

Parametreler\
_Statement_\
Doğrudan uygulanacak olan SQL ifade.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri uygulanılmak istenilen SQL ifadeye karşılık gelen RS nesnesidir.\
\
**Dikkat Edilecek Hususlar**\
Fonksiyon kullanımı ile ortaya konulmakta olan herhangi bir SQL ifadenin doğrudan SQL Server üzerinde işletimine dair yol açılmasıdır. Bu işlem uygulanılırken SQL ifadenin ExecuteStmDirect() fonksiyonu kullanımında olduğu gibi 256 karakter limiti bulunmamaktadır.\
\
Aslında burada String olarak verilebilecek olan değer 256 karakteri aşamaz fakat bu fonksiyonun bize sağladığı RS nesnesinin sahip olduğu .AppendToStm() metodu ile 256 karakterlik başka string ifadeler eklenebilmektedir. Bunun sonucunda istediğimiz uzunluktaki SQL statement ifadeyi oluşturmakta ve kullanabilmekteyiz.\
\
Bu fonksiyonlar sonucunda ortaya konulmakta olan RS nesnesinin SQL Server üzerinde işletimi sırasında .CompileStm() metodu ile derlenmesine gerek kalmamaktadır. Çünkü ifade otomatik olarak Anadil® tarafından Compile edilmektedir. RS nesnesi, SQL ifadenin oluşturulmasından sonra .ExecuteStm() metodu ile işletilecek ve gerekli sonuç alınabilecektir.\
\
Uygulama alanı olarak bu fonksiyon daha çok uzun ifadelerden oluşan SQL stament'lar için mesela script'ler gibi; kullanılabilmektedir.\
