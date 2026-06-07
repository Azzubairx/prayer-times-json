<div dir="rtl" align="right">

# 🕌 Prayer Times JSON — بيانات مواقيت الصلاة

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Countries](https://img.shields.io/badge/Countries-3-green)]()
[![Cities](https://img.shields.io/badge/Cities-275-blue)]()
[![Format](https://img.shields.io/badge/Format-JSON-orange)]()

مجموعة بيانات ثابتة (Static) بصيغة JSON لمواقيت الصلاة الرسمية تغطي **275 مدينة** في ثلاث دول. مصممة للاستخدام في التطبيقات والمواقع الإلكترونية وأجهزة IoT التي تحتاج إلى بيانات موثوقة دون الاعتماد على API خارجي.

---

## 📊 التغطية الجغرافية

| الدولة | المصدر الرسمي | عدد المدن |
|--------|--------------|----------|
| 🇱🇾 ليبيا | وزارة الأوقاف والشؤون الإسلامية | 122 مدينة |
| 🇸🇦 المملكة العربية السعودية | — | 117 مدينة |
| 🇯🇴 الأردن | — | 36 مدينة |
| **المجموع** | | **275 مدينة** |

---

## 📁 هيكل المستودع

أنت كاتب تقني خبير في GitHub ومخطط استراتيجي لمشاريع البرمجيات مفتوحة المصدر.

أريد إنشاء مستودع على GitHub يحتوي على ملفات json جاهزة لأوقات الصلوات للدول (Libya (مواقيت وزارة الأوقاف المعتمدة), KSA, and Jordan).  

ليبيا (122 مدينة)
السعودية (117 مدينة)
الأردن (36 مدينة)

أريدك أن تعطيني تسمية للمستودع، وصف له، وحتوى ملف readme.md. مع شكر ونسب الفضل لمطور تطبيق "مؤذن ليبيا" ﻷنني استخرجت المواقيت من ملف APK للتطبيق.

Show more
00:14

استحضر معايير التسمية وصياغة توثيق شامل متوازن
استحضر معايير التسمية وصياغة توثيق شامل متوازن
ملاحظة نقدية أولاً ⚠️
قبل البناء، هناك نقطة جوهرية تستحق التأمل: استخراج البيانات من APK قد يُشكّل تعارضاً مع شروط استخدام التطبيق أو حقوق الملكية الفكرية للمطوّر، حتى مع نسب الفضل إليه. الأسلم أن تتواصل مع المطوّر وتحصل على إذن صريح أو رخصة مفتوحة قبل نشر البيانات علناً. هذا يحمي المشروع قانونياً ويُعزّز علاقة تعاونية بدل كونها أحادية.

اقتراح اسم المستودع
prayer-times-data
أو البديل الأكثر وصفية:

official-prayer-times-ly-sa-jo
الأفضل للـ SEO والوضوح:

prayer-times-json
توصيتي: prayer-times-json — قصير، واضح، قابل للبحث، لا يقيّد التوسع مستقبلاً لدول أخرى.

الوصف (Repository Description)
Static JSON datasets for official Islamic prayer times covering 275 cities across Libya (Ministry of Awqaf), Saudi Arabia, and Jordan. Ready for offline use in apps, websites, and IoT devices.
محتوى ملف README.md
إليك المحتوى الكامل:

markdown
<div dir="rtl" align="right">

# 🕌 Prayer Times JSON — بيانات مواقيت الصلاة

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Countries](https://img.shields.io/badge/Countries-3-green)]()
[![Cities](https://img.shields.io/badge/Cities-275-blue)]()
[![Format](https://img.shields.io/badge/Format-JSON-orange)]()

مجموعة بيانات ثابتة (Static) بصيغة JSON لمواقيت الصلاة الرسمية تغطي **275 مدينة** في ثلاث دول. مصممة للاستخدام في التطبيقات والمواقع الإلكترونية وأجهزة IoT التي تحتاج إلى بيانات موثوقة دون الاعتماد على API خارجي.

---

## 📊 التغطية الجغرافية

|
 الدولة 
|
 المصدر الرسمي 
|
 عدد المدن 
|
|
--------
|
--------------
|
----------
|
|
 🇱🇾 ليبيا 
|
 وزارة الأوقاف والشؤون الإسلامية 
|
 122 مدينة 
|
|
 🇸🇦 المملكة العربية السعودية 
|
 — 
|
 117 مدينة 
|
|
 🇯🇴 الأردن 
|
 — 
|
 36 مدينة 
|
|
**
المجموع
**
|
|
**
275 مدينة
**
|

---

## 📁 هيكل المستودع
prayer-times-json/
│
├── 📂 data/
│   ├── 📂 ly/              # ليبيا
│   │   ├── tripoli.json
│   │   ├── benghazi.json
│   │   └── ...             # 122 ملف
│   │
│   ├── 📂 sa/              # المملكة العربية السعودية
│   │   ├── riyadh.json
│   │   ├── jeddah.json
│   │   └── ...             # 117 ملف
│   │
│   └── 📂 jo/              # الأردن
│       ├── amman.json
│       ├── zarqa.json
│       └── ...             # 36 ملف
│
├── 📂 combined/            # ملفات مدمجة لكل دولة
│   ├── libya.json
│   ├── saudi_arabia.json
│   └── jordan.json
│
└── README.md
---

## 🗂️ هيكل ملف JSON

كل ملف مدينة يتبع البنية التالية:

```json
{
  "city": "Tripoli",
  "city_ar": "طرابلس",
  "country": "LY",
  "latitude": 32.9023,
  "longitude": 13.1803,
  "times": {
    "01": {
      "fajr":    "05:12",
      "sunrise": "06:48",
      "dhuhr":   "12:15",
      "asr":     "15:22",
      "maghrib": "17:42",
      "isha":    "19:08"
    }
  }
}
```

> المفتاح الرقمي (`"01"` إلى `"12"`) يمثل رقم الشهر الميلادي.

---

## 🚀 الاستخدام

### JavaScript / Fetch API

```javascript
const response = await fetch(
  'https://raw.githubusercontent.com/azzubairx/prayer-times-json/main/data/ly/tripoli.json'
);
const data = await response.json();
const month = new Date().getMonth() + 1;
const todayTimes = data.times[String(month).padStart(2, '0')];
console.log('Fajr:', todayTimes.fajr);
```

### Python

```python
import json, datetime

with open("data/ly/tripoli.json", encoding="utf-8") as f:
    data = json.load(f)

month = str(datetime.date.today().month).zfill(2)
print(data["times"][month])
```

---

## ✅ حالات الاستخدام المناسبة

- تطبيقات الهاتف المحمول (أندرويد / iOS) التي تعمل دون إنترنت
- مواقع إلكترونية تحتاج بيانات سريعة دون latency من API
- أجهزة IoT (Raspberry Pi، ESP32) لشاشات عرض الأوقات
- تطبيقات المساجد والمراكز الإسلامية

---

## 📜 المصادر والمنهجية

- **ليبيا:** المواقيت مستمدة من الجداول الرسمية لـ **وزارة الأوقاف والشؤون الإسلامية الليبية**، وهي المرجع المعتمد رسمياً في البلاد.
- **السعودية والأردن:** مواقيت رسمية معتمدة.

---

## 🏅 شكر وتقدير خاص

> يُقدَّم الشكر الجزيل والتقدير العميق للمطوّر الكريم لتطبيق **[مؤذن ليبيا](https://play.google.com/store/apps/details?id=com.example.libyanmoathen)**، الذي أتاحت بيانات تطبيقه الأساسَ لاستخراج مواقيت الصلاة الليبية المعتمدة المستخدمة في هذا المستودع.
>
> جهده في تجميع المواقيت الرسمية لـ 122 مدينة ليبية وتضمينها في تطبيق موثوق يستحق الاعتراف والامتنان. هذا المستودع لا يسعى إلى منافسة تطبيقه، بل إلى إتاحة هذه البيانات القيّمة للمطوّرين بصيغة مفتوحة وسهلة الاندماج.
>
> ندعو المجتمع للدعم المعنوي للتطبيق الأصلي: **[رابط تطبيق مؤذن ليبيا]**

---

## ⚠️ إخلاء مسؤولية

مواقيت الصلاة الواردة هنا مستمدة من مصادر رسمية ومعتمدة وقت جمعها. قد تطرأ تعديلات طفيفة من عام لآخر بقرار من الجهات الدينية المختصة. يُنصح بمراجعة الجهات الرسمية في كل دولة للحصول على أحدث الجداول السنوية.

---

## 📄 الرخصة

هذا المستودع مرخص بموجب **[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)**.

يُسمح بالاستخدام، التعديل، وإعادة التوزيع بشرط نسب الفضل إلى هذا المستودع ومطوّر تطبيق مؤذن ليبيا.

---

<div align="center">

صُنع بـ ☕ في **طبرق، ليبيا** 🇱🇾

</div>

</div>