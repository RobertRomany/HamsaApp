# موقع همسة

صفحة واحدة بتشتغل كموقع تحميل وكبريزنتيشن. HTML وCSS وJavaScript صافي، من غير build ولا مكتبات.

## الملفات
```
index.html                  الصفحة كلها
assets/icon.svg             شعار التطبيق (الأصل)
assets/icon-192.png         نسخ PNG للشعار
assets/icon-512.png
assets/apple-touch-icon.png
.nojekyll                   علشان GitHub Pages يعرض الملفات زي ما هي
```

## تجربة محلية
افتح `index.html` في المتصفح، أو شغّل سيرفر بسيط:
```
python -m http.server 8000
```
وافتح `http://localhost:8000`. الخطوط جاية من Google Fonts فمحتاجة نت.

## تغيير لينكات التحميل
في `index.html` دوّر على `data-url=""` (فيه زرار في أول الصفحة وزرارين في آخرها). حط اللينك جواه:
```html
<button class="btn gold store" data-url="https://play.google.com/store/apps/details?id=YOUR.PACKAGE">
```
لو الـ `data-url` فاضي، الزرار بيعرض رسالة «الرابط هيتضاف هنا أول ما التطبيق يتنشر».

## النشر على GitHub Pages
1. اعمل repository جديد وارفع الملفات دي في الـ root (مش جوه فولدر).
2. من **Settings ← Pages** اختار **Deploy from a branch**، والـ branch `main` والفولدر `/ (root)`.
3. بعد دقيقة الموقع يظهر على `https://USERNAME.github.io/REPO/`.
4. المسارات كلها نسبية (`assets/...`) فبتشتغل على رابط المشروع من غير تعديل.

## صورة المعاينة عند المشاركة (واتساب وفيسبوك)
تاج `og:image` في `index.html` مسار نسبي. المنصات بتطلب **رابط كامل**، فبعد ما تعرف عنوان موقعك غيّره:
```html
<meta property="og:image" content="https://USERNAME.github.io/REPO/assets/icon-512.png">
```

## وضع العرض
زرار **وضع العرض** فوق بيفتح ملء الشاشة. الأسهم أو Space أو PageDown بتنقل بين الشرائح، والنقاط على الجنب بتنقلك لأي شريحة.
