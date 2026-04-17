# AQ Dev — Portfolio Website

موقع محفظة مشاريع احترافي مبني بـ HTML/CSS/JS الخالص، يعمل على GitHub Pages.

## 🚀 رفع الموقع على GitHub Pages

### الخطوة 1: إنشاء Repository

1. افتح [github.com](https://github.com) وسجّل دخول
2. اضغط **New repository**
3. سمّه: `YOUR_USERNAME.github.io` ← **مهم جداً** (استبدل YOUR_USERNAME باسم حسابك)
   - مثال: إذا اسم حسابك `abdulquddus` → اسم الـ repo يكون `abdulquddus.github.io`
4. اجعله **Public**
5. لا تضيف README (سنرفع الملفات مباشرة)
6. اضغط **Create repository**

### الخطوة 2: رفع الملفات

**الطريقة السهلة (بدون Git):**
1. افتح الـ repository الجديد
2. اضغط **uploading an existing file**
3. اسحب جميع ملفات المجلد (`index.html`, `sitemap.xml`, `robots.txt`, `manifest.json`, `404.html`, `js/`) وأفلتها
4. اضغط **Commit changes**

**الطريقة بـ Git (للمحترفين):**
```bash
git init
git add .
git commit -m "Initial portfolio"
git remote add origin https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git
git push -u origin main
```

### الخطوة 3: تفعيل GitHub Pages

1. اذهب لـ repository → **Settings**
2. في القائمة الجانبية: **Pages**
3. Source: **Deploy from a branch**
4. Branch: **main** → **/ (root)**
5. اضغط **Save**
6. انتظر 2-3 دقائق → سيظهر رابط موقعك

رابط موقعك سيكون: `https://YOUR_USERNAME.github.io`

---

## 📱 رفع ملفات APK للتنزيل المباشر

**GitHub Releases (الأفضل — مجاني تماماً):**

1. في الـ repository → **Releases** → **Create a new release**
2. في **Tag version** اكتب: `v1.0.0`
3. في **Release title**: `Souga v1.0.0`
4. اسحب ملف `app-release.apk` وأفلته في منطقة الملفات
5. اضغط **Publish release**
6. الرابط المباشر سيكون:
   ```
   https://github.com/YOUR_USERNAME/YOUR_REPO/releases/download/v1.0.0/app-release.apk
   ```

ضع هذا الرابط في `js/projects.js` في حقل `downloadUrl` لمشروع سوقة.

---

## ✏️ تخصيص الموقع

### تغيير معلوماتك الشخصية

في `index.html` ابحث عن وعدّل:
- `your@email.com` → بريدك الإلكتروني
- `YOUR_USERNAME` → اسم حساب GitHub
- `YOUR_TELEGRAM` → معرف Telegram
- `966XXXXXXXXX` → رقم WhatsApp مع كود الدولة
- `aqdev.github.io` → اسم موقعك الفعلي

### إضافة مشروع جديد

في `js/projects.js` انسخ القالب المعلّق وأضف مشروعك:
```js
{
  id: "my-project",        // معرف فريد (بالإنجليزي)
  slug: "my-project",      // نفس الـ id
  title: "اسم مشروعي",
  subtitle: "وصف مختصر",
  description: "وصف قصير للبطاقة",
  longDescription: "وصف تفصيلي يظهر في نافذة التفاصيل",
  type: "android",         // android | webapp | desktop | website
  platform: "Android",
  status: "released",      // released | beta | coming_soon
  version: "1.0.0",
  size: "15 MB",
  category: "تجارة",
  tags: ["Flutter", "Firebase"],
  color: "#DC143C",        // اللون الرئيسي
  icon: "🛒",              // إيموجي الأيقونة
  downloadUrl: "https://github.com/.../releases/download/.../app.apk",
  featured: true,          // يجعلها بطاقة كبيرة
  date: "2025",
  stats: { downloads: "1K+", rating: "4.8", reviews: "50+" }
}
```

### تحديث الـ sitemap بعد إضافة مشروع

في `sitemap.xml` أضف:
```xml
<url>
  <loc>https://YOUR_USERNAME.github.io/?project=YOUR_PROJECT_ID</loc>
  <lastmod>2025-04-17</lastmod>
  <priority>0.8</priority>
</url>
```

---

## 🔗 Deep Links

رابط مباشر لأي مشروع:
```
https://YOUR_USERNAME.github.io/?project=souga
```

عند مشاركة هذا الرابط → تنقل المستخدم مباشرة لصفحة تفاصيل سوقة.

---

## 🔍 ظهور في Google

بعد رفع الموقع، أرسل الـ sitemap لـ Google:
1. افتح [Google Search Console](https://search.google.com/search-console)
2. أضف موقعك
3. في القائمة: **Sitemaps** → أدخل: `sitemap.xml`
4. اضغط **Submit**

Google ستبدأ بفهرسة الموقع خلال أسبوع.
