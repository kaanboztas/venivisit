# VeniVisit (bir ChamoX Ürünü) — Derin Pazar Araştırması, Vizyon ve İş Modeli

Bu doküman, VeniVisit projesinin çekirdek buluş fikrini, küresel pazardaki konumunu, Lara–Kundu bölgesi finansal projeksiyonlarını ve kesinleşen **v2.1 Ürün Kararlarını** tüm ekip üyeleri için tek bir referans kaynağında toplar.

---

## 1. Projenin Çekirdek Vizyonu ve Çözdüğü Problem

### 1.1. Sahadaki Gerçek Sorun
Antalya (Lara–Kundu, Belek, Kemer vb.) gibi yüksek yoğunluklu 5 yıldızlı turizm bölgelerinde:
* **Turist Cephesi (A Oteli Misafiri):** Örneğin Delphin Otel'de konaklayan bir turist; hemen yanındaki Concorde, Rixos veya Cullinan gibi diğer 5 yıldızlı tesislerin mimarisini, plajını, havuzunu, A La Carte restoranlarını veya akşam şovlarını merak etmesine rağmen kapıdaki güvenlik görevlileri ve oteller arası bir geçiş protokolü olmaması nedeniyle içeri giremez.
* **Ziyaret Edilen Tesis Cephesi (B Oteli / Mekan):** Gündüz saatlerinde (havuz, plaj, spa) ve belirli akşam seanslarında (A La Carte restoranlar, etkinlik alanları) ciddi bir atıl kapasiteye sahiptir. Ayrıca bölgede halihazırda tatil yapan, satın alma gücü kanıtlanmış turiste kendi tesisini **"kulaktan kulağa değil, göz göze"** (yerinde deneyimleterek) tanıtma fırsatını kaçırmaktadır.
* **Ulaşım Kopukluğu:** Turist bir başka otele, seçkin bir restorana veya etkinliğe gitmek istediğinde rezervasyon saatiyle senkronize, güvenli ve konforlu bir **VIP taşımacılık** deneyimini tek ekrandan planlayamamaktadır.

### 1.2. VeniVisit Çözümü (v2.1 Ekosistemi)
VeniVisit; bölgede konaklayan doğrulanmış turistlerin, uygulama üzerinden **Hibrit Paket (3/5/7 Günlük Pass veya Tekil Deneyim)** satın alarak anlaşmalı **Otelleri, Restoranları, Etkinlikleri ve VIP Deneyimleri** belirli saat aralıklarında ziyaret etmesini, isterse sepetine **VIP Mercedes Vito / V-Class Transfer** eklemesini ve gittiği tesiste **Fotoğraflı Dijital QR Doğrulaması + Gidilen Tesiste Verilen Renk Kodlu Fiziksel Bileklik (Gümüş / Altın)** ile ağırlanmasını sağlayan B2B2C dijital geçiş ve mobilite ağıdır.

---

## 2. Küresel Pazar Araştırması ve Yapısal Farkımız

Dünyada "gündüz otel erişimi" (day-pass) ve "lüks konsiyerj" milyar dolarlık kanıtlanmış pazarlardır:
* **ResortPass:** 37,4 Milyon $ yatırım, 2.700+ otel (Marriott, Hilton, Hyatt, Ritz-Carlton), 5+ milyon kullanıcı. Bazı oteller yılda 3 Milyon $ ek gelir elde ediyor.
* **Dayuse:** Gündüz saatlik/günübirlik otel kullanımı segmentinde 100 Milyon € değerlemeye ulaştı.
* **SevenRooms / Resy & Blacklane:** Lüks restoran rezervasyonu ve VIP şoförlü transfer dikeylerinde faaliyet gösteriyor ancak birbirlerinden tamamen kopuk çalışıyorlar.

### VeniVisit'in Rakiplerden Ayrıştığı 5 Stratejik Nokta

| Kriter | ResortPass / Dayuse | VeniVisit Ekosistemi |
| :--- | :--- | :--- |
| **Kim Satın Alıyor?** | Otel dışındaki yerel halk / günübirlikçi | **Başka bir 5* otelde konaklayan doğrulanmış turist** |
| **Hareket Yönü** | Dışarıdan -> İçeriye | **İçeriden -> İçeriye (Oteller ve Mekanlar Arası Ağ)** |
| **Kapsam (4 Ana Sekme)** | Sadece Havuz / Spa / Oda | **1-Oteller, 2-Restoranlar, 3-Etkinlik & Gece Hayatı, 4-VIP Deneyimler** |
| **VIP Mobilite** | Yok (Kullanıcı kendi ulaşımını çözer) | **Ziyaret saatiyle tam senkronize VIP Mercedes Vito / V-Class Transfer** |
| **Güvenlik & Bileklik** | Basit rezervasyon kodu | **Fotoğraflı QR Doğrulama + Gidilen Otelde Verilen Gümüş/Altın Fiziksel Bileklik + Anında Kayıp İptali** |
| **Sadakat Köprüsü** | Tek seferlik kullanım | **Ziyaret sonrası "Gelecek Tatiliniz İçin %10 Özel İndirim" ile otellere doğrudan yeni sezon müşterisi kazandırma** |

---

## 3. Kesinleşen Ürün ve Operasyon Kuralları (Mimari Kilitler)

4 kişilik geliştirici ekibimizin ve yapay zeka ajanlarımızın tüm tasarımlarda uyacağı kesin kurallar:

1. **4 Ana Kategori Sekmesi (Keşfet Vitrini):**
   * `1-Oteller`: 5* Otellerin gündüz/akşam paketleri, havuz, plaj, aquapark, spa ve tesis keşif ziyaretleri.
   * `2-Restoranlar`: Otel içi veya bağımsız Fine Dining / A La Carte restoran masa rezervasyonları.
   * `3-Etkinlik & Gece Hayatı`: Konserler, tema parkları, gece şovları ve beach club partileri.
   * `4-VIP Deneyimler`: Özel kabana/loca, VIP spa ritüelleri ve kişiselleştirilmiş paketler.
2. **Hibrit Satış Modeli:**
   * Kullanıcı ister **3 / 5 / 7 Günlük "VeniVisit Pass"** satın alır, isterse tek bir otel/restoran/etkinlik için **tekil (kullandıkça öde) rezervasyon** yapar.
3. **Sepete Eklenen Opsiyonel VIP Taşımacılık (Mercedes Vito / V-Class):**
   * VIP transfer başlangıçta sepete eklenen opsiyonel bir hizmettir (ileride Premium Pass'lere dahil edilebilir).
   * Seçilen mekanın ziyaret saat aralığına (örn. `14:00 - 18:00`) göre VIP Mercedes Vito aracın alınış saati (`13:30 - Otel A Lobisi`) ve dönüş saati (`18:00 - Otel B Kapısı`) otomatik senkronize edilir.
4. **Yüksek Güvenlikli Fotoğraflı QR & Gidilen Tesiste Bileklik Teslimi:**
   * Dijital QR anahtar sadece kapıdan geçiş, VIP araca biniş ve masa doğrulaması içindir (içeride cüzdan/bakiye karmaşası yoktur).
   * Misafir gittiği otelin/mekanın kapısında QR kodunu okuttuğunda güvenlik ekranında **YEŞİL ONAY** ile birlikte:
     * **Misafirin Fotoğrafı ve Adı-Soyadı**
     * **Konakladığı Ana Otel ve Oda Numarası** (Örn: *Delphin Imperial — Oda 412*)
     * **Geçerlilik Saat Aralığı** (Örn: *14:00 – 18:00*)
     * **Teslim Edilecek Bileklik Kademesi:** Pakete göre **`GÜMÜŞ BİLEKLİK VERİNİZ`** (Keşif/Standart) veya **`ALTIN VIP BİLEKLİK VERİNİZ`** (Her Şey Dahil/VIP/A La Carte) uyarısı görünür.
   * Fiziksel bileklik bizzat **gidilen tesis tarafından kapıda verilir**, böylece içerideki personel misafirin VeniVisit konuğu ve statüsünü anında bilir.
5. **Kayıp / İptal Protokolü:**
   * Misafir uygulamadan *"Anahtarımı / Bilekliğimi Kaybettim"* dediğinde eski QR token anında `REVOKED` (iptal) durumuna düşer (okutulursa kırmızı ekran verir) ve saniyeler içinde yeni imzalı QR üretilir.
6. **Ziyaret Sonrası Gelecek Tatil Teklifi (Retention Engine):**
   * Ziyaret tamamlandığında turistin ekranına: *"Ziyaret ettiğiniz [Otel Adı] deneyimini beğendiniz mi? Bir sonraki tatil rezervasyonunuz için %10 VeniVisit Özel İndirim Kuponunuzu hemen alın!"* kartı düşer.

---

## 4. Finansal Model ve Komisyon Dağılımı (Lara–Kundu Projeksiyonu)

Sunum dosyalarındaki (`VeniVisit Projekt presentation.pdf`) **Worst-Case (En Kötü Senaryo)** baz alınarak sistemin muhasebe motoruna (Fintech Ledger) işlenecek birim ekonomi:

* **Bölge Kapasitesi (Mayıs–Ekim, 180 Gün):**
  * Tam Potansiyel: 22 adet 5* Otel (~485.760 sezonluk ziyaretçi).
  * Pilot / Worst-Case Hedefi: **5 adet 5* Otel**, otel başı günde sadece **5 yeni ziyaretçi**.

### Birim Paket Dağılım Tablosu (Euro Bazlı)

| Kalem | 1 Satış (1x) | Günde 5 Satış (1 Otel) | Ayda (1 Otel / 150 Satış) | Ayda 5 Otel | Ayda 20 Otel |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Paket Satış Fiyatı** | **89 €** | **445 €** | **13.350 €** | **66.750 €** | **267.000 €** |
| **Gidilen Otelin Payı (-)** | -39 € | -195 € | -5.850 € | -29.250 € | -117.000 € |
| **VeniVisit Brüt Pay** | **50 €** | **250 €** | **7.500 €** | **37.500 €** | **150.000 €** |
| **App & Altyapı Gideri (-)** | -5 € | -25 € | -750 € | -3.750 € | -15.000 € |
| **Net Brüt Kar** | **45 €** | **225 €** | **6.750 €** | **33.750 €** | **135.000 €** |
| **Fikir Telif Payı / Royalty (-)** | -12 € | -60 € | -1.800 € | -9.000 € | -36.000 € |
| **Şirkete Kalan Net Kar** | **33 €** | **165 €** | **4.950 €** | **24.750 €** | **99.000 €** |

*(Not: Sepete opsiyonel **VIP Mercedes Vito Transfer** eklendiğinde, transfer ücreti üzerinden de **VIP Filo Payı + VeniVisit Transfer Komisyonu** otomatik ayrıştırılarak Admin panelindeki gelir tablosuna eklenir).*
