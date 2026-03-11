# Kayfe Landing Page Prototype

Bu klasör, Kayfe için hazırlanan statik landing page prototipini içerir. Sayfa yalnızca HTML ve CSS ile yazılmıştır.

## Dosyalar

- `index.html`: Tek sayfa landing page yapısı
- `css/styles.css`: Tüm stil sistemi ve responsive düzen
- `imgs/`: Tasarımda kullanılan mevcut konsept görseller
- `plan.md`: Uygulamaya yönelik sıkılaştırılmış görev metni

## Neler Var

- Hero alanı ve çift CTA yapısı
- Temsili App Store ve Google Play QR kartları
- Özellikler bölümü
- 3 adımlı nasıl çalışır akışı
- İşletmeler için değer önerisi
- `details/summary` tabanlı SSS bölümü
- `mailto:` ile açılan işletme başvuru formu
- Yer tutucu iletişim bilgileri bulunan footer

## Çalıştırma

Tarayıcıda doğrudan `index.html` dosyasını açabilirsiniz.

İsterseniz basit bir lokal sunucu ile de test edebilirsiniz:

```powershell
Set-Location c:\Users\11\Desktop\kayfeweb
Start-Process index.html
```

## Sonraki Güncellemeler

- Gerçek App Store ve Google Play linklerini QR alanlarına bağla
- Footer iletişim bilgilerini gerçek bilgilerle değiştir
- `mailto:` yerine canlı form endpoint'i ekle
- Marka fontu ve son logo geldiğinde görsel sistemi güncelle