# 📊 İlerleme Takibi — avt-elektronik

> Bu dosya ekip üyelerinin çalışmalarını takip etmek için kullanılır.
> Her değişiklik PR ile gelir, Ahmet & Yaver tarafından review edilir.

## 📌 Durum Etiketleri

| Etiket | Anlam |
|--------|-------|
| ✅ Yapıldı | Tamamlandı, test edildi |
| 🔄 Yapılıyor | Aktif olarak üzerinde çalışılıyor |
| 💡 Fikir Aşaması | Henüz başlanmadı, planlama/araştırma |
| 🐛 Debug | Hata ayıklama aşamasında |
| 🔍 Review Bekliyor | PR açıldı, review bekleniyor |
| ⏸️ Beklemede | Başka bir şeye bağımlı, bekliyor |

---

## 🗂️ Görevler

### VCU (Vehicle Control Unit)

| Görev | Sorumlu | Durum | Tarih | Notlar |
|-------|---------|-------|-------|--------|
| VCU firmware mimarisi tasarımı | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| Motor kontrol algoritması | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| CAN bus haberleşme protokolü | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| Güvenlik & hata yönetimi (fault handling) | @username | 💡 Fikir Aşaması | 2026-03-26 | — |

### BMS (Battery Management System)

| Görev | Sorumlu | Durum | Tarih | Notlar |
|-------|---------|-------|-------|--------|
| Hücre voltaj & sıcaklık izleme | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| SOC (State of Charge) hesaplama | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| Aşırı şarj / derin deşarj koruması | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| Balancing devresi tasarımı | @username | 💡 Fikir Aşaması | 2026-03-26 | — |

### PCB Tasarımı

| Görev | Sorumlu | Durum | Tarih | Notlar |
|-------|---------|-------|-------|--------|
| VCU ana kartı şematik çizimi | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| BMS PCB layout & routing | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| Güç dağıtım kartı (PDU) tasarımı | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| DRC & ERC kontrolleri | @username | 💡 Fikir Aşaması | 2026-03-26 | — |

### Kablaj & Entegrasyon

| Görev | Sorumlu | Durum | Tarih | Notlar |
|-------|---------|-------|-------|--------|
| Kablo harness şeması | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| Yüksek voltaj güvenlik entegrasyonu | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| Topraklama & EMI şielding planı | @username | 💡 Fikir Aşaması | 2026-03-26 | — |

### Sensör Sistemleri

| Görev | Sorumlu | Durum | Tarih | Notlar |
|-------|---------|-------|-------|--------|
| IMU entegrasyonu & kalibrasyon | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| Hız & konum sensörü seçimi | @username | 💡 Fikir Aşaması | 2026-03-26 | — |
| Sıcaklık sensörü ağı kurulumu | @username | 💡 Fikir Aşaması | 2026-03-26 | — |

---

## 📝 Nasıl Güncellenir?

1. Bu dosyayı kendi branch'inizde düzenleyin
2. Görevinizin durumunu güncelleyin (etiketleri kullanın)
3. PR açın → `develop` branch'ine
4. Review sonrası merge edilir

### Commit Formatı
```
docs(progress): görev açıklaması - durum güncellemesi
```

### Örnek
```
docs(progress): motor kontrol algoritması - yapılıyor → review bekliyor
```

---

## 📅 Haftalık Özet

> Her Cuma günü ekip sorumlusu bu bölümü günceller.

### Hafta: [tarih aralığı]
- **Tamamlanan:**
- **Devam Eden:**
- **Blocker'lar:**
- **Gelecek Hafta Planı:**
