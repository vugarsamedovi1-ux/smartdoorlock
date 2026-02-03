# 🔐 SDMS - Smart Door Management System

![SDMS Logo](images/sdms_image_1.jpeg)

## 📋 Proje Hakkında

**SDMS (Smart Door Management System)**, konut ve iş yerlerinde kapı güvenliğini artırmak için tasarlanmış IoT tabanlı akıllı bir kapı yönetim sistemidir. ESP32 mikrodenetleyici, servo motor, Reed sensör ve Blynk mobil uygulaması kullanılarak gerçek zamanlı kapı kontrolü ve güvenlik bildirimleri sağlar.

### 🎓 Akademik Bilgiler
- **Üniversite:** İlyas Devlet Üniversitesi
- **Fakülte:** İşletme, Teknoloji ve Eğitim Fakültesi
- **Bölüm:** Bilgisayar Mühendisliği
- **Proje Türü:** Mezuniyet Projesi A
- **Yıl:** 2026
- **Şehir:** Tiflis, Gürcistan

### 👥 Proje Ekibi
- **Öğrenciler:**
  - Vugar Samadovi (Donanım & Sistem Entegrasyonu)
  - Eljun Hasiyev (Yazılım & Uygulama Geliştirme)
  
- **Danışmanlar:**
  - Davit Chkhaidze
  - Giorgi Modebadze

## 🌟 Özellikler

### Ana Özellikler
- ✅ **Gerçek Zamanlı İzleme:** Reed sensör ile kapı durumunu anlık tespit
- 📱 **Mobil Kontrol:** Blynk uygulaması ile uzaktan erişim
- 🔔 **Güvenlik Uyarıları:** Zorla açılma durumunda sesli alarm ve bildirim
- 🔒 **Otomatik Kilitleme:** Servo motor ile tam otomatik kilit mekanizması
- 💡 **LED Gösterge:** Yeşil/Kırmızı LED ile görsel durum takibi
- 🌐 **Wi-Fi Bağlantı:** IoT bulut servisleri entegrasyonu

### Teknik Özellikler
- **Mikrodenetleyici:** ESP32 (Dual-core 240MHz)
- **İletişim:** Wi-Fi 802.11 b/g/n, Bluetooth
- **Güç:** 5V DC
- **Kontrol:** Servo Motor (MG995R)
- **Sensörler:** Reed Manyetik Sensör
- **Uyarı:** Buzzer + LED göstergeler

## 🏗️ Sistem Mimarisi

### Katmanlı Mimari

1. **Kullanıcı Arayüzü Katmanı**
   - Blynk Mobil Uygulama
   - Fiziksel Buton (Manuel Kontrol)

2. **Kontrol Çekirdeği**
   - ESP32 Wi-Fi Mikrodenetleyici

3. **Yürütme Mekanizmaları**
   - Servo Motor Kilit
   - LED Göstergeler
   - Buzzer Alarm

4. **Sensör Sistemi**
   - Reed Sensör (Kapı Durumu)

5. **Ağ ve Bulut Katmanı**
   - Wi-Fi Bağlantı
   - Blynk Cloud Server

## 🔧 Donanım Bileşenleri

| Bileşen | Model | Adet | Fiyat (GEL) | Açıklama |
|---------|-------|------|-------------|----------|
| Mikrodenetleyici | ESP32 Dev Board | 1 | 24.40 | Ana kontrol ünitesi |
| Servo Motor | Tower Pro MG995R | 1 | 16.00 | Kilit mekanizması |
| Manyetik Sensör | Reed Sensör | 1 | 2.94 | Kapı durumu tespiti |
| LED | 3mm LED (Yeşil/Kırmızı) | 2 | 0.40 | Görsel gösterge |
| Buzzer | Aktif Buzzer | 1 | 4.20 | Sesli uyarı |
| Buton | Push Button | 1 | 2.26 | Manuel kontrol |
| Rezistör | 220Ω - 1kΩ | 2 | 0.50 | Akım sınırlama |
| Kablolar | Jumper Set | 1 | 11.61 | Bağlantı kabloları |
| **TOPLAM** | | | **62.31 GEL** | |

## 📊 Diyagramlar

Projede aşağıdaki teknik çizimler mevcuttur:

1. **3D Tasarım** - SDMS cihaz modeli
2. **Cihaz Diyagramı** - Bileşen yerleşimi
3. **Elektrik Diyagramı** - Güç dağıtımı
4. **Devre Şeması** - Bağlantı detayları
5. **PCB Diyagramı** - Baskı devre tasarımı
6. **Fonksiyonel Diyagram** - Sistem akış şeması

Tüm diyagramlar `images/` klasöründe yüksek çözünürlükte mevcuttur.

## 💻 Kurulum

### Gereksinimler
- Arduino IDE (1.8.x veya üzeri)
- ESP32 Board Desteği
- Blynk Kütüphanesi
- Wi-Fi Bağlantısı

### Adımlar

1. **Repository'yi Klonlayın**
```bash
git clone https://github.com/vugarsamedovi1-ux/SDMS-Smart-Door-Management-System.git
cd SDMS-Smart-Door-Management-System
```

2. **Arduino IDE Kurulumu**
- Arduino IDE'yi açın
- Preferences > Additional Board Manager URLs'e ekleyin:
  ```
  https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
  ```
- Tools > Board > Boards Manager > ESP32 araması yapın ve kurun

3. **Kütüphaneleri Yükleyin**
- Sketch > Include Library > Manage Libraries
- "Blynk" araması yapın ve kurun
- "ESP32Servo" araması yapın ve kurun

4. **Kodu ESP32'ye Yükleyin**
- `sdms-code.ino` dosyasını Arduino IDE'de açın
- Wi-Fi bilgilerinizi ve Blynk Auth Token'ı güncelleyin
- Board: "ESP32 Dev Module" seçin
- Upload butonuna tıklayın

5. **Blynk Uygulamasını Yapılandırın**
- Blynk uygulamasını indirin (iOS/Android)
- Yeni proje oluşturun
- Widget'ları ekleyin (detaylar dökümantasyonda)

## 🌐 Web Sitesi

Proje web sitesi modern, responsive ve tek sayfalık bir tasarıma sahiptir.

### Kurulum
1. `web/` klasörünü web sunucunuza kopyalayın
2. Tarayıcınızda `index.html` dosyasını açın

### Özellikler
- 📱 Tam responsive tasarım
- 🎨 Modern gradient ve animasyonlar
- 🖼️ Yüksek çözünürlüklü proje görselleri
- 📊 İnteraktif diyagram görüntüleyici
- 👥 Ekip tanıtımı
- 💰 Detaylı bütçe tablosu

### Teknolojiler
- HTML5
- CSS3 (Modern gradients, flexbox, grid)
- Vanilla JavaScript (ES6+)
- Google Fonts (Inter)

## 🔒 Güvenlik

### Uygulanan Güvenlik Katmanları

1. **Fiziksel Güvenlik**
   - Mekanik kilit blokajı
   - Zorla açılma tespiti

2. **Lojik Güvenlik**
   - Wi-Fi şifreleme (WPA2/WPA3)
   - Blynk token doğrulama
   - Komut validasyonu

3. **Uyarı Sistemi**
   - Sesli alarm (Buzzer)
   - Push bildirimleri
   - LED göstergesi

## 📱 Blynk Uygulama Yapılandırması

### Widget Listesi
1. **Button Widget** - Kapı kilitleme/açma
2. **LED Widget** - Kapı durumu göstergesi
3. **Notification Widget** - Uyarı mesajları
4. **Value Display** - Sistem durumu

### Virtual Pin Kullanımı
- V0: Kapı kilidi kontrolü
- V1: Kapı durumu
- V2: Buzzer kontrolü
- V3: LED durum

## 📈 Proje Zaman Çizelgesi

| Faz | Hafta | Aktiviteler |
|-----|-------|-------------|
| Bileşen Bağlantısı | 1-4 | Servo motor, Reed sensör, LED, Buzzer montajı |
| ESP32 Programlama | 4-7 | Kontrol mantığı geliştirme ve test |
| Sistem Montajı | 7-9 | Donanımın kapıya monte edilmesi |
| Uygulama Geliştirme | 9-12 | Blynk konfigürasyonu ve web sitesi |
| Test ve Validasyon | 12-15 | Sistem performans değerlendirmesi |

## 📜 Standartlar ve Uyumluluk

Proje aşağıdaki uluslararası standartlara uygundur:

- **IEEE 802.11** - Wi-Fi iletişim standardı
- **IEC 62368-1** - Elektronik cihaz güvenliği
- **IEC 61000** - Elektromanyetik uyumluluk
- **ISO/IEC 27001** - Bilgi güvenliği yönetimi
- **IoT Best Practices** - Veri şifreleme ve doğrulama

## 🛠️ Geliştirme

### Kod Yapısı
```
SDMS-Smart-Door-Management-System/
├── src/
│   ├── sdms-code.ino          # Ana ESP32 kodu
│   └── config.h               # Konfigürasyon dosyası
├── web/
│   ├── index.html             # Web sitesi ana sayfa
│   ├── style.css              # Stiller
│   ├── script.js              # JavaScript
│   └── images/                # Proje görselleri
├── diagrams/                  # Teknik çizimler
├── docs/                      # Dökümantasyon
└── README.md                  # Bu dosya
```

### Katkıda Bulunma
1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/YeniOzellik`)
3. Değişikliklerinizi commit edin (`git commit -m 'Yeni özellik eklendi'`)
4. Branch'i push edin (`git push origin feature/YeniOzellik`)
5. Pull Request oluşturun

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için [LICENSE](LICENSE) dosyasına bakın.

## 📞 İletişim

**Proje Ekibi:**
- Vugar Samadovi
- Eljun Hasiyev

**Üniversite:**
İlyas Devlet Üniversitesi  
İşletme, Teknoloji ve Eğitim Fakültesi  
Teknoloji Okulu - Bilgisayar Mühendisliği  
Tiflis, Gürcistan

**GitHub:** [https://github.com/vugarsamedovi1-ux/SDMS-Smart-Door-Management-System](https://github.com/vugarsamedovi1-ux/SDMS-Smart-Door-Management-System)

## 🙏 Teşekkürler

Proje danışmanlarımız Davit Chkhaidze ve Giorgi Modebadze'ye, İlyas Devlet Üniversitesi'ne ve bu projeyi destekleyen herkese teşekkür ederiz.

---

**© 2026 SDMS Project. Tüm hakları saklıdır.**

Made with ❤️ in Tbilisi, Georgia
