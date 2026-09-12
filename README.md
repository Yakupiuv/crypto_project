> **Not (12.09.2026):** Kullanılan ücretsiz API servisinin sınırlandırmaları nedeniyle Kriptolar sayfası şu an aktif çalışmamaktadır. Bu projenin temel geliştirme amacı API entegrasyonu ve veri işleme süreçlerini öğrenmektir.

# Crypto Live Tracker (Qwik)

Canlı kripto para verilerini anlık olarak çeken, işleyen ve arayüzde görüntüleyen bir web uygulamasıdır. Bu çalışma, algoritma dersi proje ödevi kapsamında geliştirilmiştir.

Projede **Qwik** kütüphanesinin tercih edilme nedeni; *Resumability* mimarisi ve yüksek *Pre-load* (ön yükleme) hızı sağlamasıdır. Bu sayede başlangıçta yüklenen veri miktarı performansı olumsuz etkilemez.

---

## Ekran Görüntüleri

| Ana Sayfa / Arayüz | Detay Görünümü |
|---|---|
| <img src="screenshoots/photo1.png" width="400"/> | <img src="screenshoots/photo2.png" width="400"/> |

| Alternatif Görünüm | Hata Sayfası (API Limit) |
|---|---|
| <img src="screenshoots/photo3.png" width="400"/> | <img src="screenshoots/photo7.png" width="400"/> |

> Ücretsiz API kullanımındaki sunucu sınırlandırmalarına karşı kullanıcı deneyimini korumak adına özel bir hata sayfası entegre edilmiştir.

---

## Performans ve Mimari

Qwik'in sunduğu performans avantajları sayesinde yüksek skorlar elde edilmiştir *(Kriptolar sayfasında API üzerinden 1.000'e yakın veri çekildiği için yüklenme süreleri değişiklik gösterebilir)*.

### Lighthouse Test Sonucu
<img src="screenshoots/photo4.png" width="700"/>

---

## Veri Akışı ve Backend

1. **CoinGecko API:** Canlı kripto verileri CoinGecko API'si üzerinden `fetch` ile çekilerek frontend tarafında işlenir.
2. **Python Servisi:** Veri işleme süreçleri için yazılan Python kodları:
   
   <img src="screenshoots/photo5.png" width="600"/>

3. **Deploy & Bağlantı:** Netlify üzerinde barındırılan ön yüze erişim sağlamak amacıyla backend servisi **Railway** üzerinden canlıya alınmıştır:
   
   <img src="screenshoots/photo6.png" width="600"/>

---

## Canlı Demo & Özellikler

* **Canlı Demo:** [algoritmaodevim.netlify.app](https://algoritmaodevim.netlify.app/)
* **Mobil Uyumluluk:** Responsive tasarım standartlarına uygun olarak tüm cihazlarda sorunsuz çalışır.
* **Teknoloji Yığını:** Qwik, JavaScript, Python, Netlify, Railway, CoinGecko API.