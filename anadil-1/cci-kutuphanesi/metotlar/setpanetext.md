# SetPaneText

Bu metod pane üzerinde bilgi yazılabilmesini sağlamaktadır.\
\
**Kullanımı**

```
CCIObject.SetPaneText(
  PaneName As String  ' pane ismi
  PaneText As String  ' pane üzerine yazılacak bilgi
)
```

**Parametreler**\
_PaneName_\
Üzerine bilgi yazılacak olan pane için önceden verilmiş olan referans ismi.\
_PaneText_\
Pane üzerinde yazılacak bilgi.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Pane sisteminde bilgi yazılması işleminde, pane uzunluğunun sınırlı olmasından dolayı kısa ve öz bilgilerin yazılması gerekmektedir. Ayrıca çok fazla pane sayısı, ve karmaşık düzenleme, genel pane anlaşılırlığının kaybolmasına neden olabilir.\
\
Ayrıca verilmek istenilen bilgi ile ilgili kullanılacak açıklama niteliğinde kısaltmalar verilen bilgiyi daha anlaşılır kılabilir.
