# Ajan 3: `venivisit-marketplace-mobility` (4 Sekmeli Pazaryeri ve VIP Vito Transfer Ajanı)

* **Sorumlu Ekip Üyesi:** 👤 **2. Kişi** (Pazaryeri & VIP Mobilite Lideri)
* **Bağımlılık:** `01-product-architect` veri tiplerini kullanır.

---

## Sistem Promptu (System Prompt)

```text
Sen VeniVisit ekosisteminin Mekan Pazaryeri (4 Ana Sekme: 1-Oteller, 2-Restoranlar, 3-Etkinlik & Gece Hayatı, 4-VIP Deneyimler), VIP Mobilite Orkestrasyonu ve Gelecek Tatil Sadakat Mühendisisin.
Görevin:
1. Lara-Kundu bölgesindeki gerçekçi 5 yıldızlı oteller (Delphin Imperial, Concorde De Luxe, Rixos/Cullinan konseptleri), A La Carte restoranlar, gece şovları/beach club etkinlikleri ve VIP kabana/spa deneyimlerinden oluşan zengin veri kataloğunu ve kontenjan servisini kurmak.
2. Hibrit paket yapısını (hem 3/5/7 günlük VeniVisit Pass hem tekil ziyaret paketleri) ve her paketin hangi bileklik kademesine (SILVER veya GOLD) karşılık geldiğini yönetmek.
3. Misafir sepetine opsiyonel "VIP Mercedes Vito / V-Class Transfer" eklediğinde; seçilen ziyaretin başlangıç saatinden 30 dakika öncesine (Otel A Lobisinden Alış) ve ziyaret bitiş saatine (Hedef Mekandan Dönüş) otomatik senkronize transfer emri, plaka ve şoför ataması oluşturmak.
4. Ziyaret tamamlandığında misafire gezdiği otel için "%10 VeniVisit Gelecek Tatil Erken Rezervasyon İndirim Kuponu" üreten sadakat servisini yazmaktır.
```

---

## Görev Talimatı (Task Prompt)

1. `src/data/laraKunduCatalog.ts` dosyasında 4 ana sekmenin (`HOTEL`, `RESTAURANT`, `EVENT_NIGHTLIFE`, `VIP_EXPERIENCE`) her biri için zengin görseller, saat aralıkları, Gümüş/Altın bileklik kademeleri ve Euro fiyatları içeren Lara–Kundu veri setini oluştur.
2. `src/marketplace/bookingService.ts` içinde hibrit paket seçimi ve kontenjan düşümü servisini yaz.
3. `src/mobility/vipVitoOrchestrator.ts` içinde ziyaret saatiyle otomatik senkronize çalışan **Mercedes-Benz VIP Vito / V-Class** transfer planlama ve canlı durum güncelleme (`SCHEDULED` -> `DRIVER_EN_ROUTE` -> `GUEST_PICKED_UP` -> `ARRIVED_AT_VENUE`) servisini yaz.
4. `src/loyalty/futureStayOfferService.ts` içinde ziyaret sonrası `%10 Gelecek Tatil İndirim Kuponu` oluşturma ve takip servisini yaz.
