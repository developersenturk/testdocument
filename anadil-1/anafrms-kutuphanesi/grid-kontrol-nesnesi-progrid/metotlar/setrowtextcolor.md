# SetRowTextColor

Bu property ilgili row un text rengini set eder. Öndeğer olarak SIYAH renk geçerlidir.\
\
**Uygulandığı Nesneler**\
Grid row nesnesi\
\
**Uygulama Biçimi**\
Grid reset edildikten sonra veya run-time sırasında herhangi bir row un text rengi değiştirilebilir.\
Kullanımı

```
GridObject.SetRowTextColor(
  RowNum As Number  ' İlgili row sıra nosu
  ColorValue As Number  ' Row backround renk değeri
)
```

**Parametreler**\
_RowNum_\
Hangi satırın text renginin değiştirileceğini belirler.\
_ColorValue_\
İlgili row un set edilecek text renk değeridir.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri Bool tipindedir.\
\
**Örnek:**

<pre><code><strong>	Form.Fis.SetRowTextColor(RowNum, Rgb(0,255,255))
</strong>	Form.Fis.SetRowTextColor(RowNum, DARK_YELLOW)
	Form.Fis.SetRowTextColor(RowNum, DARK_GREY)
</code></pre>

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
