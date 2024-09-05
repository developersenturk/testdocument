# OnCopyDocument

\-------\
\
**Kullanımı**

```
Function ModulFile_OnCopyDocument(f As Object, cff As Object, query As Bool) As Bool
 'This is called to create a copy of a document when
 'copy menu item on browser right click menu is selected.

  if ( query ) then
     ModulFile_OnCopyDocument:=True
     return
  endif


 ModulFile_OnCopyDocument:=True
EndFunction
```

**Parametreler**\
_f As Object_\
_cff As Object_\
_query As Bool_\
\
**Geri Dönüş Değeri**\
Bool\
\
**Dikkat Edilecek Hususlar**\
\-----\
\
**Örnek**

```
-----
```

**Örnek Açıklaması**\
\-----
