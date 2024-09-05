# CreateExecutable

Bu fonksiyon bir Imagine projesi yaratır.\
\
**Kullanımı**

```
Function CreateExecutable(
  ProjectName	' Yaratılacak Always programının adı
  ProjectType	' Yaratılacak Always programının tipi
) As Object
```

\
**Parametreler**\
_ProjectName_\


```
Yaratılacak Always programının adı
örnek :	 c:\Always\Malzeme\mlz_giris.ser,  
	 c:\Always\Muhasebe\wrk_rapor.rep
```

_ProjecType_

```
Yaratılacak Always programının tipi 
Proje Tipleri :
	PROJECT_REPORT
	PROJECT_PRINTEDFORM
	PROJECT_SERVICE
	PROJECT_MODULE
```

**Geri Dönüş Değeri**\
Geri dönüş değeri Always executable nesnesidir.\
\
**Dikkat Edilecek Noktalar**\
Bu fonksiyon bir Always executable (Imagine projesi) yaratır.

```
' +
' Bu örnek fonksiyon Rep_wiz.wiz projesinden alınmıştır. 
' Releaseden wizard ı kurarsanız wiz uzantılı projeleri inceleyebilirsinz.
' -
Function f_finish_Click(f As Object)
 Dim desccff As Cff
 Dim Exec As Executable
 Dim sqllines As Cff
 Dim i As Number
 Dim j As Number
 
 Hourglass(True)
 bNormalClose:=True
 Exec:=CreateExecutable(GetEnvVar("PROJECT_DEST"), 0)
 if Not Exec Then
  OutputResult("Hedef dosya yaratılamadı")
  goto ex:
 EndIf
 
 DefineAllGroups()
 DefineReportTotals()
 
 ' Write the desc.
 desccff:=CFFCreate("cff")
 desccff.Add("ID",sht1.id.ValueStr)
 desccff.Add("Name",sht1.name.ValueStr)
 desccff.Add("RepPath",sht1.path.ValueStr)
 Exec.SetDescriptor(desccff)
 desccff.Close()
 
 'Eliminate duplicates
 for i:=1 to totalnumcols
  for j:=i+1 to totalnumcols
    if fieldnames[i]=fieldnames[j] Then
      fielddeccount[j]:=fielddeccount[j]+1 ' declaretion count of field
    endif
  next
 next
 bCond:=sht99.condensed.IsChecked

 Exec.AppendCode("''''''''''''''''''''''''''''''''''''''''''''''''''''")
 Exec.AppendCode("' Bu rapor iş-bitirici tarafından oluşturulmuştur...")
 Exec.AppendCode("' Versiyon: 1.0                                     ")
 Exec.AppendCode("' Tarih: " & Date2Str(GetSystemDate())               )
 Exec.AppendCode("' Yazan: " & GetEnvVar("USERDOMAIN") & "/" & GetEnvVar("USERNAME") )
 Exec.AppendCode("''''''''''''''''''''''''''''''''''''''''''''''''''''")
 Exec.AppendCode("")

 ' Constants
 Exec.AppendCode("Const ReportName := " & chr(34) & sht1.name.ValueStr & chr(34))
 Exec.AppendCode("Const Sayfa_Başı_Yükseklik := 2")
 Exec.AppendCode("Const Sayfa_Sonu_Yükseklik := 1")

 DeclareGlobals(Exec) 
 GenerateSavedParamsDlg(Exec)
 GenerateImmediateParamsDlg(Exec)
 GenerateRunReport(Exec)
 
 if totalgroups>0 Then
   GenerateGroupSums(Exec)
 EndIf
 
 if numreptotals>0 Then
   GenerateReportSums(Exec)  
 Endif
 
 GenerateDetailLine(Exec)
 GenerateGroupHeaders(Exec)
 GenerateGroupFooters(Exec)
 GenerateReportHouseKeeping(Exec)
 GenerateRecordset(Exec)
 GenerateBinding(Exec)
 Exec.AppendCode("") 
 Exec.AppendCode("")
 
 
 Exec.AppendCode("' Oluşturulan SQL programı")
 sqllines:=querycff.OpenSubCff("SQLLines")
 if sqllines.MoveToFirstRow() Then
   do
    Exec.AppendCode("' " & sqllines.line)
    if not sqllines.MoveToNextRow() Then
      Exit
    EndIf  
   loop
 EndIf
 
 if Not Exec.Commit() Then
  OutputResult("Hedef dosya yaratılamadı")
  goto ex:
 Endif
 
 Exec.Close()
 
 OutputResult("success")
ex: 
 prevform.CloseForm()
 f.CloseForm()
 Hourglass(False)
EndFunction
```
