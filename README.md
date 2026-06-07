<div dir="rtl" align="right">

# 🕌 Prayer Times JSON — بيانات مواقيت الصلاة

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Countries](https://img.shields.io/badge/Countries-3-brightgreen)]()
[![Cities](https://img.shields.io/badge/Cities-275-blue)]()
[![Format](https://img.shields.io/badge/Format-JSON-orange)]()
[![Status](https://img.shields.io/badge/Status-Stable-success)]()

بيانات ثابتة (Static JSON) لمواقيت الصلاة الرسمية المعتمدة، تغطي **275 مدينة** موزّعة على ثلاث دول. مُصمَّمة للمطوّرين الذين يحتاجون إلى بيانات موثوقة وخفيفة الحجم دون الاعتماد على واجهة برمجية خارجية (API).

---

## 📊 التغطية الجغرافية

| الدولة | المصدر الرسمي | عدد المدن |
|:-------|:-------------|:---------:|
| 🇱🇾 ليبيا | وزارة الأوقاف والشؤون الإسلامية — المواقيت الرسمية المعتمدة | 122 |
| 🇸🇦 المملكة العربية السعودية | مواقيت رسمية معتمدة | 117 |
| 🇯🇴 الأردن | مواقيت رسمية معتمدة | 36 |
| **الإجمالي** | | **275** |

---

## 📁 هيكل المستودع

```
prayer-times-json/
│
├── data/
│   ├── ly/                      # 🇱🇾 ليبيا — 122 مدينة
│   │   ├── tripoli.json
│   │   ├── benghazi.json
│   │   └── ...
│   │
│   ├── sa/                      # 🇸🇦 المملكة العربية السعودية — 117 مدينة
│   │   ├── riyadh.json
│   │   ├── jeddah.json
│   │   └── ...
│   │
│   └── jo/                      # 🇯🇴 الأردن — 36 مدينة
│       ├── amman.json
│       ├── zarqa.json
│       └── ...
│
├── combined/                    # ملفات مدمجة لكل دولة (ملف واحد لكل الدولة)
│   ├── libya.json
│   ├── saudi_arabia.json
│   └── jordan.json
│
└── README.md
```

---

## 🗂️ بنية ملف JSON

كل ملف مدينة يتبع البنية الموحّدة الآتية:

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
    },
    "02": { "...": "..." },
    "12": { "...": "..." }
  }
}
```

> المفاتيح الرقمية `"01"` إلى `"12"` تمثّل أرقام الشهور الميلادية.  
> كل شهر يحتوي على جدول الأوقات الخاص به ليعكس التغيّر الموسمي.

---

## 🚀 أمثلة الاستخدام

### JavaScript — Fetch API

```javascript
const month = String(new Date().getMonth() + 1).padStart(2, '0');

const response = await fetch(
  'https://raw.githubusercontent.com/YOUR_USERNAME/prayer-times-json/main/data/ly/tripoli.json'
);
const data = await response.json();

const todayTimes = data.times[month];
console.log('Fajr:', todayTimes.fajr);
console.log('Maghrib:', todayTimes.maghrib);
```

### Python

```python
import json
from datetime import date

with open("data/ly/tripoli.json", encoding="utf-8") as f:
    data = json.load(f)

month = str(date.today().month).zfill(2)
times = data["times"][month]
print(f"Fajr: {times['fajr']} | Dhuhr: {times['dhuhr']} | Maghrib: {times['maghrib']}")
```

---

## ✅ حالات الاستخدام المناسبة

| حالة الاستخدام | الوصف |
|:--------------|:------|
| **تطبيقات Offline-first** | تطبيقات الهاتف المحمول التي تعمل دون اتصال دائم بالإنترنت |
| **مواقع إلكترونية** | تحميل سريع مع تقليل الاعتماد على خدمات خارجية |
| **أجهزة IoT** | Raspberry Pi وESP32 لشاشات عرض أوقات الصلاة |
| **تطبيقات المساجد** | الجداول الثابتة المعتمدة للعرض والإذاعة |

---

## 📜 المصادر والمنهجية

- **🇱🇾 ليبيا:** مستمدة من الجداول الرسمية لوزارة الأوقاف والشؤون الإسلامية الليبية، وهي الجهة الدينية الرسمية المعتمدة في البلاد.
- **🇸🇦 المملكة العربية السعودية:** مواقيت رسمية معتمدة.
- **🇯🇴 الأردن:** مواقيت رسمية معتمدة.

---

## 🏅 شكر وتقدير

> يُقدَّم الشكر الخالص والتقدير العميق لمطوّر تطبيق **مؤذن ليبيا**،
> الذي أتاحت بيانات تطبيقه الأساسَ لاستخراج مواقيت الصلاة الليبية المعتمدة
> المستخدمة في هذا المستودع.
>
> جهده في تجميع مواقيت رسمية لـ **122 مدينة ليبية** وتضمينها في تطبيق موثوق
> يستحق الاعتراف والامتنان. هذا المستودع لا يسعى إلى منافسة تطبيقه،
> بل إلى إتاحة هذه البيانات القيّمة للمطوّرين في صيغة مفتوحة وسهلة التكامل.
>
> ندعو المجتمع إلى دعم التطبيق الأصلي: **[https://play.google.com/store/apps/details?id=com.mahmoud.android.MoadenLibya]**

---

## ⚠️ إخلاء مسؤولية

المواقيت الواردة مستمدة من مصادر رسمية وقت جمعها. قد تطرأ تعديلات طفيفة من عام لآخر بقرار من الجهات الدينية المختصة في كل دولة. يُنصح دائماً بمراجعة الجهات الرسمية للحصول على أحدث الجداول السنوية المعتمدة.

---

## 📄 الرخصة

مُرخَّص بموجب **[Creative Commons Attribution 4.0 International — CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)**.

يُسمح بالاستخدام الحرّ والتعديل وإعادة التوزيع، بشرط نسب الفضل إلى هذا المستودع والإشارة إلى مطوّر تطبيق مؤذن ليبيا مصدراً للبيانات الليبية.

---

<div align="center">

صُنع بـ ☕ في **طبرق، ليبيا** 🇱🇾

*"وَأَقِيمُوا الصَّلَاةَ وَآتُوا الزَّكَاةَ" — سورة البقرة: ٤٣*

</div>

</div>