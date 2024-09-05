# Grid Hücre Nesneleri

Grid kontrol nesnesi ile çalışırken kullanıcının veri girişi yapacağı öğeler grid hücreleri olacaktır. Bu hücrelerin sahip oldukları bilgilere daha kolay bir şekilde ulaşımı sağlayabilmek için bu hücrelere nesne şeklinde yaklaşım yapısı sağlanmıştır.

Hücre nesneleri de kullanıcının verdiği anlık bilgileri içermesinden dolayı dinamik bir karakteristiğe sahiptirler ve bu yüzden de sanal nesnelerdir. Yani sonuçta bir hücre nesnesi global olarak başka bir nesneye atanamaz, sadece grid event kodu dahilinde kullanılabilir olmaktadır. Ayrıca hücre nesnesinden, grid sütun nesnelerine ulaşım da mümkündür.
