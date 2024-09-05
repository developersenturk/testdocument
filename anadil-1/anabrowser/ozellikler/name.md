# Name

Bu property Tarayıcı Kolon Adını ifade etmektedir.\
\
**Kullanımı**

```
ColDefObject.<Name> As <String>
```

**Uygulandığı Nesneler**\
Bu özellik Tarayıcı Kolon nesnelerinde uygulanmaktadır.\
\
**Property Tipi**\
WriteOnly yani salt yazılabilir bir özelliktir.\
\
**Property Değeri**\
String değer içermelidir..\
\
**İlişkili başlıklar:**\
[AddTitleEx](../metotlar/addtitleex.md)\
[CreateColDef](../fonksiyonlar/createcoldef.md)\
\
**Örnek**

```
    Dim cd As Object

    cd:=CreateColDef()
    cd.Name:="Malzeme Kodu"
```
