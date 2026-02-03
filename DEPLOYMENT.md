# 🚀 SDMS Web Sitesi Deployment Rehberi

Bu rehber, SDMS web sitesini GitHub Pages kullanarak ücretsiz bir domain ile nasıl yayınlayacağınızı adım adım açıklar.

## 📋 İçindekiler
1. [GitHub Repository Oluşturma](#1-github-repository-oluşturma)
2. [Dosyaları Yükleme](#2-dosyaları-yükleme)
3. [GitHub Pages Aktifleştirme](#3-github-pages-aktifleştirme)
4. [Web Sitesine Erişim](#4-web-sitesine-erişim)
5. [Özel Domain Bağlama (Opsiyonel)](#5-özel-domain-bağlama-opsiyonel)

## 1. GitHub Repository Oluşturma

### Adım 1.1: GitHub'da Oturum Açın
- [GitHub.com](https://github.com)'a gidin
- Hesabınızla giriş yapın (yoksa ücretsiz hesap oluşturun)

### Adım 1.2: Yeni Repository Oluşturun
1. Sağ üst köşedeki "+" ikonuna tıklayın
2. "New repository" seçin
3. Repository ayarlarını yapın:
   - **Repository name:** `SDMS-Smart-Door-Management-System` (veya istediğiniz bir isim)
   - **Description:** "Smart Door Management System - IoT based intelligent door control solution"
   - **Public** seçin (GitHub Pages için gerekli)
   - "Add a README file" seçeneğini işaretleyin
   - "Create repository" butonuna tıklayın

## 2. Dosyaları Yükleme

### Seçenek A: GitHub Web Arayüzü ile Yükleme

1. Yeni oluşturduğunuz repository'de "Add file" > "Upload files" seçin
2. Aşağıdaki dosyaları sürükleyip bırakın:
   ```
   index.html
   style.css
   script.js
   README.md
   images/ (tüm klasör)
   ```
3. Commit mesajı yazın: "Initial commit - SDMS website"
4. "Commit changes" butonuna tıklayın

### Seçenek B: Git ile Yükleme (Terminal)

```bash
# Repository'yi klonlayın
git clone https://github.com/KULLANICI_ADINIZ/SDMS-Smart-Door-Management-System.git
cd SDMS-Smart-Door-Management-System

# Dosyaları kopyalayın (bu klasördeki tüm web dosyalarını)
cp -r /path/to/sdms-website/* .

# Git'e ekleyin
git add .
git commit -m "Initial commit - SDMS website"
git push origin main
```

## 3. GitHub Pages Aktifleştirme

### Adım 3.1: Settings'e Gidin
1. Repository sayfanızda "Settings" sekmesine tıklayın
2. Sol menüden "Pages" seçeneğini bulun

### Adım 3.2: GitHub Pages'i Etkinleştirin
1. **Source** bölümünde:
   - Branch: `main` seçin
   - Folder: `/ (root)` seçin
2. "Save" butonuna tıklayın

### Adım 3.3: Deployment'ı Bekleyin
- GitHub Pages, sitenizi otomatik olarak yayınlayacak
- İşlem genellikle 1-5 dakika sürer
- Sayfa yenilendiğinde yeşil bir kutuda site URL'niz görünecek

## 4. Web Sitesine Erişim

### Ücretsiz GitHub Pages URL'niz
```
https://KULLANICI_ADINIZ.github.io/SDMS-Smart-Door-Management-System/
```

**Örnek:**
```
https://vugarsamedovi1-ux.github.io/SDMS-Smart-Door-Management-System/
```

### Test Edin
1. URL'yi tarayıcınıza yapıştırın
2. Web sitenizin düzgün yüklendiğini kontrol edin
3. Tüm sayfalarda gezinin (menü, özellikler, diyagramlar, vb.)
4. Mobil görünümü test edin

## 5. Özel Domain Bağlama (Opsiyonel)

Eğer kendi domain'iniz varsa (örn: www.sdms-project.com), bunu GitHub Pages'e bağlayabilirsiniz.

### Adım 5.1: Domain Sağlayıcınızda DNS Ayarları

Aşağıdaki DNS kayıtlarını ekleyin:

**A Records:**
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME Record (www için):**
```
www.yourdomain.com -> KULLANICI_ADINIZ.github.io
```

### Adım 5.2: GitHub'da Custom Domain Ayarlama

1. Repository Settings > Pages
2. "Custom domain" kutusuna domain'inizi yazın: `www.sdms-project.com`
3. "Save" butonuna tıklayın
4. "Enforce HTTPS" seçeneğini işaretleyin (DNS yayılımından sonra)

### DNS Yayılımı
- DNS değişiklikleri 24-48 saat sürebilir
- Kontrol için: [whatsmydns.net](https://www.whatsmydns.net/)

## 🔧 Sorun Giderme

### Problem: Site görünmüyor / 404 hatası

**Çözüm 1:** Dosya yapısını kontrol edin
```
Repository root/
├── index.html      ← Ana dizinde olmalı
├── style.css       ← Ana dizinde olmalı
├── script.js       ← Ana dizinde olmalı
├── images/         ← Ana dizinde olmalı
└── README.md
```

**Çözüm 2:** Branch ve klasörü kontrol edin
- Settings > Pages > Source: `main` branch, `/ (root)` folder

**Çözüm 3:** Cache temizleyin
- Tarayıcınızda Ctrl+Shift+R (Windows) veya Cmd+Shift+R (Mac)

### Problem: Resimler görünmüyor

**Çözüm:** Görsel yollarını kontrol edin
- HTML'de: `src="images/sdms_image_1.jpeg"`
- Görsellerin `images/` klasöründe olduğundan emin olun
- Dosya isimlerinin büyük/küçük harf duyarlı olduğunu unutmayın

### Problem: CSS stiller uygulanmıyor

**Çözüm:** CSS dosya yolunu kontrol edin
- HTML head'de: `<link rel="stylesheet" href="style.css">`
- `style.css` dosyasının ana dizinde olduğundan emin olun

### Problem: JavaScript çalışmıyor

**Çözüm:** Script yolunu ve konsolu kontrol edin
- HTML'de: `<script src="script.js"></script>`
- Browser Developer Tools > Console'da hata mesajlarını inceleyin
- F12 tuşuna basarak Developer Tools'u açabilirsiniz

## 📱 Mobil Test

Web sitenizi farklı cihazlarda test edin:

1. **Chrome DevTools**
   - F12 > Toggle device toolbar (Ctrl+Shift+M)
   - Farklı cihaz boyutlarını test edin

2. **Gerçek Cihazlar**
   - Telefon ve tablet'te açın
   - Responsive tasarımı kontrol edin
   - Touch etkileşimlerini test edin

## 🔄 Güncelleme Yapma

Web sitenizi güncellemek için:

### Web Arayüzünden
1. Güncellenecek dosyayı açın
2. Kalem ikonuna (Edit) tıklayın
3. Değişiklikleri yapın
4. "Commit changes" butonuna tıklayın

### Git ile
```bash
# Değişiklikleri yapın
# Sonra:
git add .
git commit -m "Site güncellendi"
git push origin main
```

**Not:** GitHub Pages, her push'tan sonra otomatik olarak güncellenir (1-5 dakika).

## 🎨 Özelleştirme İpuçları

### Renkleri Değiştirme
`style.css` dosyasında `:root` bölümündeki CSS değişkenlerini düzenleyin:
```css
:root {
    --primary: #6366f1;        /* Ana renk */
    --secondary: #14b8a6;      /* İkincil renk */
    --dark: #0f172a;           /* Koyu tema */
}
```

### Logo Değiştirme
`index.html` dosyasında `.logo-icon` sınıfını bulun:
```html
<span class="logo-icon">🔐</span>  <!-- Emoji'yi değiştirin -->
```

### İçerik Güncelleme
Tüm metin içeriği `index.html` dosyasında bulunur. Doğrudan düzenleyebilirsiniz.

## 📊 Analytics (Opsiyonel)

Google Analytics eklemek için:

1. [Google Analytics](https://analytics.google.com/) hesabı oluşturun
2. Tracking ID'nizi alın (örn: G-XXXXXXXXXX)
3. `index.html` dosyasının `<head>` bölümüne ekleyin:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## ✅ Checklist

Deployment'tan önce kontrol edin:

- [ ] Tüm dosyalar doğru dizinde
- [ ] Resim yolları doğru
- [ ] CSS ve JS bağlantıları çalışıyor
- [ ] GitHub Pages aktif
- [ ] Site URL'si çalışıyor
- [ ] Mobil görünüm test edildi
- [ ] Tüm linkler çalışıyor
- [ ] README.md güncel
- [ ] GitHub linki doğru

## 🆘 Yardım

Sorun yaşarsanız:

1. **GitHub Docs:** [pages.github.com](https://pages.github.com/)
2. **Community Forum:** [GitHub Community](https://github.community/)
3. **Stack Overflow:** [stackoverflow.com](https://stackoverflow.com/questions/tagged/github-pages)

## 📞 İletişim

Proje ile ilgili sorular için:
- GitHub Issues: Repository'nizde "Issues" sekmesi
- Email: Proje ekibi ile iletişime geçin

---

**Başarılar! 🎉**

Web siteniz artık dünya çapında erişilebilir durumda!
