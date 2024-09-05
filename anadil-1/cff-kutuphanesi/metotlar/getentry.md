# GetEntry

Bu metod bir entry içeriğini bize sağlamaktadır.\
\
**Kullanımı**

```
CFFObject.GetEntry() As <Variant>
```

**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri variant olarakdan current entry göstericisinin bize sağladığı entry içeriğidir.\
\
**Dikkat Edilecek Hususlar**\
Bir entry ifadenin içeriğini bu metod ile alırken, daha önceden current entry göstericisinin değerinin uygun bir şekilde ayarlanmış olması gerekmektedir. Bu yüzden de bu metod genellikle FindEntry metodu ile etkileşimli olarak kullanılmaktadır.\
\
Current entry göstericisinin değerinin doğru olmasından önce, current satır gösterici değerinin de doğru olarak daha önceden ayarlanmış olması gerekmektedir. Tabi ki bu işlem daha çok FindEntry metodunun uygulanması ile ilgilidir.\
\
Geri dönüş değerinin variant olması bilginin içeriğinin önemli olmadığını; string, number veya date olabileceğini ve hatta bu değişkenin NULL bile olabileceğini göstermektedir.
