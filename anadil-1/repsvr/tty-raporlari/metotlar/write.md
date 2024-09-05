# Write

Rapor sayfasına yazdırma işlemini yapar.\
\
**Kullanımı**

```
ReportObject.Write(
  text  As String          ' Yazdırılacak text
  TextLenght  As Number    ' Yazdırılacak textin column sayısı
  AlignmentType As Number  ' Yaslama biçimi
) As Bool
```

**Parametreler**\
_Text_\
Raporda yazdırılmak istenen text\
\
_TextLenght_\
Yazdırılacak textin maximum column sayısı\
\
_AlignmentType_\
Yaslama biçimi\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
Write Methodu, rapor sayfasına yazdırma işlemini yapar.\
Write methodunun 3 parametresi vardır. Ancak parametrelerden, TextLength ve Alignmenttype opsiyoneldir.\
2\. parametre yazdırılan texte ayrılan column sayısıdır. Eğer bu parametreye bir değer verilmezse, textin uzunluğu kadar column kullanacaktır.\
3\. parametre, yazının sağa yaslanmasını sağlar. Eğer yazıya alignment verilmemişse yaslama şekli, default olarak TTYALIGN\_LEFT olacak yani sola yaslanacaktır.\
\
**Örnek**

```
Dim r As Report
  r.Write("Bu bir denemedir",10,TTYALIGN_RIGHT)
```

Yukarıdaki örnekte "Bu bir denemedir" texti 10 karakterlik bir column de yer alacaktır. Bu nedenle de raporda "Bu bir denem" şeklinde görülecektir.
