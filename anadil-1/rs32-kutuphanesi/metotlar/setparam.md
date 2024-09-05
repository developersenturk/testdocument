# SetParam

Bu metod SQL statement'a parametre göndermeye yarar.\
**Kullanımı**

```
RSObject.SetParam(
  Value  'SQL statement'a gönderilen parametre değeri
)As Bool
```

**Parametreler**\
_Value_\
SQL statement'a gönderilen parametre değeri\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, yapılan query işleminin gerçekleşmesi durumunda True, işletimin başarısız olması durumda ise içeriği False olan Bool değerdir.\
\
**Dikkat Edilecek Konular**\
PrepareStmDirect ile yazılan bir SQL statement'a parametre gönderme işlemini yapar.

```
Dim Rs As Object
  Rs:= PrepareStmDirect("Select Field  From Table Where KeyField = ? ")
  Rs.SetParam(KeyValue)
  Rs.ExecuteStm()
```
