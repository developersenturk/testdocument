# TextColor

Bu property grid hücrelerinde yer alacak text, number ve date değerlerinin hangi renkte yazılacağını belirler. Öndeğer olarak SİYAH renk geçerlidir. Mevcut Projeler de sorun oluşmamı için SetTextColor halen set edilmek için kullanılmaktadır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi\
\
**Uygulama Biçimi**\
Grid reset edildikten sonra veya run-time sırasında istenilen renk belirlenebilir.\
\
**Kullanımı**

```
GridObject.SetTextColor As Number

 Örnek:
	  Form.Fis.TextColor:=RGB(40,50,40)
	  Form.Fis.TextColor:=DARK_BLUE
	  Form.Fis.TextColor:=DARK_GREEN
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
