# Modern Guide — تعليمات النشر والإعداد

## 📁 هيكل الملفات
```
/
├── index.html       ← الصفحة الرئيسية (كل شيء مدمج)
├── manifest.json    ← إعدادات PWA
├── sw.js            ← Service Worker للعمل بدون إنترنت
└── icons/
    ├── icon-192.png ← أيقونة التطبيق (192×192)
    └── icon-512.png ← أيقونة التطبيق (512×512)
```

## 🔐 كلمة مرور لوحة التحكم (Admin)
```
modernguide2025
```
يمكنك تغييرها في ملف index.html — ابحث عن:
```js
const ADMIN_PASS = 'modernguide2025';
```

## 📧 إعداد الإشعارات عبر EmailJS
1. اذهب إلى https://www.emailjs.com وأنشئ حساباً مجانياً
2. أضف خدمة Gmail واربطها بـ meghranihocin03@gmail.com
3. أنشئ Template وضع فيها: product, user, amount, time
4. انسخ Public Key، Service ID، Template ID
5. في index.html ابحث عن `sendEmailNotification` وعدّل:
```js
service_id: 'service_XXXX',
template_id: 'template_XXXX',
user_id: 'YOUR_PUBLIC_KEY',
```

## 📲 إعداد الأيقونات
أضف صورة الأيقونة (192×192 و 512×512 بيكسل) باسم icon-192.png و icon-512.png
في مجلد icons/ بجانب index.html

## 🌐 النشر على GitHub Pages
1. ارفع جميع الملفات على الـ repo
2. اذهب إلى Settings > Pages
3. اختر Branch: main > Save
4. سيكون موقعك على: https://hocinmaghnaoui-HM.github.io/Modern-Guide-/

## 💳 معلومات الدفع (مدمجة في الكود)
- **RedotPay ID**: 1072516062 (للدفع بالدولار)
- **CCP**: 002783651789 (للدفع بالدينار الجزائري)

## ✨ المميزات المضمّنة
- ✅ بطاقات احترافية Glassmorphism لكل منتج
- ✅ نظام شراء متكامل (اختيار وسيلة دفع + رفع إثبات)
- ✅ محاكاة تحقق ذكاء اصطناعي
- ✅ واجهة المنتج بعد الشراء (Dashboard / Reader / AI Chat)
- ✅ لوحة تحكم المحرر (Admin Panel)
- ✅ نظام حسابات (تسجيل/دخول)
- ✅ إشعارات داخلية
- ✅ PWA (قابل للتثبيت على الهاتف)
- ✅ Service Worker (عمل بدون إنترنت)
- ✅ تبديل وضع ليلي/نهاري
- ✅ تبديل اللغة عربي/إنجليزي
- ✅ حفظ البيانات في LocalStorage
- ✅ إضافة منتجات جديدة من الواجهة
