# AddForm

Bu metod Always projesine form ekler.\
\
**Uygulandığı Nesneler**\
Always Executable nesnesi.\
\
**Kullanımı**

```
AlwaysExecutable.AddForm(
  FormObjectCFF As Object	' Form ve kontrol bilgilerini içeren CFF nesnesi
  FormName As String		' Formun adı
)
```

**Parametreler**\
_FormObjectCFF_\
Form ve kontrol bilgilerini içeren CFF nesnesi\
_FormName_\
Formun adını içeren string ifade\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri boolean ifadedir.\
\
**Dikkat Edilecek Noktalar**\
Form ve form üzerinde bulunan kontrol bilgileri CFF entry leri ve alt cff ler şeklinde, bir CFF de bir araya getirilir ve bu method ile projeye eklenir. Bu method CFF in etkili bir iletişim aracı olduğunun değişik bir örneğidir.

```

Form Sabitleri:

  WS_OVERLAPPED	
  WS_POPUP	
  WS_CHILD	
  WS_MINIMIZE	
  WS_VISIBLE	
  WS_DISABLED	
  WS_CLIPSIBLINGS	
  WS_CLIPCHILDREN	
  WS_MAXIMIZE	
  WS_CAPTION	
  WS_BORDER	
  WS_DLGFRAME	
  WS_VSCROLL	
  WS_HSCROLL	
  WS_SYSMENU	
  WS_THICKFRAME	
  WS_GROUP	
  WS_TABSTOP	
  WS_MINIMIZEBOX	
  WS_MAXIMIZEBOX	
  WS_TILED	
  WS_ICONIC	
  WS_SIZEBOX	
  WS_TILEDWINDOW	
  WS_OVERLAPPEDWINDOW	
  WS_POPUPWINDOW	
  WS_CHILDWINDOW	
  WS_EX_DLGMODALFRAME	
  WS_EX_NOPARENTNOTIFY	
  WS_EX_TOPMOST	
  WS_EX_ACCEPTFILES	
  WS_EX_TRANSPARENT	
  ANA_CONTROL_BUTTON	
  ANA_CONTROL_STATICTEXT	
  ANA_CONTROL_LISTBOX	
  ANA_CONTROL_COMBO	
  ANA_CONTROL_EDIT	
  ANA_CONTROL_CHECKBOX	
  ANA_CONTROL_RADIO	
  ANA_CONTROL_TAB	
  ANA_CONTROL_GROUP	
  ANA_CONTROL_FRAME	
  ANA_CONTROL_RECTANGLE	
  ANA_CONTROL_ICON	
  ANA_CONTROL_PICTURE	
  ANA_CONTROL_PROGRID	
  ANA_CONTROL_UPDOWN	
  ANA_CONTROL_BUTTON_NONE	
  ANA_CONTROL_BUTTON_OKBUTTON	
  ANA_CONTROL_BUTTON_CANCELBUTTON	
  	
  FORMTYPE_MODULEFORM	
  FORMTYPE_TABPAGE	
  FORMTYPE_MODAL	
  FORMTYPE_MODELESS	
```

\
**Örnek**

```
  Function GenerateModuleForm(Exec As Object)
  Dim form as CFF
  Dim controls as CFF
  Dim shift As Number
  Dim bGen As Bool
  Dim i as Number
  Dim j as Number
  Dim satır as String

  form:=CFFCreate("form")

  controls:=form.Create("Controls")

  shift :=10

  For i := 1 To coltotal
        
    controls.AddRow()
    controls.Add("type",ANA_CONTROL_STATICTEXT) 
    controls.Add("xpos",5)
    controls.Add("ypos",shift)
    controls.Add("height",12)
    controls.Add("width",95)
    controls.Add("caption",captions[i])
    controls.Add("styles",SS_RIGHT + WS_CHILD)
    controls.Add("basicstyles",WS_VISIBLE)

    ' edit text   
    if fieldcont[i] = 0 or fieldcont[i] = 1 Then
      controls.AddRow()
      controls.Add("type",ANA_CONTROL_EDIT) 
      controls.Add("xpos",105)
      controls.Add("ypos",shift)
      controls.Add("height",12)
      controls.Add("width",90)
      controls.Add("name",fieldnames[i])
      controls.Add("format",fieldformats[i])
      controls.Add("styles",ES_LEFT + WS_BORDER + ES_AUTOHORSCROLL + WS_CHILD )
      controls.Add("basicstyles",WS_VISIBLE+WS_TABSTOP)
    Endif  
 
    if fieldcont[i] = 2 Then 
      controls.AddRow()
      controls.Add("type",ANA_CONTROL_STATICTEXT) 
      controls.Add("xpos",105)
      controls.Add("ypos",shift)
      controls.Add("height",12)
      controls.Add("width",90)
      controls.Add("name",fieldnames[i])
      controls.Add("format",fieldformats[i])
      if fieldorientation[i] = 1 Then
        controls.Add("styles",SS_RIGHT +WS_CHILD)
      Else
        controls.Add("styles",SS_LEFT + WS_CHILD)
      Endif
      controls.Add("basicstyles",WS_VISIBLE)
    Endif

    if fieldcont[i] = 3 Then  
      controls.AddRow()
      controls.Add("type",ANA_CONTROL_CHECKBOX) 
      controls.Add("xpos",105)
      controls.Add("ypos",shift)
      controls.Add("height",12)
      controls.Add("width",90)
      controls.Add("name",fieldnames[i])
      if fieldorientation[i] = 0 Then  
        controls.Add("styles",BS_LEFTTEXT + BS_AUTOCHECKBOX + WS_CHILD)
      Else
        controls.Add("styles", BS_AUTOCHECKBOX + WS_CHILD)
      Endif
      controls.Add("basicstyles",WS_VISIBLE+WS_TABSTOP)
    Endif
     
    ' combobox

    if fieldcont[i] = 4 Then  
      controls.AddRow()
      controls.Add("type",ANA_CONTROL_COMBO) 
      controls.Add("xpos",105)
      controls.Add("ypos",shift)
      controls.Add("height",90)
      controls.Add("width",90)
      controls.Add("name",fieldnames[i])
      controls.Add("styles",CBS_DROPDOWNLIST + WS_CHILD)
      controls.Add("basicstyles",WS_VISIBLE)
    Endif
    shift:=shift+15
  Next

  form.Add("Caption",sht1.name.valuestr)
  form.Add("FormType",FORMTYPE_MODULEFORM)
  form.Add("width",250)
  form.Add("height",50+shift) 
```

Exec._AddForm_(form,"f")

```
  Exec.AppendCode("Function f_Open(f As Object) As Bool")
  Exec.AppendCode("  Dim Control As Object")
  Exec.AppendCode("")
  Exec.AppendCode("  f.AutoDirty:=TRUE")
  
  For i:= 1 To Totalnumcols
    if   fieldcont[i] = 4 Then
      For j := 1 To deger
        if not combo[j] ="" Then
          Exec.AppendCode("  f." &fieldnames[i]& ".AddToList("&chr(34) & combo[j] &chr(34) &")")
        Endif
      Next
        Exec.AppendCode("  f." &fieldnames[i]& ".SelectItemInList(1)") 
    Endif
  Next

  Exec.AppendCode("  f_Open:=True") 
  Exec.AppendCode("EndFunction")
  Exec.AppendCode("")
  Exec.AppendCode("")
 
  Exec.AppendCode("Function " & documenttype & "_FormatTitle(CFF As Object, Title As String) As Bool")
  Exec.AppendCode("  Title:=CFF.Kod")
  Exec.AppendCode("  " & documenttype & "_FormatTitle:=True")
  Exec.AppendCode("EndFunction")
  Exec.AppendCode("")
  Exec.AppendCode("")

  Exec.AppendCode("Function "& documenttype & "_InitDoc(cci As Object, FirstTime As Bool) As Bool")
  Exec.AppendCode("  "  & documenttype & "_InitDoc:=TRUE")
  Exec.AppendCode("EndFunction")
  Exec.AppendCode("")
  Exec.AppendCode("")
  controls.Close()
```
