Windows bilgisayarında, ağ yapılandırmasını kontrol edelim. Bir komut istemi açarsanız ve ardından ipconfig yazarsanız ve çıktıda IP adresini, subnet mask ve bu bilgisayara atanmış default gatewayini görürsünüz.
![image](https://user-images.githubusercontent.com/68228757/158676237-fbdd72ac-ef3f-44ff-a782-91794fb757db.png)


Öyleyse kendinize soruyor olabilirsiniz, peki varsayılan ağ geçidi (default gateway) nedir? Basitçe söylemek gerekirse, default gateway, verileri bir ağdan diğerine ileten cihazdır. Ve çoğu zaman, bu bir router (yönlendirici) olacak.
Örneğin burada bir yerel alan ağımız var. Yönlendiricinin diğer tarafında ise başka bir ağ olan internet var.
![image](https://user-images.githubusercontent.com/68228757/158676285-7408cd6e-ec44-4620-8501-35bd14e0d813.png)


Dolayısıyla, bu bilgisayarların internetteki bir web sayfası gibi başka bir ağa erişmesi için, verilerin yönlendirici olan default gatewayden geçerek kendi yerel ağından çıkması gerekir. Ardından router verileri internete iletecektir. Özetle, default gateway budur. Bir ağdaki cihazların başka bir ağdaki cihazlarla iletişim kurmasını sağlar. Ve daha önce de söylediğim gibi, bu genellikle bir router olacak.
Bilgisayarlar aynı ağ üzerinde ise verilerin ağdan çıkması ve default gatewayden geçmesi gerekmez.
![image](https://user-images.githubusercontent.com/68228757/158676340-cb71b00a-4e78-48cb-8030-b24a7e802b62.png)


Bu da bizi bir sonraki sorumuza getiriyor. Yani bu bilgisayarlar başka bir bilgisayarla iletişim kurmak istiyorlarsa, o bilgisayarın kendi ağlarında mı yoksa farklı bir ağda mı olduğunu nasıl bilecekler. Bilgisayar aynı ağ üzerindeki bir bilgisayarla iletişim kurmak isterse direkt onunla konuşabilir. Ancak farklı bir ağdaki bir bilgisayarla iletişim kurmak istiyorsa, varsayılan default gatewayden geçmesi gerekir. Peki yine nereden biliyor? İşte burada IP adresi ve subnet mask devreye girer.
Bir IP adresi iki bölümden oluşur . İlk kısım Network ID, ikinci kısım ise Host ID. Bu nedenle, hangi bölümün ağa veya ana bilgisayara ait olduğunu söylemenin yolu, subnetmask’in geldiği yerdir. Subnet mask, IP adresine benzeyen bir sayıdır. Ve IP adresinin ağ kısmını maskeleyerek, IP adresindeki kaç bitin ağ için kullanıldığını ortaya çıkarır .
![image](https://user-images.githubusercontent.com/68228757/158676391-ceb9ab7a-366a-475d-bf36-536881c1e836.png)


Yani burada ikili biçimde IP adresi ve subnet mask’i var. Bu IP adresinin hangi kısmının ağ kısmı olduğunu söylemenin yolu , subnet mask ikili basamağı 1 olduğunda, ağı tanımlayan IP adresinin konumunu belirtecektir .
![image](https://user-images.githubusercontent.com/68228757/158676445-59e7f433-f7e9-496e-b96b-31936ce68c86.png)


Bu nedenle , alt ağ maskesindeki 1'lerle aynı hizada olan IP adresindeki tüm rakamların üzerini çizeceğiz. Ve bunu yaptığınızda, ilk üç sekizli veya kümenin ağ kısmı ve kalanın ana bilgisayar kısmı olduğunu ortaya çıkaracaktır . Dolayısıyla , IP adresinin ilk üç sayısının 192.168.0 olduğu bir ağdaki herhangi bir bilgisayar veya cihaz, bu bilgisayarların aynı ağda olduğu anlamına gelir.
![image](https://user-images.githubusercontent.com/68228757/158676510-8db54643-ed92-4d9c-8e78-55e161f53ec3.png)


Burada iki alt ağa veya alt ağa bölünmüş özel bir ağımız var . Soldaki alt ağ 192.168.0 ağında ve sağdaki alt ağ 192.168.1 ağındadır. Ve her alt ağın kendi varsayılan ağ geçidi vardır. Şimdi diyelim ki A bilgisayarı bu alt ağ üzerinde B bilgisayarı ile iletişim kurmak istiyor.
![image](https://user-images.githubusercontent.com/68228757/158676544-90fb5a33-7575-4b41-9ac0-b55e0e29f4e7.png)


Yani A bilgisayarı, aynı ağda olup olmadığını görmek için B bilgisayarının IP adresini kontrol edecek. Ve anlayabileceğiniz gibi, ilk üç sekizli olan IP adreslerinin ağ kısmı aynı olduğu için iki bilgisayar aynı ağda . Yani A bilgisayarı artık B bilgisayarının aynı ağda olduğunu biliyor .
Yani şimdi iletişimin gerçekleşmesi için A bilgisayarının B bilgisayarının MAC adresine ihtiyacı var . Bunu, ağ üzerinden B bilgisayarından MAC adresini isteyen bir ARP yayını göndererek bulur . Ardından, MAC adresine sahip olduğunda, nihayet iletişim gerçekleşebilir.
![image](https://user-images.githubusercontent.com/68228757/158676593-c30ff3ee-5643-4bd3-9a44-d5d282ba813c.png)


Başka bir senaryoda, bu alt ağdaki A bilgisayarının D bilgisayarı ile iletişim kurmak istediğini varsayalım.
![image](https://user-images.githubusercontent.com/68228757/158676617-383d5590-e385-4aa0-a978-c8fa5645bb4b.png)


Yani yine A bilgisayarı , aynı ağda olup olmadığını görmek için D bilgisayarının IP adresini kontrol edecek . Ve bu sefer de anlayabileceğiniz gibi, iki bilgisayar farklı ağlarda çünkü ilk üç sekizli olan IP adreslerinin ağ kısmı farklı.
![image](https://user-images.githubusercontent.com/68228757/158676650-1a215161-2788-4f24-af45-1c6c087edbc9.png)


Ve fark üçüncü sayıdır. A bilgisayarı 0 kullanıyor ve D bilgisayarı 1 kullanıyor. Dolayısıyla A bilgisayarı artık D bilgisayarının farklı bir ağda olduğunu biliyor. Bu yüzden onunla doğrudan iletişim kuramaz, default gateway kullanmak zorundadır.
![image](https://user-images.githubusercontent.com/68228757/158676675-d1306b90-7904-486d-97c7-a036982df094.png)


Böylece A bilgisayarı bir ARP yayını gönderecek ve bu sefer bilgisayarın değil default gatewayin MAC adresini isteyecek , çünkü D bilgisayarı farklı bir ağda ve ARP yayınları gidemediği için yayını almayacak. bir yönlendiriciyi geçmiş ardından MAC adresine sahip olduğunda, verileri varsayılan ağ geçidine gönderecek ve ardından hedefe iletilecektir.
