# RollbackTrans

Bu fonksiyon oluşturulan bir statement'ın işlemi bitmeden geri döndürülmesini sağlar.\
\
**Kullanımı**

```
Function RollbackTrans() As Bool
```

**Parametreler**\
Fonksiyonun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemli değildir.\
\
**Dikkat Edilecek Hususlar**\
Bu fonksiyon ile yapılan işlem, yazılan bir SQL statement'in transaction'ının bitmeden geri döndürülmesini sağlar.
