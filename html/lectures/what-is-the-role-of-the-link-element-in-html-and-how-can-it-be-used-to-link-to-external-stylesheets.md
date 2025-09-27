# ما هو دور عنصر `link` في HTML، وكيف يمكن استخدامه للربط بملفات الأنماط الخارجية (Stylesheets)؟

دعنا نتعلم عن عنصر `link`، وكيفية استخدامه للربط بملفات الأنماط الخارجية (External Stylesheets).

يُستخدم عنصر `link` للربط بمصادر خارجية (external resources) مثل ملفات الأنماط (stylesheets) وأيقونات الموقع (site icons). إليك البنية الأساسية لاستخدام عنصر link لملف CSS خارجي:

`<link rel="stylesheet" href="./styles.css" />`

يُستخدم الخاصية `rel` (اختصار لـ "relationship" أي "العلاقة") لتحديد العلاقة بين المصدر المرتبط ووثيقة HTML. في هذه الحالة، نحتاج إلى تحديد أن هذا المصدر المرتبط هو ملف أنماط (`stylesheet`).

## أفضل الممارسات وموقع عنصر `link`:

يُعتبر من أفضل الممارسات فصل HTML و CSS في ملفات مختلفة. يستخدم المطورون عنصر `link` لملف CSS الخارجي الخاص بهم بدلاً من كتابة كل شيء داخل وثيقة HTML.

تُستخدم الخاصية `href` لتحديد موقع (URL) المصدر الخارجي.

النقطة متبوعة بخط مائل في المثال (`./`) تخبر الحاسوب أن يبحث في المجلد الحالي، أو الدليل، عن ملف `styles.css`.

يجب وضع عنصر `link` داخل عنصر `head` كما هو موضح في المثال التالي:

```
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Examples of the link element</title>
  <link rel="stylesheet" href="./styles.css" />
</head>
```

## استخدامات متعددة لعنصر `link`:

### الخطوط والأيقونات

غالبًا ما سترى عناصر `link` متعددة داخل قاعدة أكواد احترافية تربط بملفات أنماط وخطوط وأيقونات مختلفة. إليك مثال لاستخدام عنصر `link` للربط بـ خط Google خارجي يُسمى "Playwright Cuba":

```
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Playwrite+CU:wght@100..400&display=swap"
  rel="stylesheet"
/>
```

خطوط Google هي مجموعة من الخطوط المخصصة المجانية ومفتوحة المصدر التي يمكنك استخدامها داخل أي مشروع. يمكنك اختيار الخطوط التي ترغب في استخدامها وسيوفر لك Google كود HTML و CSS الضروري.

في هذا المثال، تخبر القيمة `preconnect` لخاصية `rel` المتصفح بإنشاء اتصال مبكر بالقيمة المحددة في خاصية `href`. يتم ذلك لتسريع أوقات تحميل هذه المصادر الخارجية.

### ربط أيقونات الموقع (Favicon)

حالة استخدام شائعة أخرى لعنصر `link` هي للربط بـ الأيقونات. إليك مثال للربط بـ Favicon:

`<link rel="icon" href="favicon.ico" />`

ال Favicon، وهو اختصار لـ "favorite icon" (أيقونة المفضلة)، هو أيقونة صغيرة تُعرض عادةً في علامة تبويب المتصفح بجوار عنوان الموقع. تستخدم العديد من المواقع Favicon لعرض أيقونة علامتها التجارية.

