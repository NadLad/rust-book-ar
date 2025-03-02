# مقدمة

> ملاحظة: هذه النسخة من الكتاب هي نفسها [لغة البرمجة Rust][nsprust] المتوفرة بصيغة الكتاب المطبوع والكتاب الإلكتروني من [No Starch Press][nsp].

[nsprust]: https://nostarch.com/rust-programming-language-2nd-edition
[nsp]: https://nostarch.com/

مرحبًا بك في *لغة البرمجة Rust*، كتاب تمهيدي عن لغة Rust. تساعدك لغة البرمجة Rust في كتابة برمجيات أسرع وأكثر موثوقية. غالبًا ما تكون هناك تناقضات بين سهولة الاستخدام عالية المستوى والتحكم منخفض المستوى في تصميم لغات البرمجة؛ ولكن لغة Rust تتحدى هذا التناقض. من خلال تحقيق توازن بين القدرة التقنية القوية وتجربة المطور الرائعة، توفر لك Rust الخيار للتحكم في التفاصيل منخفضة المستوى (مثل استخدام الذاكرة) دون جميع المتاعب التي ترتبط تقليديًا بهذا النوع من التحكم.

## لمن لغة Rust

تعد Rust مثالية للكثير من الأشخاص لأسباب متنوعة. دعونا نلقي نظرة على بعض من أهم الفئات.

### فِرَق المطورين
تثبت Rust أنها أداة منتجة للتعاون بين فرق كبيرة من المطورين ذوي مستويات مختلفة من المعرفة في برمجة الأنظمة. الكود منخفض المستوى معرض لعدد من الأخطاء الدقيقة التي يمكن اكتشافها في معظم اللغات الأخرى فقط من خلال الاختبار المكثف والمراجعة الدقيقة للكود من قبل مطورين ذوي خبرة. في Rust، يلعب المترجم (compiler) دور الحارس من خلال رفض تجميع (compile) الكود الذي يحتوي على هذه الأخطاء، بما في ذلك أخطاء التزامن. من خلال العمل جنبًا إلى جنب مع المترجم، يمكن للفريق تخصيص وقتهم للتركيز على منطق البرنامج بدلاً من ملاحقة الأخطاء.

تقدم Rust أيضًا أدوات مطورين معاصرة لعالم برمجة الأنظمة:

- **Cargo**، مدير الحزم وأداة البناء المدمجة، يجعل إضافة وتجميع وإدارة الحزم سهلة ومتسقة عبر نظام Rust البيئي.
- أداة التنسيق **Rustfmt** تضمن أسلوب كتابة كود متسق عبر المطورين.
- **rust-analyzer** يدير تكامل بيئة تطوير متكاملة (IDE) لإكمال الكود وعرض رسائل الخطأ المضمنة.

باستخدام هذه الأدوات وغيرها في نظام Rust البيئي، يمكن للمطورين أن يكونوا منتجين أثناء كتابة كود الأنظمة.

### الطلاب
تعد Rust مناسبة للطلاب وكل من يهتم بتعلم مفاهيم الأنظمة. باستخدام Rust، تعلم العديد من الأشخاص مواضيع مثل تطوير أنظمة التشغيل. المجتمع مرحب للغاية ومستعد للإجابة على أسئلة الطلاب. من خلال جهود مثل هذا الكتاب، تهدف فرق Rust إلى جعل مفاهيم الأنظمة أكثر وصولًا للعديد من الأشخاص، وخاصة المبتدئين في البرمجة.

### الشركات
تستخدم مئات الشركات، الكبيرة والصغيرة، Rust في الإنتاج للعديد من المهام، بما في ذلك أدوات سطر الأوامر (CLI)، خدمات الويب، أدوات DevOps، الأجهزة المدمجة، تحليل الصوت والفيديو والتحويل، العملات المشفرة، المعلومات الحيوية، محركات البحث، تطبيقات الإنترنت للأشياء، التعلم الآلي، وحتى أجزاء كبيرة من متصفح Firefox.

### مطورو المصادر المفتوحة
Rust موجه للأشخاص الذين يرغبون في بناء لغة البرمجة Rust، المجتمع، أدوات المطورين، والمكتبات. نود أن نرحب بمساهماتكم في لغة Rust.

### الأشخاص الذين يقدرون السرعة والاستقرار
Rust موجه للأشخاص الذين يتوقون للسرعة والاستقرار في لغة البرمجة. بالسرعة، نعني كلاً من سرعة تشغيل كود Rust وسرعة الكتابة بها. تضمن فحوصات المترجم استقرار الكود من خلال إضافة الميزات وإعادة الهيكلة. هذا في مقابل الكود القديم الهش في اللغات التي تفتقر إلى هذه الفحوصات، والذي يخشى المطورون تعديله. من خلال السعي لتحقيق "التمثيلات بدون تكلفة" (zero-cost abstractions)، التي هي ميزات عالية المستوى يتم ترجمتها إلى كود منخفض المستوى بسرعة تساوي سرعة كتابة الكود يدويًا، تسعى Rust إلى جعل الكود الآمن سريعًا أيضًا.

تأمل لغة Rust في دعم العديد من المستخدمين الآخرين أيضًا؛ الأشخاص المذكورون هنا هم مجرد بعض من أصحاب المصلحة الرئيسيين. بشكل عام، أكبر طموح لـ Rust هو القضاء على التنازلات التي قابلها المبرمجون لعقود من الزمن من خلال توفير الأمان والإنتاجية، السرعة وسهولة الاستخدام. جرب Rust وانظر إذا كانت خياراتها تناسبك.

## من هو الجمهور المستهدف لهذا الكتاب

يفترض هذا الكتاب أنك قد كتبت كودًا بلغة برمجة أخرى، لكنه لا يفترض معرفة أي لغة بعينها. حاولنا أن نجعل المادة متاحة على نطاق واسع لأولئك من خلفيات برمجة متنوعة. نحن لا نخصص وقتًا طويلًا للحديث عن ماهية البرمجة *أو* كيفية التفكير فيها. إذا كنت جديدًا تمامًا على البرمجة، فسيكون من الأفضل لك قراءة كتاب يقدم مقدمة محددة للبرمجة.

## كيفية استخدام هذا الكتاب

بشكل عام، يفترض هذا الكتاب أنك تقرأه بالتسلسل من الأمام إلى الخلف. الفصول اللاحقة تبني على المفاهيم التي تم تناولها في الفصول السابقة، وقد لا تتناول الفصول الأولى التفاصيل المتعلقة بموضوع معين لكنها ستعود إليه في فصل لاحق.

ستجد نوعين من الفصول في هذا الكتاب: فصول المفاهيم وفصول المشاريع. في فصول المفاهيم، ستتعلم جانبًا من جوانب لغة Rust. في فصول المشاريع، سنبني برامج صغيرة معًا، نطبق ما تعلمته حتى الآن. الفصلان 2 و 12 و 20 هما فصول مشاريع؛ أما البقية فهي فصول مفاهيم.

الفصل 1 يشرح كيفية تثبيت Rust، وكيفية كتابة برنامج "مرحبًا، عالم!"، وكيفية استخدام Cargo، أداة إدارة الحزم وأداة البناء الخاصة بـ Rust. الفصل 2 هو مقدمة عملية لكتابة برنامج بلغة Rust، حيث ستبني لعبة تخمين الأرقام. هنا نتناول المفاهيم بشكل عام، وستقدم الفصول اللاحقة تفاصيل إضافية. إذا كنت ترغب في البدء مباشرة، فإن الفصل 2 هو المكان المناسب لذلك. الفصل 3 يغطي ميزات Rust التي تشبه ميزات لغات البرمجة الأخرى، وفي الفصل 4 ستتعلم عن نظام الملكية في Rust. إذا كنت من المتعلمين الدقيقين الذين يفضلون تعلم كل التفاصيل قبل الانتقال إلى التالي، قد ترغب في تخطي الفصل 2 والانتقال مباشرة إلى الفصل 3، ثم العودة إلى الفصل 2 عندما ترغب في العمل على مشروع يطبق التفاصيل التي تعلمتها.

الفصل 5 يناقش الهياكل (structs) والأساليب (methods)، والفصل 6 يغطي التعدادات (enums)، وتعابير `match`، وعبارة التحكم `if let`. ستستخدم الهياكل والتعدادات لإنشاء أنواع مخصصة في Rust.

في الفصل 7، ستتعلم عن نظام الوحدات (modules) في Rust وعن قواعد الخصوصية لتنظيم كودك وواجهة التطبيق البرمجية العامة (API). الفصل 8 يناقش بعض الهياكل الشائعة للبيانات التي يوفرها المكتبة القياسية، مثل المتجهات (vectors)، والسلاسل النصية (strings)، وخرائط التجزئة (hash maps). الفصل 9 يستعرض فلسفة Rust في التعامل مع الأخطاء وتقنياتها.

الفصل 10 يتناول الأنماط العامة (generics)، والخصائص (traits)، وفترات الحياة (lifetimes)، التي تمنحك القدرة على تعريف كود يعمل مع أنواع متعددة. الفصل 11 هو حول الاختبارات، التي تعتبر ضرورية لضمان صحة منطق البرنامج حتى مع ضمانات الأمان التي توفرها Rust. في الفصل 12، سنبني تطبيقًا خاصًا بنا لوظائف مختارة من أداة `grep` الخاصة بسطر الأوامر، التي تبحث عن نصوص داخل الملفات. لهذا، سنستخدم العديد من المفاهيم التي تم تناولها في الفصول السابقة.

الفصل 13 يستعرض الغلق (closures) والمكررات (iterators): ميزات في Rust تأتي من لغات البرمجة الوظيفية. في الفصل 14، سنفحص Cargo بشكل أعمق ونتحدث عن أفضل الممارسات لمشاركة مكتباتك مع الآخرين. الفصل 15 يناقش المؤشرات الذكية (smart pointers) التي توفرها المكتبة القياسية والخصائص التي تمكّن وظائفها.

في الفصل 16، سنستعرض نماذج البرمجة المتوازية المختلفة ونتحدث عن كيفية مساعدة Rust في البرمجة عبر الخيوط (threads) بكل أمان. في الفصل 17، سنبني على ذلك من خلال استكشاف تركيب Rust لـ async وawait والنموذج الخفيف للبرمجة المتوازية الذي يدعمه.

الفصل 18 ينظر في كيفية مقارنة آداب Rust بمبادئ البرمجة الكائنية (object-oriented programming) التي قد تكون مألوفًا بها.

الفصل 19 هو مرجع لأنماط البرمجة (patterns) والتطابق مع الأنماط (pattern matching)، وهي طرق قوية للتعبير عن الأفكار في برامج Rust. الفصل 20 يحتوي على مجموعة من المواضيع المتقدمة المثيرة للاهتمام، بما في ذلك Rust غير الآمن (unsafe Rust)، والمكررات (macros)، والمزيد عن فترات الحياة، والخصائص، والأنواع، والدوال، والغلقات.

في الفصل 21، سنكمل مشروعًا حيث سننفذ خادم ويب متعدد الخيوط منخفض المستوى!

أخيرًا، بعض الملاحق تحتوي على معلومات مفيدة عن اللغة بصيغة مرجعية. الملحق A يغطي الكلمات الرئيسية في Rust، الملحق B يغطي مشغلات Rust والرموز، الملحق C يغطي الخصائص القابلة للاشتقاق التي توفرها المكتبة القياسية، الملحق D يغطي بعض أدوات التطوير المفيدة، والملحق E يشرح إصدارات Rust. في الملحق F، يمكنك العثور على ترجمات للكتاب، وفي الملحق G سنغطي كيفية إنشاء Rust وما هو Rust الليلي.

لا يوجد طريقة خاطئة لقراءة هذا الكتاب: إذا أردت أن تقفز إلى الأمام، فافعل ذلك! قد تضطر للرجوع إلى الفصول السابقة إذا واجهت أي تشويش. لكن افعل ما يناسبك.

<span id="ferris"></span>

جزء مهم من عملية تعلم Rust هو تعلم كيفية قراءة رسائل الأخطاء التي يعرضها المترجم: هذه ستوجهك نحو كود يعمل بشكل صحيح. لهذا السبب، سنقدم العديد من الأمثلة التي لا يتم تجميعها مع رسالة الخطأ التي سيعرضها المترجم في كل حالة. اعلم أنه إذا أدخلت وشغلت مثالًا عشوائيًا، فقد لا يتم تجميعه! تأكد من قراءة النص المحيط لمعرفة ما إذا كان المثال الذي تحاول تشغيله مخصصًا لعرض خطأ.


| Ferris                                                                                                           | المعنى                                            |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain" alt="Ferris with a question mark"/>            | هذا الكود لا يتم تجميعه!                          |
| <img src="img/ferris/panics.svg" class="ferris-explain" alt="Ferris throwing up their hands"/>                   | هذا الكود يتسبب في حدوث خطأ (panic)!             |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain" alt="Ferris with one claw up, shrugging"/> | هذا الكود لا ينتج السلوك المرغوب فيه.             |

في معظم الحالات، سنوجهك إلى النسخة الصحيحة من أي كود لا يتم تجميعه.

## الشيفرة المصدرية

يمكنك العثور على ملفات الشيفرة المصدرية التي تم توليد هذا الكتاب منها على 
[GitHub][book].

[book]: https://github.com/rust-lang/book/tree/main/src
