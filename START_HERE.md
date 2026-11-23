# دليل التشغيل الذاتي الفوري — استوديو الفيديو الذكي
# AI Video Studio — Autonomous Bootstrap Directive

> **تعليمات موجهة إلى Antigravity / AI Agent:**
> بمجرد أن يطلب منك المستخدم تنفيذ هذا الملف، تعامل مع هذا المستند كـ **خطة تنفيذية ذاتية (Autonomous Directive)**. قم بتنفيذ المراحل التالية بالتتابع وبشكل مستقل تماماً ودون طلب أي موافقات يدوية حتى تصل إلى مرحلة المقابلة الشخصية.

---

## المرحلة الأولى: فحص وتثبيت بيئة التشغيل الأساسية

1. **فحص نظام التشغيل والأدوات الرئيسية:**
   - افحص وجود (Node.js) بإصدار LTS و (Python) بإصدار 3.10 فما فوق، و (FFmpeg).
   - إذا كان أي منها ناقصاً:
     - على نظام Windows: قم بتثبيتها بصمت عبر `winget`:
       - `winget install -e --id OpenJS.NodeJS.LTS --accept-package-agreements --accept-source-agreements`
       - `winget install -e --id Python.Python.3.11 --accept-package-agreements --accept-source-agreements`
       - `winget install -e --id Gyan.FFmpeg --accept-package-agreements --accept-source-agreements`
     - على نظام macOS: قم بتثبيتها عبر `brew` (node, python@3.11, ffmpeg).

2. **تثبيت حزم بايثون للذكاء الاصطناعي ومعالجة الصوت:**
   - نفذ أمر التثبيت للمكتبات التالية:
     `python -m pip install --upgrade pip`
     `python -m pip install faster-whisper yt-dlp opencv-python librosa soundfile pydub`

---

## المرحلة الثانية: تأسيس هيكل المجلدات الخماسي

أنشئ المجلدات الخمسة المعتمدة مع تقسيماتها الداخلية الدقيقة كالتالي:

```text
📁 Setup_and_Tools/
   ├── 📁 scripts/           (ضع به سكربت التفريغ الصوتي الآلي transcribe_whisper.py)
   ├── 📁 environment/       (ملفات فحص البيئة)
   └── 📁 skills/            (مهارات الموشن: kinetic_captions, motion_physics, sfx_sync)

📁 Reference/
   └── 📁 00_My_Brand_Identity/  (مجلد محجوز لهوية المستخدم الثابتة)

📁 Raw_Footage/
   ├── 📁 audio/
   │   ├── 📁 voiceovers/    (مكان وضع الفويس أوفر الأساسي)
   │   ├── 📁 music/         (الموسيقى التصويرية)
   │   └── 📁 sfx/           (المؤثرات الصوتية)
   ├── 📁 video/
   │   ├── 📁 screen_records/ (تسجيلات الشاشة)
   │   └── 📁 b_roll/        (اللقطات الخارجية)
   ├── 📁 assets/            (الصور والشعارات المساعدة)
   └── 📁 transcripts/       (تفريغات Whisper الزمنية)

📁 Projects/
   └── 📁 _shared/           (مكونات الكابشن والأشكال المشتركة)

📁 Exports/
   ├── 📁 shorts_reels/      (مقاس 9:16 للموبايل)
   ├── 📁 youtube_full/      (مقاس 16:9 للشاشات العريضة)
   ├── 📁 thumbnails/        (الصور المصغرة PNG)
   └── 📁 archive/           (المسودات السابقة)
```

---

## المرحلة الثالثة: تأسيس مشروع المونتاج البرمجي (Remotion Core)

1. أنشئ مشروع Remotion جديد ومستقر داخل مساحة المشاريع `Projects/`.
2. ثبّت الحزم الأساسية التالية في المشروع:
   `npm install remotion @remotion/paths @remotion/shapes @remotion/transitions @remotion/motion-blur tailwindcss lucide-react`
3. اكتب داخل `Setup_and_Tools/scripts/transcribe_whisper.py` سكربت بايثون يستقبل ملف صوتي ويستخرج منه تفريغاً دقيقاً لكل كلمة بالملي ثانية وبالفريمات (@30fps) ويحفظ الناتج بصيغة JSON و SRT داخل `Raw_Footage/transcripts/`.

---

## المرحلة الرابعة: التحقق النهائي من الجاهزية

- اختبر تشغيل:
  - `node -v`
  - `python -c "import faster_whisper; print('Whisper OK')"`
  - `ffmpeg -version`
- تأكد أن كل الأدوات تعمل بنسبة 100%.

---

## المرحلة الخامسة: بدء المقابلة الشخصية لتثبيت الهوية فوراً

بمجرد اكتمال المراحل السابقة بنجاح، توجه فوراً إلى المستخدم في نافذة المحادثة باللغة العربية بهذه الرسالة:

> **«مرحباً بك! تم فحص لابتوبك وتثبيت كافة البرمجيات (Node.js, Python, FFmpeg) وتأسيس الهيكل الخماسي للاستوديو بنجاح 100%. بصفتي مخرجك الإبداعي، سنبدأ معاً الآن مقابلة تفاعلية سريعة من 6 أسئلة لاكتشاف وتثبيت هويتك البصرية الخاصة في مجلد (Reference/00_My_Brand_Identity).»**

ثم ابدأ فوراً بسؤاله **السؤال الأول**:
1. **[مظهر وخلفية الفيديوهات]:**
   - هل تفضل:
     (أ) خلفيات داكنة فخمة مع إضاءة خافتة؟
     (ب) خلفيات دافئة حجرية بدرجات البيج المطفأ؟
     (ج) شبكة تقنية حديثة (Tech Grid)؟
     (د) تدرجات ملونة ناعمة؟

وانتظر إجابته لتسأله الأسئلة الخمسة الباقية (كثافة الكلام والرسوم، الألوان، التايبوجرافي والكابشن، العناصر الثابتة، والممنوعات)، ثم لخص هويته واحفظها داخل:
- `Reference/00_My_Brand_Identity/design_tokens.json`
- `Reference/00_My_Brand_Identity/visual_philosophy.md` (مع تثبيت قاعدته الذهبية: عناوين ورسوم توضيحية فقط وبدون فقرات كلام طويلة)
- `Reference/00_My_Brand_Identity/caption_preset.json`
- `Reference/00_My_Brand_Identity/red_lines.md`

---

## دليل الاستخدام السريع للمستخدم بعد التثبيت:

| ما تريد فعله | ما تطلبه من Antigravity في الشات |
| :--- | :--- |
| **إنشاء فيديو جديد بضربة واحدة وبدون تكرار** | استخدم **برومبت الإنتاج الشامل (Master Video Intake Prompt)** الموثق في [`README.md`](./README.md) واملأ حقوله لبدء المشروع ككبسولة معزولة بالكامل دون الحاجة لأي مراجعات لاحقة. |
| **إضافة مرجع جديد** | ضع الفيديو في `Reference/` وقل: *"حلل الفيديو المرجعي الجديد في غرفة معزولة واستخرج حركته ورسومه"* |
| **تفريغ الفويس أوفر** | ضع الصوت في `Raw_Footage/audio/voiceovers/` وقل: *"فرغ الصوت بـ Whisper واستخرج الكلمات بدقة الفريم"* |
| **معاينة الفيديو** | اكتب في الترمينال: `npm run dev` لمشاهدة الفيديو فريماً بفريم في المتصفح على `http://localhost:3000` |
| **الرندر النهائي** | *"رندر مشروع Video_XX بصيغة MP4 وطلعه في Exports/shorts_reels ومعه صورة مصغرة"* |
