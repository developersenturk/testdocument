# SetAttr

Bu metod SQL statement handle bazında attribute set edilmesini sağlar. Read Committed çalışan raporların ilgili tablo satırlarına LOCK koymaması isteniyorsa, bu method ile CURSOR tipinin STATIC veya SENSITIVITY nin INSENSITIVE set edilmesi gereklidir. Bu sayede TempDb kullanımı ile birbirini bekletmeyen, daha verimli bir çalışma ortamı sağlanır.

**Kullanımı**

```
RSObject.SetAttr(
  AttrTipi  'Attribute tipi
  AttrVal   'Attribute tip değeri
)As Bool
```

**Parametreler**\
_AttrTipi_\
Set edilmek istenen attribute tipi : örneğin SQL\_ATTR\_CURSOR\_SENSITIVITY\
\
_AttrVal_\
Set edilmek istenen attribute tipinin değeri : örneğin SQL\_INSENSITIVE\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri, yapılan işleminin gerçekleşmesi durumunda True, işletimin başarısız olması durumda ise içeriği False olan Bool değerdir.\
\
**Dikkat Edilecek Konular**\
Set etmek istediğiniz özelliği detaylı okuyup öğrenmelisiniz.

```
  Dim  rs as object
  
  rs:=PrepareStmDirect("Select * from wrk_hesap_plani ")

  'rs.AllowDirtyReads:=TRUE
  
  'Concurency
  'rs.SetAttr(SQL_ATTR_CONCURRENCY, SQL_CONCUR_READ_ONLY)  'Default
  'rs.SetAttr(SQL_ATTR_CONCURRENCY, SQL_CONCUR_LOCK)
  'rs.SetAttr(SQL_ATTR_CONCURRENCY, SQL_CONCUR_ROWVER)
  'rs.SetAttr(SQL_ATTR_CONCURRENCY, SQL_CONCUR_VALUES)

  'SQL_ATTR_CURSOR_TYPE
  'rs.SetAttr(SQL_ATTR_CURSOR_TYPE, SQL_CURSOR_STATIC)
  'rs.SetAttr(SQL_ATTR_CURSOR_TYPE, SQL_CURSOR_FORWARD_ONLY)
  'rs.SetAttr(SQL_ATTR_CURSOR_TYPE, SQL_CURSOR_KEYSET_DRIVEN)
  'rs.SetAttr(SQL_ATTR_CURSOR_TYPE, SQL_CURSOR_DYNAMIC)

  'SCROLL
  'rs.SetAttr(SQL_ATTR_CURSOR_SCROLLABLE, SQL_SCROLLABLE)
  
  'SQL_ATTR_CURSOR_SENSITIVITY
   rs.SetAttr(SQL_ATTR_CURSOR_SENSITIVITY, SQL_INSENSITIVE)
  'rs.SetAttr(SQL_ATTR_CURSOR_SENSITIVITY, SQL_SENSITIVE)
  'rs.SetAttr(SQL_ATTR_CURSOR_SENSITIVITY, SQL_UNSPECIFIED) 'Default
  
  if  Rs.ExecuteStm() Then
  
      while rs.movenext()
        outm("Bekliyor....")
        outm("Bekliyor....")
      wend
         
      rs.Close()
  Endif
```
