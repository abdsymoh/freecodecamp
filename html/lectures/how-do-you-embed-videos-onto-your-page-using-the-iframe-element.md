# كيفية تضمين مقاطع الفيديو في صفحتك باستخدام عنصر $\text{iframe}$

---

## ما هو عنصر $\text{iframe}$؟

**$\text{iframe}$** هو اختصار لـ **"إطار داخلي" (inline frame)**. إنه عنصر $\text{inline}$ يُستخدم لتضمين محتوى $\text{HTML}$ آخر مباشرةً داخل صفحة $\text{HTML}$ الحالية. يمكن أن يكون محتوى $\text{HTML}$ هذا عبارة عن **فيديو**، أو **خريطة**، أو **عنصر $\text{HTML}$ آخر**، أو حتى **صفحات ويب كاملة** أخرى.

إليك شكل البنية الأساسية لعنصر $\text{iframe}$:

```html
<iframe src="video-url" width="width-value" height="height-value" allowfullscreen></iframe>
```

### الخصائص الأساسية لعنصر $\text{iframe}$:

- **$\text{src}$**: تحدد عنوان $\text{URL}$ للصفحة أو المورد الذي تريد تضمينه.
- **$\text{width}$**: تحدد عرض الإطار المُضمن.
- **$\text{height}$**: تحدد ارتفاع الإطار المُضمن.
- **$\text{allowfullscreen}$**: تسمح للمستخدم بعرض الإطار المُضمن في وضع ملء الشاشة.
- **$\text{title}$**: يُنصح بتحديد خاصية $\text{title}$ (العنوان) للإطار المُضمن، وهي مهمة لأغراض **إمكانية الوصول (Accessibility)**.

---

## تضمين مقطع فيديو باستخدام $\text{iframe}$

لتضمين مقطع فيديو داخل $\text{iframe}$، يمكنك نسخ كود التضمين مباشرةً من خدمات الفيديو الشهيرة مثل **YouTube** و **Vimeo**، أو تحديده بنفسك من خلال توجيه خاصية **$\text{src}$** إلى رابط الفيديو.

### مثال 1: تضمين فيديو من YouTube (الكود الكامل)

```html
<h1>فيديو freeCodeCamp على YouTube مُضمن باستخدام عنصر iframe</h1>
<iframe width="560" height="315" src="https://www.youtube.com/embed/PkZNo7MFNFg?si=-UBVIUNM3csdeiWF" title="YouTube video player" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

### ملاحظة مهمة لتضمين فيديوهات YouTube:

عند نسخ رابط مشاركة (Share Link) من YouTube، يكون النطاق عادةً هو **$\text{[https://youtu.be](https://youtu.be)}$**. لتضمين الفيديو بنجاح باستخدام $\text{iframe}$، **يجب** استبدال هذا النطاق بـ **$\text{[https://youtube.com/embed/](https://youtube.com/embed/)}$**.

**مثال على التحويل:**

إذا كان رابط المشاركة هو: `https://youtu.be/gp5H0Vw39yw`
يجب أن يصبح رابط $\text{src}$ هو: `https://youtube.com/embed/gp5H0Vw39yw`

```html
<iframe src="https://youtube.com/embed/gp5H0Vw39yw?si=Rb_2nDK6abv1iIAM" title="freeCodeCamp Typescript Course" width="500" height="285" allowfullscreen></iframe>
```

### مثال 2: تضمين فيديو من مصدر آخر (مثل Pixabay)

لاحظ أن الفيديو يمكن أن يأتي من أي مكان، وليس بالضرورة من خدمات الفيديو مثل YouTube وVimeo.

```html
<h1>فيديو من Pixabay مُضمن باستخدام عنصر iframe</h1>
<iframe src="https://cdn.pixabay.com/video/2022/07/24/125310-733046613_large.mp4" width="500" height="285"></iframe>
```

---

## استخدامات أخرى لعنصر $\text{iframe}$

لا يقتصر استخدام $\text{iframe}$ على تضمين مقاطع الفيديو فحسب، بل يمكنه أيضًا تضمين الخرائط أو صفحات الويب الأخرى أو حتى محتوى $\text{HTML}$ مباشر:

### مثال: تضمين خريطة من Openstreetmap

```html
<h1>خريطة من Openstreetmap.org مُضمنة باستخدام عنصر iframe</h1>
<iframe width="425" height="350" src="https://www.openstreetmap.org/export/embed.html?bbox=3.006134033203125%2C6.150112578753815%2C3.6357879638671875%2C6.749850810550778&amp;layer=mapnik" style="border: 1px solid black"></iframe>
<br /><small> <a href="https://www.openstreetmap.org/#map=11/6.4501/3.3210"> عرض الخريطة بحجم أكبر </a></small>
```

### تضمين محتوى $\text{HTML}$ مباشر

إذا كنت ترغب في تضمين محتوى $\text{HTML}$ مباشر داخل عنصر $\text{iframe}$، يجب عليك استخدام الخاصية **$\text{srcdoc}$** بدلاً من $\text{src}$.
