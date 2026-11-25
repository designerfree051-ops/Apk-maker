# ميزانيتي — نسخة Android (APK)

## بناء الـ APK من غير Android Studio (الأسهل)
1. اعمل حساب مجاني على github.com، وبعدين New repository (اسمه أي حاجة، Public أو Private).
2. ارفع كل محتويات الفولدر ده (www, package.json, capacitor.config.json, README.md).
3. الملف `.github/workflows/build-apk.yml`: لو الرفع بالسحب ما شالش الفولدر المخفي، اعمله من Add file > Create new file واكتب الاسم بالمسار ده بالظبط والصق محتواه.
4. افتح تبويب Actions > Build APK > Run workflow. استنى 5 إلى 10 دقايق.
5. افتح التشغيلة الناجحة ونزّل Artifact اسمه mizaniyati-apk (zip)، فكّه، وانقل app-debug.apk للموبايل وثبّته (فعّل "تثبيت من مصادر غير معروفة").
6. أول ما تفتح التطبيق وافق على الإشعارات. وفي إعدادات أندرويد خلّي البطارية للتطبيق "غير مقيّدة" عشان الإشعارات توصل في ميعادها.

## بناء محلي
npm install && npx cap add android && npx cap sync android && npx cap open android

## نقل بياناتك
بيانات التطبيق في المتصفح ما بتنتقلش لوحدها. من النسخة القديمة: الإعدادات > نسخة احتياطية > انسخ النص. وفي التطبيق الجديد: الإعدادات > استرجاع > الصق.
