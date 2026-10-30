# نشر لَقمة على Render

المشروع واجهة React + Vite ويُنشر كـ **Static Site** وليس Web Service يعمل بخادم Node دائم.

## إعداد Render
- اختر **New → Static Site** واربط مستودع GitHub.
- إذا كان مجلد `laqma` هو جذر المستودع: اترك Root Directory فارغًا.
- إذا كان المشروع داخل مجلد فرعي اسمه `laqma`: اجعل Root Directory = `laqma`.
- Build Command: `npm install --include=dev && npm run build`
- Publish Directory: `dist`

يوجد ملف `render.yaml` بهذه الإعدادات، بما فيها rewrite إلى `index.html` حتى تعمل المسارات الداخلية عند تحديث الصفحة.

## ملاحظات
- استخدم Node.js 20 أو أحدث (يوجد `.node-version`).
- لا ترفع `node_modules` أو `dist` إلى Git؛ Render ينشئهما أثناء البناء.
