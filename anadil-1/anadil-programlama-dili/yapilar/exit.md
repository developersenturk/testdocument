# EXIT

Bu deyim herhangi bir döngüden istenildiği anda çıkılmasını sağlamaktadır.&#x20;

**Görevi**&#x20;

İstenildiği anda döngü işletimini sonlandırmaktır.

**Kullanımı**

```
Function Test()
  Dim a As Number
  ...
  ...
  Do
    a:=a+10
    OutM(Str(a))
    If a > 99 Then
      Exit
    EndIf
  Loop WHILE 1=1
  ...

  ...

EndFunction
```

Açıklama\
Bu deyim en yakın döngünün içinden çıkılmasını sağlamaktadır. Bu döngü WHILE veya DO döngüsü olabilmektedir. Özellikle sonsuz işletimin uygulandığı döngü uygulamalarında yararlı olabilmektedir.
