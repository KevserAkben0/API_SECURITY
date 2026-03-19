# API_SECURITY
General information I gathered from my research on the  OWASP API security top 10 .

---

##  API’ler Güvenlik Açığı İçerebilir mi?

Evet. Yaygın sebepler:

- Yanlış konfigürasyon  
- Eski kütüphaneler  
- Test eksikliği  
- Eksik doğrulama  
- Mantık hataları  

---

##  BOLA (Broken Object Level Authorization)

### Nedir?
Kullanıcıların yalnızca yetkili oldukları nesnelere erişebilmesini sağlayan kontrol mekanizmasının bozulmasıdır.

### Nasıl oluşur?
1. Girdi doğrulama eksikliği  
2. Yanlış yetkilendirme  
3. Tahmin edilebilir ID’ler  
4. Her istekte kontrol yapılmaması  

### Korunma
- Rol bazlı erişim kontrolü  
- Güçlü authentication  
- Random ID kullanımı  
- API Gateway ve Rate Limiting  

---

##  Broken Authentication

### Nedir?
Kimlik doğrulama mekanizmasının hatalı olmasıdır.

### Nasıl oluşur?
- Zayıf token doğrulama  
- Tahmin edilebilir oturumlar  
- Güvensiz JWT kullanımı  

### Korunma
- MFA kullan  
- Oturum süresini sınırla  
- Session rotation uygula  
- Brute-force koruması ekle  

---

##  BOPLA (Broken Object Property Level Authorization)

### Nedir?
Nesnenin iç özelliklerine yetkisiz erişim sağlanmasıdır.

### BOLA vs BOPLA
- BOLA → Nesne erişimi  
- BOPLA → Özellik erişimi  

### Korunma
- Yetki kontrolü  
- Güvenli veri dönüşümü  
- Whitelist kullanımı  
- Yanıt doğrulama  

---

##  Unrestricted Resource Consumption

### Nedir?
API’ye sınırsız istek gönderilerek kaynak tüketimi oluşturulmasıdır.

### Riskler
- Hizmet kesintisi (DoS)  
- Maliyet artışı  

### Korunma
- Rate limiting  
- Trafik izleme  
- Kullanım politikaları  
- Kaynak limitleri  

---

##  BFLA (Broken Function Level Authorization)

### Nedir?
Yetkisiz kullanıcıların sistem fonksiyonlarına erişebilmesidir.

### Nasıl oluşur?
- Eksik rol kontrolü  
- Admin endpoint’lerin korunmaması  
- Yanlış yapılandırma  

### Korunma
- Fonksiyon bazlı yetkilendirme  
- Güvenli oturum yönetimi  
- Düzenli güvenlik testleri  

---

##  UASBF (Unrestricted Access to Sensitive Business Flows)

### Nedir?
Kritik işlemlerin sınırsız şekilde kullanılabilmesidir.

### Nasıl oluşur?
- Rate limiting yok  
- Bot koruması yok  
- İş mantığı eksik  

### Korunma
- API gateway kullan  
- Rate limiting uygula  
- Kullanıcı davranışlarını izle  
- Güvenlik testleri yap  

---

##  SSRF (Server Side Request Forgery)

### Nedir?
Sunucunun saldırgan adına iç kaynaklara istek göndermesidir.

### Nasıl oluşur?
- URL doğrulama eksikliği  
- İç ağ erişimi açık  
- Güvenlik filtrelerinin olmaması  

### Korunma
- Allowlist kullan  
- Input validation  
- Network isolation  
- Yanıt kontrolü  

---

##  Security Misconfiguration

### Nedir?
Yanlış veya eksik sistem yapılandırmalarıdır.

### Nasıl oluşur?
- Debug mode açık  
- Gereksiz servisler aktif  
- Güvenlik ayarları eksik  

### Korunma
- Hardening  
- Güncellemeleri yap  
- Güvenlik taramaları uygula  

---

##  Improper Inventory Management

### Nedir?
API envanterinin düzgün yönetilmemesidir.

### Riskler
- Eski API’ler açık kalır  
- Shadow endpoint’ler  
- Güncel olmayan sistemler  

### Korunma
- Dokümantasyon tut  
- Versioning kullan  
- Ortamları ayır  
- Sürekli tarama yap  

---

##  Unsafe Consumption of APIs

### Nedir?
Üçüncü taraf API’lerden gelen verilere kontrolsüz güvenilmesidir.

### Nasıl oluşur?
- Veri doğrulanmaz  
- Güvensiz bağlantılar  
- API key sızıntısı  

### Korunma
- Input validation  
- HTTPS zorunlu  
- Least privilege  
- Timeout yönetimi  

---

##  Sonuç

API güvenliği, yalnızca teknik değil aynı zamanda süreç odaklı bir konudur.  
Doğru yapılandırma + sürekli test = güvenli sistem.

---

##  Teşekkürler

Bu dokümanı incelediğiniz için teşekkür ederim.

---
API güvenliği, modern uygulamaların en kritik bileşenlerinden biridir. Bu doküman, yaygın API güvenlik açıklarını ve korunma yöntemlerini özetler.

---

##  API’ler Güvenlik Açığı İçerebilir mi?

Evet. Yaygın sebepler:

- Yanlış konfigürasyon  
- Eski kütüphaneler  
- Test eksikliği  
- Eksik doğrulama  
- Mantık hataları  

---

##  BOLA (Broken Object Level Authorization)

### Nedir?
Kullanıcıların yalnızca yetkili oldukları nesnelere erişebilmesini sağlayan kontrol mekanizmasının bozulmasıdır.

### Nasıl oluşur?
1. Girdi doğrulama eksikliği  
2. Yanlış yetkilendirme  
3. Tahmin edilebilir ID’ler  
4. Her istekte kontrol yapılmaması  

### Korunma
- Rol bazlı erişim kontrolü  
- Güçlü authentication  
- Random ID kullanımı  
- API Gateway ve Rate Limiting  

---

##  Broken Authentication

### Nedir?
Kimlik doğrulama mekanizmasının hatalı olmasıdır.

### Nasıl oluşur?
- Zayıf token doğrulama  
- Tahmin edilebilir oturumlar  
- Güvensiz JWT kullanımı  

### Korunma
- MFA kullan  
- Oturum süresini sınırla  
- Session rotation uygula  
- Brute-force koruması ekle  

---

##  BOPLA (Broken Object Property Level Authorization)

### Nedir?
Nesnenin iç özelliklerine yetkisiz erişim sağlanmasıdır.

### BOLA vs BOPLA
- BOLA → Nesne erişimi  
- BOPLA → Özellik erişimi  

### Korunma
- Yetki kontrolü  
- Güvenli veri dönüşümü  
- Whitelist kullanımı  
- Yanıt doğrulama  

---

##  Unrestricted Resource Consumption

### Nedir?
API’ye sınırsız istek gönderilerek kaynak tüketimi oluşturulmasıdır.

### Riskler
- Hizmet kesintisi (DoS)  
- Maliyet artışı  

### Korunma
- Rate limiting  
- Trafik izleme  
- Kullanım politikaları  
- Kaynak limitleri  

---

##  BFLA (Broken Function Level Authorization)

### Nedir?
Yetkisiz kullanıcıların sistem fonksiyonlarına erişebilmesidir.

### Nasıl oluşur?
- Eksik rol kontrolü  
- Admin endpoint’lerin korunmaması  
- Yanlış yapılandırma  

### Korunma
- Fonksiyon bazlı yetkilendirme  
- Güvenli oturum yönetimi  
- Düzenli güvenlik testleri  

---

##  UASBF (Unrestricted Access to Sensitive Business Flows)

### Nedir?
Kritik işlemlerin sınırsız şekilde kullanılabilmesidir.

### Nasıl oluşur?
- Rate limiting yok  
- Bot koruması yok  
- İş mantığı eksik  

### Korunma
- API gateway kullan  
- Rate limiting uygula  
- Kullanıcı davranışlarını izle  
- Güvenlik testleri yap  

---

##  SSRF (Server Side Request Forgery)

### Nedir?
Sunucunun saldırgan adına iç kaynaklara istek göndermesidir.

### Nasıl oluşur?
- URL doğrulama eksikliği  
- İç ağ erişimi açık  
- Güvenlik filtrelerinin olmaması  

### Korunma
- Allowlist kullan  
- Input validation  
- Network isolation  
- Yanıt kontrolü  

---

##  Security Misconfiguration

### Nedir?
Yanlış veya eksik sistem yapılandırmalarıdır.

### Nasıl oluşur?
- Debug mode açık  
- Gereksiz servisler aktif  
- Güvenlik ayarları eksik  

### Korunma
- Hardening  
- Güncellemeleri yap  
- Güvenlik taramaları uygula  

---

##  Improper Inventory Management

### Nedir?
API envanterinin düzgün yönetilmemesidir.

### Riskler
- Eski API’ler açık kalır  
- Shadow endpoint’ler  
- Güncel olmayan sistemler  

### Korunma
- Dokümantasyon tut  
- Versioning kullan  
- Ortamları ayır  
- Sürekli tarama yap  

---

##  Unsafe Consumption of APIs

### Nedir?
Üçüncü taraf API’lerden gelen verilere kontrolsüz güvenilmesidir.

### Nasıl oluşur?
- Veri doğrulanmaz  
- Güvensiz bağlantılar  
- API key sızıntısı  

### Korunma
- Input validation  
- HTTPS zorunlu  
- Least privilege  
- Timeout yönetimi  

---

##  Sonuç

API güvenliği, yalnızca teknik değil aynı zamanda süreç odaklı bir konudur.  
Doğru yapılandırma + sürekli test = güvenli sistem.

---

##  Teşekkürler

Bu dokümanı incelediğiniz için teşekkür ederim.


---
Endpoint-labs intern project
