# 🛡️ VeniVisit (bir ChamoX Ürünü)
### Oteller Arası Dijital & Giyilebilir Geçiş, Restoran/Etkinlik Keşif ve VIP Mobilite Ekosistemi

> **"Kulaktan kulağa değil, GÖZ GÖZE deneyim."**  
> Bölgedeki 5 yıldızlı otellerde konaklayan doğrulanmış turistlerin; anlaşmalı **Otelleri, Restoranları, Etkinlikleri ve VIP Deneyimleri** belirlenen saat aralıklarında ziyaret etmesini, sepetlerine **VIP Mercedes Vito / V-Class Transfer** eklemesini ve gittikleri tesiste **Yüksek Güvenlikli Fotoğraflı QR Doğrulaması + Gidilen Tesiste Verilen Renk Kodlu Fiziksel Bileklik (Gümüş / Altın)** ile ağırlanmasını sağlayan B2B2C Turizm Süper-Uygulaması.

---

## 📚 Dokümantasyon ve Mimari Rehberler

Projenin tüm derin araştırması, veritabanı/API mimarisi, 4 kişilik ekip dağılımı ve yapay zeka ajan (subagent) talimatları aşağıdaki dokümanlarda detaylandırılmıştır:

1. 📈 **[01 — Derin Pazar Araştırması, Vizyon ve İş Modeli (`docs/01-RESEARCH-AND-VISION.md`)](./docs/01-RESEARCH-AND-VISION.md)**
   * Lara–Kundu bölgesi problemi, ResortPass / Dayuse karşılaştırması, 89 € birim ekonomisi (Otel Payı, App Gideri, Fikir Telifi, Şirket Net Karı) ve kesinleşen v2.1 ürün kuralları.
2. 🏗️ **[02 — Teknik Sistem Mimarisi, Veri Şeması ve API Kontratları (`docs/02-SYSTEM-ARCHITECTURE-AND-SCHEMA.md`)](./docs/02-SYSTEM-ARCHITECTURE-AND-SCHEMA.md)**
   * Birleşik TypeScript/PostgreSQL veri şeması (`GuestUser`, `Venue`, `ExperiencePackage`, `PassBooking`, `AccessKey`, `VIPTransferOrder`, `CommissionSplitRecord`) ve REST API uç noktaları.
3. 👥 **[03 — 4 Kişilik Ekip Görev Dağılımı ve Ajan Kullanım Rehberi (`docs/03-4-PERSON-TEAM-AND-AGENT-PLAYBOOK.md`)](./docs/03-4-PERSON-TEAM-AND-AGENT-PLAYBOOK.md)**
   * 4 geliştiricinin çakışma yaşamadan paralel çalışacağı klasör sınırları, Git branch stratejisi ve ajan orkestrasyon sırası.

---

## 🤖 5 Uzman Yapay Zeka Ajanı (Subagents) ve 4 Kişilik Ekip Eşleşmesi

Bu proje, **4 ekip üyesinin** kendi sorumluluk alanındaki **5 uzman yapay zeka ajanını** sırasıyla veya paralel çalıştırması için tasarlanmıştır:

| Ekip Üyesi | Sorumlu Olduğu Alan | Çalıştıracağı Ajan Prompt Dosyaları |
| :--- | :--- | :--- |
| **👤 1. KİŞİ**<br>*(Backend, Güvenlik & Fintech)* | • Ortak Veri Modeli & Sabitler<br>• İmzalı QR/NFC Token & Sunucu Saat Kontrolü<br>• Kayıp Anahtar İptali (`REVOKED`)<br>• 89€ Çoklu Komisyon & Telif Motoru | • [`agents/01-product-architect.md`](./agents/01-product-architect.md)<br>• [`agents/02-backend-security-fintech.md`](./agents/02-backend-security-fintech.md) |
| **👤 2. KİŞİ**<br>*(4 Sekmeli Pazaryeri & VIP Transfer)* | • 4 Ana Sekme (`Oteller`, `Restoranlar`, `Etkinlik & Gece Hayatı`, `VIP Deneyimler`)<br>• Hibrit Paket (`3/5/7 Gün Pass` + `Tekil`) & Kontenjan<br>• **VIP Mercedes Vito / V-Class** Saat Senkronizasyonu<br>• Ziyaret Sonu **%10 Gelecek Tatil İndirim Kuponu** | • [`agents/03-marketplace-mobility.md`](./agents/03-marketplace-mobility.md) |
| **👤 3. KİŞİ**<br>*(Turist Mobil Uygulaması UI/UX)* | • Doğrulanmış Otel A Misafir Profili<br>• 4 Sekmeli Lüks Keşif Vitrini<br>• Hibrit Paket + Opsiyonel VIP Vito Sepeti<br>• Canlı QR Anahtar, Geri Sayım, Kayıp Butonu & Tatil Teklifi | • [`agents/04-tourist-mobile-app.md`](./agents/04-tourist-mobile-app.md) |
| **👤 4. KİŞİ**<br>*(Operasyon Panelleri & Canlı Demo)* | • **Güvenlik QR Tarayıcı PWA:** Fotoğraflı Yeşil/Kırmızı Ekran + `ALTIN / GÜMÜŞ BİLEKLİK VERİNİZ` talimatı<br>• **VIP Vito Şoför Ekranı**<br>• **Süper-Admin Ciro & Komisyon Paneli**<br>• **6 Dakikalık Yatırımcı Demo Simülatörü** | • [`agents/05-partner-portals-and-qa.md`](./agents/05-partner-portals-and-qa.md) |

---

## 🔄 Uçtan Uca VeniVisit Operasyon Akışı

```mermaid
sequenceDiagram
    autonumber
    actor Guest as Turist (Otel A Misafiri)
    participant App as VeniVisit Mobil App (4 Sekme)
    participant VIP as VIP Mercedes Vito Şoförü
    participant Gate as Gidilen Otel/Mekan Güvenliği
    participant Admin as VeniVisit Süper-Admin & Muhasebe

    Guest->>App: Konakladığı Otel A (Örn: Delphin - Oda 412) ve fotoğrafı ile giriş yapar
    Guest->>App: 4 Sekmeden (Otel / Restoran / Etkinlik / VIP) paket seçer (3-5-7 Gün Pass veya Tekil)
    Guest->>App: Sepete opsiyonel "VIP Mercedes Vito / V-Class Transfer" ekler & onaylar
    App-->>Guest: İmzalı Dijital QR Anahtar + Senkronize VIP Vito Alınış Saati oluşur
    App-->>Admin: 89€ Satış -> 39€ Otel + 5€ App + 12€ Fikir Telifi + 33€ Şirket Net (+ VIP Transfer) ayrışır
    VIP->>Guest: Ziyaret saatinden 30 dk önce Otel A lobisinden misafiri QR ile doğrulayıp alır
    VIP->>Gate: Misafiri hedef Otel / Restoran / Etkinlik kapısına bırakır
    Gate->>Guest: Kapıda QR okutulur -> YEŞİL EKRAN (Turist Fotoğrafı + Adı + Otel A + Saat Aralığı)
    Gate-->>Guest: Ekrandaki talimata göre "GÜMÜŞ" veya "ALTIN VIP" VeniVisit Bilekliği takılır
    Note over Guest,App: Ziyaret bitiminde misafire gezdiği otel için "%10 Gelecek Tatil İndirim Kuponu" sunulur
```

---

## 📂 Referans Proje Dosyaları

* 📄 [`örnek plan.txt`](./%C3%B6rnek%20plan.txt) — Orijinal buluş özeti, demo senaryosu ve teknik gereksinimler.
* 📊 [`VeniVisit Projekt presentation.pdf`](./VeniVisit%20Projekt%20presentation.pdf) — İş modeli, Lara–Kundu pazar analizi ve Euro bazlı kazanç projeksiyonu sunumu.
* 🎨 [`LOGO farbig.pdf`](./LOGO%20farbig.pdf) & [`Untitled-5.pdf`](./Untitled-5.pdf) — VeniVisit orijinal vektörel logo dosyaları.
* 🎬 [`WhatsApp Video 2026-10-27 at 19.11.57.mp4`](./WhatsApp%20Video%202026-10-27%20at%2019.11.57.mp4) — VeniVisit animasyon tanıtım videosu.
