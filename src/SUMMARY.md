
# لغة البرمجة Rust

[لغة البرمجة Rust](title-page.md)
[تمهيد](foreword.md)
[مقدّمة](ch00-00-introduction.md)

## البداية مع البرنامج

- [البداية مع البرنامج](ch01-00-getting-started.md)
    - [تنصيب](ch01-01-installation.md)
    - [مرحبًا بالعالم !](ch01-02-hello-world.md)
    - [مرحبًا ب Cargo!](ch01-03-hello-cargo.md)

- [لعبة تخمين العدد](ch02-00-guessing-game-tutorial.md)

- [المفاهيم الشّائعة للبرمجة](ch03-00-common-programming-concepts.md)
    - [المتغيّرات والتّعديليّة](ch03-01-variables-and-mutability.md)
    - [أنواع البيانات](ch03-02-data-types.md)
    - [الدّوال](ch03-03-how-functions-work.md)
    - [التعليقات](ch03-04-comments.md)
    - [تدفّق التّحكم](ch03-05-control-flow.md)

- [الإلمام بالملكيّة](ch04-00-understanding-ownership.md)
    - [ما هي الملكيّة؟](ch04-01-what-is-ownership.md)
    - [المراجع والإقتراض](ch04-02-references-and-borrowing.md)
    - [الشّرائح](ch04-03-slices.md)

- [إستخدام الهياكل من أجل تنظيم البيانات ذات الصّلة](ch05-00-structs.md)
    - [تعريف وإنشاء الهياكل](ch05-01-defining-structs.md)
    - [مثال يستخدم الهياكل](ch05-02-example-structs.md)
    - [بُنية الطّرائق](ch05-03-method-syntax.md)

- [التّعدادات وفلترة الأنماط](ch06-00-enums.md)
    - [تعريف التّعداد](ch06-01-defining-an-enum.md)
    - [هيكل التّحكم 'match'](ch06-02-match.md)
    - [تدفّق تحكّم مختصر باستخدام 'if let'](ch06-03-if-let.md)

## اﻷساسيّات المعرفيّة لRust

- [إدارة المشاريع النّاميّة باستخدام الحِزَم والحاويات والوِحْدات](ch07-00-managing-growing-projects-with-packages-crates-and-modules.md)
    - [الحِزَم والحاويات](ch07-01-packages-and-crates.md)
    - [تعريف الوِحْدات عند التحكّم في النّطاق والخصوصيّة](ch07-02-defining-modules-to-control-scope-and-privacy.md)
    - [الإشارة إلى عنصر في شجرة الوِحْدات باستعمال المسارات](ch07-03-paths-for-referring-to-an-item-in-the-module-tree.md)
    - [جلب المسارات إلى النّطاق بفضل الكلمة المفتاحيّة use](ch07-04-bringing-paths-into-scope-with-the-use-keyword.md)
    - [تقسيم الوِحْدات إلى ملفّات](ch07-05-separating-modules-into-different-files.md)

- [المجموعات القياسيّة](ch08-00-common-collections.md)
    - [تخزين قوائم القيمات باستخدام المُتّجهات](ch08-01-vectors.md)
    - [تخزين النّصوص المشفّرة بتنسيق UTF-8 عن طريق السّلاسل النّصِّيّة String](ch08-02-strings.md)
    - [تخزين المفاتيح المرتبطة بقيمات في الخرائط الهاشيّة](ch08-03-hash-maps.md)

- [التّعامل مع الأخطاء](ch09-00-error-handling.md)
    - [الأخطاء الّتي لا تُدْرَك وpanic!](ch09-01-unrecoverable-errors-with-panic.md)
    - [الأخطاء الّتي تُدْرَك بِفضل Result](ch09-02-recoverable-errors-with-result.md)
    - [إستخدام panic! من عدمه](ch09-03-to-panic-or-not-to-panic.md)

- [الأنواع العامّة والسّمات ومدّة حياة القيمات](ch10-00-generics.md)
    - [الأنواع العامّة للبيانات](ch10-01-syntax.md)
    - [السّمات: تعريف السّلوك المشترك](ch10-02-traits.md)
    - [تحقيق صحّة المراجع باستخدام مدّة حياة القيمات](ch10-03-lifetime-syntax.md)

- [كتابة الاختبارات المؤتمتة](ch11-00-testing.md)
    - [ كيفيّة كتابة الاختبارات](ch11-01-writing-tests.md)
    - [التحكُّم في كيفيّة تشغيل الاختبارات](ch11-02-running-tests.md)
    - [تنظيم الاختبارات](ch11-03-test-organization.md)

- [مشروع إدخال وإخراج: بناء برنامج سطر أوامر](ch12-00-an-io-project.md)
    - [قبول المعاملات من سطر الأوامر](ch12-01-accepting-command-line-arguments.md)
    - [قراءة ملف](ch12-02-reading-a-file.md)
    - [إعادة الهيكلة لتحسين الوحدوية ومعالجة الأخطاء](ch12-03-improving-error-handling-and-modularity.md)
    - [تطوير وظائف المكتبة باستخدام التطوير القائم على الاختبارات](ch12-04-testing-the-librarys-functionality.md)
    - [العمل بالمتغيرات البيئية](ch12-05-working-with-environment-variables.md)
    - [توجيه رسائل الخطأ إلى المخرج القياسي للأخطاء بدلاً من المخرج القياسي](ch12-06-writing-to-stderr-instead-of-stdout.md)

##  التفكير على طريقة Rust

- [ميزات اللّغة الوظيفية: المُكرِّرات (Iterators) والإغلاقات (Closures)](ch13-00-functional-features.md)
    - [الإغلاقات: الدّوال المجهولة الّتي تتفاعل مع بيئتها](ch13-01-closures.md)
    - [معالجة سلسلة من العناصر باستخدام المُكرِّرات](ch13-02-iterators.md)
    - [تحسين مشروعنا عن الإدخال والإخراج](ch13-03-improving-our-io-project.md)
    - [مقارنة الأداء: الحَلْقات مقابل  المُكرِّرات](ch13-04-performance.md)

- [تعرّف أكثر على Cargo وCrates.io](ch14-00-more-about-cargo.md)
    - [تكيِيف البناء باستخدام هَيْئات الإعتاق](ch14-01-release-profiles.md)
    - [ نشر حاوية على Crates.io](ch14-02-publishing-to-crates-io.md)
    - [مساحات العمل في Cargo](ch14-03-cargo-workspaces.md)
    - [تنصيبت الملفّات التنفيذيّة من Crates.io باستخدام 'cargo install'](ch14-04-installing-binaries.md)
    - [توسيع Cargo باستخدام أوامر مُكيَّفة](ch14-05-extending-cargo.md)

- [المؤشِّرات الذّكية](ch15-00-smart-pointers.md)
    - [استخدام `Box<T>` للإشارة إلى البيانات الموجودة في الكومة (Heap)](ch15-01-box.md)
    - [إعتبار المؤشِّرات الذّكية مراجع اعتياديّة بفضل سمة `Deref`](ch15-02-deref.md)
    - [تنفيذ ترميز ما عند التّنظيف بفضل سمة `Drop`](ch15-03-drop.md)
    - [المؤشّر الذّكي الحاسِب لعدد المراجع `Rc<T>`](ch15-04-rc.md)
    - [النّمط التّعديلي الدّاخلي و`RefCell<T>`](ch15-05-interior-mutability.md)
    - [الحلْقات المرجعيّة الّتي قد تُسبّب تسريبًا للذاكرة](ch15-06-reference-cycles.md)

- [التّزامن من دون خوف](ch16-00-concurrency.md)
    - [استخدام الخيوط (Threads) لتشغيل التّرميزات تزامُنِيًّا](ch16-01-threads.md)
    - [بعث  الرّسائل كوسيلة لتمرير البيانات بين الخيوط](ch16-02-message-passing.md)
    - [إشتراك الحالة في وضعيّة التّزامن](ch16-03-shared-state.md)
    - [توسيع فكرة التّزامن بفضل استخدام السّمتين `Sync` و`Send`](ch16-04-extensible-concurrency-sync-and-send.md)

- [البرمجة غير المتزامنة باستخدام Async وAwait](ch17-00-async-await.md)
    - [المستقبلات (Futures) والبناء غير المتزامن (Async)](ch17-01-futures-and-syntax.md)
    - [التّزامن باستخدام Async](ch17-02-concurrency-with-async.md)
    - [التّعامل مع المستقبلات مهما كان عددها](ch17-03-more-futures.md)
    - [التدفّقات (Streams)](ch17-04-streams.md)
    - [التعمّق في السّمات الخاصّة بالبرمجة غير المتزامنة](ch17-05-traits-for-async.md)
    - [المستقبلات، المهام، والخيوط](ch17-06-futures-tasks-threads.md)

- [ميزات البرمجة الكائنيّة التّوجّه في Rust](ch18-00-oop.md)
    - [خصائص اللّغات الكائنية التّوجّه](ch18-01-what-is-oo.md)
    - [استخدام كائنات السّمات (Trait Objects) الّتي تسمح بقيمات من أنواع مختلفة](ch18-02-trait-objects.md)
    - [تنفيذ نمط تصميم كائني التّوجّه](ch18-03-oo-design-patterns.md)

## مواضيع متقدّمة

- [الأنماط والمطابقة](ch19-00-patterns.md)
    - [أين يُمكن استخدام الأنماط](ch19-01-all-the-places-for-patterns.md)
    - [الدّحوض : ماذا لو يفشل النّمط في المطابقة](ch19-02-refutability.md)
    - [بُنية الأنماط](ch19-03-pattern-syntax.md)

- [الميزات المتقدّمة](ch20-00-advanced-features.md)
    - [Rust غير الآمن](ch20-01-unsafe-rust.md)
    - [السّمات المتقدّمة](ch20-03-advanced-traits.md)
    - [الأنواع المتقدّمة](ch20-04-advanced-types.md)
    - [الدّوال والإغلاقات المتقدّمة](ch20-05-advanced-functions-and-closures.md)
    - [الماكرووات](ch20-06-macros.md)

- [مشروع نهائي: بناء خادم ويب متعدّد الخيوط](ch21-00-final-project-a-web-server.md)
    - [بناء خادم ويب أُحادي الخيط](ch21-01-single-threaded.md)
    - [تحويل خادمنا أُحادي الخيط إلى خادم متعدّد الخيوط](ch21-02-multithreaded.md)
    - [إيقاف التشغيل والتنظيف بسلاسة](ch21-03-graceful-shutdown-and-cleanup.md)

- [الملحق](appendix-00.md)
    - [أ - الكلمات المفتاحية](appendix-01-keywords.md)
    - [ب - العمليّات والرّموز](appendix-02-operators.md)
    - [ج - السمات القابلة للاشتقاق](appendix-03-derivable-traits.md)
    - [د - أدوات تطوير مفيدة](appendix-04-useful-development-tools.md)
    - [هـ - الإصدارات](appendix-05-editions.md)
    - [و - ترجمات الكتاب](appendix-06-translation.md)
	    - [ز - كيفية يُصنع Rust وإصدار "Nightly Rust"](appendix-07-nightly-rust.md)
