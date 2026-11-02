# Nova X Icon Store

مستودع فهرس متجر الأيقونات الخاص بتطبيق Nova X Launcher.

## رابط الفهرس

`https://raw.githubusercontent.com/kelaniomar31-droid/NovaX-Icon-Store/main/catalog.json`

## الحزم القابلة للاستيراد المباشر

### Arcticons — 15.3.2
- المصدر: https://github.com/Arcticons-Team/Arcticons
- أرشيف المصدر ZIP: https://github.com/Arcticons-Team/Arcticons/archive/refs/tags/15.3.2.zip
- ملف الربط: `app/src/main/res/xml/appfilter.xml`
- الأصول: `newicons/` بصيغة SVG.
- الترخيص: GPL-3.0 لكود المشروع وCC BY-SA 4.0 للأيقونات.
- يجب على المستورد تحويل SVG إلى صيغة عرض داخلية آمنة، مع الاحتفاظ بنسبة المؤلفين وإشعار الترخيص وتطبيق شرط المشاركة بالمثل على التعديلات.

### Appstract — 5.0.6
- المصدر: https://github.com/yangchoo/Appstract
- أرشيف المصدر ZIP: https://github.com/yangchoo/Appstract/archive/refs/tags/v5.0.6.zip
- ملف الربط: `app/src/main/res/xml/appfilter.xml`
- قائمة الأيقونات: `app/src/main/res/xml/drawable.xml`
- الأصول: `icons/appstract-dark/` بصيغة PNG.
- الترخيص المعلن للمستودع: Apache-2.0.
- المؤلفة الأصلية للأيقونات: Melanie Gutzmann؛ المشروع الحالي fork مجتمعي. احتفظ بإشعارات الحقوق والنسب الواردة في المصدر والترخيص.

## سياسة الاستيراد والتوزيع

- `downloadType: zip` يعني تنزيل أرشيف المصدر واستيراد الأصول إلى مساحة Nova X الخاصة، ولا يعني تثبيت تطبيق Android.
- يجب أن يقرأ المستورد `archiveRoot` و`appfilterPath` و`drawableXmlPath` و`iconAssetsPath` و`iconFormat` من بيانات كل حزمة؛ لا تفترض أن جميع الحزم لها البنية نفسها.
- لا تعرض زر «استخدام» إلا بعد نجاح التنزيل والتحقق من الأرشيف والاستيراد وفحص ملفات الصور وملفات XML.
- Arcticons يتطلب دعم SVG أو تحويله محليًا إلى صيغة صور مدعومة قبل إظهاره كحزمة مستوردة جاهزة.
- Appstract يوفر أصول PNG، ويمكن استيرادها بعد التحقق من ملفات الربط.
- لا تشغّل أي ملفات من الأرشيف. طبّق حدودًا لحجم التنزيل وفك الضغط وعدد الملفات، وامنع Zip Slip والمسارات المطلقة وXML external entities.
- لا تحذف أو تستبدل أي حزم أو ثيمات أو إعدادات موجودة مسبقًا في Nova X.
- تحقق من التراخيص واحتفظ بإشعارات الحقوق والنسب المطلوبة. لا تخلط بين ترخيص كود المشروع وترخيص الأيقونات إذا اختلفا.

## التوافق

يحتفظ الفهرس بحقول التوافق السابقة مثل `id` و`name` و`developer` و`version` و`iconCount` و`category` و`sourceUrl` و`releaseUrl`، ويضيف حقول ZIP ومسارات الأصول وصيغها. يجب أن يتعامل قارئ الفهرس مع الحقول الاختيارية بأمان، وأن يتعامل مع `schemaVersion: 2` صراحةً.
