# أدوار عناصر HTML للصوت والفيديو وكيف تعمل

تسمح لك عنصرا **`audio`** و **`video`** بإضافة محتوى صوتي ومرئي إلى مستندات HTML الخاصة بك.

### عنصر `audio` (الصوت)

يدعم عنصر **`audio`** تنسيقات صوتية شائعة مثل **mp3** و **wav** و **ogg**.

لإدراج محتوى صوتي في صفحة الويب الخاصة بك، يمكنك استخدام عنصر **`audio`** مع الخاصية **`src`** التي تشير إلى موقع ملف الصوت الخاص بك:

```html
<audio src="CrystalizeThatInnerChild.mp3"></audio>
```

إذا حاولت تشغيل هذا المثال، فلن يظهر أي شيء على الصفحة. ومع ذلك، إذا قمت بفحص الصفحة باستخدام أدوات المطور، فسترى أن عنصر **`audio`** موجود بالفعل على الصفحة.

إذا كنت تريد رؤية مشغل الصوت على الصفحة، فيمكنك إضافة عنصر **`audio`** مع الخاصية **`controls`**:

```html
<audio src="CrystalizeThatInnerChild.mp3" controls></audio>
```

---

#### خاصيات عنصر `audio`

- **`controls`**: هي خاصية منطقية (boolean attribute) تُمكّن المستخدمين من إدارة تشغيل الصوت، بما في ذلك ضبط مستوى الصوت، والإيقاف المؤقت، أو استئناف التشغيل. إذا تم حذفها، فلن تظهر أي عناصر تحكم.

- **`loop`**: هي خاصية منطقية تجعل الصوت يُعاد تشغيله باستمرار.

  مثال على استخدام **`loop`** لتشغيل أغنية "Can't stay down" لكوينسي لارسون:

  ```html
  <audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3" loop controls></audio>
  ```

  عندما تصل الأغنية إلى نهايتها، ستتكرر وتُشغل مرة أخرى من البداية.

- **`muted`**: هي خاصية منطقية تجعل الصوت يبدأ في حالة صامتة (كتم الصوت) عند وجودها في عنصر **`audio`**.

  مثال على استخدام **`muted`**:

  ```html
  <audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3" loop controls muted></audio>
  ```

  عند بدء تشغيل الأغنية في المتصفح، لن تسمع شيئًا. لسماع الموسيقى، ستحتاج إلى النقر على أيقونة مستوى الصوت.

---

#### دعم تنسيقات الملفات المتعددة

هناك اختلافات في دعم المتصفحات لأنواع ملفات صوتية مختلفة. لاستيعاب ذلك، يمكنك استخدام عناصر **`<source>`** داخل عنصر **`<audio>`** وسيحدد المتصفح أول مصدر يفهمه.

مثال على استخدام عناصر **`<source>`** متعددة لعنصر صوتي:

```html
<audio controls>
  <source src="audio.ogg" type="audio/ogg" />
  <source src="audio.wav" type="audio/wav" />
  <source src="audio.mp3" type="audio/mpeg" />
</audio>
```

سيبدأ المتصفح أولاً بنوع **ogg**، وإذا لم يتمكن من تشغيل الصوت، فسينتقل إلى النوع التالي في القائمة.

---

### عنصر `video` (الفيديو)

جميع الخاصيات التي تعلمناها حتى الآن (مثل **`src`**، **`controls`**، **`loop`**، و **`muted`**) مدعومة أيضًا في عنصر **`video`**.

يدعم عنصر **`video`** تنسيقات **mp4**، **ogg**، و **webm**.

إليك مثال على استخدام عنصر **`video`** مع الخاصيات **`loop`** و **`controls`** و **`muted`**:

```html
<video src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4" loop controls muted></video>
```

---

#### خاصيات عنصر `video` الفريدة

- **`poster`**: هذه الخاصية غير متاحة لعناصر **`audio`** وهي فريدة لعنصر **`video`**. تسمح لك بعرض صورة أثناء تنزيل الفيديو.

  مثال على استخدام الخاصية **`poster`** مع محتوى مقدم من peach.blender.org:

  ```html
  <video src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4" loop controls muted poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217" width="620"></video>
  ```

  يستخدم هذا المثال أيضًا الخاصية **`width`** لتعيين العرض إلى 620 بكسل حتى يتناسب الفيديو بشكل أفضل مع الشاشة.
