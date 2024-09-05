# Read Methodu

Bu method Text dosyadan satır okur. Satır uzunluğu 255 i aşıyorsa, örnekte verildiği gibi XML nesnesi kullanmalısınız.\
\
Kullanımı

```
  FileObject.Read() As String veya XML Object


Örnek


Dim szLine As String
Dim FileObject As Object

FileObject:=OpenTextFile("c:\Always\readme.txt") 

'Burada normal 255 sınırına kadar okuma yapılıyor
szLine:=FileObject.Read()
OUTM(szLine)


'Asagidaki örnek 255 karakterden uzun satırların okunmasını göstermektedir.
Dim szLineXML As Object
Dim FileObject As Object

FileObject:=OpenTextFile("c:\Always\test.txt") 

'Bu satırda okunan satır, szLineXML büyük string nesnesine yazılmaktadır.
szLineXML:=FileObject.Read()

szLineXML.Dump("c:\Always\test1.txt", 0)

```

\
Geri Dönüş Değeri\
Geri dönüş değeri String veya XML nesnesidir.\
