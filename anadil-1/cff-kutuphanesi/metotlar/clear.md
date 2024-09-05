# Clear

Bu metod bir CFF nesnesinin içeriğini temizlemek ve yeniden yaratmadan tekrar tekrar kullanabilmek için yazılmıştır. Tüm entryler, alt cff ler ve row lar yok edilir ve cff ilk yaratıldığı noktadaki gibi kullanıma girer. Aynı fonksiyon içerisinde tekrar tekrar temizlenip kullanılması için kullanılabilir.\
\
**Kullanımı**

```
CFFObject.Clear()
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Örnek Kullanım**

```
 Dim c1 As Object
 Dim s1 As Object
 Dim c2 As Object
 Dim s2 As Object

 c1:=CFFCreate("c1")
 c2:=CFFCreate("c2")

 c1.add("e1", 1) 
 c1.add("e2", 2) 

 s1:=c1.Create("s1")
 s1.add("e3", 3) 
 s1.add("e4", 4) 

 s1.addrow() 
 s1.add("e5", 5) 
 s1.add("e6", 6) 

 c1.addrow() 
 c1.add("e7", 7) 
 c1.add("e8", 8) 


 c1.DumpCff()

'c2
 c2.add("f1", 1) 
 c2.add("f2", 2) 

 s2:=c2.Create("s1")
 s2.add("f3", 3) 
 s2.add("f4", 4) 

 s2.addrow() 
 s2.add("f5", 5) 
 s2.add("f6", 6) 

 c2.addrow() 
 c2.add("f7", 7) 
 c2.add("f8", 8) 

'c1 cff inin içi temizleniyor
 c1.Clear()

 c1.DumpCff()

'c2 den c1 e kopyalama yapılıyor
 CFFCopy(c1, c2) 

 c1.DumpCff()
```

**İlgili Konular:** [**cffcopy**](../fonksiyonlar/cffcopy.md)
