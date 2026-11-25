# دفتر البيت: Design System

> النسخة ٣. الألوان إنديجو، والهيكل ٥ تابات. الملف ده بيوصف اللي موجود في `index.html` بالظبط، وجداول الـ Tokens اتولدت من الكود نفسه.

---

## ١) المبادئ
- **كل لون ليه وظيفة واحدة:**
  - **الإنديجو** = الأكشن والاختيار، والهيدر.
  - **ألوان الأقسام الباستيل** = هوية الحاجة («دي تبع إيه»).
  - **الأحمر** = المسح والخطأ بس.
- **قاعدة ٦٠‑٣٠‑١٠:**
  - **٦٠٪** أبيض ورمادي فاتح جداً: الخلفية والكروت.
  - **٣٠٪** باستيل الأقسام: التايلز، وكروت القوايم، والتاجات.
  - **١٠٪** إنديجو: الهيدر، والأزرار، والحاجة المختارة.
- **أكبر مقاس خط 14px.** الأهمية بتبان بالوزن (800) والمسافات، مش بكبر الخط.
- **الكلام على أي لون باستيل بيبقى غامق**، مش أبيض.
- **التباين:** كل الأزواج عدّت WCAG AA. والأبيض على `indigo-500` تباينه 4.97.

## ٢) الألوان

### Primitives
| Scale | 50 | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900 |
|---|---|---|---|---|---|---|---|---|---|---|
| `neutral` المحايد: رمادي بارد لحد الكحلي الغامق | `#F7F7F9` | `#EEF0F6` | `#DEDFE5` | `#C9CAD0` | `#A9AAB0` | `#878991` | `#6A6B73` | `#505259` | `#36383E` | `#1C1C24` |
| `indigo` الأساسي: الأكشن، والاختيار، والهيدر | `#F5F5FE` | `#EFF0FC` | `#D9DBFB` | `#B4B6F5` | `#7476E7` | `#6260DC` | `#4C4DDB` | `#393BD3` | `#2D2BA0` | `#211E6B` |
| `red` الخطأ والمسح | `#FFF7F6` | `#FEEBE9` | `#FED4D0` | `#FEB5AF` | `#FF8A83` | `#F35B58` | `#D64545` | `#AE2D30` | `#8A1F22` | `#681215` |
| `lime` قسم التنظيف | `#F5F9EC` | `#E9F1D5` | `#CCDE92` | `#BBCF77` | `#9AB133` | `#7D9201` | `#647505` | `#4F5D04` | `#3B4602` | `#283001` |
| `butter` قسم شغل المطبخ، والطبخ | `#FAF7EA` | `#F5EDD1` | `#F5D86F` | `#DCC367` | `#C3A200` | `#9F8405` | `#806A05` | `#665400` | `#4D3E00` | `#352A00` |
| `periwinkle` قسم المشاوير والمشتريات | `#F3F7FE` | `#E4EDFF` | `#B7CAED` | `#A6C5FD` | `#7FA4EB` | `#5C84D2` | `#4569B2` | `#335391` | `#243D71` | `#152952` |
| `lavender` قسم التنظيم | `#F7F5FE` | `#EDEAFC` | `#DFD9FB` | `#C6BBF1` | `#A799DC` | `#8A78C2` | `#6F5FA3` | `#584A85` | `#423667` | `#2D234A` |
| `pink` قسم المناسبات | `#FFF3F9` | `#FFE4F3` | `#F5BCDD` | `#F9A6D8` | `#E47CBD` | `#C955A0` | `#A83B84` | `#892A6A` | `#691B51` | `#4C0D39` |
| `peach` الفواتير، وتاج «قرب ميعادها» | `#FFF5ED` | `#FFE8D6` | `#F8CBA6` | `#FAB375` | `#E68C31` | `#C26E05` | `#9D5803` | `#7D4503` | `#5F3302` | `#422201` |

### ألوان الأقسام
كل قسم بيحط الـ Scale بتاعه في `--cat-50 … --cat-900`، وأي component جوه `.cat-xxx` بياخد ألوان القسم لوحده.
- **`100`:** الخلفيات.
- **`700` و`800`:** الأيقونات والنص.

| القسم | الكلاس | الـ Scale |
|---|---|---|
| تنظيف | `.cat-clean` | `lime` |
| شغل المطبخ | `.cat-kitchen` | `butter` |
| مشاوير | `.cat-shop` | `periwinkle` |
| تنظيم | `.cat-organize` | `lavender` |
| مناسبات | `.cat-events` | `pink` |
| فواتير | `.cat-bills` | `peach` |

### فترات اليوم
| الفترة | الـ Scale |
|---|---|
| الصبح | `butter` |
| الضهر | `peach` |
| بالليل | `lavender` |

### حالة المخزن
| الحالة | الكلاس |
|---|---|
| خلص | `tag-urgent` (أحمر) |
| قرب يخلص | `tag-soon` (خوخي) |
| موجود | `tag-done` (أخضر) |

### Semantic
| Token | القيمة |
|---|---|
| `--bg` | `var(--white)` |
| `--stroke` | `var(--white)` |
| `--surface` | `var(--neutral-50)` |
| `--surface-2` | `var(--neutral-50)` |
| `--line` | `var(--neutral-200)` |
| `--ink` | `var(--neutral-900)` |
| `--muted` | `var(--neutral-700)` |
| `--brand` | `var(--indigo-600)` |
| `--accent` | `var(--indigo-500)` |
| `--danger` | `var(--red-600)` |

## ٣) الخط
- **الخط:** `-apple-system / SF Arabic` على الآيفون، و**Noto Sans Arabic** على أي جهاز تاني.
- **المقاسات:**
  - `--fs-title: 14px`: العناوين والأرقام المهمة.
  - `--fs-body: 13px`: الكلام العادي.
  - `--fs-meta: 12px`: السطر الصغير والتاجات.

## ٤) الحواف والمسافات
- **الحواف:**
  - `12px` للعناصر العادية (`--r-lg`).
  - `8px` للصغيرة (`--r-md`).
  - `4px` للتاجات (`--r-sm`).
- **الدواير** بتفضل دواير (`--r-pill`).
- **الاستثناءات:**
  - الـ nav bar كبسولة.
  - الهيدر `16px` تحت لما تسكرولي.
  - ورقة المحتوى `24px` فوق.
- **المسافة على الجناب:** `16px` في كل الشاشات.
- **جوه الهيدر:** كل المسافات `16px`.

## ٥) شكل الشاشة
1. **App bar ثابت:**
   - لونه `indigo-500`، والكلام والأيقونات بيضا.
   - **اليمين:** صورتك في الهوم، أو زرار رجوع في الصفحات الفرعية.
   - **النص:** العنوان. **الشمال:** أكشن الشاشة.
   - **في الهوم:** التحية بدل العنوان.
2. **الهيدر (`.hero`):** متدرج من `indigo-500` لـ `indigo-700`، وفيه الحاجات اللي بتعرّف الصفحة. الكارت المهم بيدخل نصه جوه الورقة البيضا (`.tuck`).
3. **ورقة المحتوى (`.screen`):** بيضا، وطالعة فوق الهيدر بـ `20px`.
4. **الـ nav bar:** كبسولة بيضا عايمة، والتاب المختار `indigo-50` والكلام `indigo-600`.
5. **Bottom sheet:**
   - كل الإضافة والتعديل والتفاصيل بتفتح فيه.
   - بيطلع من تحت **أول مرة بس**. أي تحديث جواه بيحصل مكانه من غير حركة، والسكرول بيفضل مكانه.
   - بيتقفل بالسحب لتحت، أو الدوس على الخلفية، أو ✕.

## ٦) هيكل التطبيق (Information Architecture)

| التاب | السؤال | جواه |
|---|---|---|
| **النهارده** | أعمل إيه النهارده؟ | شريط أيام بيتداس (والشهر في شيت)، والمهام بالفترات، وأكلة اليوم والناقص منها، والمواعيد الجاية، وزرار + للإضافة السريعة |
| **البيت** | إيه اللي على البيت؟ | أقسام الشغل (تنظيف، شغل المطبخ، تنظيم، مشاوير، مناسبات)، وبيانات البيت (الضمانات، والأرقام المهمة) |
| **المطبخ** | هطبخ إيه؟ | تابات فوق: أكل الأسبوع، وصفاتي، اتعلمي. الوصفة بتفتح صفحة، وبعدها وضع الطبخ |
| **المشتريات** | هشتري إيه؟ | قوايمي (كل قايمة ليها اسم ولون وبتتجدد إمتى)، والمخزن |
| **الفلوس** | صرفت كام؟ | الميزانية، والفواتير، وصرفتي على إيه، ومصاريف الشهر |

**الإعدادات:** من صورتك في الهوم. والجرس بيفتح الإشعارات.

### قواعد التنقل
- **مفيش حاجة أعمق من ٣ مستويات:** تاب ← صفحة ← شيت.
- **كل حاجة ليها بيت واحد**، و«النهارده» بيعرضها بس. مثلاً الفاتورة بيتها الفلوس، وبتظهر في النهارده كعرض.
- **الدوسة على أي حاجة بتفتح تفاصيلها.** التغيير (الحالة، أو التعديل) بيحصل من جوه.
- **المسح دايماً مقصود:**
  - يا وضع تعديل ✏️ فيه ⊖ أحمر.
  - يا زرار بيتأكد منك مرتين.
- **الدوسة على التاب وانتي جواه** بترجعك لأوله.

### روابط بين التابات
| من | لـ | اللي بيحصل |
|---|---|---|
| أكلة اليوم | الوصفة | بتفتح صفحتها |
| الناقص من الأكلة | القايمة الأساسية | بيتضاف ليها |
| أكل الأسبوع | القايمة الأساسية | بيبعت المكونات |
| المخزن («خلص» أو «قرب يخلص») | القايمة الأساسية | بيتضاف ليها |
| «دفعتها» في الفاتورة | الفلوس | بيتسجل مصروف |

## ٧) قوايم المشتريات
- **كل قايمة فيها:** اسم، ولون من ألوان الأقسام، وبتتجدد إمتى (كل أسبوع / كل شهر / لما أقول).
- **«بتتجدد»** = الحاجات بتفضل في القايمة، والعلامات بس بترجع فاضية أول الأسبوع أو الشهر.
- **القايمة الأساسية** (اللي بيروحلها الناقص من الأكل والمخزن): «قايمة الأسبوع»، ولو اتمسحت بتبقى أول قايمة.

## ٨) Component tokens

### Button
| Token | القيمة |
|---|---|
| `--btn-radius` | `var(--r-lg)` |
| `--btn-h-sm` | `32px` |
| `--btn-h-md` | `40px` |
| `--btn-h-lg` | `52px` |
| `--btn-px-sm` | `12px` |
| `--btn-px-md` | `18px` |
| `--btn-primary-bg` | `var(--indigo-600)` |
| `--btn-primary-bg-pressed` | `var(--indigo-700)` |
| `--btn-primary-fg` | `var(--white)` |
| `--btn-secondary-bg` | `var(--white)` |
| `--btn-secondary-border` | `var(--indigo-200)` |
| `--btn-secondary-fg` | `var(--indigo-600)` |
| `--btn-soft-bg` | `var(--white)` |
| `--btn-soft-fg` | `var(--indigo-600)` |
| `--btn-text-fg` | `var(--indigo-600)` |
| `--btn-danger-fg` | `var(--red-600)` |
| `--btn-danger-confirm-bg` | `var(--red-50)` |
| `--btn-danger-confirm-fg` | `var(--red-700)` |
| `--btn-disabled-opacity` | `.4` |

### Icon button
| Token | القيمة |
|---|---|
| `--icon-btn-size` | `40px` |
| `--icon-btn-size-sm` | `32px` |
| `--icon-btn-on-brand-bg` | `var(--lavender-700)` |
| `--icon-btn-on-brand-fg` | `var(--lavender-50)` |
| `--icon-btn-surface-bg` | `var(--white)` |
| `--icon-btn-surface-fg` | `var(--neutral-800)` |
| `--icon-btn-surface-shadow` | `var(--elev-1)` |
| `--icon-btn-accent-bg` | `var(--indigo-50)` |
| `--icon-btn-accent-fg` | `var(--indigo-600)` |
| `--icon-btn-primary-bg` | `var(--indigo-600)` |
| `--icon-btn-primary-fg` | `var(--white)` |
| `--badge-dot` | `var(--peach-400)` |

### Check (زرار الإنجاز)
| Token | القيمة |
|---|---|
| `--check-size` | `20px` |
| `--check-border` | `var(--neutral-300)` |
| `--check-done-bg` | `var(--indigo-600)` |

### Chip

**States (الـ Chip مش زرار):**

| State | الشكل |
|---|---|
| Default | خلفية رمادي فاتح جداً + إطار رفيع، على قد الكلام |
| Selected | خلفية إنديجو فاتحة + إطار إنديجو + ✓ قبل الكلام (أو أيقونة القسم لو موجودة) |
| Disabled | من غير خلفية + إطار متقطع + كلام رمادي. لو كانت مختارة: نفس الـ Selected بشفافية ٥٠٪ |

**الفرق عن الـ Button:** الزرار بيعمل أكشن (احفظي، امسحي)، ارتفاعه 44–52px، وزنه 700–800، والـ primary لونه مليان. الـ Chip بيختار قيمة، ارتفاعه 32px، على قد الكلام وبينزل سطر جديد، والـ selected عمره ما بيبقى لون مليان.
استثناء: الأيام والدقايق (`.chip-grid.is-even`) كلها نفس العرض ومن غير ✓.

| Token | القيمة |
|---|---|
| `--chip-h` | `32px` |
| `--chip-px` | `12px` |
| `--chip-radius` | `var(--r-md)` |
| `--chip-gap` | `8px` |
| `--chip-weight` | `600` |
| `--chip-bg` | `var(--neutral-50)` |
| `--chip-fg` | `var(--neutral-700)` |
| `--chip-border` | `var(--neutral-200)` |
| `--chip-bg-pressed` | `var(--neutral-100)` |
| `--chip-bg-selected` | `var(--indigo-50)` |
| `--chip-fg-selected` | `var(--indigo-700)` |
| `--chip-border-selected` | `var(--indigo-300)` |
| `--chip-bg-disabled` | `transparent` |
| `--chip-fg-disabled` | `var(--neutral-400)` |
| `--chip-border-disabled` | `var(--neutral-300)` (dashed) |
| `--chip-disabled-selected-opacity` | `.5` |
| `--chip-count-fg` | `var(--neutral-500)` |
| `--chip-count-fg-selected` | `var(--indigo-500)` |
| `--chip-icon-bg` | `transparent` |
| `--chip-icon-fg` | `var(--cat-700, var(--neutral-800))` |

### Segmented
| Token | القيمة |
|---|---|
| `--seg-bg` | `var(--neutral-100)` |
| `--seg-fg` | `var(--neutral-700)` |
| `--seg-bg-selected` | `var(--white)` |
| `--seg-fg-selected` | `var(--indigo-600)` |

### Tag
| Token | القيمة |
|---|---|
| `--tag-h` | `22px` |
| `--tag-bg` | `var(--neutral-100)` |
| `--tag-fg` | `var(--neutral-700)` |
| `--tag-accent-bg` | `var(--indigo-50)` |
| `--tag-accent-fg` | `var(--indigo-700)` |
| `--tag-brand-bg` | `var(--indigo-100)` |
| `--tag-brand-fg` | `var(--indigo-700)` |

### الإلحاح: كل ما الميعاد يقرب اللون يسخن
| Token | القيمة |
|---|---|
| `--tag-urgent-bg` | `var(--red-100)` |
| `--tag-urgent-fg` | `var(--red-700)` |
| `--tag-soon-bg` | `var(--peach-100)` |
| `--tag-soon-fg` | `var(--peach-700)` |
| `--tag-later-bg` | `var(--lavender-50)` |
| `--tag-later-fg` | `var(--lavender-700)` |
| `--tag-done-bg` | `var(--lime-100)` |
| `--tag-done-fg` | `var(--lime-800)` |

### List item (صف المهمة)
| Token | القيمة |
|---|---|
| `--li-radius` | `var(--r-lg)` |
| `--li-min-h` | `58px` |
| `--li-bg` | `var(--surface)` |
| `--li-border` | `var(--stroke)` |
| `--li-shadow` | `none` |
| `--li-title-fg` | `var(--neutral-900)` |
| `--li-meta-fg` | `var(--cat-700, var(--neutral-700))` |
| `--li-icon-bg` | `transparent` |
| `--li-icon-fg` | `var(--cat-700, var(--neutral-800))` |
| `--li-done-bg` | `var(--white)` |
| `--li-done-fg` | `var(--neutral-600)` |
| `--li-done-opacity` | `.6` |

### Tile (كارت القسم)
| Token | القيمة |
|---|---|
| `--tile-radius` | `var(--r-lg)` |
| `--tile-cols` | `3` |
| `--tile-min-h` | `104px` |
| `--tile-ill-size` | `46px` |
| `--tile-count-size` | `24px` |
| `--tile-bg` | `var(--cat-100)` |
| `--tile-title-fg` | `var(--cat-900)` |
| `--tile-sub-fg` | `var(--cat-800)` |
| `--tile-count-bg` | `var(--white)` |
| `--tile-count-fg` | `var(--cat-800)` |
| `--tile-border` | `var(--cat-200)` |
| `--tile-border-selected` | `var(--neutral-900)` |

### Card (كروت «قريب»)
| Token | القيمة |
|---|---|
| `--card-radius` | `var(--r-lg)` |
| `--card-bg` | `var(--surface)` |
| `--card-border` | `var(--stroke)` |
| `--card-shadow` | `none` |
| `--card-title-fg` | `var(--ink)` |
| `--card-icon-bg` | `transparent` |
| `--card-icon-fg` | `var(--cat-700, var(--neutral-800))` |

### Hero، والهيدر، والتقويم، والفلوس، والطبخ، والإعدادات
| Token | القيمة |
|---|---|
| `--hero-bg` | `linear-gradient(180deg, var(--indigo-500) 0%, var(--indigo-700) 100%)` |
| `--hero-fg` | `var(--white)` |
| `--hero-fg-2` | `color-mix(in srgb, var(--white) 82%, transparent)` |
| `--hero-radius` | `0px` |
| `--hero-avatar-bg` | `var(--white)` |
| `--hero-avatar-fg` | `var(--indigo-600)` |
| `--today-card-bg` | `var(--indigo-50)` |
| `--today-card-fg` | `var(--neutral-900)` |
| `--today-card-fg-2` | `var(--neutral-600)` |
| `--week-day-bg` | `color-mix(in srgb, var(--white) 14%, transparent)` |
| `--week-day-fg` | `color-mix(in srgb, var(--white) 78%, transparent)` |
| `--week-day-num` | `var(--white)` |
| `--week-day-shadow` | `none` |
| `--week-today-bg` | `var(--white)` |
| `--week-today-fg` | `var(--indigo-600)` |
| `--cal-day-fg` | `var(--ink)` |
| `--cal-day-muted` | `var(--neutral-400)` |
| `--cal-head-fg` | `var(--muted)` |
| `--cal-selected-bg` | `var(--indigo-600)` |
| `--cal-selected-fg` | `var(--white)` |
| `--cal-today-ring` | `var(--indigo-300)` |
| `--cal-dot-size` | `5px` |
| `--cal-cell-h` | `44px` |
| `--info-label-fg` | `var(--muted)` |
| `--info-value-fg` | `var(--ink)` |
| `--info-divider` | `var(--stroke)` |
| `--bar-h` | `8px` |
| `--bar-track` | `var(--neutral-100)` |
| `--bar-fill` | `var(--cat-400, var(--lavender-500))` |
| `--budget-bg` | `var(--indigo-50)` |
| `--budget-fg` | `var(--neutral-900)` |
| `--budget-track` | `var(--indigo-100)` |
| `--budget-fill` | `var(--indigo-600)` |
| `--appbar-h` | `56px` |
| `--appbar-pad-top` | `8px` |
| `--appbar-pad-bottom` | `8px` |
| `--appbar-fg` | `var(--white)` |
| `--appbar-fg-2` | `color-mix(in srgb, var(--white) 80%, transparent)` |
| `--appbar-radius` | `16px` |
| `--sheet-top-radius` | `24px` |
| `--sheet-overlap` | `20px` |
| `--surface-shadow` | `none` |
| `--appbar-bg` | `var(--indigo-500)` |
| `--appbar-border` | `transparent` |
| `--switch-w` | `46px` |
| `--switch-h` | `28px` |
| `--switch-off` | `var(--neutral-300)` |
| `--switch-on` | `var(--indigo-600)` |
| `--switch-knob` | `var(--white)` |
| `--tile-add-border` | `var(--indigo-200)` |
| `--tile-add-fg` | `var(--indigo-600)` |
| `--cook-bg` | `var(--neutral-50)` |
| `--timer-track` | `var(--butter-100)` |
| `--timer-fill` | `var(--butter-400)` |
| `--step-num-bg` | `var(--cat-100, var(--lavender-100))` |
| `--step-num-fg` | `var(--cat-800, var(--lavender-800))` |
| `--tip-bg` | `var(--butter-50)` |
| `--tip-border` | `var(--butter-200)` |
| `--ring-track` | `var(--indigo-200)` |
| `--ring-fill` | `var(--indigo-600)` |
| `--next-bg` | `var(--white)` |
| `--next-shadow` | `var(--elev-1)` |

### Timeline (خط اليوم)
| Token | القيمة |
|---|---|
| `--timeline-line` | `var(--neutral-300)` |
| `--node-past` | `var(--neutral-700)` |
| `--node-now` | `var(--pink-400)` |
| `--node-now-halo` | `var(--pink-100)` |
| `--node-future` | `var(--neutral-300)` |
| `--period-tag-bg` | `var(--neutral-100)` |
| `--period-tag-fg` | `var(--neutral-700)` |
| `--period-ico` | `var(--neutral-700)` |

### Nav bar
| Token | القيمة |
|---|---|
| `--nav-h` | `64px` |
| `--nav-radius` | `var(--r-pill)` |
| `--nav-bg` | `var(--white)` |
| `--nav-item-fg` | `var(--neutral-400)` |
| `--nav-item-active-bg` | `var(--indigo-50)` |
| `--nav-item-active-fg` | `var(--indigo-600)` |
| `--nav-shadow` | `0 8px 30px color-mix(in srgb, var(--indigo-900) 16%, transparent), 0 1px 3px color-mix(in srgb, var(--indigo-900) 8%, transparent)` |

### Input
| Token | القيمة |
|---|---|
| `--input-h` | `48px` |
| `--input-radius` | `var(--r-lg)` |
| `--input-bg` | `var(--white)` |
| `--input-fg` | `var(--ink)` |
| `--input-placeholder` | `var(--neutral-400)` |
| `--input-border` | `var(--neutral-200)` |
| `--input-border-focus` | `var(--indigo-500)` |
| `--input-border-error` | `var(--red-500)` |
| `--label-fg` | `var(--neutral-700)` |
| `--error-fg` | `var(--red-600)` |

### Sheet
| Token | القيمة |
|---|---|
| `--sheet-bg` | `var(--white)` |
| `--sheet-radius` | `var(--r-xl)` |
| `--sheet-handle` | `var(--neutral-300)` |
| `--backdrop` | `color-mix(in srgb, var(--neutral-900) 40%, transparent)` |

### Toast
| Token | القيمة |
|---|---|
| `--toast-bg` | `var(--neutral-900)` |
| `--toast-fg` | `var(--white)` |

### Illustration
| Token | القيمة |
|---|---|
| `--ill-line` | `var(--neutral-900)` |

