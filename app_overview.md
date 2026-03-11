# Kayfe - Uygulama Genel Bakış

## Vizyon

Kayfe, zincir olmayan bağımsız kahvecileri tek bir platform altında toplayan bir sadakat (loyalty) ve sipariş uygulamasıdır. Anlaşmalı tüm kafelerde geçerli olan yıldız toplama sistemi, kampanyalar, görevler ve hediye kahve özellikleriyle kullanıcılara benzersiz bir kahve deneyimi sunar.

## Hedef Kitle

- **Kullanıcılar (B2C):** Kahve seven, farklı kafeler keşfetmek isteyen, kampanya ve ödüllerle motive olan bireyler
- **Kafe Sahipleri (B2B):** Yeni müşteri kazanmak, mevcut müşterilerini elde tutmak ve müşteri verilerini analiz etmek isteyen bağımsız kafe işletmeleri

## İş Modeli

- Kafelere aylık abonelik bazlı SaaS satışı
- Kafeler: sadakat sistemi + yeni müşteri potansiyeli + müşteri data analitiği elde eder
- Hedef: Ankara merkezli başlangıç, 300-500 kafe ağı

---

## Uygulama Yapısı

### Tab Bar Navigasyonu (5 Ana Sekme)

| Tab | Açıklama |
|-----|----------|
| **Jest** | Arkadaşlara hediye kahve gönderme |
| **Sosyal** | Liderlik tablosu, aylık yarışmalar |
| **Anasayfa** | Ana ekran, kampanyalar, yakın kafeler |
| **Kafeler** | Harita ve liste görünümünde kafe keşfi |
| **Hesap** | Profil, sipariş geçmişi, ayarlar |

---

## Ekranlar ve Özellikler

### 1. Anasayfa

- **Karşılama:** Zamana göre selamlama ("İyi günler, {isim}")
- **Yıldız İlerlemesi:** Dairesel progress göstergesi (ör: 4/7 yıldız), toplam yıldız sayısı
- **Kampanyalar Carousel:** Yatay kaydırılabilir kampanya kartları
  - "1 Kahve = 1 Yıldız"
  - "Sosyal listesinde ilk 15 kişiye hediye kahve"
  - "7 yıldız topla, hediye kahve kazan"
- **Yakınındaki Kafeleri Bul:** Konum bazlı kafe önerileri
- **Kafeler Listesi:** Anlaşmalı kafelerin kartları
- **Oyna Kazan Butonu:** Mini oyunlara yönlendiren floating button

### 2. Kafeler (Harita)

- **Harita Görünümü:** Google Maps entegrasyonu, kafe pinleri
- **Arama:** Kafe adına göre arama
- **Şehir Filtresi:** Şehir seçimi ile filtreleme
- **Kafe Listesi:** Her kafe için:
  - Kafe adı ve şube bilgisi
  - Tam adres
  - Yol tarifi butonu
  - Detay (info) butonu

### 3. Kafe Detay & Sipariş Akışı

- **Menü Listeleme:** Kafenin tüm ürünleri kategorize şekilde listelenir
- **Sepet:** Ürünler sepete eklenir
- **QR Kod Üretimi:** Sepet onaylandıktan sonra QR kod oluşur
- **Sipariş Teslimi:** Kafe sahibi/garson admin app'inden QR'ı okutarak siparişi teslim eder
- **Yıldız Kazanımı:** Teslim sonrası alınan ürünlere göre yıldız hesaplanır ve kullanıcıya eklenir

### 4. Jest (Hediye Kahve)

- **Hediye Kartı Seçimi:** Kategorize kartlar:
  - "In Love with Coffee" - kahve temalı kartlar
  - "Special Days" - özel günler (Anneler Günü, doğum günü vb.)
  - "Sorry & Thanks" - teşekkür/özür kartları
- **Alıcı Bilgileri:**
  - Telefon numarası
  - Arkadaşın adı
  - Kişisel not/mesaj
- **Gönderim:** Alıcıya bildirim gider, uygulama açıldığında popup ile hediye gösterilir
- **Hediye Alım Popup'ı:** "{İsim} sana bir hediye gönderdi!" mesajı + kart görseli + kişisel not

### 5. Sosyal (Liderlik Tablosu)

- **Aylık Yarışma:** Her ay en çok yıldız toplayana ödüller
  - Ödül örnekleri: Apple AirPods, JBL Hoparlör, Stanley Termos
- **Liderlik Sıralaması:** Kullanıcı listesi:
  - Sıra numarası
  - Avatar/profil baş harfi
  - Kullanıcı adı
  - Toplam yıldız sayısı
  - Toplam kahve sayısı (bardak ikonu)
- **Refresh:** Manuel yenileme butonu

### 6. Görevler (Kahve Maceram)

Modal olarak açılır, iki sekmeli:

#### Görevlerim Tab
- İlerleme çubuğu ile görev takibi
- Görev örnekleri:
  - "5 gün üst üste kahve iç" → 2 yıldız ödül
  - "3 farklı yerden kahve iç" → 2 yıldız ödül
  - "2 kupon kullan" → 2 yıldız ödül
- Her görev: ikon, başlık, açıklama, ilerleme (ör: 0/5), yıldız ödülü

#### Rozetlerim Tab
- **Rozet Özeti:** Kazanılan / Kazanılmayı bekleyen rozet sayısı
- **Rozet Grid:** 2x2 grid'de rozet ikonları
  - Kahve çekirdeği rozeti
  - Konum/keşif rozeti
  - Taç/VIP rozeti
  - Barista rozeti
- Rozetler kazanılmadan önce gri, kazanıldıktan sonra renkli

### 7. Mini Oyunlar (Oyna Kazan)

- **Memory Match:** Kart eşleştirme oyunu
- **Coffee Bird:** Flappy Bird tarzı kahve temalı oyun
- **Color Match:** Renk eşleştirme refleks oyunu
- Her oyundan yıldız kazanılabilir
- Oyunlar WebView veya native olarak entegre

### 8. Hesap

- **Profil Kartı:** Avatar + kullanıcı adı
- **Menü Öğeleri:**
  - Profil Yönetimi (biyografi, lucky number)
  - Geçmiş Siparişlerim
  - Kazançlarım (yıldızlar, hediyeler, kampanyalar)
  - Ayarlar
  - S.S.S.
  - Hakkımızda
  - Üye İş Yeri Olmak İstiyorum (kafe başvuru formu)
  - Şikayet ve Öneriler

---

## Temel Akışlar

### Sipariş Akışı
```
Kullanıcı kafe seçer → Menüden ürün seçer → Sepete ekler →
Siparişi onaylar → QR kod oluşur → Garson/kafe sahibi QR okutır →
Sipariş teslim edilir → Yıldızlar hesaba eklenir
```

### Yıldız Kazanma Yolları
1. **Sipariş:** Her kahve alımında ürüne göre yıldız
2. **Görevler:** Belirli görevleri tamamlayarak (streak, keşif, kupon kullanımı)
3. **Mini Oyunlar:** Oyun skorlarına göre yıldız
4. **Kampanyalar:** Özel kampanya dönemlerinde bonus yıldız

### Yıldız Harcama
- Belirli yıldız eşiğine ulaşınca ücretsiz kahve kuponu
- İlerleme: Dairesel gösterge ile kaç yıldız kaldığı görünür (ör: 4/7)

### Hediye Kahve Akışı
```
Jest tabına git → Hediye kartı seç → Alıcı telefon no gir →
Arkadaşın adını yaz → Kişisel not ekle → Gönder →
Alıcıya bildirim gider → Alıcı uygulamada hediyeyi görür ve kullanır
```

---

## Kullanıcı Rolleri

### Müşteri (Consumer App - Bu Uygulama)
- Kafe keşfi ve menü görüntüleme
- Sepet oluşturma ve QR kod üretme
- Yıldız toplama ve harcama
- Görev tamamlama ve rozet kazanma
- Hediye kahve gönderme/alma
- Liderlik tablosunda yarışma
- Mini oyun oynama
- Sipariş geçmişi görüntüleme

### Kafe Sahibi / Garson (Admin App - Ayrı Uygulama)
- QR kod okutma ile sipariş teslimi onaylama
- Menü yönetimi (ürün ekleme/düzenleme/fiyatlandırma)
- Müşteri data analitiği (en çok satan ürün, en sık gelen müşteri vb.)
- Kampanya yönetimi

---

## Teknik Mimari

### Neden Expo SDK 55?

SDK 55 bu proje için özellikle uygun çünkü birçok ihtiyacımızı native seviyede karşılıyor:

| Expo 55 Özelliği | Kayfe'de Kullanımı |
|---|---|
| **Native Tabs API** | 5 tabli ana navigasyon (Jest, Sosyal, Anasayfa, Kafeler, Hesap) — platform-native tab deneyimi, iOS'ta UITabBarController, Android'de Material tabs |
| **Apple Zoom Transition** | Kafe kartından detay sayfasına geçişlerde shared element transition (iOS'ta default aktif) |
| **Form Sheet Footers** | Sipariş onay modalı, görev detay sheet'leri için action butonları |
| **Typed Routes** | `typedRoutes: true` ile tüm route'lar type-safe, yanlış navigasyon derleme zamanında yakalanır |
| **React Compiler** | `reactCompiler: true` — otomatik memoization, manuel useMemo/useCallback gereksiz |
| **expo-image (HDR + SF Symbols)** | Kafe görselleri HDR destekli, tab/header ikonları SF Symbols ile native |
| **Xcasset Icon Support** | Tab ve header ikonları doğrudan Xcode asset catalog'dan |
| **Safe Area Handling** | Native-tabs layout'larında otomatik inset yönetimi, ekstra SafeAreaView sarmalı gereksiz |
| **Synchronous Layout Updates** | Navigasyon geçişlerinde görsel sıçrama yok |
| **expo-crypto (AES-GCM)** | QR kod payload şifreleme — siparişlerin güvenliği |
| **expo-sqlite (DevTools + tagged templates)** | Offline sipariş cache, görev ilerlemesi local storage, type-safe SQL |
| **Hermes Bytecode Diffing** | OTA update boyutu ~%75 küçülür (SDK 56'da default olacak, şimdiden opt-in edilebilir) |
| **Colors API (expo-router)** | Android'de Material 3 dynamic colors, iOS'ta adaptive renkler — tema uyumu |
| **expo-sharing (receive)** | İleride: arkadaşlardan gelen hediye kahve deep link'lerini share extension ile yakalama |

### Frontend (Bu Repo)
- **Framework:** Expo SDK 55 (React Native 0.83, React 19.2)
- **Routing:** Expo Router (file-based, typed routes, native tabs)
- **State:** (Belirlenecek - Context API / Zustand)
- **Styling:** Global CSS + themed components
- **Animations:** React Native Reanimated 4.2

### Backend
- **Platform:** Supabase
  - **Auth:** Kullanıcı kimlik doğrulama (telefon/email)
  - **Database:** PostgreSQL (kafeler, menüler, siparişler, yıldızlar, görevler, rozetler)
  - **Realtime:** Sipariş durumu güncellemeleri, bildirimler
  - **Storage:** Kafe görselleri, profil fotoğrafları, hediye kartı görselleri
  - **Edge Functions:** QR doğrulama, yıldız hesaplama, görev kontrolü, bildirim gönderimi
  - **Row Level Security:** Kullanıcı bazlı veri erişim kontrolü

### Entegrasyonlar
- **Harita:** Google Maps (kafe konumları, yol tarifi)
- **Bildirimler:** Push notifications (hediye bildirimi, kampanya, sipariş durumu)
- **QR:** QR kod üretme (kullanıcı) ve okuma (admin app)
- **Deep Linking:** URL scheme "kayfe" (hediye kahve paylaşımı, kampanya linkleri)

---

## Supabase Veritabanı Tabloları (Taslak)

| Tablo | Açıklama |
|-------|----------|
| `users` | Kullanıcı profilleri, yıldız bakiyesi |
| `cafes` | Kafe bilgileri, konum, çalışma saatleri |
| `menu_categories` | Menü kategorileri (sıcak içecekler, soğuk vb.) |
| `menu_items` | Ürünler, fiyat, yıldız değeri |
| `orders` | Siparişler, QR kodu, durum |
| `order_items` | Sipariş kalemleri |
| `stars_transactions` | Yıldız kazanım/harcama geçmişi |
| `campaigns` | Kampanyalar, başlangıç/bitiş tarihi |
| `missions` | Görev tanımları, yıldız ödülü |
| `user_missions` | Kullanıcı görev ilerlemesi |
| `badges` | Rozet tanımları |
| `user_badges` | Kullanıcının kazandığı rozetler |
| `gifts` | Hediye kahve gönderimleri |
| `gift_cards` | Hediye kartı şablonları, kategorileri |
| `leaderboard` | Aylık liderlik tablosu snapshot'ları |
| `cafe_staff` | Kafe çalışanları (admin app erişimi) |

---

## Tasarım ve UX Prensipleri

> **Not:** `imgs/` klasöründeki görseller sadece konsepti anlamak içindir.
> Kayfe'nin tasarımı sıfırdan oluşturulacak — renk paleti, ödül sistemi
> (yıldız yerine başka bir metafor olabilir) ve genel görsellik tamamen değişebilir.

### Hedef: Her Yaştan Kullanıcı İçin Kolay Kullanım

Uygulama 18 yaşındaki üniversiteli de, 60 yaşındaki emekli de rahatça kullanabilmeli.

### UI Kuralları

- **Büyük dokunma alanları:** Minimum 48x48dp tap target, parmak dostu butonlar
- **Okunabilir tipografi:** Body text en az 16px, başlıklar belirgin hiyerarşi. Sistem font scale'e saygı (Dynamic Type / Android font scaling)
- **Yüksek kontrast:** WCAG AA minimum (4.5:1 metin, 3:1 büyük metin/ikonlar). Dark ve light modda ayrı ayrı test
- **Tutarlı ikon + label:** Tabbar ve butonlarda sadece ikon yeterli değil — mutlaka altında kısa label olacak
- **Boşluk ve nefes:** Sıkışık layout yok, kartlar arası yeterli padding, scroll alanı rahat
- **Renk körü dostu:** Bilgi sadece renkle iletilmez, ikon/şekil/metin ile desteklenir

### UX Kuralları

- **Maksimum 3 adım:** Temel akışlar (sipariş ver, hediye gönder) en fazla 3 adımda tamamlanmalı
- **Tek elle kullanım:** Kritik butonlar ekranın alt yarısında, baş parmak erişim alanında (thumb zone)
- **Anında geri bildirim:** Her etkileşimde mikro-animasyon veya haptic feedback. Yükleniyor durumları skeleton/shimmer ile
- **Tanıdık pattern'ler:** Bilinen UI kalıpları kullanılacak (pull-to-refresh, swipe-to-dismiss, bottom sheet). Kullanıcıyı yeni birşey öğrenmeye zorlamayacak
- **Açık ve sade dil:** Teknik jargon yok, herkesin anlayacağı Türkçe. Buton metinleri eylem odaklı ("Sipariş Ver", "Hediye Gönder")
- **Hata kurtarma:** Yanlış yapılan her işlem geri alınabilir. Destructive action'lardan önce onay dialogu
- **Progressive disclosure:** Karmaşık bilgi tek seferde gösterilmez, katman katman açılır (ör: önce kafe kartı → detayda menü → menüde ürün detayı)
- **Boş durum (empty state):** Her liste boşken ne yapılacağını anlatan yönlendirici mesaj + CTA butonu
- **Onboarding:** İlk açılışta kısa ve atlanabilir tanıtım. Özellik keşfi contextual tooltip'lerle

### Erişilebilirlik

- Tüm görsellere `accessibilityLabel` eklenecek
- Navigasyon VoiceOver (iOS) ve TalkBack (Android) ile test edilecek
- Animasyonlar `prefers-reduced-motion` ayarına saygı gösterecek (Reanimated ile kontrol)
- Focus order mantıklı sırada olacak (tab/screen reader akışı)

### Renk Paleti (Taslak - Değişebilir)

Kesin palet tasarım aşamasında belirlenecek. Genel yön:
- **Premium ama sıcak:** Kahve markalarının soğuk kurumsal havası yerine, samimi ve davetkar
- **Dark/Light mode:** `userInterfaceStyle: "automatic"` — her iki temada da tutarlı deneyim
- **Semantic renkler:** Başarı (yeşil), uyarı (turuncu), hata (kırmızı), bilgi (mavi) sabit kalacak
- **Marka rengi:** 1 primary + 1 accent yeterli, fazla renk kullanmayacağız
