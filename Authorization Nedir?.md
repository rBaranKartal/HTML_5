# Authorization Nedir?

"Authorization" terimi, genellikle bir kullanıcının belirli bir kaynağa veya işleme erişimini kontrol etme süreci anlamına gelir. Yetkilendirme, bir kimlik doğrulama (authentication) adımından sonra gelir ve kullanıcıya veya uygulamaya belirli izinler verir. Authorization işlemleri genellikle web uygulamalarında veya API'lerde uygulanır ve birkaç farklı yöntemle yapılabilir. İşte yetkilendirme kavramının temel unsurları ve bazı yaygın yöntemleri:

## Authorization Türleri ve Yöntemleri

1. **Rol Tabanlı Erişim Kontrolü (RBAC)**
   - **Tanım:** Kullanıcılara roller atanır ve bu roller belirli izinlerle ilişkilendirilir. Kullanıcılar, sahip oldukları rollerin izin verdiği kaynaklara erişebilir.
   - **Örnek:** Bir şirketin çalışanları; yöneticiler, geliştiriciler ve pazarlama personeli gibi rollerle atanabilir. Her rolün farklı erişim izinleri olabilir.

2. **Yetkilendirme Kapsamları (Scopes)**
   - **Tanım:** API isteklerine belirli kapsamlar atanır. Kullanıcı veya uygulama, yalnızca talep edilen kapsamlar dahilindeki işlemleri gerçekleştirebilir.
   - **Örnek:** Bir OAuth 2.0 yetkilendirme sürecinde, uygulamalar "read" veya "write" gibi belirli kapsamlar talep edebilir.

3. **Politika Tabanlı Erişim Kontrolü (PBAC)**
   - **Tanım:** Erişim izinleri, bir dizi politika kuralına göre belirlenir. Politikalar, kullanıcı nitelikleri, zaman dilimleri veya belirli koşullar gibi çeşitli kriterlere dayanabilir.
   - **Örnek:** Bir finansal uygulama, yalnızca iş saatleri içinde belirli işlemlere izin veren politikalar kullanabilir.

4. **Özellik Tabanlı Erişim Kontrolü (ABAC)**
   - **Tanım:** Kullanıcıların, kaynakların ve çevresel koşulların özelliklerine dayalı olarak erişim kararları verilir.
   - **Örnek:** Bir sağlık sistemi, kullanıcının rolüne, kaynağın türüne ve erişim talebinde bulunulan zaman dilimine dayalı olarak erişim kararları verebilir.

## Authorization Protokolleri ve Standartları

1. **OAuth 2.0**
   - **Tanım:** Yetkilendirme için yaygın olarak kullanılan bir protokol olup, üçüncü taraf uygulamaların kullanıcı adına kaynaklara erişimini sağlar.
   - **Özellikler:** Yetkilendirme kodu akışı, cihaz kodu akışı, istemci kimlik bilgileri akışı gibi çeşitli akışları destekler.
   - **Örnek:** Bir kullanıcı, bir üçüncü taraf uygulamanın Google Drive dosyalarına erişmesine izin vermek için OAuth 2.0 kullanabilir.

2. **JSON Web Token (JWT)**
   - **Tanım:** Kullanıcı kimlik bilgilerini ve yetkilendirme bilgilerini güvenli bir şekilde taşıyan ve JSON formatında kodlanmış token'lar kullanır.
   - **Özellikler:** Taşınabilirlik, güvenlik ve kolay entegrasyon sağlar.
   - **Örnek:** Bir API, kullanıcının belirli bir süre boyunca belirli kaynaklara erişimini sağlamak için JWT kullanabilir.

3. **SAML (Security Assertion Markup Language)**
   - **Tanım:** Kimlik doğrulama ve yetkilendirme verilerini XML formatında taşıyan bir standarttır. Genellikle kurumsal uygulamalarda kullanılır.
   - **Özellikler:** Güvenli ve standart bir şekilde kimlik bilgisi paylaşımı sağlar.
   - **Örnek:** Bir şirketin intranet portalı, çalışanların çeşitli kurumsal kaynaklara erişimini sağlamak için SAML kullanabilir.

## Authorization Süreci

1. **Kimlik Doğrulama (Authentication)**
   - Kullanıcının kimliğinin doğrulanması.
   - Örnek: Kullanıcı adı ve şifre ile giriş yapma.

2. **Yetkilendirme (Authorization)**
   - Doğrulanmış kullanıcının belirli kaynaklara veya işlemlere erişim izninin kontrol edilmesi.
   - Örnek: Kullanıcının sadece belirli bir sayfayı görmesine izin verilmesi.

3. **Erişim Kontrol Kararları**
   - Erişim izinleri, rol, kapsam, politika veya özelliklere göre belirlenir.
   - Örnek: Yönetici rolüne sahip bir kullanıcı, tüm kullanıcı verilerine erişebilirken, normal bir kullanıcı yalnızca kendi verilerine erişebilir.

Yetkilendirme, güvenlik ve kullanıcı deneyimi açısından kritik bir öneme sahiptir. Doğru uygulandığında, sadece yetkili kullanıcıların belirli kaynaklara ve işlemlere erişimini sağlar, böylece sistem güvenliğini ve bütünlüğünü korur.
