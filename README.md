<div dir="rtl">

# PDF Editor — محرر PDF محلي

**PDF Editor** تطبيق Android عربي أولاً، يعمل محلياً بدون خادم، مبني بـ **Kotlin** و **Jetpack Compose**. يتيح قراءة ملفات PDF وتحريرها وحمايتها وتحويلها مع حفظ النتائج كنسخ جديدة على الجهاز.

الفكرة الأساسية للتطبيق أن يكون قارئ PDF هو مركز العمل، وليس مجرد شاشة عرض. يفتح المستخدم الملف، يقرأه، ثم يختار أدوات التحرير والتحويل والأمان من داخل القارئ أو من شاشة الأدوات، مع بقاء المعالجة محلية قدر الإمكان ودون رفع الملفات إلى خدمة خارجية.

</div>

> PDF Editor is an Arabic-first, offline-first Android app for reading, editing, securing, and converting PDF files. Processing happens locally on the device.

---

## لماذا PDF Editor؟

الكثير من تطبيقات PDF تعتمد على خدمات سحابية أو تفصل القراءة عن التحرير. PDF Editor يتجه إلى تجربة مختلفة:

- **محلي أولاً:** ملفاتك تبقى على جهازك، والمعالجة الأساسية تتم دون إرسال المستندات إلى خادم.
- **القارئ هو مساحة العمل:** الأدوات المهمة تظهر داخل سياق الصفحة المفتوحة.
- **نسخ آمنة:** الأدوات تحفظ نسخة جديدة ولا تعدل الأصل مباشرة.
- **عربي/إنجليزي:** واجهة ثنائية اللغة مع دعم RTL/LTR.
- **مصمم للهاتف:** الشاشات والقوائم مناسبة للاستخدام المتكرر على شاشة صغيرة.

## الميزات | Features

| القسم | الوصف | Description |
| --- | --- | --- |
| قراءة PDF | قارئ محلي مع تكبير، بحث، مصغرات، حفظ آخر موضع، ووضع قراءة مستمر | Local reader with zoom, search, thumbnails, last position, and continuous mode |
| تنظيم الصفحات | دمج، تقسيم، تدوير، إعادة ترتيب، حذف، واستخراج صفحات | Merge, split, rotate, reorder, delete, and extract pages |
| تحرير مباشر | تحديد موضع الصورة/العلامة المائية/التعليق/Redaction بالسحب داخل القارئ | Direct in-reader placement for images, watermarks, comments, and redaction |
| النماذج | تعبئة حقول PDF فوق الصفحة ثم حفظ نسخة جديدة | Fill PDF form fields over the page and save a new copy |
| التوقيع | توقيع نصي، توقيع مرسوم، وتوقيع من صورة | Text signature, drawn signature, and image-based signature |
| الحماية | تشفير بكلمة مرور، صلاحيات تفصيلية، فتح قفل، وتنظيف آمن | Password protection, permissions, unlock, and safe sanitization |
| Redaction | حجب مناطق متعددة عبر صفحات مختلفة مع Undo وتسطيح آمن | Multi-page redaction with undo and safe flattening |
| التحويل | PDF إلى صور، صور إلى PDF، استخراج نص، وOCR عربي/إنجليزي | PDF to images, images to PDF, text extraction, and Arabic/English OCR |
| التحسين | ضغط، تحجيم صفحات، تدرج رمادي، وإصلاح PDF | Compression, page resizing, grayscale, and repair |
| الإنتاجية | قوالب سريعة، فحص PDF قبل التنفيذ، معالجة دفعية WorkManager، وسجل عمليات | Presets, PDF preflight, WorkManager batch processing, and operation history |
| المشاركة | QR/Barcode لرابط الإصدارات، ومشاركة النتائج من داخل التطبيق | QR/Barcode for releases and in-app result sharing |

## تجربة القارئ

القارئ يدعم:

- فتح ملفات PDF من الجهاز أو من مشاركة التطبيقات الأخرى.
- الانتقال بين الصفحات بالسحب.
- التكبير والتصغير.
- البحث عند توفر نص قابل للاستخراج.
- مصغرات الصفحات.
- حفظ آخر صفحة تمت قراءتها لكل ملف.
- وضع قراءة مستمر أو صفحة واحدة.
- Ribbon أدوات داخل القارئ قريب من فكرة قوائم Office: مجموعة رئيسية ثم أدوات فرعية تظهر مؤقتاً.

## التحرير المباشر

يدعم التطبيق مسار تحرير مباشر داخل القارئ:

- اختيار أداة.
- تحديد موضعها على الصفحة بالسحب.
- معاينة التعديل فوق الصفحة.
- Undo داخل الجلسة قبل الحفظ.
- حفظ نسخة جديدة وفتح الناتج مباشرة.

يشمل ذلك حالياً الصور، العلامة المائية النصية، التعليقات النصية، الحماية السريعة، والنطاقات المحجوبة Redaction.

## الأمان والخصوصية

- لا يحتاج التطبيق إلى حساب لاستخدام أدوات PDF الأساسية.
- المعالجة الأساسية محلية على الجهاز.
- حماية PDF بكلمة مرور مع صلاحيات للطباعة والنسخ والتعديل.
- Redaction يتم بتسطيح الصفحات بعد الحجب حتى لا يبقى المحتوى المحجوب قابلاً للاستخراج.
- تنظيف آمن يحول الصفحات إلى صور لإزالة النص المخفي وحقول النماذج والطبقات القابلة للاستخراج.
- ملفات التوقيع وkeystore ليست جزءاً من المستودع.

## الإنتاجية

- شاشة عمليات تعرض التاريخ والمخرجات.
- قوالب سريعة مثل ضغط للمشاركة، ضغط للطباعة، حماية بدون نسخ، وعلامة مائية سرية.
- فحص PDF قبل التنفيذ: عدد الصفحات، التشفير، النماذج، وقابلية استخراج النص.
- معالجة دفعية عبر WorkManager للضغط والتدرج الرمادي.
- App Shortcuts للقارئ، الأدوات، والعمليات الأخيرة.

## التوزيع والتحديث

هذا المستودع مخصص لتوزيع ملفات APK وملف التحديث `latest.json`.

- صفحة الإصدار الأخيرة:
  `https://github.com/iOsa01/pdf-editor-releases/releases/latest`
- رابط تحميل APK مباشر:
  `https://github.com/iOsa01/pdf-editor-releases/releases/latest/download/pdf-editor-latest.apk`
- ملف التحديث الذي يقرأه التطبيق:
  `https://raw.githubusercontent.com/iOsa01/pdf-editor-releases/main/latest.json`

رمز QR داخل شاشة "حول التطبيق" يشير إلى صفحة الإصدارات الأخيرة.

## التقنيات | Tech Stack

- **Kotlin** و **Jetpack Compose**
- Android **PdfRenderer** للقراءة والمعاينة
- **PDFBox Android** لمعالجة PDF
- **Tesseract4Android** للـ OCR المحلي
- **Room** لسجل العمليات
- **DataStore** للإعدادات
- **WorkManager** للمعالجة الدفعية
- **ZXing** لتوليد QR/Barcode
- **ProfileInstaller** و Baseline Profile seed

---

## حالة الإصدار الحالي

| البند | القيمة |
| --- | --- |
| الإصدار | 0.1.0 |
| versionCode | 1 |
| الحزمة | `com.docuforge` |
| minSdk | 28 |
| targetSdk | 35 |
| نوع الملف | APK موقّع |
| الحجم التقريبي | 87MB |

تم اختبار النسخة على جهاز Android فعلي، مع اختبارات وحدة وواجهة، وفحص logcat بعد إصلاح انهيار القارئ.

## البناء | Build

```bash
export JAVA_HOME=~/java17 ANDROID_HOME=~/Android/Sdk
GRADLE_USER_HOME=/tmp/gradle-home ./gradlew :app:assembleRelease
```

الناتج:

```text
app/build/outputs/apk/release/app-release.apk
pdf-editor-latest.apk
```

### التوقيع

نسخة Release موقعة عبر `keystore.properties` المحلي، وهذا الملف ومفتاح التوقيع غير محفوظين في Git.

> Release builds are signed with the local release keystore configured through `keystore.properties`; signing secrets are not committed.

---

## رابط الإصدار | Release

🔗 **[github.com/iOsa01/pdf-editor-releases/releases/latest](https://github.com/iOsa01/pdf-editor-releases/releases/latest)**

يتحقق التطبيق من وجود تحديثات عبر:

```text
https://raw.githubusercontent.com/iOsa01/pdf-editor-releases/main/latest.json
```

---

## الرخصة | License

مشروع خاص. جميع الحقوق محفوظة. | Private project. All rights reserved.
