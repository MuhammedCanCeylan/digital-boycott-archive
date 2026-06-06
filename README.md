# 🌐 Digital Boycott Archive & NFT Marketplace Simulation

Bu proje, **1244 adet dijital varlığı (asset)** tarayıcıyı kasmadan, yüksek performansla listeleyen ve yerelde matematiksel doğrulama algoritmaları barındıran modern, Web3 / NFT marketplace temalı bir karanlık arayüz (frontend) simülasyonudur.

## 🚀 Öne Çıkan Teknik Özellikler

* **Yüksek Performanslı Render (Chunking):** 1244 resim ve logo varlığını aynı anda DOM'a basıp tarayıcı belleğini şişirmek yerine, `requestAnimationFrame` ve `BATCH = 80` mantığı kullanılmıştır. Varlıklar 80'erli paketler halinde asenkron olarak yüklenir.
* **Justified Brick Layout (Sonsuz Tuğla Duvarı):** CSS `columns` mimarisi ve `break-inside: avoid;` teknikleri kullanılarak `.webp`, `.png`, `.jpeg` ve `.svg` formatındaki tüm logolar kendi orijinal en-boy oranlarını koruyarak yapboz gibi esnek bir yapıda alt alta/yan yana listelenir.
* **Rarity & Neon Glow Mekanizması:** Varlıklara `Common`, `Uncommon`, `Rare`, `Epic`, `Legendary` gibi nadirlik seviyeleri atanmış, CSS custom properties (`--accent-glow`, `--accent`) ile hover esnasında neon parlama efektleri entegre edilmiştir.
* **Luhn Algoritması (Mod 10) ile Ödeme Kontrolü:** İstemci taraflı (client-side) ödeme simülasyonunda girilen kart numaraları, yerel JavaScript üzerinde Luhn algoritması kullanılarak matematiksel doğrulamadan geçer. Algoritmayı geçemeyen kartlar kırmızı hata flag'i tetikler.
* **Akıllı Filtreleme ve Arama:** Token ID, nadirlik derecesi ve isim bazlı dinamik arama motoru yerleşik olarak çalışır.

## 📂 Klasör Yapısı

```text
├── indirilen_logolar/   # 1244 adet optimize edilmiş logo varlığı (.webp, .svg, .png)
├── index.html           # Optimize edilmiş ana Web3 arayüzü ve JS algoritmaları
└── README.md            # Proje teknik dökümantasyonu
