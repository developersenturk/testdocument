# VarComp

Bu fonksiyon iki Anadil değişkeninin, veri tiplerini dikkate alarak, eşit olup olmadığını kontrol etmektedir. Verilen değişkenlerin veri tipleri aynı olmalıdır. Eşitlikleri kontrol edilecek değişkenlerin veri tiplerinin bilinmediği durumlarda kullanılabilir.\
\
**Kullanımı**

```
Function VarComp(
  Var1 As Variant  ' Kontrol edilecek ilk variant
  Var2 As Variant  ' Kontrol edilecek ikinci variant
)As Number
```

**Parametreler**\
_Var1_\
Eşit olup olmadığı kontrol edilecek değişkendir. String, Number veya Date olabilmektedir.\
_Var2_\
Eşit olup olmadığı kontrol edilecek ikinci değişkendir. String, Number veya Date olabilmektedir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri Number olup eğer değişkenler eşit ise 0, Var1\<Var2 ise (-1), Var1>Var2 ise (1) geri dönmektedir. Farklı veri tiplerine sahip değişkenler verildiğinde veya herhangi biri null olduğunda geri dönen değer 256 dır.\
\
**Dikkat Edilecek Hususlar**\
Boolean veri tipleri kabul edilmez.\
\
**Örnek**

```
Function form_CffTest_Click()
  Dim ret As Number

  Dim d1 As Date
  Dim d2 As Date

  'Dim d1 As String
  'Dim d2 As String

  'Dim d1 As Number
  'Dim d2 As Number

  'Eşit
  d1:=Str2Date("5/7/2004")
  d2:=Str2Date("5/7/2004")

  'İlki Büyük
  'd1:="ABCDEF"
  'd2:="ABcDEF"

  'İlki Küçük
  'd1:=123
  'd2:=123456

  ret:=VarComp(d1, d2)

  If (ret=0) Then
    MessageBox("Değişkenler eşit", "EŞİT",      MB_OK)
  Else 
    if (ret=-1) Then
       MessageBox("Değişkenler eşit DEĞİL. İlk değişken ikinciden küçük", #
               "KÜÇÜK",  MB_OK+MB_ICONINFORMATION)
    Else   
       If (ret=1) Then
            MessageBox("Değişkenler eşit DEĞİL. İlk değişken ikinciden büyük", #
               "BÜYÜK",  MB_OK+MB_ICONINFORMATION)
       Else
          If (ret=256) Then
              MessageBox("Değişkenlerin tipleri aynı değil veya birisi NULL veya Bool verilmiş", #
               "UYUMSUZ", MB_OK+MB_ICONINFORMATION)
          EndIf
       EndIf
    EndIf
  EndIf
EndFunction
```

**Örnek Açıklaması**\
İlk örnekte iki eşit DATE değere sahip, Anadil variant karşılaştırılıyor. Sırasıyla komentleri ayarlayarak, string ve number tipleri karşılaştırabilirsiniz.
