# SetFocus

Bu metod herhangi bir form üzerindeki kontrol'e focus edilmesini sağlamaktadır.\
\
**Uygulandığı Nesneler**\
Bütün kontrol nesneleri.\
\
**Kullanımı**

```
ControlObject.SetFocus()
```

\
**Parametreler**\
Metodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri önemsizdir.\
\
**Dikkat Edilecek Noktalar**\
"Focus" özelliği, hangi Windows™ uygulaması olursa olsun, kullanıcıdan gelen input bilgisini alacak olan kontrolün sahip olduğu bir flag'dır. Windows™ sisteminin yapısında, herhangi bir anda ancak bir tane kontrol "Focus" özelliğine sahip bulunmaktadır. Bu kontrol, aktif kontrol şeklinde de nitelendirilebilir.\
\
Kullanıcı bir kontrolle ilgili bir etkide veya bilgi girişinde bulunacaksa, önce o kontrolde "Focus" edilmiş olmalıdır. Yoksa o anda "Focus" a sahip olan kontrol input bilgiyi alacaktır. İşte bu metod ile hangi kontrol nesnesinin, kullanıcıdan etki alacağını belirlemekteyiz.\
\
Kullanım esnasında kullanıcı da kontroller arasında "Focus" geçişini manuel olarak mouse(fare) ile veya TAB tuşuna basarak sırayla kontroller arasında gezerek başarmaktadır.\
\
Herhangi bir form üzerinde bulunan kontrole "Focus" etmeden önce form açısından da "Focus" testinin yapılması gerekmektedir. Aslında, bu da o Windows™ uygulamasının veya form nesnesinin sahip olduğu kontrollerden herhangi birinin "Focus" flag değerinin aktif olması manasına gelmektedir. Eğer "Focus" a, o anda başka bir form nesnesi kontrolü sahipse, geliştiricinin kendi formu üzerinde "Focus" belirleme girişimi etkisiz olacaktır. Form nesnesi "Focus" test işlemi ise, metod olarak .IsFocus() şeklinde Anadil® bünyesinde yer almaktadır.
