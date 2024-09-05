# CloseEnumExecs

CloseEnumExecs Methodu, executable numarası verilen excutable'ı kapatır\
\
**Kullanımı**

```
AlwaysCallObject.CloseEnumExecs(
  EnumID As Number  ' Executable Id no	
) As Bool
```

**Parametreler**\
_EnumID_\
Kapatılmak istenen Executable'ın Id numarasıdır.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
CloseEnumExecs Methodu, executable numarası verilen excutable'ı kapatır\
\
**Örnek**

```
Dim alw As Object
Dim enum As Number
  alw:=GetAlwaysCallObject()
  enum:=alw.OpenEnumExecs(2)  'services
  alw.CloseEnumExecs(enum)
```
