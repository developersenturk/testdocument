# ShellExecute

Bu fonksiyon ilgili dosya üzerinde istenen işlemin yapılmasını sağlar. Örneğin verilen döküman Word ve komut Edit ise, dökümanın Word ile açılması sağlanır. Verilen doküman EXE ile ilgili program çalıştırılır. Verilen komut print ise doküman print edilir. Sistem ShellExecute fonksiyonunun Anadil'den kullanılabilmesi sağlanmıştır.\
\
Kullanımı

```
Function ShellExecute(
hWnd		As Number   'Baba pencere. NULL verebilirsiniz 
lpOperation	As String   'İşlem kodu : EDIT, PRINT, OPEN, FIND ve EXPLORE
lpFile		As String   'Döküman veya Executable (path bilgisi ile birlikte)
lpParameters	As String   'lpFile EXE ise program parametreleri, değilse NULL
lpDirectory	As String   'Default Directory
nShowCmd	As Number   'Window gösterim tipi 
) As Bool
```

\
Parametreler\
_hWnd_ :\
Çalıştırılan programın bağlı olduğu window handle. Amaçlanan program veya dökümanda oluşan mesagebox ların ana pencereye yollanabilmesidir. Default olarak hWndFrame kullanılmakta olduğundan NULL verebilirsiniz.\
\
_lpOperation_ :\
İşlem kodu : EDIT, PRINT, OPEN, FIND ve EXPLORE.\
\
_lpFile_ :\
Döküman veya Executable (path bilgisi ile birlikte).\
\
_lpParameters_ :\
lpFile EXE ise program parametreleri, değilse NULL.\
\
_lpDirectory_ :\
Dökümana ait programın veya EXE nin çalışacağı default directory.\
\
_nShowCmd_ :\
Window gösterim tipi:



| Kod                 | Açıklama                                                                                                                                                                                                                                                                   |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SW\_HIDE            | Hides the window and activates another window.                                                                                                                                                                                                                             |
| SW\_MAXIMIZE        | Maximizes the specified window.                                                                                                                                                                                                                                            |
| SW\_MINIMIZE        | Minimizes the specified window and activates the next top-level window in the z-order.                                                                                                                                                                                     |
| SW\_RESTORE         | Activates and displays the window. If the window is minimized or maximized, Windows restores it to its original size and position. An application should specify this flag when restoring a minimized window.                                                              |
| SW\_SHOW            | Activates the window and displays it in its current size and position.                                                                                                                                                                                                     |
| SW\_SHOWDEFAULT     | Sets the show state based on the SW\_ flag specified in the STARTUPINFO structure passed to the CreateProcess function by the program that started the application. An application should call ShowWindow with this flag to set the initial show state of its main window. |
| SW\_SHOWMAXIMIZED   | Activates the window and displays it as a maximized window.                                                                                                                                                                                                                |
| SW\_SHOWMINIMIZED   | Activates the window and displays it as a minimized window.                                                                                                                                                                                                                |
| SW\_SHOWMINNOACTIVE | Displays the window as a minimized window. The active window remains active.                                                                                                                                                                                               |
| SW\_SHOWNA          | Displays the window in its current state. The active window remains active.                                                                                                                                                                                                |
| SW\_SHOWNOACTIVATE  | Displays a window in its most recent size and position. The active window remains active.                                                                                                                                                                                  |
| SW\_SHOWNORMAL      | Activates and displays a window. If the window is minimized or maximized, Windows restores it to its original size and position. An application should specify this flag when displaying the window for the first time.                                                    |

Geri Dönüş Değeri\


```
Geri dönüş değeri, işlem başarılı ise TRUE, başarısız ise FALSE değerdir:
```

| Kod                      | Açıklama                                                                                                                                                      |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0                        | The operating system is out of memory or resources.                                                                                                           |
| ERROR\_FILE\_NOT\_FOUND  | The specified file was not found.                                                                                                                             |
| ERROR\_PATH\_NOT\_FOUND  | The specified path was not found.                                                                                                                             |
| ERROR\_BAD\_FORMAT       | The .exe file is invalid (non-Win32® .exe or error in .exe image).                                                                                            |
| SE\_ERR\_ACCESSDENIED    | The operating system denied access to the specified file.                                                                                                     |
| SE\_ERR\_ASSOCINCOMPLETE | The file name association is incomplete or invalid.                                                                                                           |
| SE\_ERR\_DDEBUSY         | The DDE transaction could not be completed because other DDE transactions were being processed.                                                               |
| SE\_ERR\_DDEFAIL         | The DDE transaction failed.                                                                                                                                   |
| SE\_ERR\_DDETIMEOUT      | The DDE transaction could not be completed because the request timed out.                                                                                     |
| SE\_ERR\_DLLNOTFOUND     | The specified dynamic-link library was not found.                                                                                                             |
| SE\_ERR\_FNF             | The specified file was not found.                                                                                                                             |
| SE\_ERR\_NOASSOC         | There is no application associated with the given file name extension. This error will also be returned if you attempt to print a file that is not printable. |
| SE\_ERR\_OOM             | There was not enough memory to complete the operation.                                                                                                        |
| SE\_ERR\_PNF             | The specified path was not found.                                                                                                                             |
| SE\_ERR\_SHARE           | A sharing violation occurred.                                                                                                                                 |

Dikkat Edilecek Hususlar\


ShellExecute Directory search için de kullanılabilir.

\
\
\
Örnek

```
if (ShellExecute(0, "Open", "c:\Always\test.doc", 0, "c:\Always", SW_SHOW)) then
   outm("Word dokümanı başarılı bir şekilde açıldı")
else
   outm("İşlem başarısız")
endif


'Excel dosyası açılıyor
nRes:= ShellExecute(0, "Open", "c:\Always\Rapor.xls", "", "c:\Always", SW_SHOW)

'Zip dosyası açılıyor
nRes:= ShellExecute(0, "Open", "c:\Always\release.zip", "", "c:\Always", SW_SHOW)

'Anadilden Imagine programı açılıyor
nRes:= ShellExecute(0, "Open", "c:\Always\Imagine.exe", "", "c:\Always", SW_SHOW)

'Bir programa parametre veriliyor
nRes:= ShellExecute(0, "Open", "c:\Always\test.exe", "par1 par2 123 par4", "c:\Always", SW_SHOW)

'c:\Always bolgesi açılıyor
nRes:= ShellExecute(0, "Explore", "c:\Always", "", "", SW_SHOW)

'c:\Always bolgesinde arama yapılıyor
nRes:= ShellExecute(0, "Find", "c:\Always", "", "", 0)
```
