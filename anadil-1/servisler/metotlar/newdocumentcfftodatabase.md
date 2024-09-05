# NewDocumentCffToDatabase

NewDocumentCffToDatabase Methodu, Always executable'larına ait yeni bir döküman yaratır, verilen CFF i dökümana verir ve dökümanın CFFToDatabase fonksiyonunun çalışmasını sağlar, dökümanı kapatır. Veri girişi sonrasında başarıyla saklanan belgelerin CFF lerinin uzak/merkezi veritabanlarında tekrar saklanmasına gereksinim duyulduğunda kullanılabilir.\
\
**Kullanımı**

```
AlwaysCallObject.NewDocumentCffToDatabase(
  DocName As String   ' Döküman adı
  CFF             As Object  ' Döküman a verilecek CFF
) As Bool
```

**Parametreler**\
_DocName_\
Yaratılacak dökümanın adı\
_CFF_\
Merkezi veritabanında ilgili modülün CFFToDatabase fonksiyonu tarafından kullanılacak olan CFF parametresidir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
NewDocumentCffToDatabase Methodu, Always executable'larına ait yeni bir döküman yaratır. Verilen CFF i ilgili modülün CFFToDatabase fonksiyonuna iletir. Saklama sonrasında dökümanı kapatır. Yerel sistemde başarıyla saklanan dökümanın uzak veritabanında da başarıyla saklanabilmesi için, CFFToDatabase bölümlerinin global değişkenlere bağlı işlem yapmaması veya CFF te bulunan bilgi dışındaki hiç bir bilgiye göre işleyişini değiştirmemesi gerekir.\
\
**Örnek**

```
    DocCff[i]:=CFFCreateFromStringRows(pCff[i])

    alwrun:=GetAlwaysCallObject()
    alwrun.NewDocumentCffToDatabase("chardoc", DocCff[i])

```
