# پورتفولیوی شخصی حرفه‌ای (GitHub Pages)

این یک تمپلیت آماده و مدرن برای صفحه شخصی (Portfolio) است که برای دیپلوی روی **GitHub Pages** طراحی شده.

---

## ساختار فایل‌ها

```
portfolio-template/
├── index.html      ← تمام متن‌ها و محتوا اینجا هستند
├── styles.css      ← ظاهر و رنگ‌ها
├── script.js       ← عملکردها (تم تاریک/روشن، منو و ...)
├── images/         ← عکس پروفایل را اینجا بگذارید
└── README.md       ← همین فایل راهنما
```

---

## قدم‌به‌قدم: چطور اطلاعات خودت را تغییر دهی؟

### ۱. تغییر اسم و عنوان

فایل `index.html` را با هر ویرایشگری (VS Code، Notepad++، حتی Notepad) باز کن.

جستجو کن و این قسمت‌ها را عوض کن:

| محل در کد | چه چیزی را عوض کنی |
|-----------|---------------------|
| `<title>Your Name \| Portfolio</title>` | اسم خودت |
| `<a href="#home" class="logo">Your<span>Name</span></a>` | اسم کوتاه در نوار بالا |
| `<h1 class="hero-name">Your Full Name</h1>` | اسم کامل |
| `<h2 class="hero-title">MS Student in Artificial Intelligence</h2>` | عنوان/نقش فعلی |
| متن پاراگراف زیر hero-title | توضیح کوتاه درباره خودت |

### ۲. تغییر عکس پروفایل

1. عکس خودت را با نام **`profile.jpg`** ذخیره کن (ترجیحاً مربع و کیفیت خوب).
2. آن را داخل پوشه **`images/`** قرار بده.
3. اگر اسم فایل را عوض کردی، در `index.html` این خط را پیدا کن و مسیر را اصلاح کن:

```html
<img src="images/profile.jpg" alt="Your Name" ... />
```

> اگر عکس نگذاری، یک آواتار خودکار با حروف اسمت نمایش داده می‌شود.

### ۳. لینک‌های سوشال مدیا

در دو جا (بخش Hero و بخش Contact) لینک‌ها را عوض کن:

```html
<a href="https://github.com/yourusername" ...>
<a href="https://linkedin.com/in/yourusername" ...>
<a href="https://scholar.google.com/citations?user=XXXX" ...>
<a href="mailto:your.email@example.com" ...>
<a href="https://x.com/yourusername" ...>
```

فقط آدرس‌ها را با لینک واقعی خودت جایگزین کن.

### ۴. بخش درباره من (About)

متن‌های داخل تگ‌های `<p>` را با متن خودت عوض کن.  
آمارهای پایین (تعداد مقاله، جایزه و ...) را هم می‌توانی تغییر دهی.

### ۵. تحصیلات (Education)

هر `<div class="timeline-item">` یک مقطع تحصیلی است.  
تاریخ، عنوان، دانشگاه و توضیحات را عوض کن.  
اگر مقطع بیشتری داری، یک `timeline-item` کامل را کپی کن و بچسبان.

### ۶. تجربه کاری (Experience)

هر `<div class="card">` یک تجربه است.  
عنوان شغل، تاریخ، نام آزمایشگاه/شرکت و توضیح را تغییر بده.

### ۷. مقالات (Publications)

هر `<article class="pub-item">` یک مقاله است.  
عنوان، نویسندگان، venue (مثل ACL 2026) و لینک‌های PDF/Code را به‌روز کن.  
اسم خودت را داخل `<strong>` بگذار تا برجسته شود.

### ۸. اخبار و افتخارات (News)

هر `<div class="news-item">` یک خبر است.  
تاریخ و متن را عوض کن.

### ۹. ایمیل در بخش تماس

```html
<a href="mailto:your.email@example.com" ...>
```

### ۱۰. تغییر رنگ اصلی (اختیاری)

در فایل `styles.css` این دو خط را پیدا کن:

```css
--primary: #6366f1;
--primary-hover: #818cf8;
```

رنگ دلخواهت را بگذار (مثلاً سبز: `#10b981`، آبی: `#3b82f6`، نارنجی: `#f97316`).

---

## چطور روی GitHub Pages دیپلوی کنم؟

### روش ساده و پیشنهادی (Static Site):

1. وارد حساب GitHub شو.
2. یک **Repository جدید** بساز با اسم دقیقاً این فرمت:
   ```
   username.github.io
   ```
   (به جای `username` همان یوزرنیم GitHub خودت را بنویس)

3. فایل‌های داخل پوشه `portfolio-template` را آپلود کن:
   - می‌توانی از طریق سایت GitHub (Upload files) آپلود کنی
   - یا با Git:
     ```bash
     git clone https://github.com/USERNAME/USERNAME.github.io.git
     cd USERNAME.github.io
     # فایل‌های template را کپی کن داخل این پوشه
     git add .
     git commit -m "Initial portfolio"
     git push
     ```

4. چند دقیقه صبر کن. سایت در آدرس زیر در دسترس خواهد بود:
   ```
   https://USERNAME.github.io
   ```

5. اگر سایت بالا نیامد:
   - به Settings → Pages برو
   - Source را روی **Deploy from a branch** بگذار
   - Branch را `main` و پوشه را `/ (root)` انتخاب کن
   - Save بزن

---

## نکات مهم

- بعد از هر تغییر، فقط فایل را Save کن و در GitHub دوباره `git push` بزن (یا از طریق سایت آپلود کن).
- نیازی به نصب Node.js یا هیچ ابزاری نیست.
- سایت کاملاً Responsive است و روی موبایل هم خوب نمایش داده می‌شود.
- تم تاریک/روشن به صورت خودکار ذخیره می‌شود.

اگر سوالی داشتی یا خواستی بخش خاصی اضافه شود (مثلاً Projects یا Skills)، بگو تا کمکت کنم.
