ملف تنزيل مكتبة لقراءة الصور واستخراج المعلومات منها 
يجب وضع مسار path

  `tesseract-ocr-w64-setup-v5.3.0.20221214.exe` هو الإصدار الحديث والصحيح الذي أوصي به. هذا سيمنحك أفضل دقة في التعرف على النص من الصور.

الآن بعد أن بدأت في تنزيل الإصدار الصحيح، يرجى المتابعة بالخطوات التالية لإكمال تثبيته وإعداده:

### **إكمال تثبيت Tesseract OCR (الإصدار 5.x.x):**

1.  **شغّل ملف `.exe`** الذي قمت بتنزيله.
2.  **أثناء عملية التثبيت (مهم جداً):**
    * عندما تصل إلى شاشة اختيار المكونات (Components)، تأكد من أنك تحدد خيار **"Additional language data" (بيانات لغة إضافية)**.
    * داخل "Additional language data"، تأكد من أنك تحدد **"Arabic (ara)"** و **"English (eng)"**. هذا يضمن أن Tesseract يمكنه قراءة النص باللغتين من الصور.
    * **لاحظ المسار الذي يتم تثبيت Tesseract فيه.** عادةً ما يكون `C:\Program Files\Tesseract-OCR`. ستحتاج إلى هذا المسار في الخطوة التالية.
3.  **أضف Tesseract إلى متغيرات البيئة (PATH):**
    * بعد اكتمال التثبيت، يجب إضافة مسار مجلد `Tesseract-OCR` إلى متغير البيئة `PATH` في Windows. هذا يسمح لـ `pytesseract` (مكتبة بايثون) بالعثور على Tesseract.
    * **كيفية القيام بذلك:**
        * اضغط على مفتاح `Windows` + `R` لفتح مربع التشغيل (Run dialog)، واكتب `sysdm.cpl` ثم اضغط `Enter`.
        * ستفتح نافذة "System Properties" (خصائص النظام). انتقل إلى علامة التبويب **"Advanced" (متقدم)**.
        * انقر على زر **"Environment Variables..." (متغيرات البيئة...)** في الأسفل.
        * في القسم السفلي "System variables" (متغيرات النظام)، ابحث عن المتغير المسمى **`Path`**.
        * انقر على `Path` لتحديده، ثم انقر على زر **"Edit..." (تحرير...)**.
        * في النافذة الجديدة، انقر على **"New" (جديد)** وأضف المسار الكامل إلى مجلد `Tesseract-OCR` الذي يحتوي على ملف `tesseract.exe` (على الأرجح `C:\Program Files\Tesseract-OCR`).
        * تأكد من أن المسار صحيح ثم انقر على "OK" في جميع النوافذ لإغلاقها.
4.  **أعد تشغيل سطر الأوامر (PowerShell):**
    * أغلق أي نوافذ PowerShell مفتوحة حالياً، ثم افتح نافذة PowerShell جديدة. هذا ضروري لتطبيق تغييرات متغيرات البيئة.

