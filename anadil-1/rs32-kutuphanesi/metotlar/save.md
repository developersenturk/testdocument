# Save

Bu method Database Binary Link Object datasını, database'e kaydeder.

Kullanımı

```
BLOObject.Save(
  RsObject,  ' SQL statement
  FieldName  ' Column adı
) As Bool
```

**Parametreler**\
_RsObject_\
SQL statement\
_FieldName_\
Column adı\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, booleandır.\
\
**Dikkat Edilecek Konular**\
Bu method Database Binary Link Object datasını, database'e kaydeder.

```
Dim stm As Object
Dim myblo As Object
  stm:=PrepareStmDirect("set textsize insert into TableName(FieldName, FieldName) 
                Values (?, ?)")
  myblo.Save(stm, FieldValue)
  stm.SetParam(FieldValue)
  stm.ExecuteStm()
  stm.Close()
  myblo.Close()
```
