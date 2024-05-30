# Oturum (Session) Nedir?

Oturum (Session), bir kullanıcı ile bir sunucu arasındaki etkileşimi belirli bir süre boyunca izlemek ve yönetmek için kullanılan bir mekanizmadır. Oturumlar, kullanıcının giriş yaptığı andan çıkış yaptığı ana kadar geçen süre boyunca kullanıcı hakkında bilgi saklamak ve bu bilgiyi kullanarak kullanıcı deneyimini kişiselleştirmek için kullanılır.

## Oturumların Temel Özellikleri

1. **Geçici Veri Saklama**
   - Kullanıcıya özgü bilgilerin geçici olarak saklanması.
   - Örneğin, kullanıcı kimliği, alışveriş sepeti içerikleri, oturum kimlik bilgileri.

2. **Oturum Kimliği (Session ID)**
   - Her oturum için benzersiz bir kimlik numarası oluşturulur.
   - Bu kimlik, sunucu tarafından yönetilir ve genellikle kullanıcı tarafında çerez (cookie) olarak saklanır.

3. **Sunucu Tarafında Saklama**
   - Oturum bilgileri genellikle sunucu tarafında saklanır.
   - Sunucu tarafında saklanan bilgiler daha güvenli ve yönetilebilir olur.

## Oturum Kullanımının Avantajları

1. **Kullanıcı Durumunu İzleme**
   - Kullanıcıların giriş yapıp yapmadığını, hangi sayfalara eriştiğini ve hangi işlemleri gerçekleştirdiğini izleme.
   - Kişiselleştirilmiş deneyim ve içerik sunma imkanı.

2. **Güvenlik**
   - Oturum kimlik doğrulama mekanizmaları, kullanıcıların kimliklerini doğrulamak ve yetkilendirme süreçlerini yönetmek için kullanılır.
   - Hassas bilgilere erişimi kontrol etme.

3. **Durum Bilgisi Saklama**
   - Alışveriş sepeti gibi kullanıcıya özel bilgilerin oturum süresince saklanması.
   - Çok adımlı işlemler ve formlar arasında bilgi taşınması.

## Oturum Kullanımının Dezavantajları

1. **Yük ve Performans**
   - Çok sayıda kullanıcıyla etkileşim halinde olan sunucular için oturum bilgilerini yönetmek performans sorunlarına yol açabilir.
   - Oturum yönetimi için ek kaynak ve bellek kullanımı gerektirir.

2. **Oturum Süresi ve Zaman Aşımı**
   - Oturumların belirli bir süre boyunca aktif olması ve sonra zaman aşımına uğraması gerekebilir.
   - Kullanıcı deneyimini olumsuz etkileyebilecek zaman aşımı sorunları.

## Oturum Yönetimi

### Oturum Başlatma

1. **Kullanıcı Girişi**
   - Kullanıcı, kimlik doğrulama bilgilerini (örneğin kullanıcı adı ve şifre) sağlar.
   - Sunucu, kullanıcıyı doğrular ve yeni bir oturum başlatır.

2. **Oturum Kimliği Oluşturma**
   - Sunucu, benzersiz bir oturum kimliği (Session ID) oluşturur ve bunu kullanıcıya gönderir.
   - Bu kimlik genellikle çerez olarak kullanıcı tarayıcısında saklanır.

### Oturum Kullanma

1. **Oturum Kimliğini Gönderme**
   - Kullanıcı, sonraki isteklerinde oturum kimliğini sunucuya gönderir.
   - Sunucu, gelen oturum kimliğini kontrol ederek kullanıcıyı tanır ve ilgili oturum bilgilerini geri yükler.

2. **Oturum Verilerini Güncelleme**
   - Kullanıcının etkileşimlerine göre oturum verileri güncellenir.
   - Örneğin, alışveriş sepetine ürün eklemek veya çıkarmak.

### Oturum Sonlandırma

1. **Kullanıcı Çıkışı**
   - Kullanıcı, oturumu sonlandırmak için çıkış yapar.
   - Sunucu, oturum bilgilerini temizler ve oturum kimliğini geçersiz kılar.

2. **Zaman Aşımı**
   - Belirli bir süre boyunca aktif olmayan oturumlar otomatik olarak sonlandırılabilir.
   - Güvenlik nedenleriyle oturum süreleri sınırlı tutulur.

## Oturum Yönetimi Örnekleri

- **Web Uygulamaları**: E-ticaret siteleri, kullanıcıların oturum bilgilerini alışveriş sepeti ve kullanıcı profilleri için saklar.
- **Bankacılık Uygulamaları**: Güvenli oturum yönetimi, kullanıcıların finansal işlemlerini gerçekleştirmesi için kritik öneme sahiptir.

Oturum yönetimi, web uygulamalarında kullanıcı deneyimini kişiselleştirmek ve güvenliği sağlamak için temel bir mekanizmadır. Doğru uygulandığında, kullanıcıların etkileşimlerini izlemek, verimli ve güvenli bir şekilde yönetmek mümkündür.
