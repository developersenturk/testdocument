# IsChecked

Bu property uygulandığı işaretleme tabanlı olarak uygulanan kontrol nesnelerinde, kullanıcının yaptığı seçimlerle ilgili düzenlemeleri kontrol etmektedir.\
\
**Uygulandığı Nesneler**\
Radio Button ve Check-Box kontrol nesneleri.\
\
**Uygulama Biçimi**\
Hem okunabilir hem de yazılabilir bir property'dir.\
\
**Kullanımı**

```
ControlObject.IsChecked As Bool
```

\
**Dikkat Edilecek Noktalar**\
Burada söz konusu olan kontrol nesneleri yani Radio Button ve Check Box için bu property mutlaka bir öndeğere sahip olmaktadır. Yani hangi form olursa olsun mutlaka eğer üzerinde bu kontrollerden biri varsa onun .IsChecked property'si bir değere sahip olacaktır.\
\
Bunun sonucunda söz konusu bu kontroller ile kullanıcının NULL bir input yapmasını, geliştirici hiçbir zaman bekleyemez.\
\
Geliştirici isterse bu property üzerinde True şeklinde bir atama ile Anadil® kodu yardımıyla seçim işlemi de uygulayabilmektedir.\
\
**Örnek**\
Aşağıdaki örnekte, form üzerinde bulunan Secim1 ve Secim2 radio button kontrollerinden ilki TRUE, ikincisi FALSE olarak işaretleniyor

```
Function kriter_Open(Form As Object) As Bool
  form.centerform()
  form.edtnumber.Format := "m;2"
  form.Secim1.IsChecked := True
  form.Secim2.IsChecked := False
  kriter_Mesut_Click(form)
  GridInit(form)
  bcancelled:=True
  kriter_Open:=TRUE
EndFunction

```
