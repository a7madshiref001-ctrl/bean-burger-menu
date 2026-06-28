# bean&burger — منيو QR رقمي

منيو رقمي ثنائي اللغة (عربي/إنجليزي) متوافق مع اشتراطات هيئة الغذاء والدواء (السعرات + مسببات الحساسية)،
مبني بنفس محرك "محصول فاخر / Luxury Crop" بألوان وهوية bean&burger (أصفر/ذهبي + بني غامق).

## التشغيل محليًا
```bash
node server.js        # ثم افتح http://localhost:5070
```
(لازم خادم محلي — الصفحة تقرأ `data/menu.json` عبر fetch.)

## تعديل المنيو
كل المحتوى في ملف واحد: **`data/menu.json`**
- `brand` — الاسم، الموقع، التقييم (`rating`)، إنستقرام، خرائط، رقم واتساب.
- `categories[].items[]` — الصنف: `name_ar/en`, `desc_ar/en`, `price` (حُط `null` عشان يظهر TODO),
  `kcal`, `allergens` (مفاتيح من `allergen_ref`), `spicy`, `veg`, `high_sodium`, `available`.

## ⚠️ يحتاج تأكيد قبل النشر
الأصناف والأسعار والسعرات في `menu.json` **أمثلة تمثيلية** (لأن منيو المطعم على قوقل مابس صورة مش نص).
لازم تتأكد/تستبدل:
1. الأصناف والأسعار الحقيقية + السعرات الفعلية.
2. التقييم الحقيقي (`brand.rating`).
3. رقم واتساب التواصل (`brand.whatsapp_admin`).
4. اللوجو الحقيقي موجود في `assets/logo.png` (شفاف) وثابت في العربي والإنجليزي.

## الهوية (Premium Dark + Gold)
~70% غامق · 20% ذهبي · 10% كريمي
- Deep Espresso: `#1A0F0A` · Dark Brown (كروت): `#2B1C15`
- Caramel Gold: `#D6A049` · Light Gold: `#e9c483` · Accent Copper: `#B46A32`
- Soft Cream (نصوص): `#F4E6D0`
- الخطوط: عربي Tajawal (عناوين) + IBM Plex Sans Arabic (نصوص) — إنجليزي Poppins (عناوين) + Inter (نصوص)
- كروت بزوايا 24px و glow ذهبي عند الـ hover، خطوط ذهبية رفيعة، بدون أي صور (تصميم نظيف).
