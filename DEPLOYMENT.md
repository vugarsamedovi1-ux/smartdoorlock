
# 🚀 SDMS ვებ-გვერდის გაშვების სახელმძღვანელო

ეს სახელმძღვანელო ნაბიჯ-ნაბიჯ განმარტავს, როგორ გამოაქვეყნოთ SDMS ვებ-გვერდი **GitHub Pages-ის გამოყენებით** უფასო დომენზე.

## 📋 შინაარსი

1. [GitHub რეპოზიტორიის შექმნა](#1-github-რეპოზიტორიის-შექმნა)
2. [ფაილების ატვირთვა](#2-ფაილების-ატვირთვა)
3. [GitHub Pages-ის ჩართვა](#3-github-pages-ის-ჩართვა)
4. [ვებ-გვერდზე წვდომა](#4-ვებ-გვერდზე-წვდომა)
5. [სპეციალური დომენის კავშირი (ვარიანტი)](#5-სპეციალური-დომენის-კავშირი-ვარიანტი)

---

## 1. GitHub რეპოზიტორიის შექმნა

### ნაბიჯი 1.1: GitHub-ზე შესვლა

* გადადით [GitHub.com](https://github.com)
* შეხვიდეთ თქვენს ანგარიშში (თუ არ გაქვთ, შექმენით უფასო ანგარიში)

### ნაბიჯი 1.2: ახალი რეპოზიტორიის შექმნა

1. ზედა მარჯვენა კუთხეში "+" აიკონზე დააჭირეთ
2. აირჩიეთ "New repository"
3. დააყენეთ რეპოზიტორიის პარამეტრები:

   * **Repository name:** `SDMS-Smart-Door-Management-System` (ან ნებისმიერი სახელი)
   * **Description:** "Smart Door Management System - IoT დაფუძნებული ჭკვიანი კარის კონტროლის გადაწყვეტილება"
   * აირჩიეთ **Public** (GitHub Pages-ისთვის საჭირო)
   * მონიშნეთ "Add a README file"
   * დააჭირეთ "Create repository"

---

## 2. ფაილების ატვირთვა

### ვარიანტი A: GitHub ვებ ინტერფეისით

1. ახალ რეპოზიტორიაში დააჭირეთ "Add file" > "Upload files"
2. გადაისვეთ და დატოვეთ შემდეგი ფაილები:

   ```
   index.html
   style.css
   script.js
   README.md
   images/ (მთელი საქაღალდე)
   ```
3. ჩაწერეთ Commit მესიჯი: "Initial commit - SDMS website"
4. დააჭირეთ "Commit changes"

### ვარიანტი B: Git-ით (Terminal)

```bash
# რეპოზიტორიის კლონირება
git clone https://github.com/KULLANICI_ADINIZ/SDMS-Smart-Door-Management-System.git
cd SDMS-Smart-Door-Management-System

# ფაილების გადატანა (ყველა ვებ ფაილი)
cp -r /path/to/sdms-website/* .

# Git-ში დამატება
git add .
git commit -m "Initial commit - SDMS website"
git push origin main
```

---

## 3. GitHub Pages-ის ჩართვა

### ნაბიჯი 3.1: Settings-ში შესვლა

1. რეპოზიტორიის გვერდზე დააჭირეთ "Settings"
2. მარცხენა მენიუდან აირჩიეთ "Pages"

### ნაბიჯი 3.2: GitHub Pages-ის აქტივაცია

1. **Source** განყოფილებაში:

   * Branch: `main`
   * Folder: `/ (root)`
2. დააჭირეთ "Save"

### ნაბიჯი 3.3: გაშვების დასრულება

* GitHub Pages ავტომატურად გამოაქვეყნებს საიტს
* პროცესი ჩვეულებრივ 1–5 წუთს სჭირდება
* გვერდის განახლების შემდეგ მწვანე ყუთში გამოჩნდება საიტის URL

---

## 4. ვებ-გვერდზე წვდომა

### უფასო GitHub Pages URL

```
https://KULLANICI_ADINIZ.github.io/SDMS-Smart-Door-Management-System/
```

**მაგალითი:**

```
https://vugarsamedovi1-ux.github.io/SDMS-Smart-Door-Management-System/
```

### ტესტირება

1. ჩასვით URL ბრაუზერში
2. გადაამოწმეთ, რომ საიტი სწორად იტვირთება
3. დაათვალიერეთ ყველა გვერდი (მენიუ, ფუნქციები, დიაგრამები და სხვ.)
4. გადაამოწმეთ მობილური ხედვა

---

## 5. სპეციალური დომენის კავშირი (ვარიანტი)

თუ გაქვთ საკუთარი დომენი (მაგ: [www.sdms-project.com](http://www.sdms-project.com)), შეგიძლიათ დააკავშიროთ GitHub Pages-თან.

### ნაბიჯი 5.1: DNS პარამეტრები დომენის მიმწოდებელთან

დამატეთ შემდეგი DNS ჩანაწერები:

**A ჩანაწერები:**

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME ჩანაწერი (www-ისთვის):**

```
www.yourdomain.com -> KULLANICI_ADINIZ.github.io
```

### ნაბიჯი 5.2: GitHub-ში Custom Domain-ის დაყენება

1. Repository Settings > Pages
2. "Custom domain" ყუთში ჩაწერეთ თქვენი დომენი: `www.sdms-project.com`
3. დააჭირეთ "Save"
4. მონიშნეთ "Enforce HTTPS" (DNS გავრცელების შემდეგ)

### DNS გავრცელება

* DNS ცვლილებები შეიძლება 24–48 საათი გაგრძელდეს
* შესამოწმებლად: [whatsmydns.net](https://www.whatsmydns.net/)

---

## 🔧 პრობლემების მოგვარება

### პრობლემა: საიტი არ ჩანს / 404

**გადაჭრა 1:** გადაამოწმეთ ფაილების სტრუქტურა

```
Repository root/
├── index.html      ← მთავარი საქაღალდე
├── style.css       ← მთავარი საქაღალდე
├── script.js       ← მთავარი საქაღალდე
├── images/         ← მთავარი საქაღალდე
└── README.md
```

**გადაჭრა 2:** Branch და ფოლდერის შემოწმება

* Settings > Pages > Source: `main` branch, `/ (root)` folder

**გადაჭრა 3:** Cache-ის გასუფთავება

* Windows: Ctrl+Shift+R
* Mac: Cmd+Shift+R

### პრობლემა: სურათები არ ჩანს

**გადაჭრა:**

* გადაამოწმეთ სურათების გზები HTML-ში: `src="images/sdms_image_1.jpeg"`
* დარწმუნდით, რომ სურათები `images/` საქაღალდეშია
* დიდი/პატარა ასოების სიზუსტე მნიშვნელოვანია

### პრობლემა: CSS არ მუშაობს

**გადაჭრა:**

* HTML `<head>`: `<link rel="stylesheet" href="style.css">`
* დარწმუნდით, რომ `style.css` მთავარი საქაღალდეშია

### პრობლემა: JavaScript არ მუშაობს

**გადაჭრა:**

* HTML: `<script src="script.js"></script>`
* Browser Developer Tools > Console-ს შეამოწმეთ შეცდომები
* F12 ღილაკი გამოიყენეთ Developer Tools-ისთვის

---

## 📱 მობილური ტესტი

ვებ-გვერდის ტესტირება სხვადასხვა მოწყობილობაზე:

1. **Chrome DevTools**

   * F12 > Toggle device toolbar (Ctrl+Shift+M)
   * სხვადასხვა ეკრანის ზომების შემოწმება

2. **რეალური მოწყობილობები**

   * გახსენით ტელეფონზე და ტაბლეტზე
   * გადაამოწმეთ responsive დიზაინი
   * ტესტირება touch ინტერაქციებზე

---

## 🔄 განახლება

### ვებ ინტერფეისიდან

1. გახსენით ფაილი რედაქტირებისთვის
2. დააჭირეთ კალმის აიკონს (Edit)
3. გააკეთეთ ცვლილებები
4. დააჭირეთ "Commit changes"

### Git-ით

```bash
git add .
git commit -m "Site güncellendi"
git push origin main
```

> შენიშვნა: GitHub Pages ავტომატურად განაახლებს საიტს push-ის შემდეგ (1–5 წუთში).

---

## 🎨 პერსონალიზაციის რჩევები

### ფერების შეცვლა

`style.css` ფაილში შეცვალეთ `:root` CSS ცვლადები:

```css
:root {
    --primary: #6366f1;        /* ძირითადი ფერი */
    --secondary: #14b8a6;      /* მეორეხარისხოვანი ფერი */
    --dark: #0f172a;           /* მუქი თემა */
}
```

### ლოგოს შეცვლა

`index.html` ფაილში მოძებნეთ `.logo-icon`:

```html
<span class="logo-icon">🔐</span>  <!-- Emoji შეცვალეთ -->
```

### კონტენტის განახლება

ყველა ტექსტი `index.html` ფაილშია, შეგიძლიათ პირდაპირ შეცვალოთ

---

## 📊 ანალიტიკა (ვარიანტი)

Google Analytics-ის დამატება:

1. შექმენით [Google Analytics](https://analytics.google.com/) ანგარიში
2. მიიღეთ Tracking ID (მაგ: G-XXXXXXXXXX)
3. დაამატეთ `<head>`-ში `index.html` ფაილში:

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

---

## ✅ შემოწმების სია

გაშვებამდე გადაამოწმეთ:

* [ ] ყველა ფაილი სწორ საქაღალდეშია
* [ ] სურათების გზები სწორია
* [ ] CSS და JS მუშაობს
* [ ] GitHub Pages აქტივია
* [ ] საიტის URL მუშაობს
* [ ] მობილური ხედვა ტესტირებულია
* [ ] ყველა ბმული მუშაობს
* [ ] README.md განახლებულია
* [ ] GitHub ბმული სწორია

---

## 🆘 დახმარება

პრობლემის შემთხვევაში:

1. **GitHub Docs:** [pages.github.com](https://pages.github.com/)
2. **Community Forum:** [GitHub Community](https://github.community/)
3. **Stack Overflow:** [stackoverflow.com](https://stackoverflow.com/questions/tagged/github-pages)

---

## 📞 კონტაქტი

პროექტთან დაკავშირებული კითხვებისთვის:

* GitHub Issues: რეპოზიტორიის "Issues" სექციაში
* Email: დაუკავშირდით პროექტის გუნდს

---

**გილოცავთ! 🎉**
თქვენი ვებ-გვერდი ახლა ხელმისაწვდომია მსოფლიოს ნებისმიერი წერტილიდან


თუ გინდა, შემიძლია შემდეგში გავაკეთო **ეს სახელმძღვანელო ვიზუალური ვერსიად**, პირდაპირ **HTML/Markdown ფორმატში ქართულად**, რომ GitHub README.md-ში პირდაპირ ჩასვათ. გინდა გავაკეთო?
