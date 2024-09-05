# TextBkColor

Bu property kontrol nesnelerinde yer alacak text, number ve date değerlerinin arka fonunun hangi renkte yazılacağını belirler. Sadece yazılabilir bir özelliktir.\
\
**Uygulandığı Nesneler**\
Form kontrol nesnesi\
\
**Kullanımı**

```
Control.TextBkColor As Number

 Örnek:
	  Form.Baslik.TextBkColor:=LIGHT_PURPLE
	  Form.Aciklama.TextBkColor:=DARK_BLUE
	  Form.Label.TextBkColor:=DARK_GREEN
```

**Renk Sabitleri**

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
