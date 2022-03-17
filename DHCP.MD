## DHCP 

Her bilgisayar veya cihaz, iletişim amacıyla bir ıp adresine sahip olmalıdır. IP adresi, ağdaki bir bilgisayar veya aygıt için bir tanımlayıcıdır. Ve bir bilgisayara bir IP adresi atamanın iki yolu vardır. Statik IP veya Dinamik IP kullanılarak yapılabilir.

Statik bir IP, bir kullanıcının bir IP adresini manuel olarak atadığı yerdir. Şimdi bu, ağ oluşturmanın başlangıcında yapılan orjinal yöntemdi. Dolayısıyla, bir ağdaki her bilgisayar için bilgisayarın ağ yapılandırma sayfasını açmanız ve manuel olarak bir IP adresi girmeniz gerekiyordu.

![image](https://user-images.githubusercontent.com/68228757/158865326-7cda1514-4870-4dae-b4bd-378daec10064.png)

Ancak bir IP adresine ek olarak, bir alt ağ maskesi (subnet mask) varsayılan ağ geçidi (default gateway) ve bir DNS sunucusu da yazmanız gerekir. Ve ağa başka bir bilgisayar veya cihaz eklemek istediğinizde, aynı şeyi yapmanız gerekiyordu. Tahmin edebileceğiniz gibi, özellikle çok sayıda bilgisayara sahip büyük bir ağla uğraşıyorsanız, bu çok fazla iş olabilir. Ayrıca, tüm IP adreslerinin benzersiz olduğundan emin olmalısınız çünkü aynı IP adresini iki kez atarsanız, bir IP çakışmasına neden olur ve bu bilgisayarların ağa erişememesine neden olur.

![image](https://user-images.githubusercontent.com/68228757/158865355-a665e9ca-ee8b-44ae-ab49-14daffcc289e.png)

Ancak bunun daha iyi ve daha kolay bir yolu vardır. Dinamik IP, bilgisayarın bir DHCP sunucusundan otomatik olarak IP adresi aldığı yerdir. DHCP sunucusu, bir bilgisayara otomatik olarak IP adresi atar. Ve bir IP adresine ek olarak, bir alt ağ maskesi, varsayılan ağ geçici ve bir DNS sunucusu da atayabilir.

![image](https://user-images.githubusercontent.com/68228757/158865376-da5bb30f-f51a-462a-b4a3-fc875947a23e.png)

Bu nedenle, burada bir örnek olarak , bir Microsoft Windows bilgisayarındaki ağ arabirim kartı için açık bir ağ bağlantı özellikleri penceremiz var . Ve burada görebileceğiniz gibi, bu bilgisayar otomatik olarak bir IP adresi alacak şekilde ayarlanmıştır.

![image](https://user-images.githubusercontent.com/68228757/158865402-9b9570ed-c7be-4030-a2bc-572fdd9ac9f8.png)

Bu seçeneği seçtiğinizde, bilgisayar ağ üzerinde bir IP adresi için bir istek yayınlayacak ve ardından DHCP sunucusu kendi havuzundan bir IP adresi atayacak ve bunu bilgisayara teslim edecektir.

![image](https://user-images.githubusercontent.com/68228757/158865435-7a27bf3e-a58b-4467-9c80-1d12cef185df.png)

Ve sonra bu yapıldığında, DHCP sunucusunun bilgisayarınıza verdiği tüm farklı ayarları doğrulayabilirsiniz. Bunu, bir Windows bilgisayarında bir komut istemi açarak ve ardından

ipconfig / all

yazıp “enter” tuşuna basarak yapabilirsiniz.
Burada görebileceğiniz gibi , bu bilgisayarda DHCP etkindir, bu da onun IP adresini bir DHCP sunucusundan aldığı anlamına gelir ve burada alt ağ maskesi, varsayılan ağ geçidi ve DNS sunucusuyla birlikte IP adresini görebilirsiniz.

![image](https://user-images.githubusercontent.com/68228757/158865499-db8fdf88-cc9e-4f7a-8bab-2e508a6df34a.png)

Yani tüm bu ayarlar DHCP sunucusu tarafından verildi. Dinamik IP adreslemenin en iyi seçim olduğunu söyleyebileceğiniz gibi, otomatiktir ve bir ağı yönetmeyi çok daha kolay hale getirir.

