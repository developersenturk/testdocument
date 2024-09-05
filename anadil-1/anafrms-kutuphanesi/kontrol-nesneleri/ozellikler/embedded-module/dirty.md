# Dirty

Bu property embedded modülde yer alan kontrol nesnelerinin kirlenmeye maruz kalıp kalmadıklarının test edilmesini sağlamaktadır.\
\
**Uygulandığı Nesneler**\
Embedded Modüldeki kontrol nesneleri.\
\
**Uygulama Biçimi**\
Okunabilir bir özelliktir.\
\
**Kullanımı**

```
ControlObject.Dirty As Bool
```

\
**Dikkat Edilecek Noktalar**\
Bu özellik formlar anlatılırken de değinilmiş olan "Dirty" mekanizmasının kullanımını temin etmektedir. "Dirty" veya kirlilik olayı herhangi bir kontrolde meydana gelen değişimin işaretidir.\
\
Embedded modüldeki, her form açıldığında ister tamamiyle yeni bir belge formu olsun isterse önceden kayıtlı bir belge formu olsun öncelikle üzerinde taşıdığı kontrollerde 'Dirty' özelliği False değeri taşımaktadır. Eğer kullanıcı bu formun sahip olduğu kontrollerden herhangi birinde içeriğini etkilemek suretiyle değişime neden olursa, o kontrol objesinin kirlilik özelliğini True içerikle set etmiş yani o kontrolün kirlenmesine yol açmış olacaktır.\
\
Geliştirici isterse Anadil® ile program yazarken, mesela bir belgeyi UPDATE ederken, gereksiz işlemleri önlemek için bu kirlilik kontrolü sayesinde, sadece değişime uğramış belge kısımları üzerinde veritabanında "SQL Update" işlemi uygulayabilir. Ayrıca kirlilik mekanizması Always® tarafından da kullanılmakta olup; kirlenmemiş bir belge kesinlikle kayıt işlemine tabi tutulmamaktadır.\
