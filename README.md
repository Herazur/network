# **Taşıma katmanı ağ protokolleri**


## TCP

Bir bilgisayar başka bir bilgisayarla iletişim kurmak istediğinde, bu iki bilgisayar arasındaki iletişimin iyi ve güvenilir olması gerekir, böylece verilerin doğru şekilde alınmasını garanti edebilir.

Örneğin, bir web sayfasını görüntülemek veya bir dosya indirmek veya bir e-postaya bakmak istediğinizde, web sayfasını hiçbir şey eksik olmadan olduğu gibi ve sırayla görüntülemeyi beklersiniz. Veya bir dosya indiriyorsanız, dosyanın sadece bir kısmını değil, tüm dosyayı istersiniz, çünkü veriler eksikse veya sıra dışıysa, bu sizin için için herhangi bir fayda sağlamaz.

TCP burada devreye girer bu yüzden. TCP İletim Kontrol Protokolü (Transmission Control Protocol) anlamına gelir ve bu TCP / IP Ağı kullanılan ana protokoller biridir. Bir web sayfasını TCP olmadan görüntülerseniz, web sayfanız tamamen karışabilir. Görüntüler eksik olabilir veya metin ters ve sıra dışı olabilir.

Artık TCP, bağlantı odaklı bir protokoldür, bu da temelde iletişim kuran iki bilgisayar arasındaki bir oturum onaylaması anlamına gelir. Böylece iki bilgisayar, herhangi bir iletişim gerçekleşmeden önce bir bağlantıyı doğrular. Ve bunu üç yönlü bir el sıkışma kullanarak yapar. Dolayısıyla ilk adım, bir bilgisayarın SYN adlı bir mesaj göndermesidir. Daha sonra alıcı , gönderene mesajı aldığını bildiren bir onay mesajı gönderir ve son olarak gönderen bilgisayar alıcıya başka bir alındı mesajı gönderir. Ve bu gerçekleştiğinde, veriler teslim edilebilir. TCP hakkında unutulmaması gereken bir diğer önemli husus da, verilerin teslimini garanti etmesidir. Yani bir veri paketi yoldan çıkarsa ve ulaşmazsa, TCP onu yeniden gönderecektir. 

## UDP

UDP, TCP'ye çok benzer. UDP ayrıca veri göndermek ve almak içindir. Ancak temel fark, UDP'nin bağlantısız olmasıdır. Bu, bir oturum oluşturulmadığı ve veri teslimini garanti etmediği anlamına gelir. Dolayısıyla, bir bilgisayar verilerini gönderdiğinde, verilerin diğer uçta alınıp alınmadığı gerçekten umursamaz ve bu nedenle UDP "ateşle ve unut" (fire-and-forget) protokolü olarak bilinir, çünkü veri gönderir ve ona ne olduğu gerçekten umrunda olmaz. Unutulmaması gereken bir diğer nokta da, veri dağıtımını garanti etmemenin gerektirdiği daha az ek yük nedeniyle UDP'nin TCP'den daha hızlı olmasıdır.

