# Dasvio Client Landing Refactor
## Icerik Odakli Master Brief (TR)

**Tarih:** 2026-05-08  
**Kapsam:** Dasvio anasayfa ve landing iceriklerinin tamamen yeniden yazilmasi  
**Ana hedef:** Tasarim onermek degil, icerik yapisini ve mesaj akislarini netlestirmek

---

## 1. Briefin Amaci

Bu dokumanin amaci, Dasvio anasayfasi icin uc seyi netlestirmektir:

1. Hangi mesaji, hangi sirayla verecegiz?
2. Hangi bolumde kullaniciya ne dedirtecegiz?
3. Hangi noktada hangi aksiyona cagri yapacagiz?

Bu belge teknik implementasyon veya gorsel stil tarifi vermez. Yalnizca icerik stratejisi, icerik hiyerarsisi, metin yapisi ve anasayfa karar akislarini tanimlar.

---

## 2. Is Problemi ve Iletisim Problemi

### 2.1 Is Problemi

Dasvio birden fazla urunu olan bir ekosistem ama kullanici bunu ilk dakikada tek bir sistem olarak anlamiyor.

### 2.2 Iletisim Problemi

1. Mesaj daginik: Ozellikler guclu ama ana hikaye tek cizgide ilerlemiyor.
2. Niyet ayrimi zayif: Demo isteyen, fiyat bakan, hemen baslamak isteyen ayni dilden karsilaniyor.
3. Ikna katmanlari eksik sirada: sorun -> cozum -> kanit -> aksiyon zinciri her yerde ayni netlikte degil.

---

## 3. Ana Mesaj Mimarisi

### 3.1 Tek Cumlelik Cekirdek Mesaj

Dasvio, restoranin tum operasyonunu tek platformda birlestirerek satisi buyutur, isi sadeleştirir ve yonetimi hizlandirir.

### 3.2 Mesaj Katmanlari

1. Katman 1 - Sonuc: Gelir artisi, operasyonel hiz, kontrol.
2. Katman 2 - Mekanizma: POS, QR menu, CRM, rezervasyon, mutfak, analitik birlikteligi.
3. Katman 3 - Kanit: Metrikler, referanslar, mini vaka anlatimlari.
4. Katman 4 - Aksiyon: Hemen basla, demo al, urune in.

### 3.3 Icerikte Kullanilacak Ana Sozluk

1. Hedef kelimeler: hiz, netlik, kontrol, tek merkez, anlik, olceklenebilir.
2. Kacinilacak kelimeler: asiri teknik terimler, anlami belirsiz hype kelimeleri.

---

## 4. Hedef Kitle ve Karar Niyetleri

### 4.1 Persona 1 - Bagimsiz Isletme Sahibi

1. Ne duymak ister: "Ugrastiran isleri azalt, gunu daha kolay yonet."
2. Ne sorar: "Kurulum zor mu? Hemen kullanabilir miyim?"
3. Hangi CTA'ya yakindir: Hemen basla.

### 4.2 Persona 2 - Operasyon Yoneticisi

1. Ne duymak ister: "Tum subeleri tek yerden izleyebilirim."
2. Ne sorar: "Anlik veri ne kadar guvenilir?"
3. Hangi CTA'ya yakindir: Demo talep et.

### 4.3 Persona 3 - Zincir Karar Verici

1. Ne duymak ister: "Standartlari merkezden korurum."
2. Ne sorar: "Buyudukce sistem nasil davranir?"
3. Hangi CTA'ya yakindir: Satisla gorus / ozel teklif.

---

## 5. Donusum Hedefleri ve Icerik Rolleri

1. Hero rolu: Ilk 8-10 saniyede ana degeri netlestirmek.
2. Orta bolum rolu: Kullanicinin kendi sorununu ekrana baglatmak.
3. Kanit bolumu rolu: "Inanmak" bariyerini asmak.
4. Fiyat bolumu rolu: "Secmek" bariyerini azaltmak.
5. Kapanis rolu: Tek ve net bir sonraki adim.

---

## 6. Detayli Anasayfa Akisi (Master Content Flow)

Bu bolum, anasayfanin en ustten en alta kadar icerik planidir. Her adimda amac, mesaj, alt metin, kanit ve CTA tanimlidir.

### 6.1 Bolum 01 - Header ve Ilk Navigasyon Mesaji

**Amac:** Daha scroll baslamadan urun kapsamini ve karar yollarini gostermek.

**Icerik yapisi:**
1. Sol: marka adi + kisa vaadin bir versiyonu.
2. Orta: Urun gruplari (Odeme, Operasyon, Buyume, Kaynaklar).
3. Sag: Giris + birincil CTA.

**Mesaj ilkesi:** "Dasvio bir ozellik degil, isletme sistemi" algisi.

**Mikro metin ornekleri:**
1. "Tumu tek platformda"
2. "2 dakikada genel bakis"
3. "Kurulum ucreti yok"

### 6.2 Bolum 02 - Hero (Deger Onermesi)

**Amac:** Kullaniciyi ilk bakista dogru cümleyle yakalamak.

**Ana baslik cizgisi (format):**
1. Sorun cagrisimi + sonuc vaadi
2. Ornek format: "Restoran yonetimindeki karmasayi azalt, karliligi artir."

**Alt metin (format):**
1. 2 cümle.
2. Ilk cümle fayda, ikinci cümle nasil.

**Guven satiri (hero alti):**
1. "Kurulum ucretsiz"
2. "14 gun deneme"
3. "Istedigin zaman iptal"

**CTA seti:**
1. Birincil: Hemen basla
2. Ikincil: Demo talep et

### 6.3 Bolum 03 - Problem Tanimi (Aci Nokta Bloku)

**Amac:** Kullaniciya "Evet, bu tam benim sorunum" dedirtmek.

**Icerik catisi:**
1. Siparis daginikligi
2. Stok belirsizligi
3. Personel koordinasyon zorlugu
4. Raporlara gec ulasma

**Yazim kalibi:**
1. "Bugun" cümlesi (mevcut sorun)
2. "Dasvio ile" cümlesi (cozum etkisi)

### 6.4 Bolum 04 - Cozum Haritasi (Ekosistem Anlatimi)

**Amac:** Urunlerin birlikte calistigini anlatmak.

**Alt bolumler:**
1. Siparis ve odeme: POS + QR
2. Mutfak ve servis: akisin hizlanmasi
3. Musteri bagliligi: CRM ve kampanya
4. Yonetim: anlik raporlar

**Icerik ilkesi:** Her alt bolumde "ne", "nasil", "ne kazandirir" uc adimi olmali.

### 6.5 Bolum 05 - Isletme Turune Gore Yol Secimi

**Amac:** Farkli segmentlerin kendine uygun yolu bulmasi.

**Segment kartlari icerigi:**
1. Restoran
2. Kafe
3. Hizli servis
4. Zincir

**Her kartta bulunacak metin:**
1. Kisa tanim
2. Oncelikli fayda
3. Ornek sonuc
4. Segmente ozel CTA

### 6.6 Bolum 06 - Is Akisi Hikayesi (Uctan Uca)

**Amac:** Dasvio'nun sadece ekran degil operasyon oldugunu gostermek.

**Hikaye sirası:**
1. Siparis alinir
2. Mutfaga duser
3. Servis tamamlanir
4. Odeme kapanir
5. Rapor guncellenir

**Icerik formati:** Her adim 1 baslik + 1 cümle + 1 olculebilir etki.

### 6.7 Bolum 07 - Sonuc Kartlari ve Kanitlar

**Amac:** "Calisir mi?" sorusuna guvenilir cevap.

**Kanit turleri:**
1. Ciro etkisi
2. Sepet ortalamasi etkisi
3. Islem hizi etkisi
4. Musteri memnuniyeti etkisi

**Kural:** Metriklerin yaninda baglam cümlesi bulunmali.

### 6.8 Bolum 08 - Musteri Hikayeleri

**Amac:** Benzer isletmelerin sonucunu gostermek.

**Her hikaye sablonu:**
1. Isletme tipi
2. Baslangic sorunu
3. Uygulanan cozum
4. 30-90 gunluk sonuc
5. Isletmeci alintisi

### 6.9 Bolum 09 - Fiyatlandirma ve Paket Secimi

**Amac:** Karari kolaylastirmak.

**Icerik zorunluluklari:**
1. Paket adi
2. Kime uygun oldugu
3. Dahil ozet
4. Dahil olmayanlarin netligi
5. Satisa konusan CTA

**Ek metin bloklari:**
1. "Plan secemiyorum" yardim metni
2. "Ne kadar surede canliya gecerim?" kisa yanit

### 6.10 Bolum 10 - Itiraz Yonetimi (Guven Bolumu)

**Amac:** Son karar oncesi tereddutleri azaltmak.

**Temel itirazlar ve yanit alanlari:**
1. "Gecis zor olur mu?"
2. "Ekip nasil alisir?"
3. "Destek ne kadar hizli?"
4. "Iptal etmek istersem ne olur?"

### 6.11 Bolum 11 - SSS Bolumu

**Amac:** Satis ekibine gitmeden once temel sorulari cevaplamak.

**Minimum SSS seti:**
1. Kurulum suresi
2. Cihaz uyumlulugu
3. Verilerin tasinmasi
4. Destek saatleri
5. Faturalama modeli
6. Sozlesme kosullari

### 6.12 Bolum 12 - Final CTA

**Amac:** Sayfayi tek net aksiyonla kapatmak.

**Kapanis metin yapisi:**
1. 1 cümlelik sonuc odakli kapanis
2. 1 destek cümlesi (risk azaltan)
3. 1 birincil + 1 ikincil CTA

---

## 7. Her Bolum Icin Ayrintili Icerik Sablonu

Asagidaki sablon, anasayfadaki her section icin ayni standartta icerik yazmak icin kullanilir.

1. Bolum amaci
2. Ana baslik (en fazla 8-10 kelime)
3. Alt aciklama (en fazla 2 cümle)
4. Kanit satiri (metrik veya guven cümlesi)
5. Birincil CTA metni
6. Ikincil CTA metni
7. O bolumde verilmek istenen tek karar

---

## 8. CTA Dil Rehberi (Icerik Perspektifi)

### 8.1 Yuksek Niyet

1. "Hemen Basla"
2. "Simdi Kayit Ol"
3. "Bugun Canliya Gec"

### 8.2 Orta Niyet

1. "Demo Talep Et"
2. "Uzmanla Gorus"
3. "Isletmene Uygun Plani Ogren"

### 8.3 Dusuk Niyet

1. "Nasil Calistigini Gor"
2. "2 Dakikada Kisa Tanitim"
3. "Sektorune Ozel Cok Satan Senaryo"

---

## 9. Form Icerigi ve Mikro Metinler

### 9.1 Demo Formu Alanlari

1. Isletme adi
2. Isletme tipi
3. Aylik siparis araligi
4. Telefon
5. E-posta
6. Not (istege bagli)

### 9.2 Alan Yardim Metinleri

1. "Bu bilgi sadece size uygun demo hazirlamak icin kullanilir."
2. "E-posta adresinize toplanti bilgisi gonderecegiz."

### 9.3 Hata Mesajlari

1. "Lutfen gecerli bir e-posta adresi girin."
2. "Telefon numarasi eksik veya hatali gorunuyor."
3. "Bu alan zorunludur."

### 9.4 Basari Mesaji

1. "Talebiniz alindi. Ekibimiz en kisa surede size ulasacak."
2. "Isterseniz simdi urun turunu secerek hizli on izleme yapabilirsiniz."

---

## 10. SSS Icerik Havuzu (Yaziya Hazir)

1. Dasvio'ya gecis ne kadar surer?
2. Mevcut menu ve urun verilerimi tasiyabilir miyim?
3. Ekip egitimi icin destek veriyor musunuz?
4. Hangi cihazlarla uyumlu?
5. Cok subeli yapida merkezi yonetim mumkun mu?
6. Paket degisikligini sonradan yapabilir miyim?
7. Teknik destek hangi saatlerde aktif?
8. Deneme suresi sonunda otomatik ucretlendirme olur mu?

---

## 11. 30-60-90 Gunluk Icerik Plani (Sayfa Sonrasi)

### 11.1 Ilk 30 Gun

1. Hero ve ana deger mesajinin netlestirilmesi
2. Fiyatlandirma metinlerinin sadeleştirilmesi
3. SSS ve guven katmaninin tamamlanmasi

### 11.2 60 Gun

1. Segment bazli mini case iceriklerinin eklenmesi
2. CTA metin varyantlarinin test edilmesi
3. Donusum hunisine gore metin iyilestirmesi

### 11.3 90 Gun

1. Performansli metinlerin kalici hale gelmesi
2. Zayif kalan bolumlerin yeniden yazimi
3. Yeni urun/ozellik duyurularinin icerik standardina baglanmasi

---

## 12. Kapsam Disi Olanlar

Bu briefin kapsaminda olmayanlar:

1. UI komponent cizimleri
2. Renk, tipografi, spacing secimi
3. Teknik kod mimarisi
4. Animasyon detaylari

---

## 13. Referans Incelenen Dosyalar

### Client
- [App.js](src/App.js)
- [DojoneoLanding.js](src/features/landing/pages/DojoneoLanding.js)
- [Header.js](src/features/landing/components/Header.js)
- [Hero.js](src/features/landing/components/Hero.js)
- [PaymentSolutions.js](src/features/landing/components/PaymentSolutions.js)
- [BusinessShowcase.js](src/features/landing/components/BusinessShowcase.js)
- [Features.js](src/features/landing/components/Features.js)
- [HowItWorks.js](src/features/landing/components/HowItWorks.js)
- [Pricing.js](src/features/landing/components/Pricing.js)
- [Testimonials.js](src/features/landing/components/Testimonials.js)
- [DemoAndCTA.js](src/features/landing/components/DemoAndCTA.js)
- [Footer.js](src/features/landing/components/Footer.js)
- [POSPage.js](src/features/landing/pages/POSPage.js)
- [QRMenuPage.js](src/features/landing/pages/QRMenuPage.js)

### Admin / Product Context
- [colors.js](../admin/src/theme/colors.js)
- [typography.js](../admin/src/theme/typography.js)
- [StatsHeader.js](../admin/src/components/common/StatsHeader.js)
- [THEME_MIGRATION_GUIDE.md](../admin/THEME_MIGRATION_GUIDE.md)
- [THEME_BATCH_PLAN_EASY_TO_HARD.md](../admin/THEME_BATCH_PLAN_EASY_TO_HARD.md)
- [MULTI_LOCATION_FRONTEND_ROADMAP(2).md](../admin/MULTI_LOCATION_FRONTEND_ROADMAP(2).md)

### Memory Context
- [dasvio-notes.md](../../memories/repo/dasvio-notes.md)
- [admin-copilot-import.md](../../memories/repo/admin-copilot-import.md)

---

## 14. Kisa Sonuc

Bu briefin basari tanimi, "daha guzel bir sayfa" degil, "daha net bir karar akisi"dir. Kullanici anasayfayi bitirdiginde su uc sorunun cevabini net almis olmalidir:

1. Dasvio bana ne kazandirir?
2. Benim isletmem icin hangi yol dogru?
3. Simdi hangi adimi atmam gerekiyor?

---

## 15. Anasayfa Icin Hazir Icerik Paketi (Final Copy Deck)

Bu bolum, anasayfa refaktorunde dogrudan kullanilabilecek metin setlerini icerir.

### 15.1 Hero Baslik Alternatifleri

1. Restoran operasyonunu sadeleştir, geliri buyut.
2. Siparisten odemeye, tek platformla tam kontrol.
3. Dasvio ile restoranini daha hizli, daha karlı yonet.
4. Daginik sistemleri birlestir, tek merkezden yonet.
5. Isini kolaylastir, musterine daha iyi deneyim sun.

### 15.2 Hero Alt Metin Alternatifleri

1. Dasvio; POS, QR menu, mutfak akis ve raporlamayi tek noktada toplar. Ekip daha hizli calisir, sen anlik olarak tum isleri takip edersin.
2. Siparis, servis, odeme ve raporlama arasindaki kopukluklari kapat. Daha az hata, daha hizli operasyon, daha net karar.
3. Restoranin gunluk karmasasini azaltan bir isletim sistemi: tek panel, tek akis, daha cok kontrol.

### 15.3 Hero Guven Satiri Alternatifleri

1. Kurulum ucreti yok
2. 14 gun deneme
3. Diledigin zaman iptal
4. Ekip egitimi destegi
5. Hızlı canliya gecis

### 15.4 Hero CTA Alternatifleri

1. Birincil: Hemen Basla
2. Birincil: Ucretsiz Dene
3. Birincil: Simdi Basvur
4. Ikincil: Demo Talep Et
5. Ikincil: 2 Dakikada Nasil Calistigini Gor

---

## 16. Bolum Bazli Uzun Icerik Metinleri

### 16.1 Problem Bolumu - Uzun Metin

Restoran yonetimi cogu zaman tek bir is degil, ayni anda bircok yangini sondurme hali. Bir yanda siparisler, bir yanda mutfak akis, diger yanda odeme ve gun sonu raporlari. Veriler farkli yerlerde oldugunda ekip yavaslar, hata artar ve karar almak zorlasir.

Dasvio bu daginik yapiyi tek bir operasyon akisina cevirir. Siparis alindigi andan odeme kapanisina kadar tum adimlar birbiriyle bagli calisir. Sonuc olarak ekip daha hizli hareket eder, yonetici daha net gorur, isletme daha saglikli buyur.

### 16.2 Cozum Haritasi - Uzun Metin

Dasvio'da her urun tek basina degil, birbiriyle konusan bir sistemin parcasi olarak calisir.

1. POS ve QR menu birlikte calisarak siparis kaynagini tek akisa toplar.
2. Mutfak akis yonetimi, siparisin dogru zamanda dogru istasyona ulasmasini saglar.
3. CRM ve kampanya katmani, tekrar ziyaret ve sepet buyuklugune odaklanir.
4. Raporlama katmani, tum bu hareketleri anlik olarak isleyerek karar almayi hizlandirir.

Bu yapi sayesinde isletme, gunluk kararlarini tahminle degil veriye dayanarak alir.

### 16.3 Isletme Turune Gore Cozum - Uzun Metin

Her isletmenin operasyon ritmi farklidir. Dasvio icerigi bu farklari gorunur kilacak sekilde kurgulanmalidir.

1. Restoran: Masa donus hizi, servis kalitesi ve maliyet kontrolu odagi.
2. Kafe: Hızlı siparis, tekrar musteri ve pratik personel kullanimi odagi.
3. Hizli servis: Islem hizi, kuyruk yonetimi ve standart operasyon odagi.
4. Zincir: Merkezi denetim, sube karsilastirmasi ve olceklenebilirlik odagi.

Her segmentte metin, tek bir cümlede suyu vermelidir: "Bu sistem benim isletme tipime gore dusunulmus."

### 16.4 Sonuc ve Kanit Bolumu - Uzun Metin

Kullanicinin karar vermesi icin sadece ozellik degil, sonuc gormesi gerekir. Bu nedenle kanit bolumu metrik listesinden degil, baglamli sonuc cumlelerinden olusmalidir.

Ornek yapi:

1. "QR menu ile siparis suresi kisaldi, yogun saatlerde masa donus hizi artti."
2. "Kampanya yonetimi ile ortalama sepet tutarinda artis yakalandi."
3. "Tek panel raporlama ile gun sonu degerlendirmesi daha hizli tamamlandi."

Metrik varsa mutlaka "hangi kosulda" ve "hangi surede" elde edildigi belirtilmelidir.

### 16.5 Fiyatlandirma Gecis Metni - Uzun Metin

Paket secimi, kullanicinin en cok duraksadigi noktalardan biridir. Bu bolumdeki icerik "fiyat gostermek" yerine "dogru paketi secmeyi kolaylastirmak" amaciyla yazilmalidir.

Metin tonu:

1. Acik
2. Karsilastirilabilir
3. Gizli kosul barindirmayan

Kullaniciya su hissi verilmelidir: "Ne odedigimi, ne aldigimi ve ne zaman degistirebilecegimi net biliyorum."

### 16.6 Guven ve Itiraz Bolumu - Uzun Metin

Bu bolum satis baskisi yapan bir dilde degil, belirsizligi azaltan bir dilde yazilmalidir.

Odak cumleleri:

1. "Gecis surecinde yalniz degilsiniz."
2. "Ekip alisma sureci icin rehberlik saglaniyor."
3. "Ihtiyaciniz buyudukce planinizi esnetebilirsiniz."
4. "Memnun kalmazsaniz cikis sureci nettir."

---

## 17. Tam Detayli Anasayfa Akis Senaryosu (Scroll-By-Scroll)

Bu senaryo, kullanicinin sayfayi asagidan yukariya degil yukaridan asagiya nasil deneyimleyecegini metin perspektifinden anlatir.

### 17.1 Scroll 1 - Ilk Temas

Kullanici markayi gorur ve sunu anlar: "Bu site restoran operasyonunu kolaylastirmayi vadediyor."

Gorunmesi gereken metin unsurlari:

1. Ana baslik
2. 1-2 cümlelik net alt aciklama
3. Guven satirlari
4. Iki net CTA

### 17.2 Scroll 2 - Sorun Eslestirme

Kullanici su anki aci noktasini gorur: "Evet, bizde de bu sorun var."

Gorunmesi gereken metin unsurlari:

1. 3-4 aci nokta basligi
2. Her aci noktaya kisa baglam
3. Cozume baglayan tek gecis cümlesi

### 17.3 Scroll 3 - Cozum Mimarisi

Kullanici suyu anlar: "Bu urunler ayri ayri degil, birlikte calisiyor."

Gorunmesi gereken metin unsurlari:

1. Uctan uca akis anlatimi
2. Her adimda net fayda
3. Bu bolum sonu orta niyet CTA

### 17.4 Scroll 4 - Segment Eslestirme

Kullanici kendi isletme tipini secerek ilgili mesaji gorur.

Gorunmesi gereken metin unsurlari:

1. Segment adi
2. O segmente ozel birinci problem
3. O segmente ozel birinci fayda
4. Segmente ozel CTA

### 17.5 Scroll 5 - Kanit ve Guven

Kullanici "Calisir mi?" sorusuna cevap bulur.

Gorunmesi gereken metin unsurlari:

1. Metrik kartlari
2. Kisa musteri alintilari
3. "Nasildi -> ne degisti" anlatimi

### 17.6 Scroll 6 - Karar ve Kapanis

Kullanici paket secer veya demo birakir.

Gorunmesi gereken metin unsurlari:

1. Paketlerin kime uygun oldugu
2. SSS ile son belirsizliklerin kapanmasi
3. Final CTA ve destek metni

---

## 18. Persona Bazli Mesaj Setleri (Hazir)

### 18.1 Bagimsiz Isletme Sahibi Icin Mesajlar

1. Gunun her anina yetismek zorunda degilsiniz.
2. Dasvio, ekip icindeki daginikligi azaltir ve operasyonu sadeleştirir.
3. Siz isletmenin yonunu dusunurken sistem gunluk akisi toplar.

### 18.2 Operasyon Yoneticisi Icin Mesajlar

1. Tek panelde anlik gorunurluk, daha hizli karar.
2. Subeler arasi farklari erken gor, hizli aksiyon al.
3. Raporu bekleme, operasyonu canli izle.

### 18.3 Zincir Karar Verici Icin Mesajlar

1. Standart operasyonu tum subelerde koru.
2. Merkezi yonetimle buyumeyi kontrol altinda tut.
3. Buyurken karmaşa degil sistem buyusun.

---

## 19. Anasayfa Icin Hazir Mikro Metin Kutuphanesi

### 19.1 Guven Rozeti Metinleri

1. Ucretsiz kurulum
2. Hizli canliya gecis
3. Rehberli onboarding
4. Esnek paket gecisi
5. Destek ekibi yaninizda

### 19.2 Ara Gecis Cumleleri

1. Simdi bunu adim adim gorelim.
2. Peki bu sistem gercekte nasil calisiyor?
3. Isletme tipine gore fark ne yaratiyor?
4. Sonuclara birlikte bakalim.

### 19.3 Bos Durum Metinleri

1. Henuz veri yok. Ilk adimi atinca metrikler burada gorunecek.
2. Bu alanda yakinda daha fazla ornek hikaye paylasacagiz.
3. Isterseniz bu asamada demo talebi birakabilirsiniz.

### 19.4 Hata Mesaji Metinleri

1. Bir seyler ters gitti. Lutfen tekrar deneyin.
2. Baglanti hatasi olustu. Kisa bir sure sonra yeniden deneyebilirsiniz.
3. Bilgiler kaydedilemedi. Alanlari kontrol edip tekrar gonderin.

---

## 20. SSS Bolumu Icin Hazir Yanitlar

### 20.1 Dasvio'ya gecis ne kadar surer?

Gecis suresi isletmenizin operasyon karmasina gore degisir. Temel kurulumlar genelde kisa surede tamamlanir. Menu yapisi, cihaz durumu ve ekip buyuklugune gore planlama birlikte netlestirilir.

### 20.2 Mevcut menu ve urun verilerimi tasiyabilir miyim?

Evet. Mevcut verilerinizi aktarmak icin uygun tasima adimlari belirlenir. Hedef, operasyonu durdurmadan gecisi planli sekilde tamamlamaktir.

### 20.3 Ekip egitimi icin destek veriyor musunuz?

Evet. Ekip adaptasyonunu hizlandirmak icin onboarding ve kullanim rehberligi saglanir. Amaç, sistemin gunluk rutinde hizlica benimsenmesidir.

### 20.4 Hangi cihazlarla uyumlu?

Kullanim senaryosuna gore uygun cihaz setleri planlanir. Mevcut altyapiyla calisma durumu ve gerekli tamamlayici ihtiyaclar birlikte degerlendirilir.

### 20.5 Cok subeli yapida merkezi yonetim mumkun mu?

Evet. Cok subeli yapilar icin merkezi takip ve operasyon karsilastirma kabiliyetleriyle subeler arasi standardizasyon desteklenir.

### 20.6 Paket degisikligini sonradan yapabilir miyim?

Ihtiyaciniz degistikce paketinizi guncelleyebilirsiniz. Hedef, isletme buyurken sistemin de birlikte esneyebilmesidir.

### 20.7 Teknik destek hangi saatlerde aktif?

Destek kanallari ve cevap sureleri paket ve ihtiyaca gore net olarak paylasilir. Oncelik, operasyonu aksatmadan hizli geri donus saglamaktir.

### 20.8 Deneme suresi sonunda otomatik ucretlendirme olur mu?

Deneme ve devam kosullari onceden acikca belirtilir. Surpriz maliyet olusmamasina yonelik bilgilendirme sureci net sekilde ilerletilir.

---

## 21. Form ve Donusum Akisi Icerik Detayi

### 21.1 Demo Talep Formu Acilis Metni

Isletmenize en uygun senaryoyu gosterebilmemiz icin kisa bir bilgi birakin. Ekibimiz size uygun bir demo akisiyla ulasacak.

### 21.2 Form Alan Basliklari (Hazir)

1. Isletme Adi
2. Isletme Turu
3. Aylik Siparis Araligi
4. Iletisim Telefonu
5. Is E-postasi
6. Ek Not (Opsiyonel)

### 21.3 Form Yardim Metinleri (Hazir)

1. Isletme Turu: "Size uygun kullanim senaryosunu hazirlamak icin."
2. Siparis Araligi: "Plan ve akis onerimizi daha dogru sekillendirmek icin."
3. Is E-postasi: "Demo daveti ve ozet bilgileri bu adrese gonderilir."

### 21.4 Form Sonrasi Mesajlar

1. Anlik onay: "Talebiniz alindi."
2. Beklenti yonetimi: "Ekibimiz en kisa surede sizinle iletisime gececek."
3. Yonlendirme: "Bu arada isletme tipinize ozel cozumleri inceleyebilirsiniz."

---

## 22. CTA Varyant Paketi (A/B/C)

### 22.1 Birincil CTA Varyantlari

1. Hemen Basla
2. Simdi Basvur
3. Ucretsiz Dene
4. Bugun Canliya Gec

### 22.2 Ikincil CTA Varyantlari

1. Demo Talep Et
2. Uzmanla Gorus
3. Nasil Calistigini Gor
4. Isletmene Uygun Paketi Ogren

### 22.3 Kapanis CTA Varyantlari

1. Dasvio ile baslamak icin ilk adimi simdi at.
2. Operasyonunu tek merkezde toplamak icin ekibimizle gorus.
3. Isletmene uygun akis planini birlikte cikaralim.

---

## 23. Redaksiyon ve Dil Kontrol Kurallari

1. Her paragraf tek bir fikir tasimali.
2. 20 kelimeyi asan cümleler mumkunse bolunmeli.
3. Teknik terimler yerine isletme dili kullanilmali.
4. Her bolumde en az bir karar cümlesi olmali.
5. Abartili kesinlik bildiren ifadelerden kacınılmali.
6. "Nasil" ve "Neden" sorulari metin icinde karsilanmali.

---

## 24. Icerik Teslim Kontrol Listesi

1. Hero metinleri (3 baslik + 3 alt metin) tamam mi?
2. Problem bolumunde 4 aci nokta net mi?
3. Cozum haritasinda urun birlikteligi anlasilir mi?
4. Segment bolumunde her segmentin ayrik faydasi yazili mi?
5. Kanit bolumunde baglamli metrik var mi?
6. Fiyat bolumunde "kime uygun" ifadeleri net mi?
7. Itiraz bolumunde en az 4 tereddut yanitlandi mi?
8. SSS bolumunde temel karar sorulari var mi?
9. Form hata/basari metinleri tamam mi?
10. Final CTA cümlesi tek ve net mi?
