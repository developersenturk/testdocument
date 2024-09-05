# ListSelItem

Bu property çoktan seçimli kontrol nesnelerinde, kullanıcının yaptığı, number cinsinden seçimin alınmasını sağlamaktadır.\
\
**Uygulandığı Nesneler**\
Combo-Box ve List-Box kontrol nesneleri.\
\
**Uygulama Biçimi**\
Sadece okunur bir property'dir.

**Kullanımı**

```
ControlObject.ListSelItem As String
```

\
**Dikkat Edilecek Noktalar**\
Listeden seçimli olarak kullanılmakta olan kontrol nesnelerinde son kullanıcının yapmış olduğu tercihin index numarasını bu özellik ile öğrenebilmekteyiz.\
\
İndexleme numarası 0(sıfır) dan itibaren başlamaktadır yani ilk combo içeriğinin index numarası 0'dır. Eğer son kullanıcı henüz seçimini yapmamışsa bu özelliğin okunması ile -1 değeri elde edilecektir.
