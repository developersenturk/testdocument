# SetFont

Bu metod herhangi bir kontrolun fontunu değiştirir.\
\
**Kullanımı**

```
Control.SetFont(Font as String, Size as Number, Style as Number)
```

\
**Parametreler**\
_Font_\
Fontun adı\
_Size_\
Fontun büyüklüğü\
_Style_\
Fontun stili\
\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Font Stilleri**\
Font stili olarak BOLD, UNDERLINE ve ITALIC sabitlerinin kombinasyonlarını kullanabilirsiniz. Eğer özel bir stil istemiyorsanız font stilini 0 veriniz.\
\
**Örnek**

```
f.ctrl.SetFont("Courier New", 10, BOLD + ITALIC)
```
