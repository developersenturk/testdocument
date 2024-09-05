# TitleColor

Bu property color property ile aynı işleve sahip yeni bir property dir. İlgili grid kolonunun başlık rengini set eder. Öndeğer olarak SİYAH renk geçerlidir.\
\
**Uygulandığı Nesneler**\
Grid kolon nesnesi\
\
**Uygulama Biçimi**\
Grid reset edildikten sonra veya run-time sırasında herhangi bir kolonun başlık rengi değiştirilebilir.\
\
**Kullanımı**

```
GridColObject.TitleColor As Number

 Örnek:
	Form.Fis.tl_borc.TitleColor:=Rgb(0,0,255)
	Form.Fis.aciklama.TitleColor:=LIGHT_BLUE
	Form.Fis.malzemekodu.TitleColor:=DARK_RED
	' Okubabilir bir özelliğe de sahiptir.
```

\
**Renk Sabitleri**\


```
			RGB 		        Sabit	
                 RGB(255, 255, 255)             WHITE
                 RGB(192, 192, 192)             LIGHT_GREY
                 RGB(255,   0, 0)               LIGHT_RED
                 RGB(255, 255, 0)               LIGHT_YELLOW
                 RGB(  0, 255, 0)               LIGHT_GREEN
                 RGB(  0, 255, 255)             LIGHT_AQUA
                 RGB(  0,   0, 255)             LIGHT_BLUE
                 RGB(255,   0, 255)             LIGHT_PURPLE
                 RGB(  0,   0, 0)               BLACK
                 RGB(128, 128, 128)             DARK_GREY
                 RGB(128,   0, 0)               DARK_RED
                 RGB(128, 128, 0)               DARK_YELLOW
                 RGB(  0, 128, 0)               DARK_GREEN
                 RGB(  0, 128, 128)             DARK_AQUA
                 RGB(  0,   0, 128)             DARK_BLUE
                 RGB(128,   0, 128)             DARK_PURPLE

```
