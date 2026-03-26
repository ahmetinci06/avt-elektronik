# ⚡ AVT Racing — Elektronik Ekibi

> **avt-elektronik** — PCB tasarımları, firmware, devre şemaları ve VCU (Vehicle Control Unit) geliştirme deposu.

[![Ana Hub](https://img.shields.io/badge/Ana%20Hub-avt--hub--dev-blue)](https://github.com/ahmetinci06/avt-hub-dev)
[![TEKNOFEST 2026](https://img.shields.io/badge/TEKNOFEST-2026-red)](https://teknofest.org)

---

## 📋 Hakkında

Bu repo, AVT Racing aracının tüm elektronik sistemlerini kapsar: VCU, BMS, motor sürücü devreleri, sensör ağı, güç elektroniği ve firmware.

**Merkezi Hub:** [avt-hub-dev](https://github.com/ahmetinci06/avt-hub-dev)

---

## 👥 Elektronik Ekibi

| İsim | Rol |
|------|-----|
| Onur Musaoğlu | Elektronik |
| Deniz Bayrak | Elektronik |
| Şeyma Hacıosmanoğlu | Elektronik |
| Can Aral Çol | Elektronik |
| Ömer Soner | Elektronik |
| Emir Gülserin | Elektronik |

---

## 📁 Klasör Yapısı

```
avt-elektronik/
├── vcu/                        # Vehicle Control Unit
│   ├── firmware/               # VCU firmware (C/C++)
│   │   ├── src/                # Kaynak kodlar
│   │   ├── include/            # Header dosyaları
│   │   └── lib/                # Kütüphaneler
│   ├── pcb/                    # VCU PCB tasarımı
│   │   ├── schematic/          # Şema dosyaları
│   │   ├── layout/             # PCB layout
│   │   └── gerber/             # Üretim dosyaları
│   └── docs/                   # VCU dökümanları
├── bms/                        # Battery Management System
│   ├── firmware/
│   └── pcb/
├── motor-driver/               # Motor sürücü kartı
│   ├── firmware/
│   └── pcb/
├── sensors/                    # Sensör modülleri
│   ├── imu/                    # IMU modülü
│   ├── gps/                    # GPS modülü
│   └── temperature/            # Sıcaklık sensörleri
├── power/                      # Güç elektroniği
│   ├── dcdc-converter/
│   └── protection/
├── communication/              # Haberleşme (CAN, UART, SPI)
├── test/                       # Test devreleri ve fixture'lar
├── references/                 # Datasheet'ler, standartlar
│   └── datasheets/
└── docs/
    ├── GITHUB-GUIDE.md
    ├── wiring-diagram.md
    └── system-overview.md
```

---

## 🔧 Kullanılan Yazılımlar

| Yazılım | Alan | Format |
|---------|------|--------|
| KiCad | PCB tasarımı (önerilen) | `.kicad_sch`, `.kicad_pcb` |
| Altium Designer | PCB tasarımı | `.SchDoc`, `.PcbDoc` |
| STM32CubeIDE | VCU firmware | `.c`, `.h` |
| PlatformIO | Embedded development | `platformio.ini` |
| LTSpice | Devre simülasyonu | `.asc` |

---

## 🖥️ Firmware Geliştirme

### Gereksinimler
```bash
# STM32 toolchain
arm-none-eabi-gcc --version

# PlatformIO (önerilen)
pip install platformio

# OpenOCD (debug için)
```

### Derleme ve Yükleme
```bash
cd vcu/firmware

# PlatformIO ile:
pio run                    # Derle
pio run --target upload    # Yükle
pio run --target monitor   # Serial monitor

# CMake ile:
mkdir build && cd build
cmake .. && make
```

---

## 🌿 Branch Yapısı

```
main          ← Test edilmiş, stabil firmware ve PCB
  └── develop ← Aktif geliştirme
        ├── feature/can-bus-protokol
        ├── feature/bms-kontrol
        ├── design/vcu-pcb-v2
        └── fix/motor-sürücü-kalibrasyon
```

### Branch İsimlendirme
```
feature/<özellik>           # Yeni firmware özelliği
design/<bileşen>-v<sürüm>  # PCB tasarımı
fix/<konu>                   # Bug/hata düzeltme
test/<konu>                  # Test kodu
```

---

## ⚠️ Önemli Kurallar

1. **Test etmeden main'e merge etme** — donanım bozulabilir!
2. Gerber dosyaları PCB sipariş vermeden önce DRC'den geçirilmeli
3. Firmware commit'lerinde hangi donanım versiyonu için olduğunu belirt
4. Datasheet'leri `references/datasheets/` klasörüne ekle

---

## 🚀 Hızlı Başlangıç

```bash
git clone git@github.com:ahmetinci06/avt-elektronik.git
cd avt-elektronik
git checkout develop
git checkout -b feature/yaptığın-iş
```

Detaylı rehber: [docs/GITHUB-GUIDE.md](docs/GITHUB-GUIDE.md)

---

## 📚 Kaynaklar

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [docs/GITHUB-GUIDE.md](docs/GITHUB-GUIDE.md)
- [Ana Hub — avt-hub-dev](https://github.com/ahmetinci06/avt-hub-dev)

---

*🏎️ AVT Racing — TEKNOFEST 2026 | Elektronik Ekibi*
