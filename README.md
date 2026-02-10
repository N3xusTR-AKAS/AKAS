# AKAS – Acil Konum Aktarım Sistemi

**Açılım:** Acil Konum Aktarım Sistemi  

AKAS, deprem, enkaz ve diğer acil durum senaryolarında Android cihazları kullanarak **canlı tespiti ve konumlandırma** yapan gelişmiş bir sistemdir. Sistem, internet veya GPS olmasa bile cihazların **Bluetooth ve Wi-Fi mesh ağı** üzerinden birbirleriyle iletişim kurmasını ve göreli konum haritası oluşturmasını sağlar. Haritalandırma tamamlandığında, alarm tetiklenir ve enkaz altındaki canlıların **konumu görsel arayüz üzerinden** dış referans cihazına iletilir.  

---

## 🌟 Özellikler

- **Dağıtık Haritalandırma:** Cihazlar kendi aralarında mesh ağı kurar ve enkazın sanal haritasını çıkarır.  
- **Göreli Konumlandırma:** GPS veya pusula olmasa bile, RSSI ve sensör verileriyle konum belirleme.  
- **Pusula & IMU Destekli Yönleme:** Pusula varsa yön bilgisi eklenir, yoksa seviye tespiti yapılır.  
- **Alarm Sistemi:** Haritalandırma tamamlandığında yüksek sesli ikaz verir.  
- **JSON Veri Çıkışı (GUI ile Görselleştirilmiş):**  

---

## 🗺️ Örnek Harita Görünümü (GUI Tarzı)

| Cihaz | Komşular       | Kat / Seviye | Notlar            |
|-------|----------------|-------------|-----------------|
| A     | B, C           | Üst         | —               |
| B     | A, C, D        | Orta        | —               |
| C     | B, D, E        | Orta / Merkez | Canlı olasılığı yüksek |
| D     | B, C           | Orta        | —               |
| E     | C              | Alt         | Ses tespit edildi |

> Bu tablo aslında JSON çıktısının **GUI uyumlu görselleştirilmiş hali**.  
> Dış referans cihazında bu bilgiler renkli ve interaktif şekilde görüntülenir.

---

## 🚨 Kullanım Alanları

- Deprem sonrası enkaz kurtarma operasyonları  
- Afet ve acil durum tatbikatları  
- Canlı tespit ve saha analizi  

---

## ⚠️ Önemli Not

Bu proje **kapalı kaynaklıdır**.  
- Kodun kullanımı, dağıtımı veya değiştirilmesi **yazılı izin olmadan yasaktır**.  
- Saha testleri ve kullanım için ilgili kurumların onayı gereklidir.  

---

## 🔒 Lisans

**No License – Tüm hakları saklıdır © 2026 İbrahim Anadol**  

---

