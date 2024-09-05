# TitleColor

Bu property tüm grid kolonlarının başlık renklerinin değiştirilebilmesini sağlar. Öndeğer olarak SİYAH renk geçerlidir.\
\
**Uygulandığı Nesneler**\
Grid nesnesi\
\
**Uygulama Biçimi**\
Grid reset edildikten sonra veya run-time sırasında tüm kolonların başlıkları için tek renk belirlenebilir.\
\
**Kullanımı**

```
GridObject.TitleColor As Number

 Örnek:
	  Form.Fis.TitleColor:=RGB(40,50,40)
	  Form.Fis.TitleColor:=DARK_BLUE
	  Form.Fis.TitleColor:=DARK_GREEN
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
