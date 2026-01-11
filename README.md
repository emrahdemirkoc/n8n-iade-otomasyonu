# E-Ticaret İade Süreci Otomasyonu

Bu proje, e-ticaret sitelerindeki iade taleplerini n8n kullanarak otomatize eder.

## Özellikler
- Müşteri iade talebi oluşturur.
- Yönetici onayı istenir.
- Kargo kodu otomatik üretilir.
- ## 🛠️ Kullanılan Teknolojiler
- **n8n:** İş akışı (workflow) otomasyonu ve yönetimi için.
- **JavaScript:** Fonksiyon node'larında veri işlemek için.
- **JSON:** Veri transferi ve yapılandırma formatı.
- **Webhook:** E-ticaret sitesinden anlık veri almak için.
- **Git & GitHub:** Versiyon kontrolü ve dokümantasyon.
- ## 🔄 Sistem Mimarisi ve Akış
Bu otomasyon, müşteri ile lojistik firması arasındaki köprüyü kurar. Veri akışı şu şekildedir:

`[Müşteri Formu] -> (Webhook) -> [n8n Sunucusu] -> [Yönetici Onayı] -> [Kargo API] -> [Müşteri E-postası]`

**Adım Adım Süreç:**
1. **Veri Yakalama:** E-ticaret sitesinden gelen iade talebi Webhook ile anlık olarak yakalanır.
2. **Doğrulama:** Gelen sipariş numarası veritabanından (Google Sheets/SQL) sorgulanır.
3. **Karar Mekanizması:**
   - İade sebebi "Kusurlu Ürün" ise yöneticiye fotoğraf iletiliir.
   - İade sebebi "Beden Uyumsuzluğu" ise otomatik onay verilir.
4. **Sonuçlandırma:** Kargo entegrasyonundan iade kodu oluşturulur ve müşteriye SMS/Mail olarak iletilir.
## Kurulum
**Gereksinimler:** Bu otomasyonu çalıştırmak için n8n sürüm 1.0 veya üzeri gereklidir.
## 🗺️ Yol Haritası (Roadmap)
- [x] GitHub Student Pack onayı alındı ✅
- [ ] DigitalOcean sunucu kurulumu ⏳
- [ ] Webhook bağlantılarının test edilmesi
- [ ] Telegram bot entegrasyonu
---
## 📞 İletişim & Destek
Bu proje veya benzer n8n otomasyonları hakkında danışmanlık almak isterseniz:
👉 **Web Sitemi Ziyaret Edin:** [emrahdemirkoc.com](https://emrahdemirkoc.com)
📧 **E-posta:** emrahdemirkoc@gmail.com
