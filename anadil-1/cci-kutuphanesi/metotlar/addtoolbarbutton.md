# AddToolbarButton

Bu metod bir toolbar üzerindeki button'ları eklenmesini sağlamaktadır.\
**Kullanımı**

```
CCIObject.AddToolbarButton(
  ToolbarName As String  ' toolbar ismi
  ImageNo As Number      ' bitmap resim index numarası
  CmdNum As Number       ' button referans numarası
)
```

**Parametreler**\
_ToolbarName_\
Daha önceden belirlenmiş olan toolbar ismidir.\
_ImageNo_\
Bitmap resim içersindeki button'a karşılık gelen resim numarasıdır.\
_ButtonCmd_\
Button için verilen referans numarasıdır. Butona ilişkin daha sonraki metod uygulamalarında kullanılacaktır.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Hususlar**\
Toolbar button'larından daha önceden bahsederken, her button'un üzerindeki resmin aslında birer bitmap resmi olduğunu daha önceden belirtmiştik. Imagine® altında geliştirilen uygulamalarda, button resimleri meydana getirilirken grup halinde düşünülmektedir; yani bütün toolbar button'ları tek bir resim olarak ele alınmaktadır.\
\
Her button resmi de 16\*16 pixel olduğundan, oluşturma esnasında yüksekliği 16 olan genişliği ise 16'nın katları olabilen bir bitmap resmi gerekmektedir.\
\
İstenilen bitmap resim numarası bu grup halinde yer alan tek resimden index numarası verilmek suretiyle belirlenmektedir. Indexleme numarası ise 0(sıfır) dan itibaren başlamaktadır.
