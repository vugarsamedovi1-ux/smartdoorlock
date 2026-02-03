# 🚀 SDMS Web Sitesi - Hızlı Başlangıç

## 📦 Paket İçeriği

```
sdms-website/
├── index.html              # Ana web sayfası
├── style.css               # Stil dosyası
├── script.js               # JavaScript dosyası
├── images/                 # Proje görselleri (16 adet)
│   ├── sdms_image_1.jpeg   # Logo
│   ├── sdms_image_2.png    # 3D Tasarım
│   ├── sdms_image_3.png    # Cihaz Diyagramı
│   ├── sdms_image_4.png    # Elektrik Diyagramı
│   ├── sdms_image_5.png    # Devre Şeması
│   ├── sdms_image_6.png    # PCB Diyagram
│   ├── sdms_image_7.png    # Fonksiyonel Diyagram
│   ├── sdms_image_8.png    # ESP32
│   ├── sdms_image_9.png    # Servo Motor
│   ├── sdms_image_10.png   # Reed Sensör
│   ├── sdms_image_11.png   # LED
│   ├── sdms_image_12.png   # Buzzer
│   ├── sdms_image_13.png   # Button
│   ├── sdms_image_14.png   # Rezistör
│   ├── sdms_image_15.png   # Jumper Kablolar
│   └── sdms_image_16.png   # Üniversite Logosu
├── README.md               # Detaylı proje dökümantasyonu
├── DEPLOYMENT.md           # GitHub Pages yayınlama rehberi
└── LICENSE                 # MIT Lisansı
```

## ⚡ 3 Adımda Yayınlama

### 1️⃣ GitHub Repository Oluşturun
```
1. github.com/new adresine gidin
2. Repository adı: SDMS-Smart-Door-Management-System
3. Public seçin
4. Create repository butonuna tıklayın
```

### 2️⃣ Dosyaları Yükleyin
```
1. "uploading an existing file" linkine tıklayın
2. Tüm dosyaları sürükleyip bırakın (images klasörü dahil)
3. "Commit changes" butonuna tıklayın
```

### 3️⃣ GitHub Pages'i Aktifleştirin
```
1. Settings > Pages'e gidin
2. Source: main branch, / (root) seçin
3. Save butonuna tıklayın
4. 1-2 dakika bekleyin
```

**✨ Tebrikler! Siteniz yayında:**
```
https://KULLANICI_ADINIZ.github.io/SDMS-Smart-Door-Management-System/
```

## 🌐 Alternatif: Yerel Test

Dosyaları bilgisayarınızda test etmek için:

### Yöntem 1: Doğrudan Açma
```
index.html dosyasına çift tıklayın
Tarayıcınızda açılacaktır
```

### Yöntem 2: Python HTTP Server (Önerilen)
```bash
# Terminal'de proje klasörüne gidin
cd sdms-website

# Python 3 ile server başlatın
python -m http.server 8000

# Tarayıcıda açın: http://localhost:8000
```

### Yöntem 3: VS Code Live Server
```
1. VS Code'da klasörü açın
2. Live Server eklentisini kurun
3. index.html'e sağ tıklayın
4. "Open with Live Server" seçin
```

## 📱 Özellikler

✅ **Tam Responsive** - Mobil, tablet, desktop uyumlu
✅ **Modern Tasarım** - Gradientler, animasyonlar, hover efektleri
✅ **İnteraktif Menü** - Smooth scroll navigasyon
✅ **Diyagram Görüntüleyici** - Tab sistemi ile 6 farklı diyagram
✅ **Bileşen Galerisi** - Detaylı teknik özellikler
✅ **SEO Optimize** - Meta tags ve semantic HTML
✅ **Hızlı Yükleme** - Optimize edilmiş görseller

## 🎨 Özelleştirme

### Renkleri Değiştirmek
`style.css` dosyasını açın, 7-16. satırlardaki renkleri değiştirin:
```css
--primary: #6366f1;     /* Ana renk (mavi-mor) */
--secondary: #14b8a6;   /* İkincil renk (turkuaz) */
--dark: #0f172a;        /* Koyu tema */
```

### Logo Değiştirmek
`index.html` dosyasında 32. satırdaki emoji'yi değiştirin:
```html
<span class="logo-icon">🔐</span>
```

### İçerik Güncellemek
`index.html` dosyasındaki metinleri doğrudan düzenleyin.

## 🔧 Bileşenler

### Ana Sayfa Bölümleri
1. **Hero** - Proje başlığı ve tanıtım
2. **About** - Proje hakkında detaylar
3. **Features** - 6 ana özellik kartı
4. **Architecture** - 5 katmanlı sistem mimarisi
5. **Diagrams** - 6 teknik diyagram
6. **Components** - 8 donanım bileşeni + bütçe tablosu
7. **Team** - Ekip üyeleri ve üniversite bilgisi
8. **GitHub** - Repository bağlantısı
9. **Footer** - Linkler ve iletişim

### Teknik Detaylar
- **HTML5** - Semantic tags
- **CSS3** - Flexbox, Grid, Custom Properties, Animations
- **JavaScript (ES6+)** - Smooth scroll, tab switching, lazy loading
- **Google Fonts** - Inter font family
- **Responsive** - Mobile-first approach

## 📊 Sayfa Boyutları

| Dosya | Boyut | Açıklama |
|-------|-------|----------|
| index.html | ~25 KB | Ana sayfa |
| style.css | ~28 KB | Tüm stiller |
| script.js | ~8 KB | İnteraktif özellikler |
| images/ | ~7.4 MB | 16 yüksek çözünürlüklü görsel |
| **TOPLAM** | **~7.5 MB** | Tüm site |

## ✅ Checklist

Deployment öncesi kontrol:

- [ ] Tüm dosyalar mevcut
- [ ] Görseller images/ klasöründe
- [ ] index.html ana dizinde
- [ ] GitHub repository oluşturuldu
- [ ] Dosyalar yüklendi
- [ ] GitHub Pages aktif
- [ ] Site URL'si çalışıyor
- [ ] Mobil görünüm test edildi

## 🆘 Sık Sorulan Sorular

**S: Görseller görünmüyor?**
A: Dosya yapısını kontrol edin. images/ klasörü index.html ile aynı dizinde olmalı.

**S: Stil uygulanmıyor?**
A: style.css dosyasının ana dizinde olduğundan emin olun.

**S: GitHub Pages çalışmıyor?**
A: Settings > Pages'de Branch'in "main" ve folder'ın "/" olduğunu kontrol edin.

**S: Site yavaş yükleniyor?**
A: Görseller optimize edilmiş durumda. GitHub Pages'in CDN'i 1-2 saniyede yükleme sağlar.

**S: Mobilde menü açılmıyor?**
A: JavaScript'in yüklendiğinden emin olun. Console'da (F12) hata var mı kontrol edin.

## 📞 Destek

Sorun yaşarsanız:
1. DEPLOYMENT.md dosyasını okuyun (detaylı rehber)
2. README.md dosyasını kontrol edin (teknik detaylar)
3. GitHub Issues'da soru sorun

## 🎉 Başarılar!

Artık profesyonel bir SDMS web siteniz var!

**Paylaşın:**
- Arkadaşlarınızla
- Sosyal medyada
- CV'nizde

**İletişim:**
- GitHub: vugarsamedovi1-ux
- Proje: SDMS-Smart-Door-Management-System

---

Made with ❤️ in Tbilisi, Georgia | © 2026 SDMS Project
