# Wordpress Sıkılaştırma Kılavuzu

## WordPress Nedir?

WordPress, dünyada en çok kullanılan blog sistemlerinden biridir, açık kaynaklı ve ücretsiz olarak dağıtılmaktadır. WordPress kullanarak kısa süre içinde kendi sunucunuza kurulum yapabilir, sitenizi yayınlayabilir ve sitenize içerik eklemeye yani bloglamaya başlayabilirsiniz.

WordPress açık kaynaklı bir yazılım olduğu için dünyanın her yerinden isteyen herkesin katkıda bulunmasına açıktır; “created by and for the community” denir, yani topluluk tarafından ve yine topluluk için geliştirilmekte ve desteklenmektedir. Bu şekilde her geçen gün daha da kullanışlı ve sağlam bir sistem haline gelmektedir.

## Güvenlik Nedir?
Temel olarak güvenlik, sistemleri mükemmel bir şekilde güvenliğe alma anlamına gelmemektedir. Bu genellikle uygulanamaz ya da erişilemez bir noktadır. Güvenlik bu bağlamda riskleri azaltmak ya da riski ortadan kaldırmak şeklinde düşünülebilir. Bu doğrultuda bu kılavuzda riskleri azaltan ve WordPress sitesini hedef olmak ve bilinen saldırı metodlarından korumak için bazı adımlar anlatılacaktır.

## Sunucu Sistemi

Güvenlik için ilk adım sunucu sisteminin güvenliğidir. Güvenilir bir sunucu hizmeti veren birimden ya da firmadan hizmet almanız verilerinizin ve sitenizin güvenliği için çok önemlidir.

## Yedekleme

Wordpress sitesinin sıklıkla yedeğini almalısınız. Bu herhangi bir felaket durumunda verileri kurtarmak ve geriye dönük olarak bazı incelemeler yapılması için önemlidir. Güncelleme, eklenti yükleme ya da buna benzer sitede yapılacak değişikliklerden önce ayrı bir yedek alınması gereklidir. Yapılan değişiklik ya da yükleme işlemi sırasında ortaya çıkabilecek bir sorunda işlem öncesine dönme imkanı sağlayacaktırş.

## Parola Güvenliği

Sisteme erişmekte ve wordpress yönetici yetkisi bulunan kullanıcıların parolalarının yeteri kadar güvenli olduğundan emin olunuz. Sözlük kelimeleri içeren ve basit kombinasyonlardan oluşan parolalardan kaçınınız. Başka bir yerde kullandığınız parolaların aynısını kullanmayınız. Parola sıfırlama seçenekleri ile e-posta adresinize gönderilecek bir bağlantı ile erişim sağlanabileceğini unutmayınız. Bu nedenle aynı şekilde e-posta adresinize erişiminiz ile ilgili güvenlik tedbirlerini de alınız.

## Eklentiler ve Tema Güvenliği

3. parti eklentiler ve temalar kullanırken çok dikkatli olunuz. Bilmediğiniz kaynaklardan gelen herhangi bir eklenti ya da tema gibi bir uygulamayı sitenize entegre edip aktifleştirdiğinizde bilmediğiniz kodları çalıştırmış olursunuz. O an için her şey yolunda görünse bile bir süre sonra saldırganın erişimini kolaylaştıracak bir açık kapı içeriyor olabilir. Bu konuda dikkatli ve seçici davranmak gerekir.

## WordPress’i Güncelleme

Günvel bir sürüm kullanmak önemlidir. Herhangi bir yazılımda olduğu gibi WordPress’in de geliştirmeler ve güvenlik yamalarını içeren güncellemeleri takip etmeniz gerekmektedir. Güncellemeden önce mutlaka yedek alınız. Güncelleme ile ilgili detaylı bilgiyi WordPress dokümanlarında bulabilirsiniz ancak burada bir temel noktadan bahsetmek istiyorum, wordpress.org sitesi haricindeki herhangi bir kaynaktan güncelleme ya da yama alıp kullanmayınız. Wordpress yönetim panelinden güncelleme yapabileceğiniz gibi doğrudan wordpress.org sitesinden paket indirerek kurabilirsiniz. Bunun dışında herhangi bir kaynaktan güncelleme yapmadığınızdan emin olunuz.

## FTP Erişimi
Sunucuya erişiminiz sırasında SFTP kullanmalısınız. Servis sağlayınız bunu desteklemiyorsa talep etmelisiniz. FTP yerine SFTP ile erişim sağlandığı koşulda parola ve verilerini şifrelenerek gönderilir ve bir saldırgan tarafından ele geçirilemez.

## Dosya İzinleri
WordPress’in bazı özellikleri sunucu tarafından bazı klasör ve dosyalara yazma izni gerektirmektedir. Sağlayıcı tarafından php dosyalarınızın size ayrılmış kullanıcı ile çalıştırılacağı ve güvenli bir altyapı talep ediniz. Böylece size tahsis edilmiş kullanıcı ile çalıştırılan php kodları yine aynı kullanıcı ile erişmesi gereken yerlere erişebilecektir. Web sunucusu kullanıcısına yazma izni vermek zorunda kalmayacağınız bu yapı daha güvenlidir.

Genel olarak WordPress sisteminde tüm dosyalar sizin kullanıcınız sahipliğinde olmalıdır. Sitenizin barındırıldığı sistemde eğer gerekliyse sadece gerektiği kadar web sunucu kullanıcısına yazma izni vermelisiniz. Sistemin yapısı şu şekildedir:

    /

Kök WordPress klasörü, bütün dosyalar sadece kullanıcınız tarafından yazılabilir olmalıdır.

    /wp-admin/

Yönetim arayüzü klasörü, bütün dosyalar sadece kullanıcınız tarafından yazılabilir olmalıdır.

    /wp-includes/

WordPress’in diğer uygulama parçaları, bütün dosyalar sadece kullanıcınız tarafından yazılabilir olmalıdır.

    /wp-content/

Kullanıcılar tarafından sağlanan içerikler, bütün dosyalar sadece kullanıcınız tarafından yazılabilir olmalıdır. Eğer sadece gerekiyorsa sunucu kullanıcısına da yazma izni verilmelidir.

Bu klasör içerisinde:

    /wp-content/themes/

Tema dosyalarını içerir. Yönetim arayüzündeki editörü kullanacaksanız buradaki dosyalara da sunucu kullanıcısına yazma izni verilmelidir aksi takdirde sadece sizin kullanıcınıza yazma izni verilmelidir.

    /wp-content/plugins/

Eklentilerin bulunduğu klasör, bütün dosyalar sadece kullanıcınız tarafından yazılabilir olmalıdır. Bazı eklentiler farklı izinler gerektirebilir.

## Dosya izinlerini düzenlemek

Sunucuya konsol erişiminiz varsa iki komut ile basitçe değişiklik yapabilirsiniz.

### Klasörler için:

    find /path/to/your/wordpress/install/ -type d -exec chmod 755 {} \;

### Dosyalar için:
    find /path/to/your/wordpress/install/ -type f -exec chmod 644 {} \;


## wp-admin Erişim Güvenliği
Sunucu tarafında erişimi kısıtlayan BasicAuth metoduyla kullanıcı adı ve şifre ile klasöre erişimin kısıtlanmasıyla ikinci bir güvenlik adımı ekleyebilirsiniz. 

## Wp-includes Erişim Güvenliği
Kod parçalarının bulunduğu klasöre ikinci bir güvenlik katmanı eklenebilir. .htaccess dosyasında mod-rewrite ile herkesin doğrudan erişmesi gerekmeyen dosyaları engelleyebiliriz. Aşağıdaki .htaccess koduyla bu işlem yapılabilir. WordPress’in otomatik olarak bu değişikliği ezmesini engellemek için # BEGIN WordPress ve # END WordPress etiketlerinin dışına yazdığınızdan emin olun.

    # Block the include-only files.
    <IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteBase /
    RewriteRule ^wp-admin/includes/ - [F,L]
    RewriteRule !^wp-includes/ - [S=3]
    RewriteRule ^wp-includes/[^/]+\.php$ - [F,L]
    RewriteRule ^wp-includes/js/tinymce/langs/.+\.php - [F,L]
    RewriteRule ^wp-includes/theme-compat/ - [F,L]
    </IfModule>
    
    
    # BEGIN WordPress

## wp-config.php güvenliği
wp-config dosyası bazı hassas veriler içermektedir. Bu nedenle sadece okumaya erişim verilerek mümkünse web root dışında bir yere yerleştirilmedir. Bir klasör yukarı almak olası bir erişim durumunda dosya içeriğini web erişiminden kısıtlayacaktır.
Mümkünse 400 erişim izniyle sadece sizin kullanıcınızın okuyacağı şekilde dosya izinlerini değiştiriniz. Web sunucu kullanıcısı farklı ise 440 izni vermeniz gerekebilir.

Ayrıca bu klasöre .htaccess ile erişimi de kısıtlamak ikinci bir güvenlik adımı ekleyecektir.

    <files wp-config.php>
    order allow,deny
    deny from all
    </files>

## Dosya Düzenlemeyi Kapatmak
WordPress Yönetim Arayüzü varsayılan olarak yöneticilere PHP dosyalarını düzenleme imkanı sunmaktadır. Wp-config.php dosyasına aşağıdaki satırı ekleyerek bunu kapatınız.

    define('DISALLOW_FILE_EDIT', true);

Bu yöntem bir şekilde erişim sağlamış saldırganın sitenize artniyetli dosyalar yüklemesine engel olur ve bazı saldırıları engeller.

## Kayıt alma ve İzleme
Log dosyalarınızı ve değişen dosyalarınızı izlemelisiniz. Bilginiz haricinde değişen dosyalar ve şüpheli durumları ayrıca araştırıp gerekli tedbirleri almalısınız. Bunun için http://ossec.github.io aracını kullanabilirsiniz.

Yukarıdaki açıklamalar ve önlemler herhangi bir güncellik ve kesinlik garantisi altında değildir, kullanım sorumluluğu tamamen kullanıcıya aittir.. Wordpress sitesini takip etmeniz önerilir.
