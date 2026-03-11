## Kayfe Landing Page Sıkı Görev Metni

Amaç: Kayfe için tek sayfalık, statik, tamamen HTML ve CSS ile hazırlanmış bir landing page prototipi üret.

Zorunlu kapsam:
- Sayfa Türkçe olacak.
- Yapı tek sayfa olacak.
- Kod yalnızca HTML ve CSS ile yazılacak. JavaScript ekleme, ancak HTML/CSS ile çözülemeyen kritik bir ihtiyaç varsa düşün.
- Tasarım responsive olacak. En az mobil, tablet ve masaüstü kırılımı düşün.
- `imgs/` klasöründeki mevcut görseller tasarıma dahil edilecek.
- QR alanları gerçek store bağlantılarına gitmeyecek. Bunlar temsili olacak ve açık biçimde "yakında" mesajı taşıyacak.
- Bölümler mutlaka bulunacak: hero, özellikler, nasıl çalışır, işletmeler bölümü, sıkça sorulan sorular, işletme başvuru formu, iletişim/footer.
- İşletme başvuru formu ilk sürümde `mailto:` ile çalışacak.
- Footer içinde yer tutucu iletişim bilgileri gösterilecek.

İçerik öncelikleri:
- Hem son kullanıcıya hem kafe sahibine hitap et.
- Kahve sadakati, hediye kahve, keşif, QR ile sipariş ve işletme analitiği gibi ana değer önerilerini görünür yap.
- Kahve tonlarında sıcak ama premium bir görsel dil kur.
- CTA yapısı iki odaklı olsun: uygulamayı keşfet ve işletme başvurusu yap.

Tasarım kuralları:
- Ortalama bir SaaS şablonuna benzemesin.
- Açık zemin, güçlü kontrast, katmanlı arka plan, kartlar ve belirgin tipografik hiyerarşi kullan.
- Renk sistemi CSS değişkenleri ile tanımlansın.
- Hover ve focus durumları belirgin olsun.
- Erişilebilirlik ihmal edilmesin: semantik etiketler, görünür focus, yeterli kontrast, anlamlı alt metinler.

Teknik teslimatlar:
- `index.html`
- `css/styles.css`
- `README.md`

HTML içinde mutlaka bulunması gerekenler:
- Üst navigasyon ve anchor linkler
- Güçlü hero alanı
- Temsili iki store QR kartı
- Özellik kartları
- 3 adımlı nasıl çalışır akışı
- İşletmeler için değer önerisi ve başvuru çağrısı
- `details/summary` ile SSS bölümü
- `mailto:` tabanlı işletme başvuru formu
- İletişim ve sosyal/kurumsal footer yapısı

CSS içinde mutlaka çözülmesi gerekenler:
- Mobilde tek kolon, geniş ekranda çok kolonlu düzen
- Hero görsel kompozisyonu
- Kart sistemi
- QR blok görselleştirmesi
- Form alanları ve butonlar
- Section spacing ve tipografi ölçeği

Kabul kriterleri:
1. Sayfa tek başına açıldığında eksiksiz bir landing page hissi vermeli.
2. QR kartları temsili olduğunu net anlatmalı.
3. Form `mailto:` ile çalışmalı.
4. İçerik hem son kullanıcıyı hem kafe sahiplerini ikna edecek yapıda olmalı.
5. Kod temiz, okunabilir ve kolay genişletilebilir olmalı.

Çalışma sırası:
1. HTML iskeletini kur.
2. CSS tasarım sistemini yaz.
3. Görselleri ve içerikleri yerleştir.
4. Responsive ayarları tamamla.
5. README ile kullanım ve özelleştirme notlarını ekle.

Not:
- Gerçek App Store ve Google Play linkleri daha sonra bağlanacak.
- Gerçek iletişim bilgileri daha sonra güncellenecek.
- Gerekirse ikinci iterasyonda form backend'e bağlanacak.