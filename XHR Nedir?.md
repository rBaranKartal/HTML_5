# XHR Nedir?

XHR (XMLHttpRequest), web tarayıcılarında sunucularla asenkron veri alışverişi yapmak için kullanılan bir API'dir. Bu, sayfanın tamamını yeniden yüklemeden web sayfalarına veri göndermeyi ve veri almayı sağlar.

## XMLHttpRequest'in Temel Özellikleri

1. **Asenkron Veri Alışverişi**
   - Sunucuyla arka planda iletişim kurarak web sayfasının tamamını yeniden yüklemeden veri alışverişi yapar.
   - Kullanıcı deneyimini iyileştirir ve sayfa yükleme sürelerini azaltır.

2. **HTTP İstekleri Gönderme ve Alma**
   - GET, POST, PUT, DELETE gibi HTTP yöntemleriyle istekler gönderilebilir.
   - Sunucudan veri alabilir ve sunucuya veri gönderebilir.

3. **Çapraz Tarayıcı Desteği**
   - Tüm modern web tarayıcıları tarafından desteklenir.
   - JavaScript kullanarak kolayca entegre edilebilir.

## XMLHttpRequest Kullanımı

### Temel Adımlar

1. **XMLHttpRequest Nesnesi Oluşturma**
   - `new XMLHttpRequest()` kullanarak yeni bir XMLHttpRequest nesnesi oluşturulur.

2. **Açma (Open)**
   - `xhr.open(method, url, async)` ile isteğin türü (GET, POST vb.) ve hedef URL belirtilir. İsteğin asenkron olup olmadığı da belirlenir (genellikle `true`).

3. **İsteği Gönderme (Send)**
   - `xhr.send(data)` ile istek sunucuya gönderilir. Gerekirse istekle birlikte veri de gönderilebilir.

4. **Yanıtı İşleme**
   - `xhr.onreadystatechange` veya `xhr.onload` olayları kullanılarak sunucudan gelen yanıt işlenir.

### Örnek Kullanım

```javascript
// Yeni bir XMLHttpRequest nesnesi oluşturma
var xhr = new XMLHttpRequest();

// GET isteği açma
xhr.open('GET', 'https://api.example.com/data', true);

// Yanıt geldiğinde çalışacak fonksiyonu tanımlama
xhr.onreadystatechange = function() {
  if (xhr.readyState === 4 && xhr.status === 200) {
    // Yanıtı işleme
    console.log(xhr.responseText);
  }
};

// İsteği gönderme
xhr.send();
