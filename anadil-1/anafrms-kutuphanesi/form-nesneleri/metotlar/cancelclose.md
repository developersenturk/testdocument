# CancelClose

Bu metod herhangi bir formun Always® terminalinden kapatılmasını önlemektedir.\
\
**Kullanımı**

```
FormObject.CancelClose() 
```

\
**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**

Bu metod sadece myform\_OnClose Event'i içersinde çalışabilmektedir. Bir formun kapatılması sizin iradeniz dışında, sahip olduğu sol üst köşesinde yer alan kontrol kutusundaki 'Close' seçeneği ile kapatılmaya çalışılırsa bu metod yoluyla Always® tarafından, tabi ki sizin yazacağınız program koduna bağlı olmak üzere, myform\_OnClose Event'i içersinde bazı ek işlemler veya kontroller yapabilir bu metod yardımıyla da formun kapatılmasına engel olabilirsiniz.

Herhangi bir formun kapatma işleminden önce Always® tarafından "close\_flag" kontrolü yapılmakta ve bu metod bu flag değerini etkilemek suretiyle kapatma işlemine engel olabilmektedir.
