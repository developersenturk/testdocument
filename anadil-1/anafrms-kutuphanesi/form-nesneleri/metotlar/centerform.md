# CenterForm

Bu metod herhangi bir formun Always terminalinde merkezi bir şekilde görünümünü sağlamaktadır.\
\
**Kullanımı**

```
FormObject.CenterForm()
```

\
**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**

Bu metod yardımıyla da oluşturulmuş olan herhangi bir formun Always terminali dahilinde merkezi bir şekilde yerleştirilmesi sağlanabilmektedir. Form istenilen her zaman bu metod yardımıyla merkezileştirilebilir.

Merkezleme kriteri ise Always terminalinin en ortasına gelecek şekilde formun yerleştirilmesidir. Merkezleme Windows'un o anda kullanıldığı ekran çözünürlüğünden bağımsız olarak gerçekleştirilmektedir. Bu metodun kullanılması için en uygun yer myform\_Open event'i olabilir.
