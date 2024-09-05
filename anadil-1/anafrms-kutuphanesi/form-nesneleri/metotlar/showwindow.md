# ShowWindow

Bu metod ilgili form uzerinde ShowWindow(hWnd, nCmdShow ) fonksiyonunu çalıştırır..

**Kullanımı**

```
FormObject.ShowWindow(
  nCmdShow 'SW Sabiti 
)
```

**Parametreler**\
_nCmdShow_

```
	Show Window komut sabitidir : 
		SW_HIDE			: Ilgili formu gorunmez yapar.
		SW_SHOW			: Ilgili formu gorunur yapar.
		SW_MAXIMIZE		: Formu maximize yapar.
		SW_MINIMIZE		: Formu minimize yapar.
		SW_RESTORE		: Formu bir onceki durumuna döndürür.
		SW_SHOWMAXIMIZED	: Maximize yapar ve aktifleştirir.
		SW_SHOWMINIMIZED	: Minimize yapar ve aktif window yapar.
 		SW_SHOWMINNOACTIVE	: Formu Minimize yapar ve aktif window aktif kalır.
		SW_SHOWNA		: Formu görünür yapar ve aktif window aktif kalır.
		SW_SHOWNOACTIVATE	: Formu görünür yapar ve aktif window aktif kalır.
		SW_FORCEMINIMIZE	: Cevap vermeyen bir başka thread e ait form
					  minimize edilebilir. (Win NT 5.0 ve sonrası için)
		WM_MDIMAXIMIZE		: Mdi formlari maximize yapar
		WM_MDIRESTORE		: Mdi formlari bir onceki durumuna döndürür

```

**Geri Dönüş Değeri**\
BOOLEAN : Geri dönüş değeri işlem başarılı ise TRUE değilse FALSE olur.\
Örnek

```
        f.ShowWindow( SW_HIDE)		' Form f gizlenir
        f.ShowWindow( SW_SHOW)		' Form f görünür hale gelir
        f.ShowWindow( SW_MAXIMIZE )	' Form f Maximize olur
        f.ShowWindow( SW_RESTORE)	' Form f bir önceki durumuna döner
        f.ShowWindow( SW_SHOWNOACTIVATE)' Form görünür hale gelirken mevcut aktif window yine aktif kalır
```

**Dikkat Edilecek Noktalar**

Örneğin maximize edilmiş form FormObject.Restore() methodu ile ilk durumuna dönebilir veya FormObject.Minimize() methodu ile minimize edilebilir. Bu methodların tamamı tabsheetlere veya embedded child formlara uygulanamazlar.

```
```

MDI Formlarda oluşan birden fazla sysmenu probleminin çözümü:

```
Mdi formların "Activate" eventi, WM_MDIACTIVATE window mesajı içinde tetiklenmektedir. 
Bu nedenle "Activate" eventi içinde ShowWindow (SW_MAXIMIZE) gibi komutlar MDI form için kullanılırsa, 
birden fazla sysmenu oluşabilir.  Bunun çözümü, WM_MDIMAXIMIZE sabitini kullanmaktır. 
Bu durumda Always SendMessage yerine PostMessage ile WM_MDIMAXIMIZE mesajını iletmektedir.
```
