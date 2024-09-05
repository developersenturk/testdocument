# CallServiceTransactedThread

CallServiceTransactedThread Methodu Service Call nesnesini ayrı bir thread ortamında çağırır ve aynı zamanda Rs hatalarını biriktirir.\
\
**Kullanımı**

```
ServiceObject.CallServiceTransactedThread() As Bool
```

**Parametreler**\
Methodun parametresi yoktur.\
\
**Geri Dönüş Değeri**\
Geri dönüş değeri booleandır.\
\
**Dikkat Edilecek Noktalar**\
CallServiceTransactedThread Methodu Service Call nesnesini ayrı bir thread ortamında çağırır ve aynı zamanda SQL'de oluşan hataları biriktirir.
