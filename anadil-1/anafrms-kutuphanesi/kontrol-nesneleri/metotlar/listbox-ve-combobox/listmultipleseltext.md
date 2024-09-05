# ListMultipleSelText

Bu metod ile list-box listesinden seçilmiş olan bir veya birden fazla seçenek (ListBox Multiple Selection), CFF object olarak elde edilir. CFF yapısı : count, i1(sira no),s1(text1),i2,s2,...\
\
Uygulandığı Nesneler\
List-Box kontrolleri.\
\
**Kullanımı**

```
CFFObject := ControlObject.ListMultipleSelText ( )
```

**Geri Dönüş Değeri**\
Geri dönüş değeri OBJECT tir. Seçim listesini içeren CFF objectin formatı aşağıda örnek bölümünde verilmiştir.\
**Dikkat Edilecek Noktalar**\
CFFObject.count : seçim sayısını belirtir. CFFObject.i1 : ilk seçimin ListBox daki sıra nosudur. CFFObject.s1 : ilk seçimin ListBox daki ifadesidir. CFFObject.i2 : ikinci seçimin ListBox daki sıra nosudur...\
\
**Örnek Kullanım**

```
Dim LB_Selected As Object 'CFF
LB_Selected:=f.Ayarlist.ListMultipleSelText()
'
'Asagida LB_Selected adı ile tanımlanmış olan CFF in içeriği örnek olması açısından verilmiştir:
'Ayarlist adlı ListBox üzerinde, kullanıcı iki satır seçim yapmıştır. (Count : 2)
'İlk seçim 3. sıra (i1:3) ve ilk seçeneğin ifadesi "Vade Tanımları" dır.
'İkinci seçim 5. sıra (i2:5) ve bu seçeneğin ifadesi de "Durum Tanımları" dır.
CFF: LB_Selected Entries ------- count : 2.000000 i1 : 3.000000 s1 :
Vade Tanımları i2 : 5.000000 s3 : Durum Tanımları
```
