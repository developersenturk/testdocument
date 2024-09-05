# HtmlHelp

Bu fonksiyon verile HTML yardim dosyasini acar. ShellExecute fonksiyonu ile de yardim dosyalari acilabilir. Ancak bu fonksiyon daha cok (etkilesimli egitim) TrainingCard uygulamalari yapabilmek icin konulmustur. Ilgili TrainingCard yardim dosyasina eklenmis event tuşlarına basıldığında, Anadil uygulamasının bunu algılayabilmesi gerekmektedir. Anadil programlarinda TrainingCard form eventi tetiklenmekte ve ilgili tuşa ait numara bu event e verilmektedir.\
\
Kullanımı

```
Function HtmlHelp(
lpFile		As String   'Yardim dosyasi
) As Number
```

\
Parametreler\
_lpFile_ :\
Yardim dosyasinin adi.\


Geri Dönüş Değeri\


```
Geri dönüş değeri, işlem başarılı ise açılan help programının window handle numarasıdır.

```

\
\
Örnek

```
Dim nHwnd as number

nHwnd:=HtmlHelp("c:\Always\imagine.chm")

```
