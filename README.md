# AKAS – Acil Konum Aktarım Sistemi

**Açılım:** Acil Konum Aktarım Sistemi  

AKAS, deprem, enkaz ve diğer acil durum senaryolarında Android cihazları kullanarak **canlı tespiti ve konumlandırma** yapan gelişmiş bir sistemdir. Sistem, internet veya GPS olmasa bile cihazların **Bluetooth ve Wi-Fi mesh ağı** üzerinden birbirleriyle iletişim kurmasını ve göreli konum haritası oluşturmasını sağlar. Haritalandırma tamamlandığında, alarm tetiklenir ve enkaz altındaki canlıların **konumu JSON formatında** dış referans cihazına iletilir.  

---

## Özellikler

- **Dağıtık Haritalandırma:** Tüm cihazlar kendi aralarında mesh ağı kurarak enkazın sanal haritasını çıkarır.  
- **Göreli Konumlandırma:** GPS veya pusula yoksa bile, RSSI ve sensör verileriyle (IMU, mikrofon, titreşim) merkez tabanlı konum belirleme.  
- **Pusula ve IMU Destekli Yönleme:** Pusula varsa yön bilgisi eklenir, yoksa yalnızca merkez ve seviye tespiti yapılır.  
- **Alarm Sistemi:** Haritalandırma tamamlandığında cihazlar yüksek sesli ikaz verir ve ekipleri bilgilendirir.  
- **JSON Veri Çıkışı:** Enkaz altındaki merkez noktayı, güven skorunu ve diğer kritik bilgileri dış cihaza iletir.  
- **Offline Çalışma:** İnternet veya mobil veri olmadan tamamen cihazlar arası iletişimle çalışabilir.  
- **Çoklu Cihaz Uyumu:** 50 ve üzeri cihazla geniş alanlarda doğruluk ve güven artırılır.

---

## Kullanım Alanları

- Deprem sonrası enkaz kurtarma operasyonları  
- Afet ve acil durum tatbikatları  
- Canlı tespit ve saha analizi  

---

## Örnek JSON Çıktısı

```json
{
  "cluster_id": "TR-IST-ENKAZ-443",
  "relative_map": {
    "A": {"neighbors": ["B","C"], "level": "üst"},
    "B": {"neighbors": ["A","C","D"]},
    "C": {"neighbors": ["B","D","E"], "center": true},
    "D": {"neighbors": ["B","C"]},
    "E": {"neighbors": ["C"], "level": "alt"}
  },
  "victim_probability": 0.91,
  "sound_detected": true,
  "node_count": 50
}
