# MessageBox

Bu fonksiyon Standart Fonksiyonları kullanarak ekranda bir mesaj kutusu oluşturur.\
\
Kullanımı

```
Function MessageBox(
  Bilgi As String,   ' verilmek istenilen mesaj
  Başlık As String,  ' mesaj kutusu üst bilgisi
  F_Type As Number   ' MessageBox fonksiyon tipi
)As Number
```

Parametreler\
_Bilgi_\
Mesaj kutusu içinde yazılacak olan string bir ifadedir.\
_Başlık_\
Mesaj kutusunun üzerindeki window caption bilgisi olarak yazılacak olan string bir ifadedir.\
_F\_Type_\
MessageBox fonksiyonları tipinden hangisi kullanılacak ise onun isminin yazıldığı ifadedir. İsim yazılması yanıltmasın çünkü ismin de karşılığı bir numara olarak zaten Anadil içersinde önceden tanımlanmıştır.\
\
Geri Dönüş Değeri\
Kullanılan MessageBox tipine göre değişen sayısal bir ifadedir. Bu sayısal ifade ise genel WinAPI uygulamalarında bazı anlamlı kelimeler ile ifade edilmektedir. Bu şekildeki kullanım, geliştirici açısından da büyük kolaylıklar temin etmekte, gereksiz bazı sayıların akılda tutulması zorunluluğundan kurtarmaktadır.\
\


| MesageBox Tipi       | GERİ DÖNÜŞ DEĞERLERİ         |
| -------------------- | ---------------------------- |
| MB\_OK               | IDOK                         |
| MB\_OKCANCEL         | IDOK - IDCANCEL              |
| MB\_YESNO            | IDYES - IDNO                 |
| MB\_YESNOCANCEL      | IDYES - IDNO - IDCANCEL      |
| MB\_RETRYCANCEL      | IDRETRY - IDCANCEL           |
| MB\_ABORTRETRYIGNORE | IDABORT - IDRETRY - IDIGNORE |

Görüldüğü gibi geri dönüş değeri MessageBox kutusunun ekranda görünmesinden sonra hangi butona basıldığında dair bilgi vermektedir. İstenildiği taktirde bu referans isimlerine karşılık gelen sayılar da elde edilebilir ve hatta bu numaralar da fonksiyon tipini belirtmek için kullanılabilir.\
\
Dikkat Edilecek Hususlar\
Standart fonksiyonlarda genel olarak son kullanıcının bir bilgi vermekte veya yapılmak istenilen iş ile ilgili olarak bir seçim yapılacaksa bu seçim son kullanıcıdan alınmaktadır. Bilgilendirme işlem ise bir olay sonucunda ortaya çıkan bir durumdur.\
\
Daha önce meydana gelen bu olayda veya yapılacak olan seçimin önemini kullanıcıya daha iyi ifade edebilmek amacıyla Mesaj kutularının sahip olduğu bazı iconlar vardır. İşte bu icon'lar kullanılmak istenildiğinde standart fonksiyonun yanında '+' işaretinden sonra belirtilebilmektedir.\
\
Mesaj kutuları içersinde kullanılabilecek icon'lar aşağıda sunulmuştur:\


* MB\_ICONINFORMATION
* MB\_ICONSTOP
* MB\_ICONQUESTION
* MB\_ICONEXCLAMATION

Bu icon'ların kullanımı ile son kullanıcının yapılan işle ilgili dikkati daha iyi bir şekilde çekilebilmektedir.\
\
Örnek

```
Function F()
  Dim GeriDönüş As Number
  GeriDönüş:= MessageBox(	"Lütfen bir butona basınız.", #
              "Merhaba Dünya!", #
              MB_YESNOCANCEL + MB_ICONQUESTION)
  If GeriDönüş = IDYES Then
    MessageBox("YES Tuşuna Basıldı.","SONUÇ",MB_OK)
  Else
    If GeriDönüş = IDNO Then
      MessageBox("NO Tuşuna Basıldı.","SONUÇ",MB_OK)
    Else 
      If GeriDönüş = IDCANCEL Then
        MessageBox("CANCEL Tuşuna Basıldı.","SONUÇ",MB_OK)
      Else
        MessageBox("Hatalı Durum!","ERROR",MB_OK)
      EndIf
    EndIf
  EndIf
EndFunction
```

\
Örnek Açıklaması\
Burada örnek olarak son kullanıcıya herhangi bir olay sonrasında yapılabilecek sorgulama işlemi gösterilmeye çalışılmıştır. Ekranda gelen mesaj kutusunda başlık olarak "Merhaba Dünya!" gösterilmiş butonlarla yapılan seçimlere göre de sonuç olarak diğer mesaj kutuları ile bilgilendirme yapılmıştır.\
\
Görüldüğü gibi en son çıkan Mesaj kutusu ile yapılan seçim sonucu ortaya çıkan geri dönüş değeri göz önünde tutulmamıştır. Bu tür, bazı tek seçimli Mesaj kutularında çokça uygulanan bir metoddur.
