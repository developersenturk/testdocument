# Constant

Bir Anadil® programi işletimi boyunca değerleri hiçbir zaman değişmeyen veya değişmeden kullanılacak ifadeler için uygulanmaktadırlar. Genellikle global olarak tanımlanmakta ve uygulanmaktadırlar.

Tanımlanırken de özel bir sekilde `Dim` ve `As` kullanılmadan `Const` yardımcı kelimesi ile belirtilmektedirler. İçerdikleri değer, `number`, `string` veya `boolean` tiplerden biri olabilmektedir.

**Örnek**

```
Const Reg_Path := "Always/Toolbar"		' string olabilen değer
Const B_Açik := True				' BOOL olabilen bir ifade

Function Test()
  ...
  ...<deyim>ler
  ...
    If sonuc=KDV_ORANI Then
    ...<deyim>ler
    EndIf
  ...
  ...<deyim>ler
  ...
EndFunction
```
