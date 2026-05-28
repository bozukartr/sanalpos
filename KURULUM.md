# SanalPOS — Kurulum Rehberi

## Dosyalar
- `index.html` — uygulama
- `manifest.json` — PWA tanımı (kurulabilir uygulama)
- `service-worker.js` — çevrimdışı çalışma + önbellek
- `qr.js` — QR kod üreticisi (dekont için)
- `icon-192.png`, `icon-512.png` — uygulama ikonları

**Önemli:** Tüm dosyalar aynı klasörde, bir web sunucusunda **HTTPS** üzerinden yayınlanmalıdır. NFC ve PWA kurulumu `file://` veya HTTP'de çalışmaz.

## En kolay yayınlama: Netlify Drop
1. https://app.netlify.com/drop adresine gidin
2. Bu klasörün tamamını sürükleyip bırakın
3. Verilen `https://...netlify.app` adresini Android telefonda **Chrome** ile açın

## Alternatif: GitHub Pages
1. Bir repo oluşturun, bu 6 dosyayı yükleyin
2. Settings → Pages → Source: main / root
3. Verilen `https://kullanici.github.io/repo` adresini açın

## Telefona uygulama olarak kurma (PWA)
- Android Chrome'da sayfayı açın → menü (⋮) → **"Ana ekrana ekle"**
- Uygulama tam ekran, kendi ikonuyla açılır

## Kullanım
- Açılışta **PIN**: `1234` (demo)
- NFC tetiklemesi yalnızca **Android Chrome + HTTPS**'te gerçek kart okutunca çalışır
- iPhone / masaüstünde uyarı görünür (beklenen davranış)

## Yapılacaklar (sonraki adımlar)
- Gerçek banka/sanal POS entegrasyonu (`onCardTapped` içine ödeme isteği)
- Hata/red senaryoları, PIN ayarlama ekranı
- Gün sonu mutabakat (settlement) gönderimi
- Yasal metinler, KVKK/PCI uyumu
