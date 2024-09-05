# CreateBLO

Bu fonksiyon Binary Link Object yaratır.

**Kullanımı**

```
Function CreateBLO() As Object
```

**Parametreler**\
Fonksiyonun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, BLO nesnesidir.\
\
**Dikkat Edilecek Konular**\
Database'de saklanan bir nesnenin, Imagine'dan kullanılabilmesi için yaratılması gereken Binary Link Object nesnesidir.

```
Dim stm As Object
Dim myblo As Object
  stm:=PrepareStmDirect("Select FieldName from Table where KeyField=?")
  stm.SetParam(KeyValue)
  stm.ExecuteStm()
  If stm.MoveNext() Then
    myblo:=CreateBlo()
    myblo.Load(stm, FieldName)
  EndIf
```
