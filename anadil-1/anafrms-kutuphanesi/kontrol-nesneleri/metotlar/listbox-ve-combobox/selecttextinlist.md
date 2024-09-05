# SelectTextInList

Bu metod ile list-box kontrolünün içeriğinden birinin seçilebilmesi sağlanmaktadır.\
\
**Uygulandığı Nesneler**\
Combo-Box ve List-Box kontrolleri.\
\
**Kullanımı**

```
ControlObject.SelectTextInList( 
  Text As String  ' listeden seçilecek ifade
)
```

**Parametreler**\
_Text_\
Control içersinden seçilmek istenilen ifade.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
**Dikkat Edilecek Noktalar**\
Listeden yapılan seçimlerde, içersindeki çoklu seçim alternatiflerinden Anadil® kodu yardımıyla seçim yapabilmemizi sağlamaktadır. Parametre olarak verdiğimiz ifade seçilecek olan ifadedir. Seçilen ifadeden başka bir ifadenin seçilmesi durumunda, combo kontrolün, other styles SORT özelliğini seçmelisiniz\
\
Ayrıca list box seçim işleminde combo-box seçimlerinde kullanılan index numarasına dayalı metod da kullanılabilmektedir. (SelectItemInList)
