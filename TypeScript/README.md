# TypeScript

مشروع عن TypeScript: الأنواع الأساسية، الواجهات والكلاسات، التعامل مع DOM،
الأنواع المتقدمة، الـ namespaces، الملفات المحيطة (ambient)، والـ nominal typing.

## المفاهيم

| المفهوم | الشرح |
| --- | --- |
| `interface` | وصف شكل الكائن: أي خصائص فيه وأنواعها |
| `readonly` | خاصية تُحدَّد وقت الإنشاء فقط ولا يمكن تغييرها بعدها |
| `?` | خاصية اختيارية قد تكون موجودة أو لا |
| `[key: string]: any` | index signature — يسمح بإضافة أي خاصية إضافية |
| `extends` | واجهة ترث خصائص واجهة أخرى |
| نوع الدالة | واجهة تصف توقيع الدالة نفسها (المعاملات والمُرجَع) |
| `implements` | كلاس يلتزم بتنفيذ ما تطلبه الواجهة |
| Union `A \| B` | قيمة قد تكون من نوعين |
| Type predicate | `x is Director` — تخبر TypeScript بالنوع بعد الفحص |
| String literal type | `'Math' \| 'History'` — قيم نصية محددة فقط |
| Ambient file `.d.ts` | تعريف أنواع لمكتبة JavaScript ما فيها أنواع |
| `/// <reference />` | توجيه ثلاثي الشرطات لربط ملف تعريفات |
| `namespace` | تجميع الأنواع والكلاسات تحت اسم واحد |
| Declaration merging | توسيع نفس الواجهة من أكثر من ملف |
| Brand / Nominal typing | إضافة خاصية مميزة تمنع الخلط بين نوعين متشابهين |

## المهام

| المجلد | المحتوى |
| --- | --- |
| `task_0` | واجهة `Student` + بناء جدول بـ Vanilla JS |
| `task_1` | `Teacher` و `Directors` و `printTeacher` و `StudentClass` |
| `task_2` | أنواع متقدمة: `Director` / `Teacher` / `createEmployee` / `isDirector` / `executeWork` / `Subjects` / `teachClass` |
| `task_3` | Ambient namespaces: `interface.ts` و `crud.js` و `crud.d.ts` |
| `task_4` | Namespaces و declaration merging: `Cpp` و `Java` و `React` |
| `task_5` | Brand convention و nominal typing: `MajorCredits` و `MinorCredits` |

## التشغيل

```bash
cd task_0        # أو أي مجلد آخر
npm install
npm run build    # يجب أن يظهر: No type errors found
npm run start-dev
```

`task_4` يُبنى بـ `tsc` مباشرة (namespaces مع `outFile`) وليس بـ webpack.
