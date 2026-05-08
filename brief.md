# Dasvio Main Landing Redesign Brief

> Tarih: 8 Mayıs 2026  
> Kapsam: apps/client içindeki ana landing sayfasının (`/`) tam yeniden tasarımı  
> Amaç: Dasvio'yu tek ürün gibi değil, restoranın tüm operasyonunu yöneten tek platform olarak anlatan yeni bir ana sayfa tasarlamak

## 1. Bu Brief Neden Var?

Mevcut client projesinde pazarlama yüzeyi parçalı durumda:

- Ana landing (`/`) ayrı bir anlatı kullanıyor.
- Ürün detay sayfaları (`/qr-menu`, `/pos`, `/reservation`, `/crm-whatsapp`) kendi başına güçlü ama birbirinden kopuk görsel diller taşıyor.
- Kod içinde eski adlandırmalar var (`Kasse360`, `Dojoneo`), ancak kamuya açık marka dili net biçimde `Dasvio` olmalı.

Yeni landing'in görevi sadece daha güzel görünmek değil. Asıl görev:

- Dasvio'yu "QR menü yapan bir tool" gibi değil, "restoran işletim sistemi" olarak konumlamak.
- Küçük işletme sahibi ile zincir restoran operasyon yöneticisine aynı sayfada doğru değer önerisini vermek.
- Mevcut feature set'i gerçekçi şekilde sergilemek.
- Kullanıcıyı ürün detay sayfalarına, demo talebine veya kayıt akışına yönlendirmek.

Not:

- Eski brief'te geçen `landing-sketch/index.html` referansı artık kaynak olarak kabul edilmemeli.
- Bu doküman yeni kaynak dokümandır.

## 2. Ürün Gerçekliği: Landing'de Anlatılması Gereken Asıl Yetkinlikler

Bu bölüm tasarımcının "hangi vaatler gerçek, hangileri secondary" ayrımını doğru yapması için var.

### A. Ana ürün sütunları

1. POS ve mağaza içi operasyon
- Sipariş ve ödeme akışı
- Cihaz yönetimi
- Revenue center yönetimi
- Satış kanalları
- Fiş/print yönetimi
- Tükendi / override mantıkları

2. QR Menü ve misafir deneyimi
- Dijital menü
- Tema builder
- Draft/publish mantığı
- Spotlight / öne çıkan ürünler
- Galeri / görsel menü
- Çok dilli yapı
- Alerjen filtresi
- Masa bazlı OBW akışı

3. Rezervasyon ve CRM / WhatsApp
- Rezervasyon yönetimi
- Masa planı
- Hatırlatma mesajları
- Müşteri geçmişi ve notları
- Müşteri iletişimi

4. Çok şubeli kurumsal yönetim
- Master menü yönetimi
- Şube atamaları
- Override özeti
- Fiyat kademeleri
- Kampanya ve combo yönetimi
- Şube karşılaştırma ve merkezi kontrol

5. Entegrasyonlar ve analitik
- Getir / Trendyol / benzeri platform akışları
- Bağlantı yönetimi
- Mapping / store status / reviews / claims / pricing yüzeyleri
- Operasyon ve satış raporları

### B. İkincil ama önemli modüller

- Stok yönetimi / Cozent
- Dijital signage / müşteri ekranı
- Event yönetimi
- PWA / halka açık müşteri akışları

### C. Landing'de öne çıkarılmaması gereken şeyler

- İçeride gerçekten doğrulanmamış "AI" vaatleri
- Çok teknik mimari detaylar
- Mikroservis, altyapı ve deployment dili
- Her modülü eşit ağırlıkta anlatma çabası

Landing'de öncelik sırası şu olmalı:

1. İşletmenin tüm operasyonunu tek yerden yönetme
2. Misafir deneyimi ile operasyon panelini aynı ekosistemde birleştirme
3. Çok şubeli ve entegrasyonlu işletmelere ölçek vaadi

## 3. Hedef Kitle

### Birincil kitle

Bağımsız restoran sahibi / işletme müdürü

- Günlük operasyonun içinden geliyor.
- POS, menü, rezervasyon, müşteri takibi birbirinden kopuk olduğu için yoruluyor.
- Kısa sürede şunu anlamak istiyor: `Bu sistem bana zaman kazandırır mı, satış artırır mı, ekibi rahatlatır mı?`

### İkincil kitle

Çok şubeli yapı yöneten operasyon sorumlusu

- Şubeler arası fiyat, menü, kampanya ve performans farklarını kontrol etmek istiyor.
- Şunu duymak istiyor: `Merkezden kontrol ederim, şubelerde olanı görürüm.`

### Üçüncül kitle

Teknik karar verici / dijital dönüşüm tarafı

- Entegrasyon, cihaz, operasyon sürekliliği ve veri görünürlüğü ile ilgilenir.
- Ona güven veren yüzey: entegrasyonlar, dashboard kalitesi, ürün olgunluğu.

## 4. Pozisyonlama

Landing'in tek cümlelik stratejik cümlesi:

**Dasvio, restoranınızın POS, QR menü, rezervasyon, CRM ve çok şubeli operasyonlarını tek platformda birleştiren işletim sistemidir.**

Anlatım şu üç hissi aynı anda vermeli:

- Güvenilir
- Modern
- Operasyonel olarak güçlü

Bu sayfa bir fintech gibi soğuk olmamalı.
Bu sayfa bir food app gibi de görünmemeli.
Doğru his: `misafir deneyimi + arka ofis kontrolü + premium operasyon disiplini`.

## 5. Ton ve Marka Dili

### Olması gereken ton

- Net
- Kendinden emin
- Sıcak ama profesyonel
- Abartısız ama iddialı
- Somut fayda odaklı

### Olmaması gereken ton

- Aşırı startup jargonu
- Boş slogan dili
- "AI her şeyi çözüyor" yaklaşımı
- Çok kurumsal ve soğuk enterprise dili

### Marka notu

- Kamuya açık isim her yerde `Dasvio` olmalı.
- İç kod adları (`Kasse360`, `Dojoneo`) tasarım diline taşınmamalı.

## 6. Ana Mesaj Hiyerarşisi

Tasarımcı headline ve görsel sistemi bu hiyerarşiye göre kurmalı.

### Ana mesaj

Restoranın tüm operasyonu tek platformda.

### Destek mesajları

- Misafir deneyimi ve operasyon aynı ekosistemde birleşir.
- QR menü, POS, rezervasyon ve CRM parçalı değil; birbiriyle bağlı çalışır.
- Şube sayısı arttıkça Dasvio daha değerli hale gelir.

### Hero için önerilen headline yönleri

Bu üç yönden biri seçilebilir:

1. `Restoranınızın Akıllı İşletim Sistemi`
2. `Ön tarafta misafir deneyimi, arka tarafta tam kontrol`
3. `POS'tan QR menüye, şubeden analitiğe tüm operasyon tek ekranda`

### Hero alt metin yönü

Kısa, tek nefeste okunan ve modüler ürünleri bağlayan bir metin olmalı:

`Dasvio; POS, QR Menü, rezervasyon, CRM, entegrasyonlar ve çok şubeli yönetimi tek platformda birleştirir.`

### Ana CTA

- `Demo Talep Et`

### İkincil CTA

- `Ürünü Gör`
- veya `Nasıl Çalıştığını Gör`

Not:

- Mevcut client içinde kayıt ve demo akışları var; bu nedenle CTA'ler gerçek dönüşüm aksiyonlarına bağlanabilecek kadar net olmalı.

## 7. Tasarım Hedefi

Yeni landing tek bir ürün şirketinin tek bir ana sayfası gibi hissettirmeli.

Şu anki dağınık yapıdaki temel problem:

- Ana landing sıcak, editorial ve yumuşak
- POS sayfası brutalist
- About sayfası farklı bir manifesto dili taşıyor
- Diğer ürün sayfaları başka bir visual system gibi davranıyor

Yeni tasarım bunları tek çatı altında toplamalı.

### Tasarım ilkeleri

1. Tek güçlü görsel sistem
- Farklı ürünleri tanıtırken farklı marka gibi görünmemeli.

2. Çift yüzey mantığı
- Misafirin gördüğü mobil yüzeyler ile işletmecinin gördüğü admin/operasyon yüzeyleri birlikte gösterilmeli.

3. Gerçek ürün hissi
- Soyut blob ve generic SaaS illüstrasyonları yerine ürün ekranları, device mockup'ları, branch/analytics/panel kompozisyonları kullanılmalı.

4. Premium hospitality hissi
- Yalnızca teknik değil, mekansal ve misafir odaklı bir estetik olmalı.

5. Modüler hikaye
- Ana landing ekosistemi anlatsın; alt ürün sayfaları detaya indirsin.

## 8. Önerilen Bilgi Mimarisi

Landing aşağıdaki akışta tasarlanmalı.

### 1. Sticky header + mega menu

Amaç:

- Ürün ekosistemini hızlıca taratmak
- Ana CTA'yi sürekli görünür tutmak

İçerik:

- Logo
- Ürünler / Çözümler mega menüsü
- Fiyat / Kaynaklar / Hakkımızda benzeri üst seviye linkler
- Demo CTA
- Giriş veya panel CTA

Mega menü içinde mutlaka ayrışması gereken grup başlıkları:

- POS
- QR Menü
- Rezervasyon
- CRM & Sadakat
- Çok Şubeli Yönetim
- Entegrasyonlar
- Analitik

### 2. Hero

Amaç:

- 5 saniyede doğru konumlandırma yapmak

İçerik:

- Güçlü headline
- Kısa açıklama
- 2 CTA
- 3 küçük güven cümlesi

Görsel yön:

- Sol tarafta söylem, sağ tarafta birleşik ürün kompozisyonu
- Tek bir laptop yerine daha güçlü bir kompozisyon önerilir:
  - admin dashboard
  - POS yüzeyi
  - mobil QR menü

Buradaki kritik mesaj:

`Bir sistem, üç yüzey: ekip, kasa, misafir`

### 3. Trust / proof bar

Amaç:

- Ürünün ciddi ve olgun olduğunu göstermek

İçerik tipleri:

- işletme sayısı
- sipariş hacmi
- aktif şehir / lokasyon
- uptime / canlı operasyon hissi
- entegrasyon logoları

Not:

- Sayısal veriler placeholder olarak tasarlanabilir; nihai rakamlar ürün/iş ekibinden teyit edilmeden sabitlenmemeli.

### 4. Platform overview bento

Amaç:

- Dasvio'nun sadece tek ürün olmadığını hızlıca göstermek

Bu bölümde 5-6 ana kart önerilir:

1. POS ve ödeme
2. QR Menü ve misafir deneyimi
3. Rezervasyon ve CRM
4. Analitik ve raporlama
5. Çok şubeli kontrol
6. Entegrasyonlar

Her kartta:

- kısa başlık
- tek cümlelik açıklama
- küçük ekran parçası veya mockup kırpımı
- ilgili detay sayfasına yönlenen link

### 5. Misafir yolculuğu bölümü

Amaç:

- Müşteri tarafını somutlaştırmak

Anlatılacak akış:

1. QR tarar
2. Menüyü kendi dilinde görür
3. Ürünü inceler
4. Alerjen / kategori / görsel bazlı karar verir
5. Masa bağlamında sipariş / ödeme / akış ilerler

Vurgulanacak gerçek capability'ler:

- çok dil
- tema özelleştirme
- gallery / spotlight
- masa bazlı akış
- mobil öncelikli deneyim

Görsel öneri:

- 2 veya 3 telefon frame'i
- biri karşılama ekranı
- biri kategori/ürün akışı
- biri sepet veya masa bağlamı

### 6. Operasyon cockpit bölümü

Amaç:

- İşletmecinin gördüğü kontrol katmanını göstermek

Anlatılacak capability'ler:

- cihaz yönetimi
- revenue center
- satış kanalları
- ürün / kategori / fiyat yönetimi
- raporlar

Görsel öneri:

- geniş dashboard kompozisyonu
- kartlar, tablo, grafik, cihaz durumu ve sipariş akışı birlikte görünmeli

Bu bölümün hissi:

`kaos değil, kontrol`

### 7. Çok şubeli yönetim bölümü

Amaç:

- Zincir restoran değer önerisini çok net vermek

Anlatılacak capability'ler:

- master menü
- şube atamaları
- override özeti
- fiyat kademeleri
- combo ve kampanya builder
- şube karşılaştırma

Görsel öneri:

- sol tarafta branch matrix / assignment yapısı
- sağ tarafta merkezi dashboard veya çok şubeli overview
- alternatif olarak harita + performans listesi

Bu bölüm ana landing'de kesinlikle yer almalı; Dasvio'nun ayırt edici değerlerinden biri burada.

### 8. Entegrasyonlar ve büyüme bölümü

Amaç:

- Dasvio'nun izole bir ürün olmadığını göstermek

Anlatılacak capability'ler:

- platform bağlantıları
- katalog / mapping akışları
- store status
- reviews / claims / pricing / reports

Görsel öneri:

- logo wall yerine daha operasyonel bir kurgu
- örneğin bağlantı kartları, mapping görünümü, status panelleri

Bu bölüm `bağlanabilirlik` ve `ölçeklenebilirlik` mesajı vermeli.

### 9. İkincil modüller bandı

Amaç:

- Ana landing'i uzatmadan ekosistemin genişliğini göstermek

Kompakt kartlar:

- Stok Yönetimi
- Signage / Mutfak ekranı
- Events
- PWA / teslimat odaklı yüzeyler

Bu alan ana yıldız değil, ama `Dasvio burada da var` duygusunu vermeli.

### 10. Sosyal kanıt / case snapshot

Amaç:

- İnsanların bu ürünü gerçekten kullandığını hissettirmek

İçerik önerileri:

- kısa müşteri alıntıları
- sektör bazlı kullanım senaryoları
- restoran / kafe / zincir örnekleri

Eğer net testimonial yoksa şu alternatif kullanılabilir:

- `Hangi işletme tipi için uygundur?` bölümü
- restoran, kafe, bar, QSR, zincir gibi segment kartları

### 11. Final CTA

Amaç:

- Sayfayı tek aksiyonla kapatmak

CTA yönü:

- Demo talep et
- veya uzmanla görüş

Altında şu güven cümleleri olabilir:

- hızlı kurulum
- ekiple onboarding
- modüler geçiş

## 9. Görsel Yön

### Genel estetik

Önerilen estetik: `premium hospitality meets operational software`

Yani:

- Çok steril beyaz SaaS hissi değil
- Çok karanlık cyber dashboard hissi değil
- Sıcak nötr tonlar + koyu kontrol yüzeyleri + temiz arayüz ritmi

### Renk yönü

Şu yaklaşım önerilir:

- ana zemin: kırık beyaz / taş tonları
- güçlü metin: koyu kömür / espresso
- vurgu: muted amber, olive, veya kontrollü koyu yeşil / sıcak indigo
- yardımcı yüzeyler: sisli gri, kum, açık taş

Amaç:

- restoran dünyasına yakın durmak
- aynı anda yazılım ürünü ciddiyeti taşımak

### Tipografi yönü

Tek başına default teknoloji fontu istemiyoruz.

Öneri:

- ana sans: güçlü, çağdaş, okunaklı bir UI ailesi
- yardımcı display: headline'larda sıcak ve karakterli bir eşlikçi aile

Önemli kriterler:

- Türkçe karakter desteği kusursuz olmalı
- mobilde okunabilir kalmalı
- fazla lüks moda markası hissine kaymamalı

### Görsel dil

- gerçek ürün ekranları kullanılsın
- device mockup'ları sadece dekor değil, ürün akışını anlatsın
- fotoğraf kullanılırsa gerçek mekan, servis ve masa atmosferi hissettirsin
- stok fotoğraf hissi minimize edilmeli

## 10. Motion ve Etkileşim

Motion dili gösteriş için değil, anlam için kullanılmalı.

İstediğimiz davranışlar:

- hero'da kontrollü reveal
- section geçişlerinde hafif ritim
- mega menu ve kart hover'larında net microinteraction
- sticky header davranışı

İstemediğimiz davranışlar:

- parallax şovuna dönüşmesi
- çok fazla floating blob
- her elemanın bağıra bağıra animasyonlu olması

## 11. Tasarımcının Hazırlaması Gereken Deliverable'lar

Minimum beklenti:

1. Desktop ana landing tasarımı
2. Mobile ana landing tasarımı
3. Header + mega menu state'leri
4. Hero için ana görsel kompozisyon
5. 5-6 section için component mantığında tasarım sistemi
6. CTA, kart, stat, testimonial ve proof bileşenleri için tekrar kullanılabilir pattern'ler

Ek olarak istenenler:

- section bazlı notlar / kullanım açıklamaları
- görsel asset ihtiyaç listesi
- hangi bölümlerde gerçek screenshot gerektiğinin işaretlenmesi

## 12. Implementasyon Kısıtları

Bu tasarım daha sonra mevcut React + Tailwind tabanlı client projesine uygulanacak. Bu yüzden:

- Çok kırılgan, yalnızca görsel şov için kurulmuş layout'lardan kaçınılmalı.
- Tasarım gerçek component mantığıyla bölünebilir olmalı.
- Desktop ve mobile arasında sadece küçülen değil, yeniden organize olan bir yapı düşünülmeli.
- CTA'ler gerçek akışlara bağlanabilecek kadar net olmalı.
- Çok fazla farklı kart tipi üretmek yerine sürdürülebilir sistem tercih edilmeli.

## 13. Tasarımda Özellikle Gösterilmesi Gereken Gerçek Ürün Unsurları

Bu unsurlar brief içinde kritik kabul edilmeli:

- misafir ekranı + operasyon ekranı ikilisi
- çok dil desteği
- QR tema özelleştirme mantığı
- cihaz / terminal görünürlüğü
- branch / enterprise kontrol yüzeyi
- entegrasyon ağı
- raporlama ve operasyon dashboard'u

## 14. Kaçınılması Gereken Yanlış Çerçeveler

Designer aşağıdaki yanlış pozisyonlara düşmemeli:

1. Sadece QR menü ürünü gibi göstermek
2. Sadece ödeme terminali şirketi gibi göstermek
3. Fazla fintech, fazla bankacılık görünümü vermek
4. Fazla generic SaaS görünmek
5. Her modüle ayrı mini marka yapmak

## 15. Gerekli Asset ve İçerik Listesi

Tasarım başlamadan önce ideal olarak toplanması gerekenler:

- gerçek admin dashboard screenshot'ları
- gerçek QR menü screenshot'ları
- POS / cihaz fotoğrafları veya yüksek kaliteli render'lar
- entegrasyon logoları
- teyitli metrikler
- 2-3 gerçek müşteri yorumu veya case bilgisi
- nihai fiyatlandırma yapısı varsa güncel paket bilgisi

## 16. Kısa Özet

Bu landing'in işi şudur:

- Dasvio'nun gerçek ürün gücünü tek hikâyede toplamak
- misafir deneyimi ile arka ofis kontrolünü aynı platform altında göstermek
- küçük işletmeden çok şubeli zincire kadar ölçeklenen bir sistem hissi vermek

Sayfa şu cümleyi görsel olarak söylemeli:

**Dasvio, restoranın ön yüzünü de arka operasyonunu da aynı sistemde birleştirir.**

Tasarım bu cümleyi ilk ekranda hissettirebiliyorsa doğru yoldayız.
