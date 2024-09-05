# BackColor

Bu property grid arka fonun rengini get ve set eder. Öndeğer olarak BEYAZ renk geçerlidir. Mevcut Projeler de sorun oluşmamı için SetBkColor halen set edilmek için kullanılmaktadır.\
\
**Uygulandığı Nesneler**\
Grid kontrol nesnesi\
\
**Uygulama Biçimi**\
Grid reset edildikten sonra veya run-time sırasında istenilen renk belirlenebilir.\
\
**Kullanımı**

```
GridObject.BackColor As Number

 Örnek:
	  Form.Fis.BackColor:=RGB(128,128,128)
	  Form.Fis.BackColor:=LIGHT_YELLOW
	  Form.Fis.BackColor:=DARK_AQUA
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
