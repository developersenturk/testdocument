# SetRowBkColor

Bu property ilgili row un backround rengini set eder. Öndeğer olarak BEYAZ renk geçerlidir.\
\
**Uygulandığı Nesneler**\
Grid row nesnesi\
\
**Uygulama Biçimi**\
Grid reset edildikten sonra veya run-time sırasında herhangi bir row un arka fon rengi değiştirilebilir.\
Kullanımı

```
GridObject.SetRowBkColor(
  RowNum As Number  ' İlgili row sıra nosu
  ColorValue As Number  ' Row backround renk değeri
)
```

**Parametreler**\
_RowNum_\
Hangi satırın fon renginin değiştirileceğini belirler.\
_ColorValue_\
İlgili row un set edilecek arka fon renk değeridir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri Bool tipindedir.\
\
**Örnek**:

```
	Form.Fis.SetRowBkColor(RowNum, Rgb(0,0,255))
	Form.Fis.SetRowBkColor(RowNum, LIGHT_YELLOW)
	Form.Fis.SetRowBkColor(RowNum, LIGHT_GREY)
```

```
	Renk Sabitleri


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
