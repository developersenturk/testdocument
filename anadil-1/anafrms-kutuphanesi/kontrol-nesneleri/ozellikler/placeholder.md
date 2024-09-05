# PlaceHolder

Bu özellik format özelliği ile belirlenen maske üzerinde kullanılacak boş karakter sembolünü belirlememizi sağlar. Örneğin 0(###) ### ## ## maskesi veri girişi sırasında 0(\_\_\_) \_\_\_ \_\_ \_\_ olarak görünecektir. Bunun yerine 0(\*\*\*) \*\*\* \*\* \*\* olarak görünmesini istiyorsak PlaceHolder özelliği ile \* karakteri PlaceHolder yapmalıyız.\
\
**Kullanımı**

```
ControlObject.PlaceHolder As String
```

\
**Dikkat Edilecek Hususlar**\
\
**Örnek**

```
 f.mut_no.PlaceHolder:='*' 



Maske kullanım örnekleri

Format ifadesi x veya X karakteri ile başlıyorsa maske olduğu anlaşılmaktadır. 
Maske kullanımı Editbox kontrollerinde geçerlidir. Grid hücrelerinde kullanıma 
açılmamıştır.Maske ifadesinde sayısal karakter için #, 
her türlü harf için ? ve sabit herhangi bir rakam veya harf kullanabiliriz.
# : Nümerik karakter girilebilir
? : Alfanümerik (Hem alfabetik hem de nümerik) karakter girilebilir.
_ : PlaceHolder : Silinen karakterlerin yerine Always bu karakteri yerleştirecektir.	      
Format belirleme sırasında öndeğer olarak "_" karakteri atanır.	      
f.mut_no.PlaceHolder:='%' methodu ile değiştirilebilir.
```

[**İlgili komutlar: Format Property**](format.md)
