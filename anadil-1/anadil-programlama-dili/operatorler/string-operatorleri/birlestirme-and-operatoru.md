# Birleştirme(& Operatörü)

Bu operatör iki string(karakter dizisi) ifade arasında birleştirme işlemi uygulamaktadır.\
Kullanımı\
sonuç\_ifade := \<karakter\_ifadesi1> & \<karakter\_ifadesi2>\
Açıklama\
Birleştirme işleminde string tipinden başka bir değişken tipi kullanılamaz. Eğer başka tipler kullanılmak istenirse uygun çevirim fonksiyonları ile string tipine dönüştürülmeleri gerekmektedir. İşlem sonunda oluşan yeni ifade de string kimliğe sahiptir.\
Örnek

```
Function F()
  Dim sayı1 As Number
  Dim sonuç As String
  sayı1:= 100
  sonuç:= "25 ile 4'ün çarpımı " & STR(sayı1) & #
          " değerine eşittir."
  MessageBox(sonuç,"Örnek Uygulama", MB_OK)
EndFunction
```

\
Örnek Açıklaması\
Yukardaki örnek uygulamada sayı1 değişkenine 100 değeri atanıyor ve sonuç string değişkenine de, sayı1 değişkeni ile "25 ile 4' ün çarpımı = " karakter ifadesinin birleşimi eşitlenmektedir.
