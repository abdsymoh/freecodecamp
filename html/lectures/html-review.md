## مراجعة أساسيات HTML

**أساسيات HTML**

- **دور HTML:** تمثل HTML محتوى وبنية صفحة الويب.
- **عناصر HTML (HTML Elements):** العناصر هي اللبنات الأساسية لمستند HTML. وهي تمثل العناوين، الفقرات، الروابط، الصور، والمزيد. تتكون معظم عناصر HTML من وسم فتح (`<elementName>`) ووسم إغلاق (`</elementName>`).
  - **بنية الأساسية:**
    ```html
    <elementName>Content goes here</elementName>
    ```
- **العناصر الفارغة (Void Elements):** العناصر الفارغة لا يمكن أن تحتوي على أي محتوى ولها وسم بداية فقط. الأمثلة تشمل عنصري `img` و `meta`.
  ```html
  <img /><meta />
  ```
  - من الشائع رؤية بعض قواعد الأكواد التي تتضمن شرطة مائلة للأمام (/) داخل العنصر الفارغ. كلاهما مقبول:
  <!-- end list -->
  ```html
  <img /><img />
  ```
- **السمات (Attributes):** السمة هي قيمة توضع داخل وسم الفتح لعنصر HTML. توفر السمات معلومات إضافية حول العنصر أو تحدد كيف يجب أن يتصرف العنصر.
  - **البنية الأساسية للسمة:**
    ```html
    <element attribute="value"></element>
    ```
  - **السمة المنطقية (Boolean Attribute):** هي سمة يمكن أن تكون موجودة أو غائبة في وسم HTML. إذا كانت موجودة، تكون القيمة **صحيحة**، وإلا فهي **خاطئة**. تشمل أمثلة السمات المنطقية `disabled`، `readonly`، و `required`.
- **التعليقات (Comments):** تُستخدم التعليقات في البرمجة لترك ملاحظات لنفسك وللمطورين الآخرين في الكود الخاص بك.
  - **بنية التعليق في HTML:**
    ```html

    ```

---

**عناصر HTML الشائعة**

- **عناصر العناوين (Heading Elements):** يوجد ستة عناصر عناوين في HTML. تُستخدم عناصر العناوين `h1` حتى `h6` للدلالة على أهمية المحتوى الذي يليها. كلما كان الرقم أقل، زادت الأهمية، لذا فإن عناصر `h2` أقل أهمية من عناصر `h1`.
  ```html
  <h1>most important heading element</h1>
  <h2>second most important heading element</h2>
  <h3>third most important heading element</h3>
  <h4>fourth most important heading element</h4>
  <h5>fifth most important heading element</h5>
  <h6>least important heading element</h6>
  ```
- **عناصر الفقرة (Paragraph Elements):** تُستخدم للفقرات على صفحة الويب.
  ```html
  <p>This is a paragraph element.</p>
  ```
- **عناصر `img`:** يُستخدم عنصر `img` لإضافة الصور إلى صفحة الويب. تُستخدم السمة **`src`** لتحديد موقع تلك الصورة. من الممارسات الجيدة لعناصر الصور تضمين سمة أخرى تسمى السمة **`alt`**.
  - **مثال على عنصر `img` مع سمتي `src` و `alt`:**
    ```html
    <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice of lasagna on a plate." />
    ```
- **عنصر `body`:** يُستخدم لتمثيل المحتوى لمستند HTML.
  ```html
  <body>
    <h1>CatPhotoApp</h1>
    <p>This is a paragraph element.</p>
  </body>
  ```
- **عناصر `section`:** يُستخدم هذا العنصر لتقسيم المحتوى إلى أقسام أصغر.
  ```html
  <section>
    <h2>About Me</h2>
    <p>Hi, I am Jane Doe and I am a web developer.</p>
  </section>
  ```
- **عناصر `div`:** هذا العنصر هو عنصر HTML عام لا يحمل أي معنى دلالي. يُستخدم كحاوية عامة لاحتواء عناصر HTML أخرى.
  ```html
  <div>
    <h1>I am a heading</h1>
    <p>I am a paragraph</p>
  </div>
  ```
- **عناصر الربط (`a` - Anchor Elements):** تُستخدم هذه العناصر لتطبيق الروابط على صفحة الويب. تُستخدم السمة **`href`** لتحديد المكان الذي يجب أن ينتقل إليه الرابط عندما ينقر المستخدم عليه.
  ```html
  <a href="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg">cute cats</a>
  ```
- **عناصر القائمة غير المرتبة (`ul`) والقائمة المرتبة (`ol`):**
  - لإنشاء قائمة بعلامات (نقاط) يجب استخدام عنصر **`ul`** مع عنصر **`li`** واحد أو أكثر متداخلاً بداخله:
    ```html
    <ul>
      <li>catnip</li>
      <li>laser pointers</li>
      <li>lasagna</li>
    </ul>
    ```
  - لإنشاء قائمة مرتبة من العناصر، يجب استخدام عنصر **`ol`**:
    ```html
    <ol>
      <li>flea treatment</li>
      <li>thunder</li>
      <li>other cats</li>
    </ol>
    ```
- **عنصر التأكيد (`em` - Emphasis Element):** يُستخدم لوضع تأكيد على جزء من النص.
  ```html
  <p>Cats <em>love</em> lasagna.</p>
  ```
- **عنصر الأهمية القوية (`strong` - Strong Importance Element):** يُستخدم لوضع تأكيد قوي على النص للإشارة إلى شعور بالإلحاح والجدية.
  ```html
  <p><strong>Important:</strong> Before proceeding, make sure to wear your safety goggles.</p>
  ```
- **عنصرا `figure` و `figcaption`:** يُستخدم عنصر **`figure`** لتجميع محتوى مثل الصور والرسوم البيانية. يُستخدم عنصر **`figcaption`** لتمثيل تسمية توضيحية (caption) لذلك المحتوى داخل عنصر `figure`.
  ```html
  <figure>
    <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Two tabby kittens sleeping together on a couch." />
    <figcaption>Cats <strong>hate</strong> other cats.</figcaption>
  </figure>
  ```
- **عنصر `main`:** يُستخدم لتمثيل المحتوى الرئيسي لصفحة الويب.
- **عنصر `footer`:** يوضع هذا العنصر في أسفل مستند HTML وعادةً ما يحتوي على معلومات حقوق النشر وغيرها من روابط الصفحة المهمة.
  ```html
  <footer>
    <p>No Copyright - <a href="https://www.freecodecamp.org">freeCodeCamp.org</a></p>
  </footer>
  ```

---

**المعرفات والتجميع**

- **المعرفات (IDs):** معرفات عناصر فريدة لعناصر HTML. يجب استخدام أسماء ID مرة واحدة فقط في كل مستند HTML.
  ```html
  <h1 id="title">Movie Review Page</h1>
  ```
  - لا يمكن أن تحتوي أسماء ID على مسافات. إذا كان اسم الـ ID الخاص بك يحتوي على كلمات متعددة، يمكنك استخدام شرطات بين الكلمات:
    ```html
    <div id="red-box"></div>
    ```
- **الفئات (Classes):** تُستخدم الفئات لتجميع العناصر لأغراض التنسيق والسلوك.
  ```html
  <div class="box"></div>
  ```
  - بخلاف الـ ID، يمكنك إعادة استخدام اسم الفئة نفسه في جميع أنحاء مستند HTML. يمكن أن تحتوي قيمة الفئة أيضًا على مسافات:
    ```html
    <div class="box red-box"></div>
    <div class="box blue-box"></div>
    ```

---

**الأحرف الخاصة والربط**

- **كيانات HTML (HTML entities):** كيان HTML، أو مرجع حرفي (character reference)، هو مجموعة من الأحرف تُستخدم لتمثيل حرف محجوز في HTML. تتضمن الأمثلة رمز العطف (`&amp;`) ورمز "أصغر من" (`&lt;`).
  ```html
  <p>This is an &lt;img /&gt; element</p>
  ```
- **عنصر `link`:** يُستخدم هذا العنصر للربط بموارد خارجية مثل أوراق الأنماط وأيقونات الموقع.
  - **البنية الأساسية لاستخدام عنصر `link` لملف CSS خارجي:**
    ```html
    <link rel="stylesheet" href="./styles.css" />
    ```
  - تُستخدم السمة **`rel`** لتحديد العلاقة بين المورد المرتبط ومستند HTML. تُستخدم السمة **`href`** لتحديد موقع URL للمورد الخارجي.
- **عنصر `script`:** يُستخدم هذا العنصر لتضمين كود قابل للتنفيذ.
  ```html
  <body>
    <script>
      alert("Welcome to freeCodeCamp");
    </script>
  </body>
  ```
  - على الرغم من أنه يمكنك تقنيًا كتابة كل كود JavaScript الخاص بك داخل وسمي `script`، فمن الأفضل ربطه بملف JavaScript خارجي.
  - **مثال على استخدام عنصر `script` للربط بملف JavaScript خارجي:**
    ```html
    <script src="path-to-javascript-file.js"></script>
    ```
  - تُستخدم السمة **`src`** هنا لتحديد موقع ملف JavaScript الخارجي هذا.

---

**الهيكل الأساسي والترميز (Boilerplate and Encoding)**

- **هيكل HTML الأساسي (HTML boilerplate):** هو هيكل يتضمن البنية الأساسية والعناصر الأساسية التي يحتاجها كل مستند HTML.
  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="utf-8" />
      <title>freeCodeCamp</title>
      <link rel="stylesheet" href="./styles.css" />
    </head>
    <body></body>
  </html>
  ```
- **`DOCTYPE`:** يُستخدم لإخبار المتصفحات بإصدار HTML الذي تستخدمه.
- **عنصر `html`:** يمثل العنصر الأعلى مستوى أو جذر مستند HTML. لتحديد لغة المستند، يجب استخدام السمة **`lang`**.
- **عنصر `head`:** يحتوي قسم `head` على بيانات وصفية مهمة وهي معلومات خلف الكواليس تحتاجها المتصفحات ومحركات البحث.
- **عناصر `meta`:** تمثل هذه العناصر البيانات الوصفية لموقعك. تحتوي هذه العناصر على تفاصيل حول أشياء مثل ترميز الأحرف، وكيف يجب أن تعرض مواقع الويب مثل تويتر رابط صفحتك، والمزيد.
- **عنصر `title`:** يُستخدم لتعيين النص الذي يظهر في علامة تبويب أو نافذة المتصفح.
- **ترميز الأحرف UTF-8 (UTF-8 character encoding):** ترميز UTF-8، أو UCS Transformation Format 8، هو ترميز أحرف موحد يُستخدم على نطاق واسع على الويب. ترميز الأحرف هو الطريقة التي تستخدمها أجهزة الكمبيوتر لتخزين الأحرف كبيانات. تُستخدم السمة **`charset`** داخل عنصر `meta` لتعيين ترميز الأحرف إلى UTF-8.

---

**تحسين محركات البحث والمشاركة الاجتماعية (SEO and Social Sharing)**

- **تحسين محركات البحث (SEO - Search Engine Optimization):** هي ممارسة تعمل على تحسين صفحات الويب بحيث تصبح أكثر وضوحًا وتحتل مرتبة أعلى في محركات البحث.
- **عنصر `Meta` (description):** يُستخدم لتوفير وصف قصير لصفحة الويب ويؤثر على تحسين محركات البحث (SEO).
  ```html
  <meta name="description" content="Discover expert tips and techniques for gardening in small spaces, choosing the right plants, and maintaining a thriving garden." />
  ```
- **علامات Open Graph (Open Graph tags):** يتيح بروتوكول Open Graph إمكانية التحكم في كيفية ظهور محتوى موقع الويب الخاص بك عبر منصات التواصل الاجتماعي المختلفة، مثل فيسبوك ولينكدإن وغيرها الكثير.
  - يمكنك تعيين هذه الخصائص من خلال مجموعة من عناصر `meta` داخل قسم `head` في HTML.
  - **خاصية `og:title`:** تُستخدم لتعيين العنوان الذي يظهر لمنشورات وسائل التواصل الاجتماعي.
    ```html
    <meta content="freeCodeCamp.org" property="og:title" />
    ```
  - **خاصية `og:type`:** تُستخدم لتمثيل نوع المحتوى الذي تتم مشاركته على وسائل التواصل الاجتماعي. تشمل أمثلة هذا المحتوى المقالات، المواقع الإلكترونية، مقاطع الفيديو، أو الموسيقى.
    ```html
    <meta property="og:type" content="website" />
    ```
  - **خاصية `og:image`:** تُستخدم لتعيين الصورة المعروضة لمنشورات وسائل التواصل الاجتماعي.
    ```html
    <meta content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png" property="og:image" />
    ```
  - **خاصية `og:url`:** تُستخدم لتعيين عنوان URL الذي سينقر عليه المستخدمون لمنشورات وسائل التواصل الاجتماعي.
    ```html
    <meta property="og:url" content="https://www.freecodecamp.org" />
    ```

---

**عناصر الوسائط والتحسين (Media Elements and Optimization)**

- **العناصر المستبدلة (Replaced elements):** العنصر المستبدل هو عنصر يتم تحديد محتواه بواسطة مورد خارجي بدلاً من CSS نفسه. مثال على ذلك هو عنصر `iframe`. يرمز `iframe` إلى الإطار المضمن (inline frame). وهو عنصر مضمن يُستخدم لتضمين محتوى HTML آخر مباشرة داخل صفحة HTML.
  ```html
  <iframe src="https://www.example.com" title="Example Site"></iframe>
  ```
  - يمكنك تضمين السمة **`allowfullscreen`** التي تسمح للمستخدم بعرض الإطار المضمن بوضع ملء الشاشة.
    ```html
    <iframe src="video-url" width="width-value" height="height-value" allowfullscreen></iframe>
    ```
  - هناك بعض العناصر المستبدلة الأخرى، مثل `video` و `embed`. وبعض العناصر تتصرف كعناصر مستبدلة في ظل ظروف محددة. مثال على عنصر `input` مع تعيين السمة `type` إلى `image`:
    ```html
    <input type="image" alt="Descriptive text goes here" src="example-img-url" />
    ```
- **تحسين الوسائط (Optimizing media):** هناك ثلاثة أدوات يجب مراعاتها عند استخدام الوسائط، مثل الصور، على صفحات الويب الخاصة بك: **الحجم**، و**التنسيق**، و**الضغط**. تُستخدم خوارزمية الضغط لتقليل حجم الملفات أو البيانات.
- **تنسيقات الصور (Image formats):** اثنان من تنسيقات الملفات الأكثر شيوعًا هما PNG و JPG، لكن هذه لم تعد التنسيقات الأكثر مثالية لتقديم الصور. ما لم تكن بحاجة إلى دعم للمتصفحات القديمة، يجب أن تفكر في استخدام تنسيق أكثر تحسينًا، مثل WEBP أو AVIF.
- **تراخيص الصور (Image licenses):** الصورة التي تقع ضمن الملكية العامة (public domain) ليس لها حقوق نشر مرفقة بها وهي مجانية للاستخدام دون أي قيود. تعتبر الصور المرخصة تحديدًا بموجب ترخيص Creative Commons 0 ملكية عامة. قد يتم إصدار بعض الصور بموجب ترخيص متساهل، مثل ترخيص Creative Commons، أو ترخيص BSD الذي تستخدمه freeCodeCamp.
- **SVGs:** تتتبع رسومات المتجهات القابلة للتطوير (Scalable Vector Graphics) البيانات بناءً على المسارات والمعادلات لرسم النقاط والخطوط والمنحنيات. وهذا يعني أن الرسم المتجهي، مثل SVG، يمكن توسيعه إلى أي حجم دون التأثير على الجودة.

---

**تكامل الوسائط المتعددة (Multimedia Integration)**

- **عنصرا `audio` و `video`:** يسمح لك عنصرا `audio` و `video` بإضافة محتوى صوت وفيديو إلى مستندات HTML الخاصة بك.
  - يدعم عنصر `audio` تنسيقات الصوت الشائعة مثل mp3 و wav و ogg.
  - يدعم عنصر `video` تنسيقات mp4 و ogg و webm.
  - **مثال على عنصر `audio`:**
    ```html
    <audio src="CrystalizeThatInnerChild.mp3"></audio>
    ```
  - إذا كنت تريد رؤية مشغل الصوت على الصفحة، يمكنك إضافة عنصر `audio` مع السمة **`controls`**:
    ```html
    <audio src="CrystalizeThatInnerChild.mp3" controls></audio>
    ```
    - السمة **`controls`** هي سمة منطقية (boolean attribute) يمكن إضافتها إلى عنصر لتمكين عناصر تحكم التشغيل المضمنة. إذا تم حذفها، فلن تظهر أي عناصر تحكم.
  - **السمة `loop`:** هي سمة منطقية تجعل الصوت يعاد تشغيله باستمرار.
    ```html
    <audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3" loop controls></audio>
    ```
  - **السمة `muted`:** عند وجودها في عنصر `audio`، ستبدأ السمة المنطقية `muted` تشغيل الصوت في حالة كتم الصوت.
    ```html
    <audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3" loop controls muted></audio>
    ```
- **عنصر `source`:** نظرًا للاختلافات في دعم المتصفحات لأنواع ملفات الصوت المختلفة، يمكنك استخدام عناصر **`source`** داخل عنصر `audio` وسيقوم المتصفح باختيار أول مصدر يفهمه.
  - **مثال على استخدام عناصر `source` متعددة لعنصر `audio`:**
    ```html
    <audio controls>
      <source src="audio.ogg" type="audio/ogg" />
      <source src="audio.wav" type="audio/wav" />
      <source src="audio.mp3" type="audio/mpeg" />
    </audio>
    ```
  - يتم دعم جميع السمات التي تعلمناها حتى الآن أيضًا في عنصر `video`.
  - **مثال على استخدام عنصر `video` مع سمات `loop` و `controls` و `muted`:**
    ```html
    <video src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4" loop controls muted></video>
    ```
- **السمة `poster`:** إذا كنت ترغب في عرض صورة أثناء تنزيل الفيديو، يمكنك استخدام السمة **`poster`**. هذه السمة غير متاحة لعناصر `audio` وهي فريدة لعنصر `video`.
  ```html
  <video src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4" loop controls muted poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217" width="620"></video>
  ```

---

**أنواع سمة `target`**

- **السمة `target`:** تخبر هذه السمة المتصفح بمكان فتح عنوان URL لعنصر الربط (`a`). هناك أربع قيم محتملة مهمة لهذه السمة: **`_self`**، و **`_blank`**، و **`_parent`**، و **`_top`**.
  - **قيمة `_self`:** هي القيمة الافتراضية للسمة `target`. تفتح هذا الرابط في سياق التصفح الحالي. في معظم الحالات، ستكون علامة التبويب أو النافذة الحالية.
    ```html
    <a href="https://freecodecamp.org" target="_self">Visit freeCodeCamp</a>
    ```
  - **قيمة `_blank`:** تفتح هذا الرابط في سياق تصفح جديد. عادةً ما يفتح هذا في علامة تبويب جديدة.
    ```html
    <a href="https://freecodecamp.org" target="_blank">Visit freeCodeCamp</a>
    ```
  - **قيمة `_parent`:** تفتح هذا الرابط في أصل السياق الحالي. على سبيل المثال، إذا كان موقعك يحتوي على `iframe`، فإن قيمة `_parent` في ذلك الـ `iframe` ستفتح في علامة تبويب/نافذة موقعك، وليس في الإطار المضمن.
    ```html
    <a href="https://freecodecamp.org" target="_parent">Visit freeCodeCamp</a>
    ```
  - **قيمة `_top`:** تفتح هذا الرابط في أعلى سياق تصفح - فكر "أصل الأصل". هذا مشابه لـ `_parent`، ولكن سيتم فتح الرابط دائمًا في علامة تبويب/نافذة المتصفح الكاملة، حتى للإطارات المضمنة المتداخلة.
    ```html
    <a href="https://freecodecamp.org" target="_top">Visit freeCodeCamp</a>
    ```

---

**المسارات المطلقة مقابل المسارات النسبية**

- **تعريف المسار (Path definition):** المسار هو سلسلة تحدد موقع ملف أو دليل في نظام الملفات. في تطوير الويب، تسمح المسارات للمطورين بالربط بموارد مثل الصور، وأوراق الأنماط، والسكريبتات، وصفحات الويب الأخرى.
- **بنية المسار (Path Syntax):** هناك ثلاثة رموز أساسية يجب معرفتها:
  1.  **الشرطة المائلة (slash):** والتي يمكن أن تكون مائلة للخلف (`\`) أو مائلة للأمام (`/`) اعتمادًا على نظام التشغيل الخاص بك. تُعرف الشرطة المائلة بـ "فاصل المسار" (path separator).
  2.  **النقطة الواحدة (`.`):** تشير إلى الدليل الحالي.
  3.  **النقطتان (`..`):** تشيران إلى الدليل الأصل (parent directory).
  <!-- end list -->
  - **أمثلة:**
    ```
    public/index.html
    ./favicon.ico
    ../src/index.css
    ```
- **المسار المطلق (Absolute Path):** هو رابط كامل لمورد. يبدأ من الدليل الجذر (root directory)، ويشمل كل دليل آخر، وأخيرًا اسم الملف وامتداده. يشمل المسار المطلق أيضًا البروتوكول - الذي يمكن أن يكون `http`، `https`، و `file` واسم النطاق إذا كان المورد على الويب.
  - **مثال على مسار مطلق يربط بشعار freeCodeCamp:**
    ```html
    <a href="https://design-style-guide.freecodecamp.org/img/fcc_secondary_small.svg"> View fCC Logo</a>
    ```
- **المسار النسبي (Relative Path):** يحدد موقع ملف بالنسبة إلى دليل الملف الحالي. لا يشمل البروتوكول أو اسم النطاق، مما يجعله أقصر وأكثر مرونة للروابط الداخلية داخل نفس الموقع.
  - **مثال على الربط بصفحة `about.html` من صفحة `contact.html`، وكلاهما في نفس المجلد:**
    ```html
    <p>
      Read more on the
      <a href="about.html">About Page</a>
    </p>
    ```

---

**حالات الرابط (Link states)**

- **`:link`:** هذه هي الحالة الافتراضية. تمثل رابطًا لم يزره المستخدم أو ينقر عليه أو يتفاعل معه بعد.
- **`:visited`:** تنطبق هذه الحالة عندما يكون المستخدم قد زار الصفحة المرتبط بها بالفعل. افتراضيًا، يحول هذا الرابط إلى اللون البنفسجي.
- **`:hover`:** تنطبق هذه الحالة عندما يمرر المستخدم مؤشر الماوس فوق رابط.
- **`:focus`:** تنطبق هذه الحالة عندما نركز على رابط.
- **`:active`:** تنطبق هذه الحالة على الروابط التي يقوم المستخدم بتنشيطها. هذا يعني عادة النقر على الرابط بزر الماوس الأساسي.
