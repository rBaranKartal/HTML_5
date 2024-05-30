# Durum Kodu (Status Code) Nedir?

Durum kodları, HTTP protokolü çerçevesinde, bir istemci (client) tarafından yapılan HTTP isteğine sunucunun (server) verdiği yanıtın durumunu bildiren üç haneli sayısal kodlardır. Bu kodlar, istemciye isteğin başarılı olup olmadığını ve eğer başarısızsa nedenini belirtir.

## Durum Kodu Kategorileri

1. **1xx: Bilgilendirme (Informational)**
   - İstek alındı ve işlem devam ediyor.
   - Örnek: `100 Continue`, `101 Switching Protocols`

2. **2xx: Başarı (Success)**
   - İstek başarıyla alındı, anlaşıldı ve kabul edildi.
   - Örnek: `200 OK`, `201 Created`, `204 No Content`

3. **3xx: Yönlendirme (Redirection)**
   - İsteğin tamamlanması için ek işlem gerekiyor.
   - Örnek: `301 Moved Permanently`, `302 Found`, `304 Not Modified`

4. **4xx: İstemci Hatası (Client Error)**
   - İstek hatalıdır veya yetkilendirme gerektirir.
   - Örnek: `400 Bad Request`, `401 Unauthorized`, `403 Forbidden`, `404 Not Found`

5. **5xx: Sunucu Hatası (Server Error)**
   - Sunucu isteği yerine getiremedi.
   - Örnek: `500 Internal Server Error`, `502 Bad Gateway`, `503 Service Unavailable`

## Yaygın Kullanılan HTTP Durum Kodları

### 1xx: Bilgilendirme

- **100 Continue**
  - İstemciye, isteğin başlangıç kısmının alındığını ve devam etmesi gerektiğini belirtir.
- **101 Switching Protocols**
  - Sunucunun, istemci tarafından talep edilen protokol değişikliğini kabul ettiğini belirtir.

### 2xx: Başarı

- **200 OK**
  - İstek başarıyla tamamlandı.
  - Genellikle GET ve POST istekleri için kullanılır.

- **201 Created**
  - İstek başarıyla tamamlandı ve yeni bir kaynak oluşturuldu.
  - Genellikle POST istekleri için kullanılır.

- **204 No Content**
  - İstek başarıyla tamamlandı ancak geri dönecek içerik yok.
  - Genellikle PUT ve DELETE istekleri için kullanılır.

### 3xx: Yönlendirme

- **301 Moved Permanently**
  - Kaynak kalıcı olarak yeni bir URI'ye taşındı.
  - İstemcinin gelecekteki isteklerini yeni URI'ye yapması gerekir.

- **302 Found**
  - Kaynak geçici olarak farklı bir URI'de bulunur.
  - İstemcinin gelecekteki isteklerini eski URI üzerinden yapması beklenir.

- **304 Not Modified**
  - İstek koşullu bir GET isteği idi ve kaynak değiştirilmedi.
  - İstemci, önbelleğe alınmış versiyonu kullanmalıdır.

### 4xx: İstemci Hatası

- **400 Bad Request**
  - İstek sunucu tarafından anlaşılamadı veya hatalıydı.
  - Örnek: Söz dizimi hataları.

- **401 Unauthorized**
  - İstek yetkilendirme gerektiriyor ve başarısız oldu.
  - Kullanıcı kimlik doğrulama bilgileri sağlanmalıdır.

- **403 Forbidden**
  - Sunucu isteği anladı ancak işlemeyi reddetti.
  - Yetkisiz erişim denemesi.

- **404 Not Found**
  - İstenen kaynak sunucuda bulunamadı.
  - Yanlış URL veya kaynak mevcut değil.

### 5xx: Sunucu Hatası

- **500 Internal Server Error**
  - Sunucu beklenmeyen bir durumla karşılaştı ve isteği yerine getiremedi.
  - Genel sunucu hatası.

- **502 Bad Gateway**
  - Sunucu, geçerli bir yanıt almak için başka bir sunucuya başvurdu ancak geçersiz bir yanıt aldı.
  - Ağ geçidi veya proxy hatası.

- **503 Service Unavailable**
  - Sunucu şu anda isteği işleyemiyor.
  - Geçici aşırı yüklenme veya bakım çalışması nedeniyle.

## HTTP Durum Kodları Kullanım Örnekleri

- **200 OK**: Bir web sayfasının başarıyla yüklendiği durumda.
- **404 Not Found**: İstemcinin talep ettiği bir sayfanın sunucuda bulunmadığı durumda.
- **500 Internal Server Error**: Sunucuda beklenmeyen bir hatanın oluştuğu durumda.

Durum kodları, web uygulamalarının ve istemci-sunucu iletişiminin yönetilmesinde kritik öneme sahiptir. İstemciye, yapılan isteğin durumu hakkında bilgi sağlar ve gerekli işlemleri yapmasına olanak tanır.
