# NAS ve SAN Arasındaki Fark Nedir?

NAS
--
NAS, (Network Attached Storage) ağa bağlı depolama anlamına gelir. Verileri, ağınızdaki tüm cihazlarınızdan erişilebilecek merkezi bir yerde depolamak istiyorsanız, bunu ağa bağlı bir depolama cihazı kullanarak yapabilirsiniz.
![image](https://user-images.githubusercontent.com/68228757/158702612-44a3d2bb-fef9-42eb-81e0-cebc5c171362.png)

NAS, verileri depolamak için kullanılan bir depolama cihazıdır ve verileri depolamaktan başka hiçbir şey yapmaz. Yedeklilik için RAID yapılandırmasında birden fazla sabit sürücüye sahip olacak bir kutudur
ve ayrıca doğrudan bir switch veya router’a bağlanacak bir ağ arayüz kartına sahip olacaktır, böylece verilere bir ağ üzerinden erişilebilir. NAS tipik evlerde kullanılan paylaşılan sürücü olarak erişilebilir ve ayrıca orta ölçekli işletmelerce kullanılmaktadır.

NAS’ın ana dezavantajlarından biri, tek bir arıza noktasına sahip olmasıdır. Örnek olarak, bir bileşenin, NAS’daki güç kaynağının arızalanması gibi bir arıza durumunda. O zaman diğer tüm cihazlar, verilerine erişemeyecek.
![image](https://user-images.githubusercontent.com/68228757/158702671-bc48c0b2-6f3b-477e-ad0d-5641ffc8d414.png)

SAN
--

SAN veya (Storage Area Network) depolama alanı ağı, büyük miktarlarda veriyi depolayan ve bunlara erişim sağlayan özel bir yüksek hızlı ağdır.
![image](https://user-images.githubusercontent.com/68228757/158702691-c584dea8-f158-4437-a814-00e14418f987.png)

Dolayısıyla, temelde veri depolama için kullanılan özel bir ağdır ve bu ağ, birden çok disk dizisinden(disk array), anahtarından(switch) ve sunucudan(server) oluşur.
![image](https://user-images.githubusercontent.com/68228757/158702748-28843d83-331e-4944-b062-0fbbb98a4f7e.png)

Ve bu cihazlardan birden fazlasına sahip olduğu için, bir SAN hataya dayanıklıdır. Ve veriler de birkaç disk dizisi arasında paylaşılır. Bu nedenle, bir anahtar veya disk dizisi veya bir sunucu çökerse, verilere yine de erişilebilir.
Ve bir sunucu eriştiğinde SAN üzerindeki veriler, sanki yerel bir sabit diskmiş gibi verilere erişir. Çünkü işletim sistemleri, bir SAN’ı NAS’ta olduğu gibi paylaşılan bir ağ sürücüsü yerine yerel bağlı bir sabit sürücü olarak tanır. Ve SAN’lar da son derece ölçeklenebilirdir çünkü ağda kesinti olmadan
daha fazla depolama alanı eklemek kolaylıkla yapılabilir.
![image](https://user-images.githubusercontent.com/68228757/158702769-2f86ff04-b39c-4a8e-aa44-b59ccc8e35f4.png)

Bir SAN yüksek hızlı bir ağdır Ve bunun sebebi bir SAN’da tüm cihazların birbirine bağlı olması anlamına gelir. birbirlerine bağlıdırlar ve SAN’lar için bir standart olan fiber kanal kullanılarak birbirine bağlanırlar . Fiber kanal, fiber optiktir ve saniyede 2 gigabit arasında, saniyede 128 gigabayta kadar hıza sahiptir .
![image](https://user-images.githubusercontent.com/68228757/158702796-942a9e3a-c55e-4881-a5a2-cbc8b6628552.png)

Bu nedenle fiber kanal son derece hızlıdır ve aynı zamanda çok pahalıdır ve günümüzde çoğu SAN fiber kanal kullanır. Ama aynı zamanda fiber kanala alternatif olarak bazı SAN’lar bunun yerine iSCSI kullanır. Bu fiber kanala göre daha ucuz bir alternatiftir, ancak fiber kanal kadar hızlı değildir.
Şimdi SAN kullanmanın ana nedenlerinden biri, SAN’ların ağ trafiğinden etkilenmemesidir. Yerel bir alan ağında meydana gelebilecek darboğazlar gibi Ve bunun nedeni, SAN’ların gerçekten bir yerel alan ağının parçası olmamasıdır . SAN’lar bölümlere ayrılmıştır. Temelde tek başına bir ağdır ve daha önce bahsettiğim gibi SAN’ların diğer nedenleri yüksek oranda ölçeklenebilir ve ayrıca çok yedeklidirler. Ve ayrıca tahmin edebileceğiniz gibi SAN’lar ucuz değildir. Çok yüksek bir maliyetle gelirler, bu nedenle esas olarak büyük şirketler ve büyük kuruluşlar tarafından kullanılırlar.
