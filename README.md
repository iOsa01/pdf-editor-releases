<div dir="rtl">

# PDF Editor — محرر PDF محلي

**PDF Editor** تطبيق Android عربي أولاً، يعمل محلياً بدون خادم، مبني بـ **Kotlin** و **Jetpack Compose**. يتيح قراءة ملفات PDF وتحريرها وحمايتها وتحويلها مع حفظ النتائج كنسخ جديدة على الجهاز.

</div>

> PDF Editor is an Arabic-first, offline-first Android app for reading, editing, securing, and converting PDF files. Processing happens locally on the device.

---

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

## التوزيع | Distribution

🔗 **[github.com/iOsa01/pdf-editor-releases/releases/latest](https://github.com/iOsa01/pdf-editor-releases/releases/latest)**

يتحقق التطبيق من وجود تحديثات عبر:

```text
https://raw.githubusercontent.com/iOsa01/pdf-editor-releases/main/latest.json
```

---

## الرخصة | License

مشروع خاص. جميع الحقوق محفوظة. | Private project. All rights reserved.
