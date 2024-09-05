# ReturnToRoot

Bu metod bütün satırların da üstünde yer almakta olan en üst seviyeye gitmektedir.\
\
**Kullanımı**

```
CFFObject.ReturnToRoot()
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
İsminden de anlaşıldığı gibi bu metod current(aktif) satır bilgisinin değerini mevcut satırların en üstünde yer alan, o anki CFF nesnesinin kök satırına değiştirmektedir.\
\
Current(aktif) satır gösterici bilgisini root değere eşitlemek hiçbir zaman, eğer root dahilinde entry kaydı yapılmışsa, current entry göstericisi değerini ilk entry'yi işaret edecek şeklinde, garanti etmemektedir. Bu yüzden current entry gösterici değerini, ilk entry'yi işaret edecek şekilde düzenleme yapmak en sağlıklı olanıdır.
