<style>



/* ══════════════════════════════════════════
   1. استدعاء الخطوط المحلية (من فولدر Fonts)
   ══════════════════════════════════════════ */

@font-face {
    font-family: 'Cairo';
    src: url('Fonts/Cairo-Regular.ttf') format('truetype');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-family: 'Cairo';
    src: url('Fonts/Cairo-Bold.ttf') format('truetype');
    font-style: normal;
}

/* لو عندك خطوط للأكواد زي Fira Code ضيفها هنا بنفس الطريقة */

:root {
    --sans: 'Cairo', sans-serif;
    --mono: 'Consolas', 'Monaco', monospace; /* أو استبدله بـ Fira Code لو موجود */
}

/* ══════════════════════════════════════════
   2. تحسينات الأكواد والتعليقات والطباعة
   ══════════════════════════════════════════ */
/* ── ألوان السينتاكس الاحترافية ── */
.hljs-keyword, .kw { color: #bb9af7 !important; font-weight: bold; } /* بنفسجي فاتح */
.hljs-string, .st { color: #9ece6a !important; }                    /* أخضر هادي */
.hljs-type, .cls { color: #7aa2f7 !important; }                     /* أزرق احترافي */
.hljs-title.function_, .fn { color: #7dcfff !important; }           /* لبني صريح */
.hljs-params { color: #e0af68 !important; }                         /* برتقالي مطفي */
.hljs-number, .num { color: #ff9e64 !important; }                   /* برتقالي غامق */
.hljs-comment, .com { color: #565f89 !important; font-style: italic !important; } /* أزرق رمادي للتعليقات */

/* تلوين التعليقات باللون الأخضر */
.hljs-comment, .com, .comment {
    color: #2db45d !important; /* أخضر واضح */
    font-style: italic !important;
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;
}

/* ضمان ظهور الألوان في الـ PDF (مهم لـ Playwright) */
pre, code, div, span, lesson, card, pill,hl {
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;
}

/* خلفية الأكواد */
/* ── حاوية الكود الاحترافية (The Pre Container) ── */
pre {
    background: #1a1b26 !important; /* لون ليلي هادي ومريح للعين */
    border: 1px solid #292e42;
    border-left: 4px solid var(--teal);
    border-radius: 12px;
    padding: 1.5rem;
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
    position: relative;
    overflow: hidden;
    direction: ltr; /* الكود دايمًا من الشمال لليمين */
    text-align: left;
    margin: 1.2rem 0;
}

/* ── ألوان السينتاكس الاحترافية (Tokyo Night Palette) ── */
.hljs-keyword, .kw { color: #bb9af7 !important; font-weight: bold; } /* الكلمات المحجوزة */
.hljs-string, .st { color: #9ece6a !important; }                    /* النصوص */
.hljs-type, .cls { color: #7aa2f7 !important; font-weight: 700; }    /* أنواع البيانات */
.hljs-title.function_, .fn { color: #7dcfff !important; }           /* الدوال */
.hljs-params { color: #e0af68 !important; }                         /* الباراميترات */
.hljs-number, .num { color: #ff9e64 !important; }                   /* الأرقام */
.hljs-comment, .com { color: #565f89 !important; font-style: italic !important; } /* التعليقات */
.hljs-operator, .op { color: #89ddff !important; }                  /* المعاملات = + - */

/* ── الكود اللي جوه الكلام (Inline Code) ── */
code {
    font-family: var(--mono);
    font-size: 0.9em;
    background: rgba(122, 162, 247, 0.1);
    color: #7aa2f7;
    padding: 2px 6px;
    border-radius: 4px;
    border: 1px solid rgba(122, 162, 247, 0.2);
}

/* ── تخصيص الكود اللي جوه pre عشان مياخدش ستايل الـ inline ── */
pre code {
    background: transparent !important;
    border: none !important;
    padding: 0 !important;
    color: #c0caf5 !important; /* لون النص العادي جوه الكود */
    display: block;
    line-height: 1.6;
}

/* ── علامة الـ C++ اللي في الجنب ── */
pre::after {
    content: 'C++';
    position: absolute;
    top: 0;
    right: 0;
    background: #292e42;
    color: #565f89;
    font-size: 0.65rem;
    padding: 3px 10px;
    border-bottom-left-radius: 8px;
    font-family: var(--mono);
    font-weight: bold;
}

/* ══════════════════════════════════════════
   3. بقية التنسيقات (تعديلات بسيطة للأداء)
   ══════════════════════════════════════════ */

body {
    font-family: var(--sans);
    line-height: 1.6;
    background-color: #fdfdfd;
}

/* أي تعديلات تانية في الـ CSS بتاعك ضيفها تحت هنا */

:root {
  --bg:         #0d0f14;
  --bg2:        #13161f;
  --bg3:        #1a1e2e;
  --border:     #252a3a;
  --text:       #d4d8e8;
  --muted:      #6b7394;
  --teal:       #3dd6c8;
  --amber:      #f0a050;
  --rose:       #e0607e;
  --sky:        #5aafde;
  --lime:       #8fc93a;
  --lavender:   #a78de8;
  --coral:      #e87c52;
  --teal-bg:    rgba(61,214,200,.08);
  --amber-bg:   rgba(240,160,80,.08);
  --rose-bg:    rgba(224,96,126,.08);
  --sky-bg:     rgba(90,175,222,.08);
  --lime-bg:    rgba(143,201,58,.08);
  --lavender-bg:rgba(167,141,232,.08);
  --coral-bg:   rgba(232,124,82,.08);
  --indigo:       #667eea;
  --indigo-bg:    rgba(102,126,234,.08);
  --emerald:       #34d399;
  --emerald-bg:    rgba(52,211,153,.08);
  --fuchsia:       #d946ef;
  --fuchsia-bg:    rgba(217,70,239,.08);
  --cyan:       #22d3ee;
  --cyan-bg:    rgba(34,211,238,.08);
  --gold:       #fbbf24;
  --gold-bg:    rgba(251,191,36,.08);
  --pink:       #f472b6;
  --pink-bg:    rgba(244,114,182,.08);

  --radius:     6px;
  --font:       'Cairo','Segoe UI',Tahoma,sans-serif;
  --mono:       'JetBrains Mono','Courier New',monospace;
}

*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html{-webkit-print-color-adjust:exact;print-color-adjust:exact;}

body{
  background:var(--bg);color:var(--text);font-family:var(--font);
  font-size:16px;line-height:1.6;direction:rtl;text-align:right;
  max-width:900px;margin:0 auto;padding:1.5rem;
}

/* ── Headings ── */
h1{font-size:36px;font-weight:700;color:var(--teal);border-right:4px solid var(--teal);padding-right:.85rem;margin:1.8rem 0 .7rem;line-height:1.3;}
h2{font-size:28px;font-weight:700;color:var(--amber);border-right:3px solid var(--amber);padding-right:.75rem;margin:1.5rem 0 .6rem;line-height:1.3;}
h3{font-size:26px;font-weight:700;color:var(--sky);margin:1.2rem 0 .5rem;line-height:1.3;}
h4{font-size:22px;font-weight:600;color:var(--lavender);margin:1rem 0 .4rem;line-height:1.3;}
p{margin:.4rem 0;font-size:18px;line-height:1.65;}
ul,ol{padding-right:1.4rem;margin:.4rem 0;}
li{margin-bottom:.3rem;font-size:18px;line-height:1.65;}
strong{color:var(--amber);}
em{color:var(--muted);font-style:italic;}
hr{border:none;border-top:1px solid var(--border);margin:2.2rem 0;}

/* ── inline code ── */
code{
  font-family:var(--mono);font-size:.85em;background:var(--bg2);color:var(--teal);
  padding:.12em .42em;border-radius:4px;border:1px solid var(--border);
  direction:ltr;unicode-bidi:embed;white-space:nowrap;
}


/* ── table ── */
table{width:100%;border-collapse:collapse;font-size:.95rem;margin:.9rem 0;background:var(--bg2);border-radius:var(--radius);overflow:hidden;border:1px solid var(--border);}
thead tr{background:var(--bg3);}
th{color:var(--teal);font-weight:700;padding:.6rem .9rem;text-align:right;border-bottom:2px solid var(--border);font-size:.9rem;}
td{padding:.5rem .9rem;border-bottom:1px solid var(--border);vertical-align:top;}
tr:last-child td{border-bottom:none;}

tbody tr:nth-child(even){background:rgba(255,255,255,.015);}

blockquote{border-right:3px solid var(--sky);border-left:none;background:var(--sky-bg);margin:.9rem 0;padding:.7rem 1.1rem;border-radius:var(--radius);color:#a8d4ef;font-size:1rem;}

/* ══════════════════════════════════════════
   CUSTOM ELEMENTS
   ══════════════════════════════════════════ */

/* ── wrap ── */
wrap {
    display: block;
    padding: 2rem 2rem 2.5rem 2rem;
    border-radius: 16px;
    border-top: 5px solid var(--border);
    border-right: 1px solid rgba(255, 255, 255, 0.05);
    border-bottom: 1px solid rgba(255, 255, 255, 0.05);
    border-left: 1px solid rgba(255, 255, 255, 0.05);
    background: linear-gradient(180deg, rgba(255,255,255,0.03) 0%, rgba(0,0,0,0) 100%);
    box-shadow: 0 10px 40px rgba(0,0,0,0.2);
    margin: 3rem 0;
    position: relative;
    counter-reset: example-counter;
}

wrap[color="sky"] { border-top-color: var(--sky); background: linear-gradient(180deg, var(--sky-bg) 0%, rgba(0,0,0,0) 100%); }
wrap[color="teal"] { border-top-color: var(--teal); background: linear-gradient(180deg, var(--teal-bg) 0%, rgba(0,0,0,0) 100%); }
wrap[color="gold"] { border-top-color: var(--gold); background: linear-gradient(180deg, var(--gold-bg) 0%, rgba(0,0,0,0) 100%); }
wrap[color="indigo"] { border-top-color: var(--indigo); background: linear-gradient(180deg, var(--indigo-bg) 0%, rgba(0,0,0,0) 100%); }
wrap[color="fuchsia"] { border-top-color: var(--fuchsia); background: linear-gradient(180deg, var(--fuchsia-bg) 0%, rgba(0,0,0,0) 100%); }
wrap[color="emerald"] { border-top-color: var(--emerald); background: linear-gradient(180deg, var(--emerald-bg) 0%, rgba(0,0,0,0) 100%); }
wrap[color="lavender"] { border-top-color: var(--lavender); background: linear-gradient(180deg, var(--lavender-bg) 0%, rgba(0,0,0,0) 100%); }
wrap[color="cyan"] { border-top-color: var(--cyan); background: linear-gradient(180deg, var(--cyan-bg) 0%, rgba(0,0,0,0) 100%); }

wrap::before {
    content: '';
    position: absolute;
    top: -5px;
    right: 20px;
    width: 30px;
    height: 5px;
    background: var(--bg);
}


/* ── lesson ── */
lesson {
  display: block;
  text-align: center;
  margin: 2rem 0 .9rem;
  padding: .75rem .5rem;
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
  position: relative;
  font-size: 1.3rem;
  font-weight: 700;
  color: var(--amber);
  direction: rtl; /* مهمة عشان ترتيب الكلام */
}

/* الخط اللي فوق العنوان */
lesson::before {
  content: '';
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 48px;
  height: 2px;
  background: var(--amber);
  border-radius: 2px;
}
lesson::before, lesson::after, 
sec::before, sec::after,
.lesson-number, [counter] {
    display: none !important;
    content: "" !important;
    counter-increment: none !important;
}


lesson[color="teal"]  {color:var(--teal);border-color:var(--teal);}    lesson[color="teal"]::before   {background:var(--teal);}
lesson[color="sky"]   {color:var(--sky);border-color:var(--sky);}      lesson[color="sky"]::before    {background:var(--sky);}
lesson[color="rose"]  {color:var(--rose);border-color:var(--rose);}    lesson[color="rose"]::before   {background:var(--rose);}
lesson[color="lime"]  {color:var(--lime);border-color:var(--lime);}    lesson[color="lime"]::before   {background:var(--lime);}
lesson[color="lavender"]{color:var(--lavender);border-color:var(--lavender);}lesson[color="lavender"]::before{background:var(--lavender);}
lesson[color="coral"] {color:var(--coral);border-color:var(--coral);}  lesson[color="coral"]::before  {background:var(--coral);}
lesson[color="pink"]{color:var(--pink);border-color:var(--pink);} lesson[color="pink"]::before{background:var(--pink);}
lesson[color="gold"]{color:var(--gold);border-color:var(--gold);} lesson[color="gold"]::before{background:var(--gold);}
lesson[color="cyan"]{color:var(--cyan);border-color:var(--cyan);} lesson[color="cyan"]::before{background:var(--cyan);}
lesson[color="fuchsia"]{color:var(--fuchsia);border-color:var(--fuchsia);} lesson[color="fuchsia"]::before{background:var(--fuchsia);}
lesson[color="emerald"]{color:var(--emerald);border-color:var(--emerald);} lesson[color="emerald"]::before{background:var(--emerald);}
lesson[color="indigo"]{color:var(--indigo);border-color:var(--indigo);} lesson[color="indigo"]::before{background:var(--indigo);}

/* ── sec (section) ── */
sec {
    display: block;
    font-family: 'Cairo', sans-serif;
    font-weight: 800 !important; /* جرب تخليه 800 أو bold */
    font-size: 24px;
    color: var(--sky);
    margin: 20px 0;
    -webkit-print-color-adjust: exact;
}

sec[color="amber"]   {border-color:var(--amber);   background:var(--amber-bg);   color:var(--amber);}
sec[color="rose"]    {border-color:var(--rose);    background:var(--rose-bg);    color:var(--rose);}
sec[color="sky"]     {border-color:var(--sky);     background:var(--sky-bg);     color:var(--sky);}
sec[color="lime"]    {border-color:var(--lime);    background:var(--lime-bg);    color:var(--lime);}
sec[color="lavender"]{border-color:var(--lavender);background:var(--lavender-bg);color:var(--lavender);}
sec[color="coral"]   {border-color:var(--coral);   background:var(--coral-bg);   color:var(--coral);}
sec[color="pink"]   {border-color:var(--pink);background:var(--pink-bg);color:var(--pink);}
sec[color="gold"]   {border-color:var(--gold);background:var(--gold-bg);color:var(--gold);}
sec[color="cyan"]   {border-color:var(--cyan);background:var(--cyan-bg);color:var(--cyan);}
sec[color="fuchsia"]   {border-color:var(--fuchsia);background:var(--fuchsia-bg);color:var(--fuchsia);}
sec[color="emerald"]   {border-color:var(--emerald);background:var(--emerald-bg);color:var(--emerald);}
sec[color="indigo"]   {border-color:var(--indigo);background:var(--indigo-bg);color:var(--indigo);}

/* ── sub ── */
sub{
  display:flex;align-items:center;gap:.5rem;
  margin:1.4rem 0 .55rem;font-size:18px;font-weight:700;color:var(--sky);
  vertical-align:baseline;
}
sub::before{content:'';width:7px;height:7px;background:var(--sky);border-radius:50%;flex-shrink:0;}
sub[color="amber"]   {color:var(--amber);}    sub[color="amber"]::before   {background:var(--amber);}
sub[color="rose"]    {color:var(--rose);}     sub[color="rose"]::before    {background:var(--rose);}
sub[color="lime"]    {color:var(--lime);}     sub[color="lime"]::before    {background:var(--lime);}
sub[color="coral"]   {color:var(--coral);}    sub[color="coral"]::before   {background:var(--coral);}
sub[color="lavender"]{color:var(--lavender);} sub[color="lavender"]::before{background:var(--lavender);}
sub[color="teal"]    {color:var(--teal);}     sub[color="teal"]::before    {background:var(--teal);}
sub[color="pink"]    {color:var(--pink);}     sub[color="pink"]::before    {background:var(--pink);}
sub[color="gold"]    {color:var(--gold);}     sub[color="gold"]::before    {background:var(--gold);}
sub[color="cyan"]    {color:var(--cyan);}     sub[color="cyan"]::before    {background:var(--cyan);}
sub[color="fuchsia"]    {color:var(--fuchsia);}     sub[color="fuchsia"]::before    {background:var(--fuchsia);}
sub[color="emerald"]    {color:var(--emerald);}     sub[color="emerald"]::before    {background:var(--emerald);}
sub[color="indigo"]    {color:var(--indigo);}     sub[color="indigo"]::before    {background:var(--indigo);}

/* ── note ── */
note{
  display:flex;gap:.7rem;align-items:flex-start;margin:.7rem 0;
  padding:.9rem 1.1rem;border-radius:var(--radius);font-size:18px;font-weight:600;
  line-height:1.6;border-right:3px solid;
  background:var(--sky-bg);border-color:var(--sky);color:#a8d4ef;
}
note[type="warn"]   {background:var(--amber-bg);   border-color:var(--amber);   color:#e8c48a;}
note[type="tip"]    {background:var(--lime-bg);    border-color:var(--lime);    color:#b8d97a;}
note[type="danger"] {background:var(--rose-bg);    border-color:var(--rose);    color:#eca8b8;}
note[type="remember"]{background:var(--lavender-bg);border-color:var(--lavender);color:#c4b3f0;}
note[type="success"]{background:rgba(61,214,200,.07);border-color:var(--teal);  color:#88d8d2;}

/* ── hl (highlight inline) ── */
hl, .hl {
    /* الخط الموحد للأكواد */
    font-family: var(--mono), monospace; 
    font-size: 0.92em;
    font-weight: 700;
    
    /* اللون الافتراضي (لما تستخدم hl بدون تحديد لون) */
    background: rgba(90, 175, 222, .12); 
    color: var(--sky);
    
    /* التنسيقات العامة */
    border-radius: 5px;
    padding: 0.1em 0.4em;
    line-height: 2;
    display: inline;
    
    /* إجبار الـ PDF على إظهار الألوان */
    -webkit-print-color-adjust: exact !important;
    print-color-adjust: exact !important;
}

/* الألوان المخصصة (Attribute Selectors) */
hl[color="teal"]     { background: rgba(61, 214, 200, .12)  !important; color: var(--teal) !important; }
hl[color="amber"]    { background: rgba(240, 160, 80, .12)  !important; color: var(--amber) !important; }
hl[color="rose"]     { background: rgba(224, 96, 126, .12)  !important; color: var(--rose) !important; }
hl[color="lime"]     { background: rgba(143, 201, 58, .12)  !important; color: var(--lime) !important; }
hl[color="lavender"] { background: rgba(167, 141, 232, .12) !important; color: var(--lavender) !important; }
hl[color="coral"]    { background: rgba(232, 124, 82, .12)   !important; color: var(--coral) !important; }
hl[color="pink"]    { background: rgba(244,114,182, .12)   !important; color: var(--pink) !important; }
hl[color="gold"]    { background: rgba(251,191,36, .12)   !important; color: var(--gold) !important; }
hl[color="cyan"]    { background: rgba(34,211,238, .12)   !important; color: var(--cyan) !important; }
hl[color="fuchsia"]    { background: rgba(217,70,239, .12)   !important; color: var(--fuchsia) !important; }
hl[color="emerald"]    { background: rgba(52,211,153, .12)   !important; color: var(--emerald) !important; }
hl[color="indigo"]    { background: rgba(102,126,234, .12)   !important; color: var(--indigo) !important; }

/* ── t (tag inline) ── */
t{
  display:inline-block;padding:.13em .7em;font-size:15px;font-weight:900;
  border-radius:4px;vertical-align:middle;line-height:1.55;
  font-family:var(--mono);letter-spacing:.06em;
  background:rgba(90,175,222,.1);color:var(--sky);border:1px solid rgba(90,175,222,.28);
}
t[color="teal"]    {background:rgba(61,214,200,.1); color:var(--teal);    border-color:rgba(61,214,200,.28);}
t[color="amber"]   {background:rgba(240,160,80,.1); color:var(--amber);   border-color:rgba(240,160,80,.28);}
t[color="rose"]    {background:rgba(224,96,126,.1); color:var(--rose);    border-color:rgba(224,96,126,.28);}
t[color="lime"]    {background:rgba(143,201,58,.1); color:var(--lime);    border-color:rgba(143,201,58,.28);}
t[color="lavender"]{background:rgba(167,141,232,.1);color:var(--lavender);border-color:rgba(167,141,232,.28);}
t[color="coral"]   {background:rgba(232,124,82,.1); color:var(--coral);   border-color:rgba(232,124,82,.28);}
t[color="pink"]   {background:rgba(244,114,182,.1); color:var(--pink);   border-color:rgba(244,114,182,.28);}
t[color="gold"]   {background:rgba(251,191,36,.1); color:var(--gold);   border-color:rgba(251,191,36,.28);}
t[color="cyan"]   {background:rgba(34,211,238,.1); color:var(--cyan);   border-color:rgba(34,211,238,.28);}
t[color="fuchsia"]   {background:rgba(217,70,239,.1); color:var(--fuchsia);   border-color:rgba(217,70,239,.28);}
t[color="emerald"]   {background:rgba(52,211,153,.1); color:var(--emerald);   border-color:rgba(52,211,153,.28);}
t[color="indigo"]   {background:rgba(102,126,234,.1); color:var(--indigo);   border-color:rgba(102,126,234,.28);}

/* ── card ── */
card{
  display:block;background:var(--bg2);border:1px solid var(--border);
  border-radius:var(--radius);padding:1rem 1.2rem;margin:.9rem 0;
}
card::before{
  content:attr(title);display:block;font-size:1.2rem;font-weight:700;color:var(--teal);
  margin-bottom:.6rem;padding-bottom:.5rem;border-bottom:1px solid var(--border);
}
card[color="amber"]::before{color:var(--amber);}
card[color="rose"]::before {color:var(--rose);}
card[color="sky"]::before  {color:var(--sky);}
card[color="pink"]::before  {color:var(--pink);}
card[color="gold"]::before  {color:var(--gold);}
card[color="cyan"]::before  {color:var(--cyan);}
card[color="fuchsia"]::before  {color:var(--fuchsia);}
card[color="emerald"]::before  {color:var(--emerald);}
card[color="indigo"]::before  {color:var(--indigo);}

/* ── pills / pill ── */
pills{display:flex;flex-wrap:wrap;gap:.4rem;margin:.5rem 0;display:flex;}
pill{
  font-size:15px;font-weight:700;display:inline-flex;align-items:center;
  gap:.3rem;padding:.22em .65em;border-radius:99px;direction:ltr;
  border:1px solid var(--border);background:var(--bg3);color:var(--text);
}
pill[color="teal"]    {border-color:rgba(61,214,200,.3); color:var(--teal);    background:rgba(61,214,200,.06);}
pill[color="amber"]   {border-color:rgba(240,160,80,.3); color:var(--amber);   background:rgba(240,160,80,.06);}
pill[color="rose"]    {border-color:rgba(224,96,126,.3); color:var(--rose);    background:rgba(224,96,126,.06);}
pill[color="lime"]    {border-color:rgba(143,201,58,.3); color:var(--lime);    background:rgba(143,201,58,.06);}
pill[color="lavender"]{border-color:rgba(167,141,232,.3);color:var(--lavender);background:rgba(167,141,232,.06);}
pill[color="sky"]     {border-color:rgba(90,175,222,.3); color:var(--sky);     background:rgba(90,175,222,.06);}
pill[color="pink"]     {border-color:rgba(244,114,182,.3); color:var(--pink);     background:rgba(244,114,182,.06);}
pill[color="gold"]     {border-color:rgba(251,191,36,.3); color:var(--gold);     background:rgba(251,191,36,.06);}
pill[color="cyan"]     {border-color:rgba(34,211,238,.3); color:var(--cyan);     background:rgba(34,211,238,.06);}
pill[color="fuchsia"]     {border-color:rgba(217,70,239,.3); color:var(--fuchsia);     background:rgba(217,70,239,.06);}
pill[color="emerald"]     {border-color:rgba(52,211,153,.3); color:var(--emerald);     background:rgba(52,211,153,.06);}
pill[color="indigo"]     {border-color:rgba(102,126,234,.3); color:var(--indigo);     background:rgba(102,126,234,.06);}

/* ── cl (callout) ── */
cl{
  display:block;border:1px solid var(--border);border-right:4px solid var(--sky);
  border-radius:var(--radius);background:var(--bg2);
  padding:1rem 1.2rem;margin:1rem 0;font-size:17px;
}
cl::before{
  content:attr(title);display:block;font-weight:700;color:var(--sky);
  margin-bottom:.4rem;font-size:17px;
}
cl[color="amber"]{border-right-color:var(--amber);}cl[color="amber"]::before{color:var(--amber);}
cl[color="teal"] {border-right-color:var(--teal);}  cl[color="teal"]::before {color:var(--teal);}
cl[color="rose"] {border-right-color:var(--rose);}  cl[color="rose"]::before {color:var(--rose);}
cl[color="lime"] {border-right-color:var(--lime);}  cl[color="lime"]::before {color:var(--lime);}
cl[color="lavender"]{border-right-color:var(--lavender);}cl[color="lavender"]::before{color:var(--lavender);}
cl[color="pink"]{border-right-color:var(--pink);}cl[color="pink"]::before{color:var(--pink);}
cl[color="gold"]{border-right-color:var(--gold);}cl[color="gold"]::before{color:var(--gold);}
cl[color="cyan"]{border-right-color:var(--cyan);}cl[color="cyan"]::before{color:var(--cyan);}
cl[color="fuchsia"]{border-right-color:var(--fuchsia);}cl[color="fuchsia"]::before{color:var(--fuchsia);}
cl[color="emerald"]{border-right-color:var(--emerald);}cl[color="emerald"]::before{color:var(--emerald);}
cl[color="indigo"]{border-right-color:var(--indigo);}cl[color="indigo"]::before{color:var(--indigo);}

/* ── ex (example) ── */
ex{
  display:block;border:1px solid var(--border);border-right:4px solid var(--amber);
  border-radius:var(--radius);background:var(--bg2);margin:1.1rem 0;overflow:hidden;
  counter-increment:example-counter;padding:.9rem 1.1rem;font-size:17px;
}
ex::before{
  content:'مثال ' counter(example-counter);display:block;
  background:var(--bg3);color:var(--amber);font-family:var(--font);
  font-size:.85rem;font-weight:700;padding:.45rem 1rem;
  border-bottom:1px solid var(--border);margin:-.9rem -1.1rem .9rem;
  direction:rtl;text-align:right;
}

/* ── out (output) ── */
out{
  display:block;background:#0a0c10;border:1px solid var(--border);
  border-left:3px solid var(--lime);border-radius:var(--radius);
  padding:.9rem 1.2rem;margin:.5rem 0 .9rem;
  font-family:var(--mono);font-size:.9rem;direction:ltr;text-align:left;
  position:relative;color:#a8e8a0;line-height:1.9;white-space:pre;
}
out::before{
  content:'output';position:absolute;top:.4rem;right:.75rem;
  font-size:.65rem;color:var(--lime);letter-spacing:.1em;text-transform:uppercase;opacity:.7;
}
out .err{color:var(--rose);}
out .hi {color:var(--teal);}
out .cm {color:var(--muted);}

/* ── syn (syntax box) ── */
syn{
  display:block;background:#0e1018;border:1px solid var(--border);
  border-top:2px solid var(--lavender);border-radius:var(--radius);
  padding:.85rem 1.2rem;margin:.85rem 0;
  font-family:var(--mono);font-size:.95rem;direction:ltr;text-align:left;
  line-height:2;overflow-x:auto;
}
syn::before{
  content:attr(label);display:block;font-family:var(--font);font-size:.8rem;
  color:var(--muted);direction:rtl;text-align:right;
  margin-bottom:.4rem;padding-bottom:.4rem;border-bottom:1px solid var(--border);
}
syn:not([label])::before{display:none;}

/* ── divider ── */
divider{
  display:flex;align-items:center;gap:.7rem;margin:1.7rem 0;
  color:var(--muted);font-size:1.1rem;letter-spacing:.1em;font-weight:900;
  text-transform:uppercase;font-family:var(--mono);
}
divider::before,divider::after{content:'';flex:1;height:1px;background:var(--border);}

/* ── br-page ── */
br-page{display:block;page-break-after:always;}

/* ── steps / step ── */
steps{display:block;list-style:none;padding:0;margin:.7rem 0;counter-reset:s;}
step{
  display:flex;align-items:flex-start;gap:.7rem;
  margin-bottom:.55rem;font-size:17px;counter-increment:s;
}
step::before{
  content:counter(s);min-width:1.55rem;height:1.55rem;
  display:flex;align-items:center;justify-content:center;
  background:var(--bg3);border:1px solid var(--border);border-radius:50%;
  font-size:.75rem;font-weight:700;color:var(--teal);
  flex-shrink:0;margin-top:.22rem;font-family:var(--mono);
}

/* ── kv ── */
kv{display:flex;gap:.85rem;margin:.38rem 0;font-size:17px;align-items:flex-start;}
kv::before{content:attr(k);font-weight:700;color:var(--amber);white-space:nowrap;min-width:90px;}

/* ── defs / def ── */
defs{display:block;margin:.6rem 0;}
def{
  display:grid;grid-template-columns:160px 1fr;gap:.5rem 1rem;
  padding:.45rem 0;border-bottom:1px solid var(--border);
  font-size:17px;align-items:baseline;
}
def:last-child{border-bottom:none;}
def::before{content:attr(term);color:var(--teal);font-weight:700;font-family:var(--mono);font-size:15px;}

/* ── cmp (compare) ── */
cmp{display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin:1rem 0;}
good,bad{
  display:block;background:var(--bg2);border:1px solid var(--border);
  border-radius:var(--radius);padding:1rem;min-width:0;
}
good::before{content:attr(title);display:block;font-weight:700;font-size:17px;margin-bottom:.6rem;padding-bottom:.5rem;border-bottom:1px solid var(--border);color:var(--lime);}
bad::before {content:attr(title);display:block;font-weight:700;font-size:17px;margin-bottom:.6rem;padding-bottom:.5rem;border-bottom:1px solid var(--border);color:var(--rose);}

/* ── tl / tls / tli (timeline) ── */
/* ✅ تكبير الفهرس بالكامل */
tl{
  display:block;position:relative;margin:1.2rem 0;padding-right:2rem;
}
tl::before{
  content:'';position:absolute;right:.7rem;top:.6rem;bottom:.6rem;
  width:2px;background:var(--border);border-radius:2px;
}
tls{
  display:block;position:relative;margin:1.6rem 0 .75rem;padding:.65rem 1.2rem;
  border-radius:var(--radius);font-size:1.4rem;font-weight:900;
  border-right:3px solid var(--teal);background:var(--teal-bg);color:var(--teal);
}
tls::before{
  content:'';position:absolute;right:-1.75rem;top:50%;transform:translateY(-50%);
  width:16px;height:16px;border-radius:50%;background:var(--teal);border:2px solid var(--bg);z-index:1;
}
tli{
  display:block;position:relative;margin-bottom:.65rem;padding:.65rem 1.2rem;
  background:var(--bg2);border:1px solid var(--border);
  border-radius:var(--radius);font-size:1.4rem;color:var(--text);font-weight:600;
}
tli::before{
  content:'';position:absolute;right:-1.45rem;top:50%;transform:translateY(-50%);
  width:10px;height:10px;border-radius:50%;background:var(--border);border:2px solid var(--bg);z-index:1;
}

/* colors for tls / tli */
tls[color="amber"]   {border-color:var(--amber);background:var(--amber-bg);color:var(--amber);}tls[color="amber"]::before   {background:var(--amber);}
tls[color="rose"]    {border-color:var(--rose); background:var(--rose-bg); color:var(--rose);} tls[color="rose"]::before    {background:var(--rose);}
tls[color="sky"]     {border-color:var(--sky);  background:var(--sky-bg);  color:var(--sky);}  tls[color="sky"]::before     {background:var(--sky);}
tls[color="lime"]    {border-color:var(--lime); background:var(--lime-bg); color:var(--lime);} tls[color="lime"]::before    {background:var(--lime);}
tls[color="lavender"]{border-color:var(--lavender);background:var(--lavender-bg);color:var(--lavender);}tls[color="lavender"]::before{background:var(--lavender);}
tls[color="coral"]   {border-color:var(--coral);background:var(--coral-bg);color:var(--coral);}tls[color="coral"]::before   {background:var(--coral);}
tls[color="pink"]   {border-color:var(--pink);background:var(--pink-bg);color:var(--pink);}tls[color="pink"]::before   {background:var(--pink);}
tls[color="gold"]   {border-color:var(--gold);background:var(--gold-bg);color:var(--gold);}tls[color="gold"]::before   {background:var(--gold);}
tls[color="cyan"]   {border-color:var(--cyan);background:var(--cyan-bg);color:var(--cyan);}tls[color="cyan"]::before   {background:var(--cyan);}
tls[color="fuchsia"]   {border-color:var(--fuchsia);background:var(--fuchsia-bg);color:var(--fuchsia);}tls[color="fuchsia"]::before   {background:var(--fuchsia);}
tls[color="emerald"]   {border-color:var(--emerald);background:var(--emerald-bg);color:var(--emerald);}tls[color="emerald"]::before   {background:var(--emerald);}
tls[color="indigo"]   {border-color:var(--indigo);background:var(--indigo-bg);color:var(--indigo);}tls[color="indigo"]::before   {background:var(--indigo);}

tli[color="teal"]    {border-right:3px solid rgba(61,214,200,.3);}  tli[color="teal"]::before    {background:rgba(61,214,200,.5);}
tli[color="amber"]   {border-right:3px solid rgba(240,160,80,.3);}  tli[color="amber"]::before   {background:rgba(240,160,80,.5);}
tli[color="rose"]    {border-right:3px solid rgba(224,96,126,.3);}  tli[color="rose"]::before    {background:rgba(224,96,126,.5);}
tli[color="sky"]     {border-right:3px solid rgba(90,175,222,.3);}  tli[color="sky"]::before     {background:rgba(90,175,222,.5);}
tli[color="lime"]    {border-right:3px solid rgba(143,201,58,.3);}  tli[color="lime"]::before    {background:rgba(143,201,58,.5);}
tli[color="lavender"]{border-right:3px solid rgba(167,141,232,.3);} tli[color="lavender"]::before{background:rgba(167,141,232,.5);}
tli[color="coral"]   {border-right:3px solid rgba(232,124,82,.3);}  tli[color="coral"]::before   {background:rgba(232,124,82,.5);}
tli[color="pink"]   {border-right:3px solid rgba(244,114,182,.3);}  tli[color="pink"]::before   {background:rgba(244,114,182,.5);}
tli[color="gold"]   {border-right:3px solid rgba(251,191,36,.3);}  tli[color="gold"]::before   {background:rgba(251,191,36,.5);}
tli[color="cyan"]   {border-right:3px solid rgba(34,211,238,.3);}  tli[color="cyan"]::before   {background:rgba(34,211,238,.5);}
tli[color="fuchsia"]   {border-right:3px solid rgba(217,70,239,.3);}  tli[color="fuchsia"]::before   {background:rgba(217,70,239,.5);}
tli[color="emerald"]   {border-right:3px solid rgba(52,211,153,.3);}  tli[color="emerald"]::before   {background:rgba(52,211,153,.5);}
tli[color="indigo"]   {border-right:3px solid rgba(102,126,234,.3);}  tli[color="indigo"]::before   {background:rgba(102,126,234,.5);}


/* ── badge ── */
badge{
  display:inline-block;padding:.17em .55em;border-radius:99px;
  font-size:.9rem;font-weight:700;letter-spacing:.04em;
  text-transform:uppercase;font-family:var(--mono);
}
badge[type="done"]  {background:rgba(143,201,58,.1); color:var(--lime);    border:1px solid rgba(143,201,58,.28);}
badge[type="wip"]   {background:rgba(240,160,80,.1); color:var(--amber);   border:1px solid rgba(240,160,80,.28);}
badge[type="todo"]  {background:var(--bg3);          color:var(--muted);   border:1px solid var(--border);}
badge[type="hard"]  {background:rgba(224,96,126,.1); color:var(--rose);    border:1px solid rgba(224,96,126,.28);}
badge[type="new"]   {background:rgba(61,214,200,.1); color:var(--teal);    border:1px solid rgba(61,214,200,.28);}
badge[type="review"]{background:rgba(167,141,232,.1);color:var(--lavender);border:1px solid rgba(167,141,232,.28);}

/* ── inline syntax colors ── */
/* ✅ تكبير الكلاسات من .83em → .95em */
.kw {font-family:var(--mono);font-size:.95em;color:var(--lavender);font-weight:700;}
.fn {font-family:var(--mono);font-size:.95em;color:var(--lime);}
.cls{font-family:var(--mono);font-size:.95em;color:var(--sky);font-weight:700;}
.op {font-family:var(--mono);font-size:.95em;color:var(--coral);}
.cm {font-family:var(--mono);font-size:.95em;color:var(--muted);font-style:italic;}
.st {font-family:var(--mono);font-size:.95em;color:var(--amber);}

.break {
    page-break-before: always;
}


/* ── Section Covers ── */
cover {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 75vh;
    margin: 0;
    padding: 0;
}
cover-circle {
    width: 380px;
    height: 380px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    font-family: 'Cairo', sans-serif;
    font-size: 44px;
    font-weight: 900;
    line-height: 1.4;
    border: 12px solid;
    background: var(--bg2);
    padding: 30px;
    box-shadow: 0 0 60px rgba(0,0,0,0.5), inset 0 0 40px rgba(0,0,0,0.5);
    text-shadow: 0 4px 10px rgba(0,0,0,0.4);
    -webkit-print-color-adjust: exact;
    print-color-adjust: exact;
}

cover-circle[color="sky"] { border-color: var(--sky); color: var(--sky); box-shadow: 0 0 25px rgba(90,175,222,0.4), 0 0 80px rgba(90,175,222,0.15), inset 0 0 30px rgba(90,175,222,0.15); }
cover-circle[color="teal"] { border-color: var(--teal); color: var(--teal); box-shadow: 0 0 25px rgba(61,214,200,0.4), 0 0 80px rgba(61,214,200,0.15), inset 0 0 30px rgba(61,214,200,0.15); }
cover-circle[color="gold"] { border-color: var(--gold); color: var(--gold); box-shadow: 0 0 25px rgba(251,191,36,0.4), 0 0 80px rgba(251,191,36,0.15), inset 0 0 30px rgba(251,191,36,0.15); }
cover-circle[color="indigo"] { border-color: var(--indigo); color: var(--indigo); box-shadow: 0 0 25px rgba(102,126,234,0.4), 0 0 80px rgba(102,126,234,0.15), inset 0 0 30px rgba(102,126,234,0.15); }
cover-circle[color="fuchsia"] { border-color: var(--fuchsia); color: var(--fuchsia); box-shadow: 0 0 25px rgba(217,70,239,0.4), 0 0 80px rgba(217,70,239,0.15), inset 0 0 30px rgba(217,70,239,0.15); }
cover-circle[color="emerald"] { border-color: var(--emerald); color: var(--emerald); box-shadow: 0 0 25px rgba(52,211,153,0.4), 0 0 80px rgba(52,211,153,0.15), inset 0 0 30px rgba(52,211,153,0.15); }
cover-circle[color="lavender"] { border-color: var(--lavender); color: var(--lavender); box-shadow: 0 0 25px rgba(167,141,232,0.4), 0 0 80px rgba(167,141,232,0.15), inset 0 0 30px rgba(167,141,232,0.15); }
cover-circle[color="cyan"] { border-color: var(--cyan); color: var(--cyan); box-shadow: 0 0 25px rgba(34,211,238,0.4), 0 0 80px rgba(34,211,238,0.15), inset 0 0 30px rgba(34,211,238,0.15); }
</style>

<!-- ═══════ HEADER ═══════ -->
<h1 style="text-align:center;"> ملخص الكورس العاشر </h1>

<h4 style="text-align:center;font-size:20px">من : عبدالرحمن محيي الدين</h4>

<hr>

<!-- ═══════ فهرس الكورس ═══════ -->

<wrap>

<sec color="sky">البرمجة الكائنية — C++ OOP</sec>

<tl>

  <tls color="sky">البداية وفهم OOP</tls>
  <tli color="sky"><a href="#l-what-is-oop-and-why" style="text-decoration:none; color:inherit;">What is OOP and Why?</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 5</span></tli>
  <tli color="sky"><a href="#l-classes-and-objects" style="text-decoration:none; color:inherit;">Classes and Objects</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 9</span></tli>
  <tli color="sky"><a href="#l-class-members" style="text-decoration:none; color:inherit;">Class Members</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 12</span></tli>
  <tli color="sky"><a href="#l-objects-in-memory" style="text-decoration:none; color:inherit;">Objects In Memory</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 14</span></tli>
  <tli color="sky"><a href="#l-access-specifiersmodifiers" style="text-decoration:none; color:inherit;">Access Specifiers/Modifiers</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 15</span></tli>

  <tls color="teal">الخصائص والتغليف</tls>
  <tli color="teal"><a href="#l-properties-set-and-get" style="text-decoration:none; color:inherit;">Properties Set and Get</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 20</span></tli>
  <tli color="teal"><a href="#l-read-only-property" style="text-decoration:none; color:inherit;">Read Only Property</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 23</span></tli>
  <tli color="teal"><a href="#l-properties-set-and-get-through-" style="text-decoration:none; color:inherit;">Properties Set and Get through "="</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 25</span></tli>

  <tls color="teal">Encapsulation & Abstraction</tls>
  <tli color="teal"><a href="#l-first-principle-of-oop-encapsulation" style="text-decoration:none; color:inherit;">First Principle of OOP: Encapsulation</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 29</span></tli>
  <tli color="teal"><a href="#l-second-principle-of-oop-abstraction" style="text-decoration:none; color:inherit;">Second Principle of OOP: Abstraction</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 31</span></tli>


  <tls color="gold">Constructors &amp; Memory</tls>
  <tli color="gold"><a href="#l-constructors" style="text-decoration:none; color:inherit;">Constructors</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 36</span></tli>
  <tli color="gold"><a href="#l-copy-constructors" style="text-decoration:none; color:inherit;">Copy Constructors</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 39</span></tli>
  <tli color="gold"><a href="#l-destructors" style="text-decoration:none; color:inherit;">Destructors</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 43</span></tli>
  <tli color="gold"><a href="#l-static-members" style="text-decoration:none; color:inherit;">Static Members</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 46</span></tli>
  <tli color="gold"><a href="#l-static-methods" style="text-decoration:none; color:inherit;">Static Methods</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 49</span></tli>


  <tls color="indigo">Inheritance — الوراثة</tls>
  <tli color="indigo"><a href="#l-third-principle-of-oop-inheritance" style="text-decoration:none; color:inherit;">Third Principle of OOP: Inheritance</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 53</span></tli>
  <tli color="indigo"><a href="#l-parameterized-constructor-of-the-base-class" style="text-decoration:none; color:inherit;">Parameterized Constructor of the Base Class</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 58</span></tli>
  <tli color="indigo"><a href="#l-function-overriding" style="text-decoration:none; color:inherit;">Function Overriding</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 62</span></tli>
  <tli color="indigo"><a href="#l-multi-level-inheritance" style="text-decoration:none; color:inherit;">Multi Level Inheritance</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 66</span></tli>
  <tli color="indigo"><a href="#l-access-specifiersmodifiers-review" style="text-decoration:none; color:inherit;">Access Specifiers/Modifiers Review</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 70</span></tli>
  <tli color="indigo"><a href="#l-inheritance-visibility-modes" style="text-decoration:none; color:inherit;">Inheritance Visibility Modes</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 73</span></tli>
  <tli color="indigo"><a href="#l-inheritance-types" style="text-decoration:none; color:inherit;">Inheritance Types</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 77</span></tli>
  <tli color="indigo"><a href="#l-up-casting-vs-down-casting" style="text-decoration:none; color:inherit;">Up Casting vs Down Casting</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 79</span></tli>
  <tli color="indigo"><a href="#l-virtual-functions" style="text-decoration:none; color:inherit;">Virtual Functions</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 82</span></tli>
  <tli color="indigo"><a href="#l-staticearly-binding-vs-dynamiclate-binding" style="text-decoration:none; color:inherit;">Static/Early Binding vs Dynamic/Late Binding</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 85</span></tli>

  <tls color="fuchsia">Polymorphism</tls>
  <tli color="fuchsia"><a href="#l-fourth-principleconcept-of-oop-polymorphism" style="text-decoration:none; color:inherit;">Fourth Principle/Concept of OOP: Polymorphism</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 89</span></tli>
  <tli color="fuchsia"><a href="#l-interfaces-pure-virtual-functions-and-abstract-classes" style="text-decoration:none; color:inherit;">Interfaces: Pure Virtual Functions and Abstract Classes</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 90</span></tli>

  <tls color="emerald">Friends</tls>
  <tli color="emerald"><a href="#l-friend-class" style="text-decoration:none; color:inherit;">Friend Class</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 97</span></tli>
  <tli color="emerald"><a href="#l-friend-functions" style="text-decoration:none; color:inherit;">Friend Functions</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 99</span></tli>

  <tls color="lavender">Misc</tls>
  <tli color="lavender"><a href="#l-structure-inside-class" style="text-decoration:none; color:inherit;">Structure Inside Class</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 102</span></tli>
  <tli color="lavender"><a href="#l-nested-classes" style="text-decoration:none; color:inherit;">Nested Classes</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 103</span></tli>
  <tli color="lavender"><a href="#l-passing-objects-to-functions" style="text-decoration:none; color:inherit;">Passing Objects to Functions (ByRef/ByVal)</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 105</span></tli>
  <tli color="lavender"><a href="#l-objects-and-vectors" style="text-decoration:none; color:inherit;">Objects and Vectors</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 106</span></tli>
  <tli color="lavender"><a href="#l-objects-and-dynamic-array" style="text-decoration:none; color:inherit;">Objects and Dynamic Array</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 107</span></tli>
  <tli color="lavender"><a href="#l-objects-with-parameterized-constructor-and-array" style="text-decoration:none; color:inherit;">Objects with Parameterized Constructor and Array</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 108</span></tli>

  <tls color="cyan">Other</tls>
  <tli color="cyan"><a href="#l-this-pointer" style="text-decoration:none; color:inherit;">‘this’ pointer</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 110</span></tli>
  <tli color="cyan"><a href="#l-separate-classes-in-libraries" style="text-decoration:none; color:inherit;">Separate Classes In Libraries</a> <span style="float:left; font-family:var(--mono); font-size:0.85em; opacity:0.6;">Page : 113</span></tli>






</tl>

<p style="text-align:center; color: #88ff4dff; font-weight: bold; font-family: 'Cairo', sans-serif; margin-top: 15px;">
    (الفهرس قابل للنقر  )
</p>

</wrap>

<hr>

<div class="page-break"></div>
<!-- ═══════ درس ١ ═══════ -->

<br-page></br-page>

<cover><cover-circle color="sky">البداية وفهم OOP</cover-circle></cover>

<br-page></br-page>

<wrap color="sky">

<a id="l-what-is-oop-and-why"></a>
<lesson color="sky">What is OOP and Why?</lesson>


<h2>
 خلينا نبدأ بمثال عن الفرق بين :

 الـ <hl color="lime">Functional Programming

 </hl> والـ <hl color="lavender">Object-Oriented Programming</hl></h2>

#### هيكون مشروع لتنظيم سستم جامعي 
#### المشروع هنعمله مرتين: مرة بالـ <t color="lime">FP</t> ومرة بالـ <t color="lavender">OOP</t> عشان نشوف الفرق

<divider>أولاً — Functional Programming</divider>

### كل الدوال اللي هنحتاجها في مشروع الجامعة:

<card title="📋 قائمة الدوال في FP">
<pills>
  <pill color="lime">AddStudent()</pill>
  <pill color="lime">UpdateStudent()</pill>
  <pill color="lime">DeleteStudent()</pill>
  <pill color="lime">SendEmailToStudent()</pill>
  <pill color="lime">AddDoctor()</pill>
  <pill color="lime">EditDoctor()</pill>
  <pill color="lime">DeleteDoctor()</pill>
  <pill color="lime">AssignCourseToDoctor()</pill>
  <pill color="lime">AddEmployee()</pill>
  <pill color="lime">UpdateEmployee()</pill>
  <pill color="lime">DeleteEmployee()</pill>
  <pill color="lime">CalculateSalary()</pill>
  <pill color="lime">PaySalary()</pill>
  <pill color="lime">AddCourse()</pill>
  <pill color="lime">UpdateCourse()</pill>
  <pill color="lime">DeleteCourse()</pill>
  <pill color="lime">EnrollStudentInCourse()</pill>
  <pill color="lime">HowManyStudentsInCourse()</pill>
</pills>
</card>

<note>هيكون في الآخر عندك عشرات وممكن مئات الدوال، ولازم تعرف كل واحدة خاصة بإيه بالظبط</note>
<note type="warn">⚠️ المشكلة مش في العدد — المشكلة في طريقة التعامل معاهم وصعوبتها لما المشروع يكبر</note>

<br-page/>
<div class="page-break"></div>
<divider>ثانياً — Object-Oriented Programming</divider>

### ما هي جميع **الأشياء** التي تريد برمجتها في مشروع الجامعة؟
#### هترد تقولي عايز ابرمج الطلاب و الدوال اللي بتتحكم فيهم , الدكاترة و الدوال اللي بتتحكم فيهم , الكورسات و الدوال اللي بتنظمهم
#### البرمجة الشيئية بتساعدنا نجمع كل الدوال الخاصة بكائن معين تحته مباشرةً

<cmp>
<good title="🎓 Student Object">
<pills>
  <pill color="lime">Name</pill>
  <pill color="lime">Email</pill>
  <pill color="lavender">AddStudent()</pill>
  <pill color="lavender">UpdateStudent()</pill>
  <pill color="lavender">DeleteStudent()</pill>
  <pill color="lavender">SendEmail()</pill>
  <pill color="lavender">EnrollInCourse()</pill>
</pills>
</good>
<good title="👨‍🏫 Doctor Object">
<pills>
  <pill color="lime">Name</pill>
  <pill color="lime">Email</pill>
  <pill color="lavender">AddDoctor()</pill>
  <pill color="lavender">EditDoctor()</pill>
  <pill color="lavender">DeleteDoctor()</pill>
  <pill color="lavender">AssignCourse()</pill>
</pills>
</good>
</cmp>

<cmp>
<good title="🧾 Employee Object">
<pills>
  <pill color="lime">Name</pill>
  <pill color="lime">Email</pill>
  <pill color="lavender">AddEmployee()</pill>
  <pill color="lavender">UpdateEmployee()</pill>
  <pill color="lavender">DeleteEmployee()</pill>
  <pill color="lavender">CalculateSalary()</pill>
  <pill color="lavender">PaySalary()</pill>
</pills>
</good>
<good title="📚 Course Object">
<pills>
  <pill color="lavender">AddCourse()</pill>
  <pill color="lavender">UpdateCourse()</pill>
  <pill color="lavender">DeleteCourse()</pill>
  <pill color="lavender">EnrollStudent()</pill>
  <pill color="lavender">StudentsCount()</pill>
</pills>
</good>
</cmp>

<note type="success">✅ بدل ما كان عندك 18 دالة عشوائية مبعثرة، بقى عندك 4 كائنات واضحة وكل كائن تحته دواله الخاصة فقط</note>
<note>🧠 العقل البشري بيفهم العالم على شكل أشياء وليس دوال مبعثرة , ولهذا OOP أقرب لطريقة تفكيرنا فا احسنلك بكتير تفكر بالطريقة دي</note>

## مزايا البرمجة الشيئية

<defs>
  <def term="التنظيم">كل بيانات الكائن ودواله في مكان واحد — سهل تلاقيهم وتعدل عليهم</def>
  <def term="إعادة الاستخدام">تقدر تستخدم نفس الكلاس في أكتر من مشروع من غير ما تعيد كتابة الكود</def>
  <def term="الصيانة">لو في باج في Student، بتصلحه في مكان واحد بس وبيتصلح في كل المشروع</def>
  <def term="التوسع">تقدر تضيف كلاس جديد زي Admin من غير ما تلمس الكود القديم خالص</def>
  <def term="قرب التفكير">العقل البشري بيفهم العالم على شكل أشياء — OOP أقرب لطريقة تفكيرنا الطبيعية</def>
</defs>

<br-page></br-page>

<a id="l-classes-and-objects"></a>
<lesson color="sky">Classes and Objects</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثاني: الكلاسات والكائنات</h4>

<divider>ليه سميناه Class؟</divider>

**قبل ما نبدا محتاجين نفهم ليه الاسم ده بالذات.** كلمة <t color="amber">Class</t> في البرمجة جاية من كلمة <hl>تصنيف (Classification)</hl> .

لما بنقول "طلاب"، "دكاترة"، أو "سيارات"، إحنا بنعمل تصنيف للأشياء دي في عقلنا. كل تصنيف في الدنيا له حاجتين:

 - صفات مشتركة
 - وسلوكيات مشتركة.
 
  وده بالضبط اللي بنعمله في الـ OOP؛ الكلاس هو تصنيف برمجي بنحط جواه كل ما يخص هذا النوع من الأشياء. وده طبعاً امتداد للي قلناه الدرس اللي فات، إننا بننظم العالم على شكل أشياء، والأشياء دي لازم يكون ليها تصنيف تخرج منه.

<card title="💡 مثال">

* **Student** هو الـ **Class** (التصنيف العام).
* **Ahmed** هو الـ **Object** (الكائن الفعلي اللي خرج من التصنيف ده).

</card>

---

<divider>الكلاس هو Data Type</divider>

إنت قبل كده درست الـ <t color="sky">struct</t> وعرفنا إنه بيجمع بيانات مع بعض. لازم تفهم نقطة جوهرية هنا: الـ **struct** هو نوع بيانات، والـ **class** برضه هو نوع بيانات إنت اللي بتنشئه بنفسك، زي ما الـ <t color="purple">int</t> والـ <t color="rose">string</t> أنواع بيانات جاهزة.

يعني تقدر ببساطة تعمل متغيرات منه كده (بحيث ان clsperson هو اسم الكلاس):

<hl>clsPerson p1;</hl>

<hl>clsPerson p2;</hl>

### الفرق بين الـ struct والـ class

* الـ **struct**: كان بيشيل متغيرات فقط.
* الـ **class**: يقدر يشيل **متغيرات** (بيانات) بالإضافة إلى **دوال** (سلوكيات).
* و بالمناسبة في فروقات تانية و في استخدامات كمان جوا ال**struct** بس ده مش موضوعنا دلوقتي

<note type="success"> الكلاس بيجمع البيانات والوظائف اللي بتتعامل مع البيانات دي في مكان واحد.</note>

---

### خلينا نبني الكلاس تدريجياً : 

```cpp
class clsPerson 
{
    string FirstName; // بنعرف متغيرات زي ما كنا بنعرفها في الاستراكتشر
    string LastName;  

    string FullName() // بس الجديد هنا انك تقدر تعرف دوال كمان
    {
        return FirstName + " " + LastName;
    }
};

int main() 
{
    clsPerson Person1; 
    Person1.FirstName = "Mohammed"; // ❌ هنا هيطلع Error!
}

```

هنا هيطلع Error لأن فيه قاعدة في C++ بتقول إن أي حاجة جوه الكلاس بتكون **Private** افتراضياً. الكلاس عامل زي الصندوق المقفول، لا يمكن الوصول للي جواه من خارج الكلاس (زي الـ main).

<div class="break"></div>
<divider>استخدام الـ <t color="lime">public:</t></divider>

عشان نسمح للـ <t color="amber">main</t> أو لأي حد بره الكلاس إنه يستخدم الحاجات اللي جواه، لازم نستخدم الكلمة المفتاحية <t color="lime">public:</t>. دي معناها إن كل اللي جاي تحت الكلمة دي مسموح الوصول له من خارج الكلاس.

<card title="💻 الكود النهائي">

```cpp
#include <iostream>
using namespace std;

class clsPerson  {
    int x; // ده هيفضل برايفيت

public: 
    // خصائص (Attributes)
    string FirstName;
    string LastName;
    // وظيفة داخل الكلاس (Method)
    string FullName() {
        return FirstName + " " + LastName;
    }
}; // اياك تنسى السيمي كولون بعد تعريف الكلاسات

int main()  {
    // هنعمل اوبجيكت جديد بقا باستخدام الكلاس 
    clsPerson Person1; 

    // ملء البيانات
    Person1.FirstName = "Mohammed";
    Person1.LastName = "Abu-Hadhoud";
    // استدعاء الدالة اللي جوه الكلاس
    cout << Person1.FullName() << endl;
}

```

</card>

---

<divider>معلومة هامة</divider>

أنواع البيانات اللي إنت متعود عليها زي الـ <t color="teal">int</t> والـ <t color="sky">string</t> هي في الأساس **Classes** في لغة C++.

لما بتعرف <t color="purple">string name;</t> إنت فعلياً بتعمل **Object** من كلاس اسمه <t color="rose">string</t> جاهز في اللغة، والكلاس ده جواه دوال وخصائص زيه زي <t color="amber">clsPerson</t> اللي عملناه بالظبط. إنت الآن بدأت تصمم أنواع بيانات خاصة بيك بدل ما تكتفي باستخدام الأنواع الجاهزة فقط.

--- 

<a id="l-class-members"></a>
<lesson color="sky">Class Members</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثالث: أعضاء الكلاس</h4>

قبل ما نبدأ، ده الكود اللي اشتغلنا عليه الدرس اللي فات عشان نطبق عليه:

```cpp
class clsPerson {
    int x; 

public: 
    string FirstName;
    string LastName;

    string FullName() {
        return FirstName + " " + LastName;
    }
};

```
<div class="break"></div>

<divider>إيه هي الـ Members؟</divider>

أي شيء يتم تعريفه داخل الكلاس (بين القوسين <t color="lime">{ }</t>) يسمى **عضو** أو **Member**. وفي الكلاسات، الأعضاء بينقسموا لنوعين أساسيين:

### ١. أعضاء البيانات (Data Members)

دي المتغيرات اللي بتعرفها جوه الكلاس، وهي اللي بتشيل "بيانات" أو "خصائص" الكائن. في لغات تانية ممكن تسمع عنها باسم **Fields** أو **Attributes**.

في الكود اللي فوق، الـ Data Members هي:

* <t color="teal">x</t>
* <t color="sky">FirstName</t>
* <t color="purple">LastName</t>

### ٢. وظائف الأعضاء (Member Methods / Functions)

دي الدوال اللي بتعرفها جوه الكلاس، وهي اللي بتمثل "سلوك" أو "أفعال" الكائن. في الـ OOP بنحب نسميها **Methods**.

في الكود اللي فوق، الـ Member Method هي:

* <t color="rose">FullName()</t>

---

<note type="success">أي Object هتعمله من الكلاس ده، هيكون له نسخة خاصة به من كل الـ Members دي.</note>

<div class="break"></div>
<a id="l-objects-in-memory"></a>
<lesson color="sky">Objects In Memory</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الرابع: كيف تُخزن الكائنات في الذاكرة؟</h4>

لما بنعرف كائن (Object) من كلاس معين، إحنا بنحجز له مكان في الذاكرة. بس هل كل حاجة جوه الكلاس بتتكرر مع كل كائن جديد؟ الحقيقة لا، وهنا تكمن الفكرة.

<divider>البيانات تختلف, والوظائف واحدة</divider>

تخيل إن عندك كلاس <t color="amber">clsPerson</t> وعملت منه 100 أوبجيكت. إيه اللي بيحصل في الرام؟

1. **البيانات (Data Members)**: كل أوبجيكت بياخد نسخة خاصة بيه تماماً من المتغيرات (<t color="lime">FirstName</t>, <t color="teal">Salary</t>, إلخ). وده منطقي، لأن كل شخص له اسمه وراتبه المختلف.
2. **الدوال (Member Functions)**: <hl color="rose">لا تتكرر!</hl> الـ C++ بتحجز نسخة واحدة فقط من الدالة في الذاكرة، وكل الأوبجيكتات بتشاور على نفس النسخة دي وتستخدمها.

<card title="💡 ليه الدوال مش بتتكرر؟">
لأن كود الدالة ثابت ومش بيتغير من كائن للتاني. دالة <t color="teal">FullName()</t> وظيفتها دايماً هي دمج اسمين؛ فمن الهدر إننا ننسخ نفس الكود 100 مرة في الرام.
</card>

---

<divider>حجم الأوبجيكت في الذاكرة</divider>

 حجم الأوبجيكت بيساوي إيه؟
**حجم الأوبجيكت = مجموع أحجام الـ Data Members فقط.** ( الدكتور مذكرهاش بس حسيت انها معلومة مهمة )

الدوال لا تدخل نهائياً في حساب حجم الأوبجيكت.

```cpp
class clsExample {
    int x;    // 4 bytes
    int y;    // 4 bytes
    void Print() { /* لا تأخذ مساحة من حجم الأوبجيكت */ }
};
// حجم الأوبجيكت هنا هيكون 8 bytes فقط
```

<div class="break"></div>
<a id="l-access-specifiersmodifiers"></a>
<lesson color="sky">Access Specifiers/Modifiers</lesson>


لما بنبني كلاس، بنحتاج نجاوب علي سؤال مهم: **مين المسموح له يشوف أو يعدل على البيانات دي؟**

 في حاجة اسمها <hl color="teal">(Access Specifiers)</hl> المعنى الحرفي : <hl color="teal">محددات الوصول</hl>
 
  عبارة عن  كلمات مفتاحية بنستخدمها عشان ندي "صلاحيات" قراءة أو تعديل لـ <t>Members</t> معينة جوه الكلاس، ونمنعها عن أماكن تانية.

عشان نفهم ده، لازم نعرف الأول مين اللي ممكن يكون عايز يستخدم الـ Members دي؟
عندنا 3 أطراف:

1. <badge type="done">المبرمج داخل الكلاس</badge>: الكود اللي بيتكتب جوه الكلاس نفسه.
2. <badge type="wip">الكلاسات الوارثة</badge>: كلاسات تانية بتاخد نسخة من الكلاس ده (ودي حاجة اسمها الوراثة Inheritance هناخدها بعدين بالتفصيل).
3. <badge type="new">المستخدم خارج الكلاس</badge>: المبرمج اللي بيعمل Object في الـ <hl color="coral">main</hl> وعايز يستخدمه.

---

<h2 style="text-align:center">الأنواع الثلاثة لمحددات الوصول</h2>

بنستخدم المحددات دي عشان نرد على سؤال واحد: **مين له الصلاحية؟**

<defs>
<def term="1. Private (خاص)">

بيخلي الصلاحية للأكواد داخل الكلاس فقط بدون تدخل اي كلاس او فانكشن خارجي
**(بالمناسبة دي الـ Default أو الحالة الافتراضية لأي ميمبر)**.

</def>
<def term="2. Protected (محمي)">
بيخلي الصلاحة جوا الكلاس زي البرايفيت + بيدي الصلاحية كمان لكلاسات تانية اسمها الكلاسات الوارثة - دي كلاسات بتورث تعليمات أو بيانات من كلاسات تانية (مش موضوعنا دلوقتي هنتكلم في باستفاضة بعدين)
</def>
<def term="3. Public (عام)">بيخلي الصلاحية ببساطة متاحة للجميع</def>
</defs>

<card title="💡 ليه أصلاً بخبي حاجات وأعملها Private؟">

تخيل إنك سايق عربية. إنت كـ (مستخدم) مسموح لك تتعامل مع الدريكسيون والفرامل **(Public)**.
لكن هل مسموح لك تفتح الموتور وتلعب في البساتم وانت سايق؟ طبعاً لا الموتور **(Private)**.

إحنا بنخبي الدوال والمتغيرات اللي بتمشي "مهام الكلاس الداخلية" عشان **منزعجش المستخدم بتفاصيل معقدة**، وعشان **نمنعه يبوظ حاجة بالغلط** توقف السيستم.

</card>

#### خلينا نكتب كود بيشمل التلات أنواع ونشوف إزاي بيتعاملوا مع بعض..

### ١. المنطقة المحظورة (Private)

هنعرف متغير ودالة، ومحدش هيقدر يستخدمهم غير الكلاس نفسه.

```cpp
class clsPerson {
private: 
    // مسموح الوصول ليها داخل هذا الكلاس فقط
    int Variable1 = 5;
    int Function1() {
        return 40;
    }
```

### ٢. منطقة الورثة (Protected)

هنا بنجهز حاجات عشان لو كلاس تاني "ورث" الكلاس بتاعنا يقدر يشوفها (تجاهل تفاصيل الوراثة دلوقتي).

```cpp
protected:
    // مسموح الوصول ليها داخل الكلاس والكلاسات الوارثة فقط
    int Variable2 = 100;
    int Function2() {
        return 50;
    }
```
<div class="break"></div>

### ٣. المنطقة العامة (Public)

هنا بنحط الحاجات اللي المستخدم هيتعامل معاها مباشرة في الـ <t>main</t>.

```cpp
public:
    // متاح للجميع (داخل، خارج، وورثة)
    string FirstName;
    string LastName;
    string FullName() {
        return FirstName + " " + LastName;
    }

    // الدالة دي بابليك لكنها بتشتغل كمان زي البرايفيت و البروتيكتيد عادي
    float Function3() {
        return Function1() * Variable1 * Variable2;
    }
};
```

### ٤. الاستخدام في الـ Main

دلوقتي المستخدم هيعمل Object ويتعامل مع المسموح له بس:

```cpp
int main() {
    clsPerson Person1;
    
    // المستخدم قادر يعدل الخصائص الـ Public
    Person1.FirstName = "Mohammed";
    Person1.LastName = "Abu-Hadhoud";
    
    // استدعاء الدوال الـ Public
    cout << "Person1: " << Person1.FullName() << endl;
    
    // Function3 قدرت تشتغل وتجيب نواتج من الـ Private والـ Protected بأمان
    cout << "Result : " << Person1.Function3() << endl;

    // ❌ لو حاولت تكتب Person1.Variable1 هيطلع Error فوراً!
}
```
<div class="break"></div>
<note type="success">

 الخلاصة: الـ Access Modifiers هي بوابات الحماية بتاعتك. اللي عايز الناس تستخدمه خليه <hl>public</hl>، واللي يخص شغل الكلاس الداخلي خبيه في الـ <hl>private</hl>.

 </note>


<br-page></br-page>

</wrap>

<cover><cover-circle color="teal">الخصائص والتغليف</cover-circle></cover>

<br-page></br-page>


<wrap color="teal">

<a id="l-properties-set-and-get"></a>
<lesson color="teal">Properties Set and Get</lesson>

<h4 style="text-align:center;font-size:20px">الدرس السادس: الخصائص (Set & Get)</h4>

<divider>قاعدة جديدة: لا للمتغيرات العامة (Public Variables)</divider>

النهاردة هندخل في واحد من أهم مفاهيم البرمجة الكائنية. من هنا ورايح، في قاعدة مهمة جداً لازم نتبناها: **غلط جداً إنك تسيب متغيرات الكلاس <t>public</t> وتسمح لأي حد يوصلها ويعدلها بحرية** (حتى لو لغة C++ بتسمح بكده).

الصح الاحترافي هو:

1. تخلي كل متغيراتك <t color="lime">private</t>.
2. تعمل دالة لتغيير القيمة بنسميها **Propertie Set**.
3. تعمل دالة لقراءة القيمة بنسميها **Propertie Get**.

<card title=" سؤال منطقي ">
طب ليه الغلبة دي كلها؟ ليه ألغي عمومية المتغيرات , وأقعد أكتب دالتين لكل متغير لمجرد إني أقرأه أو أعدله؟ <div></div>
خلي السؤال ده في دماغك، وهنجاوب عليه بالتفصيل في آخر الدرس .

</card>

---

خلينا نبني الكلاس ونشوف إزاي هنطبق العادات البرمجية الجديدة:

**1. تعريف المتغيرات في المنطقة الخاصة (Private):**
هنبدأ بوضع المتغيرات بعيداً عن أعين المستخدم، وهنستخدم الـ <t color="sky">_</t> كعلامة لينا إن دي متغيرات داخلية.

```cpp
class clsPerson 
{
private:
    string _FirstName; // الـ أندرسكور بتسهل علينا الوصول لمتغيرات البرايفيت داخل الكلاس
    string _LastName;
```
<div class="page-break"></div>

**2. إنشاء بوابة التعديل (Property Set):**
دلوقتي المستخدم في الـ <t color="purple">main</t> ملوش وصول مباشر للمتغيرات، فبنعمله "بوابة" يبعت منها القيمة الجديدة.

```cpp
public:
    void setFirstName(string FirstName) 
    {
        _FirstName = FirstName;
    }
```

**3. إنشاء بوابة القراءة (Property Get):**
وعشان يقدر يقرأ القيمة، بنعمله دالة ترجع له اللي متخزن جوه المتغير الخاص.

```cpp
    string FirstName() 
    {
        return _FirstName;
    }
```

**4. تكرار العملية لباقي الخصائص:**
بنفس المنطق، هنعمل Set و Get للمتغير الثاني <t color="rose">_LastName</t>.

```cpp
    void setLastName(string LastName) 
    {
        _LastName = LastName;
    }

    string LastName() 
    {
        return _LastName;
    }

```
<div class="page-break"></div>

**5. الاستخدام في الـ Main:**
دلوقتي شوف إزاي شكل التعامل مع الأوبجيكت اختلف؛ بقينا بنستخدم "الدوال" بدل "المتغيرات".

```cpp
int main() 
{
    clsPerson Person1;

    // بنستخدم الـ Set عشان نبعت القيمة
    Person1.setFirstName("Mohammed");
    Person1.setLastName("Abu-Hadhoud");

    // بنستخدم الـ Get (نفس اسم الدالة) عشان نسترجع القيمة
    cout << "First Name: " << Person1.FirstName() << endl;
    cout << "Full Name:  " << Person1.FullName() << endl;
}
```

---

<h1 style="text-align:center;">طب وليه الغلبة دي؟ </h1>

دلوقتي نجاوب على السؤال: ليه حولنا المتغيرات لـ <hl>private</hl> وعملنا دوال <hl>public</hl> للوصول والتعديل؟

الفايدة العظيمة هي إنك بتمتلك **التحكم الكامل**؛ إنت دلوقتي واقف "حارس" على البيانات، وبتقدر تعمل حاجات مستحيل تعملها لو المتغير كان <t color="amber">public</t>:

<defs>
<def term="١. سجل التعديلات (Audit Trail)">

في أنظمة البنوك مثلاً، مش عايزين القيمة القديمة تضيع. لما بنستخدم دالة ***Set***، بنقدر قبل ما نغير القيمة نحتفظ بالقيمة القديمة، ونسجل تاريخ التعديل، ومين الموظف اللي عدل. <div></div>
انما لو المتغير Public، القيمة القديمة هتمسح فوراً ومحدش هيعرف مين عمل إيه.

</def>

<def term="٢. التحقق من صحة البيانات (Validation)">

تقدر جوه دالة الـ **Set** تحط شروط (مثلاً: الاسم ميكونش فيه أرقام، أو العمر ميكونش بالسالب). لو البيانات غلط، الدالة بترفض تعدل المتغير وبتحمي البرنامج من الانهيار.

</def>

<def term="٣. الحماية الأمنية (Security)">

ممكن تخلي المتغير <t>للقراءة فقط</t>؛ ببساطة هتعمل دالة Get بس، ومش هتعمل Set. كده إنت ضمنت إن مفيش كود بره الكلاس يقدر يغير القيمة دي أبداً.

</def>
</defs>

<note type="success">✅ الخلاصة: إحنا لغينا الوصول المباشر عشان نحط "نقطة تفتيش" تضمن سلامة وأمن البيانات.</note>

---
<a id="l-read-only-property"></a>
<lesson color="teal">Read Only Property</lesson>

<h4 style="text-align:center;font-size:20px">الدرس السابع: خاصية القراءة فقط</h4>

 ساعات بنحتاج متغيرات في الكلاس تكون "للقراءة فقط"؛ يعني المستخدم يقدر يشوف قيمتها بس مستحيل يقدر يغيرها بعد ما الكائن يتنشئ.

<divider>إزاي بنعمل Read Only؟</divider>

القاعدة بسيطة جداً:

1. بنخلي المتغير <t color="lime">private</t>.
2. بنعمل له دالة **Get** فقط.
3. **مش بنعمل** له دالة Set نهائياً.

بهذه البساطة، أنت قفلت الطريق على أي حد يحاول يعدل القيمة من بره، وفي نفس الوقت سمحت له يقرأها براحته.

---
خلينا نضيف خاصية الـ <t color="teal">ID</t> لكلاس الشخص ونخليها غير قابلة للتعديل:

**1. تعريف الـ ID في المنطقة الخاصة:**
هنفترض إن كل شخص له ID ثابت (زي رقم الهوية)، هنعرفه ونبدره بقيمة ابتدائية.

```cpp
class clsPerson 
{
private:
    int _ID = 10; // رقم تعريف ثابت لا نريد لأحد تغييره
    string _FirstName;
    string _LastName;

```

**2. إنشاء بوابة القراءة (Get) وتجاهل الـ (Set):**
هنا هنعمل دالة ترجع الـ ID.

```cpp
public:
    // خاصية قراءة فقط (Read Only Property)
    int ID() 
    {
        return _ID;
    }

```

**3. باقي الدوال (كما هي):**
المستخدم يقدر يعدل الاسم الأول والأخير عادي، لكن الـ ID "خط أحمر".

```cpp
    void setFirstName(string FirstName) { _FirstName = FirstName; }
    string FirstName() { return _FirstName; }

    void setLastName(string LastName) { _LastName = LastName; }
    string LastName() { return _LastName; }
};

```

**4. التجربة في الـ Main:**

```cpp
int main() 
{
    clsPerson Person1;

    // مسموح نقرأ الـ ID عادي
    cout << "ID: " << Person1.ID() << endl;

    // ❌ محاولة التعديل:
    // Person1.setID(20); -> Error: الدالة غير موجودة أصلاً!
    // Person1._ID = 20;  -> Error: المتغير Private!

    return 0;
}
```
<div class="break"></div>
<a id="l-properties-set-and-get-through-"></a>
<lesson color="teal">Properties Set and Get through "="</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثامن: استخدام الـ Set والـ Get عن طريق علامة "="</h4>

<divider>مقدمة: هل نقدر نجمع بين الأمان والسهولة؟</divider>

الدروس اللي فاتت عرفنا ليه بنخفي المتغيرات ونعملها <t color="sky">private</t>، ونعملها بوابات <t color="purple">Set</t> و <t color="rose">Get</t> عشان نحميها. بس ظهرت مشكلة صغيرة: المبرمجين اشتكوا إن شكل الكود بقى طويل ومزعج!
يعني بدل ما أكتب السطر السهل ده: <t color="amber">Person1.FirstName = "Mohammed";</t>
بقيت مضطر أكتب: <t color="lime">Person1.SetFirstName("Mohammed");</t>

هل في طريقة تخليني أستخدم علامة اليساوي <t color="teal">=</t> السهلة والمريحة للعين، وفي نفس الوقت الكود من جوه يستدعي دوال الـ <t color="sky">Set</t> والـ <t color="purple">Get</t> عشان يحافظ على الحماية؟ الإجابة هي: **أيوة، باستخدام الخصائص (Properties).**

<divider>تطبيق الكود خطوة بخطوة</divider>

هنكتب الكلاس بتاعنا عادي جداً زي ما اتعلمنا، المتغير <t color="rose">private</t> والدوال <t color="amber">public</t>، بس هنضيف سطر واحد سحري:

**1. الكلاس الأساسي (نفس اللي اتعلمناه):**

```cpp
#include <iostream>
using namespace std;

class clsPerson
{
private:
    string _FirstName;

public:
    void SetFirstName(string FirstName) {
        _FirstName = FirstName;
    }

    string GetFirstName() {
        return _FirstName;
    }
```

**2. السطر الجديد:**

هنا بنعرف "متغير وهمي" بيشتغل كـ Property:

```cpp
    __declspec(property(get = GetFirstName, put = SetFirstName)) string FirstName; 
};
```

**3. الاستخدام في الـ Main:**
بص بقى الروقان في الـ <t color="lime">main</t>، إنت مش محتاج تنادي الدوال بنفسك، إنت بتتعامل مع المتغير الوهمي <t color="teal">FirstName</t> كأنه <t color="sky">public</t>:

```cpp
int main()
{
    clsPerson Person1;

    // الطريقة القديمة (شغالة بس طويلة):
    // Person1.SetFirstName("Mohammed");
    // cout << Person1.GetFirstName() << endl;

    // الطريقة الجديدة (نفس الأمان بس أسهل بكتير):
    Person1.FirstName = "Mohammed"; // السطر ده في الخفاء بينادي SetFirstName
    cout << Person1.FirstName;      // السطر ده في الخفاء بينادي GetFirstName
};

```
<divider>إيه السطر ده وبيعمل إيه بالظبط؟</divider>

**ملحوظة صغيرة : الجزء ده مش مهم اوي تقراه لو مش مهتم بكيفية عمله , الشرح الجاي ده مكتوب بواسطة جيميناي.**

بما إن السطر ده شكله يخض شوية، خلينا نفصصه حتة حتة عشان تفهمه 100%:

<br-page></br-page>
الكود هو: 

<syn>

__declspec(property(get = GetFirstName, put = SetFirstName))

 string FirstName;

</syn>

<defs>
<def term="1. __declspec">

دي اختصار لـ **Declaration Specification**. دي مش كلمة من أصل لغة C++، دي "إضافة" عملتها شركة مايكروسوفت عشان تدي أوامر خاصة للمترجم (Compiler) بتاعها. هنا إحنا بنقول للمترجم: "ركز معايا أنا هعرف لك حاجة بمواصفات خاصة".

</def>

<def term="2. (property(...))">

المواصفات الخاصة دي هي إننا عايزين نعمل **Property** (خاصية). الخاصية دي بتمثل "كوبري" بين المتغير الـ private والدوال الـ public.

</def>

<def term="3. get = GetFirstName">

هنا بنقول للمترجم: لما حد يحاول يقرأ أو يطبع الخاصية دي، متديلوش قيمة مباشرة، لكن **روح استدعي دالة <t color="sky">GetFirstName</t>** وهات الناتج بتاعها.

</def>

<def term="4. put = SetFirstName">

كلمة <t color="purple">put</t> هنا معناها "وضع" أو "تعيين" (زي الـ Set). بنقول للمترجم: لما حد يكتب علامة <t color="rose">=</t> ويحاول يحط قيمة في الخاصية دي، **روح استدعي دالة <t color="amber">SetFirstName</t>** وابعتلها القيمة دي.

</def>

<def term="5. string FirstName;">

ده **الاسم الوهمي** اللي المبرمج هيستخدمه في الـ <t color="lime">main</t>، ونوعه <t color="teal">string</t>. ده مجرد "واجهة" (Interface). لما تستخدمه، هو بيترجم لاستدعاء الدوال اللي حددناها فوق.

</def>
</defs>

<card title="💡 الخلاصة ببساطة">
إنت عملت متغير مزيف اسمه <t color="sky">FirstName</t>.
لما بتكتب <t color="purple">Person1.FirstName = "Mohammed"</t>، المترجم بياخد السطر ده ويمسحه في الخفاء، ويكتب مكانه <t color="rose">Person1.SetFirstName("Mohammed")</t>.
إنت كده كسبت سهولة القراءة والكتابة، وكسبت أمان وسيطرة الـ Set والـ Get!
</card>

<div class="page-break"></div>
<divider>⚠️ تنبيه هام ⚠️</divider>

<note type="warn">

الموضوع ده بنشرحه **من باب العلم بالشيء** فقط!
السطر ده اللي بيبدأ بـ <t color="amber">__declspec</t> هو اختراع خاص بـ **Microsoft Visual Studio** ولأنظمة **ويندوز** فقط.
لو أخدت الكود ده وحاولت تشغله على نظام Linux، أو Mac، أو استخدمت مترجم تاني زي GCC أو Clang، **الكود هيضرب Error ومش هيشتغل**.

</note>

<note>

لغة C++ القياسية (Standard C++) مفيهاش خصائص مدمجة (Properties) زي لغة C# مثلاً. عشان كده، المبرمجين المحترفين في C++ بيفضلوا دايماً يستخدموا دوال الـ <t>Set</t> والـ <t>Get</t> العادية عشان الكود بتاعهم يشتغل على أي جهاز وأي نظام تشغيل بدون مشاكل.

</note>

<div class="break"></div>
<a id="l-first-principle-of-oop-encapsulation"></a>
<lesson color="teal">First Principle of OOP: Encapsulation</lesson>

<h4 style="text-align:center;font-size:20px">الدرس التاسع: المبدأ الأول - الكبسلة (Encapsulation)</h4>

<divider>أهلاً بك في المبادئ الأربعة العظيمة</divider>

البرمجة الكائنية (OOP) كلها مبنية على 4 عواميد أو مبادئ أساسية. لو فهمتهم، إنت كده شربت الـ OOP.

 النهاردة هناخد أول وأهم عمود فيهم، وهو الـ **Encapsulation** (الكبسلة أو التغليف).

الحلو في الموضوع إنك فعلياً **طبقت المبدأ ده بإيدك** في الدروس اللي فاتت، إحنا النهاردة بس هنديله اسمه العلمي ونفهم فلسفته.

<divider>يعني إيه Encapsulation وليه اتسمت كده؟</divider>

كلمة Encapsulation جاية من كلمة **Capsule** (كبسولة الدواء).

تخيل كبسولة الدوا اللي بتشتريها من الصيدلية؛ الكبسولة دي من جواها فيها بودرة ومواد كيميائية متفاعلة مع بعض (دي البيانات والتفاصيل المعقدة). لكن من بره، المادة الفعالة دي متغلفة بغلاف ناعم وبسيط. إنت كمريض (مستخدم) بتبلع الكبسولة زي ما هي عشان تخف، من غير ما تضطر تفتحها وتتعامل مع المواد الكيميائية اللي جواها وتوجع دماغك بنسب الخلط.

الـ Encapsulation في البرمجة بيعمل نفس الفكرة بالظبط، وبيتكون من شقين:

1. **التجميع (Bundling):** تجميع البيانات (Data) والدوال اللي بتشغل البيانات دي (Methods) في مكان واحد مقفول عليهم، اللي هو الـ **Class**.
2. **الإخفاء والحماية (Data Hiding):** إننا نخفي التفاصيل المعقدة والبيانات الحساسة جوه الكبسولة (باستخدام الـ <t color="purple">private</t>)، ونسمح للمستخدم يتعامل معاها من بره عن طريق "واجهة بسيطة" ومحكومة (باستخدام الـ <t color="rose">public</t> زي دوال الـ Set والـ Get).


<divider>إحنا ليه بنعمل كده أصلاً؟</divider>

لو تفتكر في أول درس خالص، إحنا اتفقنا إننا بنبص للعالم على إنه مجموعة "كائنات" (Objects)، وكل كائن له:

* **صفات (Attributes)**: زي لونه، وزنه، اسمه.
* **سلوكيات (Behaviors)**: زي إنه بيتحرك، بياكل، بيحسب راتبه.

زمان قبل الـ OOP، كان المبرمجين بيكتبوا المتغيرات (الصفات) في حتة، والدوال (السلوكيات) في حتة تانية خالص في البرنامج، والدنيا بتسيح على بعضها وكل دالة تقدر تلعب في أي متغير.

لكن المبدأ بتاع الـ Encapsulation جه قالك: **لأ!**
بما إن "الاسم" و "الراتب" يخصوا كائن "الموظف"، وبما إن دالة "حساب الضريبة" بتشتغل على راتب الموظف ده، يبقى نلمهم كلهم ونحطهم جوه كبسولة واحدة اسمها <t color="amber">clsEmployee</t>.
أي حاجة تخص الموظف هتفضل مقفول عليها جوه الكلاس بتاعه، ومفيش أي كود من بره يقدر يتدخل في بياناته إلا بالاستئذان (عن طريق الدوال العامة اللي إحنا سامحين بيها).

<card title=" الخلاصة ">
الـ <b>Encapsulation</b> هو إنك تبني "صندوق أسود" (الكلاس). جوا الصندوق ده إنت لامم المتغيرات والدوال اللي بتخدم على بعض، وقافل عليهم بقفل (Private). ومطلع من الصندوق ده زراير بسيطة (Public) عشان اليوزر يدوس عليها ويشغل الصندوق من غير ما يبوظ التروس اللي جوه.
</card>

---

<note type="success">✅ إنت كده فهمت أول مبدأ من مبادئ الـ OOP. إنت بتطبقه في كل مرة بتعمل فيها كلاس وتحط داتا private وتعملها Getters و Setters.</note>


<div class="break"></div>
<a id="l-second-principle-of-oop-abstraction"></a>
<lesson color="teal">Second Principle of OOP: Abstraction</lesson>

<h4 style="text-align:center;font-size:20px">الدرس العاشر: المبدأ الثاني - التجريد (Abstraction)</h4>

<divider>يعني إيه Abstraction؟</divider>

مبدأ التجريد أو الـ **Abstraction** هو المبدأ التاني من المبادئ الأربعة للـ OOP، وهو مبدأ مفيد جداً ومريح لأقصى درجة.
ببساطة، الـ Abstraction هو فكرة **إظهار الأشياء المهمة فقط للمستخدم، وإخفاء كل التفاصيل المعقدة اللي مالهاش لازمة بالنسبة له.**

---

<divider>مثال عملي من حياتنا: كاميرا الموبايل</divider>

عشان نفهم الفكرة صح، تخيل إنك ماسك موبايلك وعايز تاخد صورة لشخص. إنت بتعمل إيه؟ بتفتح الكاميرا وتضغط على "زرار" واحد بس عشان الصورة تتلقط.

لكن هل سألت نفسك الزرار ده بيعمل إيه ورا الكواليس؟
الزرار ده فعلياً بيمثل "دالة" (Function) بتشغل مجموعة كبيرة جداً من الدوال التانية المعقدة جداً، زي مثلاً:

* دالة بتضبط العدسة (Focus).
* دالة بتضبط الإضاءة (Exposure).
* دالة بتلقط الألوان.
* دالة بتعالج الصورة (Processing).
* دالة بتحفظ الصورة في الذاكرة.

كل دي دوال شغالة في الخلفية عشان تدعم عمل دالة التقاط الصورة، بس الشركة المصنعة للموبايل "خبت" عنك كل ده، وطلعتلك واجهة بسيطة فيها زرار واحد بس اسمه **<t color="lime">TakePhoto</t>**.

<br-page></br-page>

<divider>ليه بنخبي التفاصيل دي؟</divider>

وإحنا بنكتب الكلاس بتاعنا، ليه بنخفي مثلاً الـ 10 دوال المساعدة دي ونخلي دالة واحدة بس هي اللي ظاهرة للمستخدم في الـ <t color="teal">public</t>؟

<defs>
<def term="١. الأمان (Security)">

أكيد إحنا مش عايزين حد يتدخل في العمليات الداخلية المعقدة ويبوظها بالغلط، بس في الحقيقة <t color="rose">مش ده السبب الرئيسي للـ Abstraction</t> .

</def>
<def term="٢. تسهيل الحياة">

السبب الجوهري هو إننا <hl color=lime>مش عايزين نوجع دماغك</hl>
إنت كمستخدم للكلاس (أو المبرمج اللي هيجي يشتغل على الكود بعدك) مش هتستفاد أي حاجة لو ظهرتلك 10 دوال مختلفة ومطلوب منك تناديهم بترتيب معين عشان تاخد صورة. إنت عايز "الخلاصة".

</def>
</defs>

إحنا بنسهل حياة المبرمج؛ بنخلي كل الدوال المعقدة دي <t color="sky">private</t> تشتغل جوه الكلاس بس وتخدم على بعضها، وبنعمل **تجريد (Abstraction)** للعملية دي كلها في دالة واحدة بس <t color="purple">public</t> هي اللي هتفيدك وتعملك المطلوب بضغطة واحدة.

<card title="الخلاصة">

* الـ <b>Encapsulation</b> (الدرس اللي فات): كان هدفه "تجميع" البيانات والدوال في كبسولة وحمايتهم.
* الـ <b>Abstraction</b> (درس النهاردة): هدفه "تبسيط" الواجهة اللي بتتعامل معاها، وإخفاء "وجع الدماغ" والتعقيد الداخلي عنك.

</card>


<br-page></br-page>
#### بمناسبة كود الآلة الحاسبة , ده الحل بتاعي ابقى بص عليه
```cpp
#include <iostream>
#include <string>
using namespace std;

class clsCalculator {
    double _CurrentResult = 0.0; 
    double _PreviousResult = 0.0;
    string _MyLastChange = "nothing";

public:
    void PrintResult() {
        cout << "The Result after " + _MyLastChange << " is : " << _CurrentResult << endl;
    }
    void CancelLastOp() {
        _CurrentResult = _PreviousResult;
        _MyLastChange = "Cancelling";
    }
    void Clear() {
        _CurrentResult = 0.0;
        _MyLastChange = "Clearing";
    }
    // --------- Ops ----------
    void Add(double newNumber) {
        _PreviousResult = _CurrentResult;
        _CurrentResult += newNumber;
        _MyLastChange = "Adding " + to_string(newNumber);
    }
    void Subtract(double newNumber) {
        _PreviousResult = _CurrentResult;
        _CurrentResult -= newNumber;
        _MyLastChange = "Subtracting " + to_string(newNumber);
    }
    void Multiply(double newNumber) {
        _PreviousResult = _CurrentResult;
        _CurrentResult *= newNumber;
        _MyLastChange = "Multiplying by " + to_string(newNumber);
    }
    void Divide(double newNumber) {
        _PreviousResult = _CurrentResult;
        if (newNumber == 0) {
            newNumber = 1; 
            cout << "Division by zero is prohibited." << endl;
        } // هنا حالة القسمة علي الصفر اللي الدكتور قال عليها

        _CurrentResult /= newNumber;
        _MyLastChange = "Divide by " + to_string(newNumber);
    }
};
int main() {
    clsCalculator Calculator1;
    Calculator1.Clear();
    Calculator1.Add(10);
    Calculator1.PrintResult();
    Calculator1.Add(100);
    Calculator1.PrintResult();
    Calculator1.Subtract(20);
    Calculator1.PrintResult();
    Calculator1.Divide(0);
    Calculator1.PrintResult();
    Calculator1.Divide(2);
    Calculator1.PrintResult();
    Calculator1.Multiply(3);
    Calculator1.PrintResult();
    Calculator1.CancelLastOp();
    Calculator1.PrintResult();
    Calculator1.Clear();
    Calculator1.PrintResult();
}
```

<br-page></br-page>

</wrap>

<cover><cover-circle color="gold">Constructors & Memory</cover-circle></cover>

<br-page></br-page>


<wrap color="gold">

<a id="l-constructors"></a>
<lesson color="gold">Constructors</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الحادي عشر: الكونستراكتور (Constructors)</h4>

في الدروس اللي فاتت كنا بنعمل الكائن (Object) الأول، وبعدين نفضل نستخدم دوال الـ <t color="rose">Set</t> عشان نديله البيانات بتاعته واحدة واحدة. لكن أحياناً بنبقى عايزين الكائن ده يتولد "جاهز" ببياناته الأساسية، أو بمعنى أصح، عايزين **نجبر** المستخدم إنه يدخل البيانات دي لحظة إنشاء الكائن ومينفعش يكريته وهو فاضي. هنا بيجي دور الـ **Constructor**.

---

<divider>المشكلة: كائن فارغ بدون هوية</divider>

عشان نفهم الفكرة، خلينا نكتب كلاس <t color="amber">clsAddress</t> اللي بيخزن بيانات العنوان، بس من غير الكونستراكتور، ونشوف إيه المشكلة اللي هتقابلنا:
*(ملاحظة: دمجنا <t color="lime">AddressLine1</t> و <t color="teal">AddressLine2</t> في متغير واحد <t color="sky">_AddressLine</t> للتبسيط).*

```cpp
#include <iostream>
using namespace std;

class clsAddress{
private:
    string _AddressLine;
    string _POBox;
    string _ZipCode;

public:
    // دوال الـ Set والـ Get
    void SetAddressLine(string AddressLine) { _AddressLine = AddressLine; }
    string AddressLine() { return _AddressLine; }

    void SetPOBox(string POBox) { _POBox = POBox; }
    string POBox() { return _POBox; }

    void SetZipCode(string ZipCode) { _ZipCode = ZipCode; }
    string ZipCode() { return _ZipCode; }
    // دالة الطباعة
    void Print(){
        cout << "\nAddress Details:\n";
        cout << "_____________________";
        cout << "\nAddressLine : " << _AddressLine << endl;
        cout << "POBox       : " << _POBox << endl;
        cout << "ZipCode     : " << _ZipCode << endl;
    }
};

int main()
{
    // أنشأنا الكائن بدون ما نديله أي بيانات
    clsAddress Address1; 
    // لو طبعنا دلوقتي، إيه اللي هيحصل؟
    Address1.Print(); 
}

```
<out>
Address Details:
_____________________
AddressLine : 
POBox       : 
POBox       :
ZipCode     : 
</out>

<note type="warn">

**فين المشكلة هنا؟**
لو شغلت الكود ده، دالة <t>Print</t> هتطبعلك قيم فاضية (Empty Strings)! 
في أنظمة كتير، ده يعتبر "عيب برمجي". مش صح إنك تسمح للمستخدم يعمل عنوان فاضي ملوش ملامح وبعدين ينسى يعبيه بالبيانات. الأصح إننا **نجبره** يمرر المتغيرات دي <b>لحظة عمل الكلاس على طول</b>.

</note>

---

<divider>الحل: يعني إيه Constructor؟</divider>

كلمة **Construction** في الإنجليزي معناها "بناء"، و **Constructor** معناها "البنّاء".

في البرمجة، الكونستراكتور ده عبارة عن **دالة (Function) مميزة جداً**، وظيفتها إنها "تبني" الكائن وتجهزه لحظة ولادته. الدالة دي فيها شوية شروط بتميزها عن أي دالة تانية:

1. **الاستدعاء الإجباري:** بتشتغل أوتوماتيك (إجباري) لحظة إنشاء الكائن (Object).
2. **الاسم المطابق:** لازم يكون اسمها **نفس اسم الكلاس بالظبط**، حرف بحرف.
3. **بدون نوع إرجاع:** الدالة دي مش بترجع أي حاجة، ولا حتى بنكتب قبلها <t color="purple">void</t>.

<card title="💡 الـ Default Constructor (الكونستراكتور الافتراضي)">
لو إنت معملتش كونستراكتور بإيدك (زي الكود اللي فوق)، لغة C++ بتعملك واحد "مخفي" وفاضي بيسموه <b>Default Constructor</b>، وده اللي بيخليك تقدر تكتب <t color="lime">clsAddress Address1;</t> من غير ما يديك إيرور. بس بمجرد ما إنت تعمل كونستراكتور خاص بيك بياخد باراميترات، الكونستراكتور المخفي ده بيتلغي، ولازم المستخدم يلتزم باللي إنت عملته.
</card>

---

<divider>التطبيق: استخدام الكونستراكتور</divider>

دلوقتي هنكتب الكود تاني ، بس المرة دي هنحط "البنّاء" بتاعنا (دالة <t color="rose">clsAddress</t> اللي بتاخد باراميترات) عشان نجبر المستخدم يبعت البيانات:

```cpp
#include <iostream>
using namespace std;

class clsAddress {
private:
    string _AddressLine;
    string _POBox;
    string _ZipCode;

public:
    // ⬇️ ده هو الكونستراكتور (البنّاء) ⬇️
    clsAddress(string AddressLine, string POBox, string ZipCode) {
        _AddressLine = AddressLine;
        _POBox = POBox;
        _ZipCode = ZipCode;
    }
    void SetAddressLine(string AddressLine) { ... }
    string AddressLine() { ... }

    void SetPOBox(string POBox) { ... }
    string POBox() { ... }

    void SetZipCode(string ZipCode) { ... }
    string ZipCode() { ... }
    void Print(){ ... }
};

int main() {
    // بنمرر البيانات بين قوسين لحظة تعريف الكائن (اجباريا)
    clsAddress Address1("Queen Alia Street", "11192", "5555");
    // دلوقتي لو طبعت، الكائن جاهز وبياناته مظبوطة 
    Address1.Print();
}

```

<note type="success"> **الخلاصة:** الكونستراكتور هو الطريقة الاحترافية عشان نضمن إن أي كائن (Object) هيتولد في البرنامج بتاعنا، هيكون معاه البيانات الأساسية بتاعته من أول لحظة، ومفيش مجال للنسيان أو الخطأ.</note>

<br-page></br-page>
<a id="l-copy-constructors"></a>
<lesson color="gold">Copy Constructors</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثاني عشر: نسخ الكائنات (Copy Constructor)</h4>

<divider>المشكلة: التكرار الممل</divider>

تخيل إنك عملت كائن (Object) اسمه <t color="amber">Address1</t> ومليته ببيانات كتير (الشارع، رقم العمارة، صندوق البريد، إلخ). بعد شوية، احتجت تعمل كائن جديد <t color="lime">Address2</t> بس عايزه ياخد **نفس بيانات** <t color="teal">Address1</t> بالظبط.
هل من المنطقي إنك ترجع تمرر نفس القيم الطويلة دي تاني للكونستراكتور؟ أكيد لأ.

---

<divider>الحل: الـ Copy Constructor</divider>

الحل ببساطة إننا وقت ما بننشئ الكائن الجديد، نساويه بالكائن القديم على طول بالشكل ده:
<t color="sky">clsAddress Address2 = Address1;</t>

عشان السطر ده يشتغل بطريقتنا الخاصة، بنعمل دالة بتبني الكائن الجديد عن طريق إنها "تنسخ" بيانات كائن قديم مبعوت لها. الدالة دي اسمها **Copy Constructor**.

هنا بيظهر مفهوم مهم أخدناه قبل كده **Function Overloading (تعدد الدوال)**:
إحنا دلوقتي بقى عندنا في الكلاس "اتنين" كونستراكتور بنفس الاسم (<t color="purple">clsAddress</t>):

1. واحد بياخد نصوص عادية (Strings).
2. والتاني بياخد كائن كامل (Object) من نفس نوع الكلاس.
الـ Compiler ذكي، ولما بتيجي تنشئ الكائن بيشوف إنت باعت إيه وبناءً عليه بيقرر يشغل أي واحد فيهم.

<br-page></br-page>

#### بص على الكود بعد ما ضفنا الـ Copy Constructor:

```cpp
#include <iostream>
using namespace std;

class clsAddress
{
private:
    string _AddressLine1;
    string _AddressLine2;
    string _POBox;
    string _ZipCode;

public:
    clsAddress(string AddressLine1, string AddressLine2, string POBox, string ZipCode){
        _AddressLine1 = AddressLine1;
        _AddressLine2 = AddressLine2;
        _POBox = POBox;
        _ZipCode = ZipCode;
    }

    // الكونستراكتور الناسخ (Copy Constructor)
    // بنستقبل الأوبجيكت القديم كـ Reference (&) 
    clsAddress(clsAddress & old_obj){
        _AddressLine1 = old_obj.AddressLine1();
        _AddressLine2 = old_obj.AddressLine2();
        _POBox = old_obj.POBox();
        _ZipCode = old_obj.ZipCode();
    }

    void SetAddressLine1(string AddressLine1) { ... }
    string AddressLine1() { ... }
    
    void SetAddressLine2(string AddressLine2) { ... }
    string AddressLine2() { ... }
    
    void SetPOBox(string POBox) { ... }
    string POBox() { ... }
    
    void SetZipCode(string ZipCode) { ... }
    string ZipCode() { ... }

    void Print() { ... }
};

int main()
{
    // إنشاء الكائن الأول (هنا هيستدعي الكونستراكتور الأساسي)
    clsAddress Address1("Queen Alia Street", "B 303", "11192", "5555");
    Address1.Print();

    // إنشاء الكائن التاني ونسخ الأول فيه (هنا هيستدعي الـ Copy Constructor)
    clsAddress Address2 = Address1;
    Address2.Print();

    system("pause>0");
    return 0;
}

```

---

<divider>⚠️ معلومة مهمة ⚠️</divider>

<note type="warn">

<hl color=amber>هل كتابة الـ Copy Constructor ضرورية دايماً؟</hl>
في الأساس: <hl>لأ، مش ضروري تكتبه بإيدك!</hl>
لغة C++ بتعملك واحد افتراضي (Default Copy Constructor) في الخفاء، بيقوم بنسخ كل المتغيرات من الكائن القديم للجديد أوتوماتيك، والكود كان هيشتغل من غيره عادي جداً.
<hl color="red">أومال بنتعلمه ليه؟</hl>
لازم تكون فاهمه كويس جداً وتعرف إزاي تعمله بإيدك، لأنك قدام لما تتعامل مع الـ (Pointers) والـ (Dynamic Memory Allocation)، الكونستراكتور الافتراضي بتاع C++ هيعملك مشاكل وكوارث (حاجة اسمها Shallow Copy)، وساعتها هتبقى <hl color=rose>مُجبر</hl> تكتب الـ Copy Constructor بنفسك عشان تحل المشكلة دي.

</note>

<div class="break"></div>
<a id="l-destructors"></a>
<lesson color="gold">Destructors</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثالث عشر: الهادم (Destructor)</h4>

<divider>الهادم vs البنّاء</divider>

لو كان الـ **Constructor** هو "شهادة الميلاد" للكائن، فالـ **Destructor** هو "شهادة الوفاة". هو دالة خاصة بتشتغل أوتوماتيك أول ما الأوبجيكت يخلص مهمته ويتحذف من الذاكرة.

<note type="remember">

<hl color=lime>قاعدة مهمة:</hl>
على عكس الكونستراكتور اللي ممكن تعمل منه كذا نسخة (Overloading)، الـ Destructor <t color=rose>مستحيل يكون منه غير واحد بس</t> في الكلاس، ومبياخدش أي باراميترات، فبالتالي ملوش Overloading.

</note>

---

<divider>الكود وتجربة الحياة والموت</divider>

بص على الكود ده، هنشوف فيه طريقتين لموت الأوبجيكت؛ واحدة "طبيعية" بمجرد انتهاء الدالة، وواحدة "يدوية" لما بنستخدم الـ Pointer:

```cpp
#include <iostream>
using namespace std;

class clsPerson
{
public:
    string FullName;

    // Constructor: بيشتغل أول ما الأوبجيكت يتبني
    clsPerson()
    {
        FullName = "Mohammed Abu-Hadhoud";
        cout << "\nHi, I'm Constructor";
    }




    // Destructor: بيشتغل أول ما الأوبجيكت يتم تدميره
    // لاحظ علامة (~) قبل الاسم
    ~clsPerson()
    {
        cout << "\nHi, I'm Destructor";
    }
};

void Fun1()
{
    // أوبجيكت عادي (Automatic Object)
    clsPerson Person1;
} // بمجرد الخروج من القوس ده، Person1 بيتدمر أوتوماتيك

void Fun2()
{
    // أوبجيكت محجوز في الـ Heap (Dynamic Object)
    clsPerson* Person2 = new clsPerson;

    // لازم نستخدم delete يدويًا عشان نمسحه من الذاكرة
    // أول ما نكتب السطر ده، الـ Destructor هيشتغل فورًا
    delete Person2;
}

int main()
{
    cout << "--- Calling Fun1 ---";
    Fun1(); 

    cout << "\n\n--- Calling Fun2 ---";
    Fun2();

    cout << "\n\nMain Ended.";
    system("pause>0");
    return 0;
}

```

---

<divider>شرح لما يحدث خلف الكواليس</divider>

في الكود اللي فات، إنت شوفت حالتين لموت الكائن، ودول أهم حاجتين لازم تفهمهم في تعامل الـ Destructor مع الذاكرة:

<defs>
<def term="١. الموت التلقائي (Stack)">

في <t color="teal">Fun1</t>، بمجرد ما الدالة بتخلص، الـ C++ بتنضف الـ Stack وبتمسح أي أوبجيكت اتعمل جواه. هنا الـ Destructor بيشتغل لوحده من غير تدخلك.

</def>
<def term="٢. الموت اليدوي (Heap)">

في <t color="sky">Fun2</t>، إحنا استخدمنا كلمة <t color="purple">new</t>. الأوبجيكت ده بيفضل "عايش" في الذاكرة حتى لو الدالة خلصت! وعشان كدة <b>إجباري</b> تستخدم <t color="rose">delete</t>. لو نسيتها، الـ Destructor مش هيشتغل أبدًا، وهتفضل الذاكرة محجوزة (وده اللي بنسميه Memory Leak).

</def>
</defs>

---

<divider>متى نحتاج فعلياً لكتابة الـ Destructor؟</divider>

في الأغلب، لو الكلاس بتاعك فيه متغيرات عادية (int, string)، مش هتحتاج تكتب Destructor لأن لغة C++ بتعرف تنضفهم لوحدها. لكن بنحتاجه في حالات معينة:

* **حجز ذاكرة يدوي:** لو الكونستراكتور بيحجز مساحة باستخدام <t color="rose">new</t> لـ Pointer جوه الكلاس، لازم الـ Destructor هو اللي يعمل <t color="amber">delete</t>.
* **فتح ملفات:** لو الكلاس بيفتح ملف نصي، بنستخدم الـ Destructor عشان نتأكد إن الملف اتقفل أياً كان اللي حصل في البرنامج.
* **قواعد البيانات:** لقفل الاتصال بالسيرفر (Connection) بمجرد انتهاء عمل الكائن.

<note type="success"> <b>الخلاصة:</b> الـ Destructor هو "عامل النظافة" الخاص بالأوبجيكت، بيضمن إن برنامجك مبيستهلكش ذاكرة على الفاضي، وموجود منه نسخة واحدة بس لكل كلاس.</note>

<div class="break"></div>
<a id="l-static-members"></a>
<lesson color="gold">Static Members</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الرابع عشر: الأعضاء الساكنة (Static Members)</h4>

<divider>المفهوم الأساسي</divider>

العضو العادي في الكلاس (Non-static) بيتم تكراره مع كل كائن (Object) بتعمله، يعني كل كائن عنده نسخته الخاصة من المتغيرات.
أما الـ **Static Member**، فهو متغير "مشترك" بين كل الكائنات. هو مكان واحد بس في الذاكرة، الكل بيقرأ منه والكل بيعدل فيه.

---

<divider>شرح الكود خطوة بخطوة</divider>

### ١. تعريف المتغيرات داخل الكلاس

هنبدأ بتعريف الكلاس ونحط فيه نوعين من المتغيرات: واحد عادي (<t> var </t>) وواحد ساكن (<t>counter</t>).

```cpp
class clsA
{
public:
    int var;          // متغير عادي: كل أوبجيكت هيكون ليه var خاصة بيه في الذاكرة.
    static int counter; // متغير ساكن: الذاكرة هتحجز مكان واحد بس لـ counter لكل الأوبجيكتات.

    clsA()
    {
        // بما إن counter مشترك، فكل ما كائن جديد يتولد (الكونستراكتور يشتغل)
        // هيزود نفس المكان في الذاكرة بمقدار 1.
        counter++;
    }
    
    void Print() { ... }
};
```

---

### ٢. خطوة الـ Initialization (مهمة جداً)

في C++، المتغير الـ <t color="lime">static</t> لازم "يتعرف" ويأخد قيمة ابتدائية بره الكلاس، وإلا الكود مش هيشتغل.
#### بنكتب النوع، بعدين اسم الكلاس، بعدين ( :: )، بعدين اسم المتغير

```cpp
int clsA::counter = 0; 
```

---

### ٣. إنشاء الكائنات والتعامل مع المتغيرات

دلوقتي لما نعمل 3 كائنات، الـ <t color="teal">var</t> هتتكرر 3 مرات، لكن الـ <t color="sky">counter</t> هيفضل واحد بس وقيمته هتزيد مع كل ولادة كائن جديد.

```cpp
int main()
{
    clsA A1, A2, A3; // هنا counter بقى = 3 لأن الـ Constructor اشتغل 3 مرات.

    A1.var = 10;
    A2.var = 20;
    A3.var = 30;

    A1.Print();
    A2.Print();
    A3.Print();
```
<out>
var = 10      counter = 3
var = 20      counter = 3
var = 30      counter = 3
</out>

---

<br-page></br-page>
### ٤. إثبات أن المتغير "مشترك"

أقوى دليل على إن الـ <t color="purple">static</t> مشترك هو إننا نغير قيمته من كائن واحد، ونشوف هيحصل إيه في الباقيين:

```cpp
    // لو غيرنا counter من خلال A1 فقط
    A1.counter = 500; 

    cout << "\nAfter changing counter in A1:\n";
    
    A1.Print(); 
    A2.Print();  
    A3.Print(); 
}
```
<out>
var = 10      counter = 500
var = 20      counter = 500
var = 30      counter = 500
</out>
---

<divider>نقاط هامة للفهم</divider>

<defs>
<def term="١. مكان التخزين">

المتغير الـ <t color="amber">static</t> مش بيعيش جوه الأوبجيكت، هو بيتحجز في مكان خاص في الذاكرة أول ما البرنامج يبدأ وقبل حتى ما تعمل أول أوبجيكت.

</def>
<def term="٢. الوصول المباشر">

بما إنه مشترك، إنت تقدر توصله عن طريق اسم الكلاس مباشرة حتى لو مفيش اي أوبجيكت! يعني ينفع تكتب <t color="lime">clsA::counter = 10;</t> في أي مكان.

</def>
</defs>

<div class="break"></div>
<a id="l-static-methods"></a>
<lesson color="sky">Static Methods</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الخامس عشر: الدوال الساكنة (Static Methods)</h4>

<divider>المفهوم الأساسي</divider>

زي ما عرفنا إن المتغير الـ **Static** بيكون مشترك بين كل الكائنات، الـ **Static Method** هي دالة بتخص "الكلاس نفسه" مش بتخص "كائن معين".

الفرق الجوهري إنك تقدر تستدعي الدالة دي من غير ما تعمل أي أوبجيكت أصلاً! هي موجودة ومتاحة بمجرد تشغيل البرنامج لأنها مرتبطة باسم الكلاس.

---

<divider>شرح الكود خطوة بخطوة</divider>

### ١. تعريف الدالة داخل الكلاس

بص على الفرق في التعريف بين الدالة العادية والدالة الساكنة:

```cpp
class clsA 
{
public:
    // دالة ساكنة: مش محتاجة أوبجيكت عشان تشتغل
    static int Function1()
    {
        return 10;
    }

    // دالة عادية: لازم تعمل أوبجيكت عشان تقدر تناديها
    int Function2()
    {
        return 20;
    }
};

```

---

### ٢. الاستدعاء عن طريق اسم الكلاس 

دي الميزة الأكبر؛ تقدر تنادي الدالة باستخدام اسم الكلاس مباشرة ونقطتين فوق بعض (<t>::</t>).

```cpp
int main()
{   
    // نادينها مباشرة من الكلاس.. مفيش أوبجيكت في السطر ده!
    cout << clsA::Function1() << endl; 

    // ❌ السطر اللي جاي ده هيديك ايرور لو حاولت تعمله:
    // cout << clsA::Function2() << endl; 
}

```

---

### ٣. الاستدعاء عن طريق الأوبجيكت

رغم إنها بتخص الكلاس، إلا إن لغة C++ بتسمح لك برضو تناديها من خلال الأوبجيكت عادي، بس ده مش الاستخدام الشائع لها.

```cpp
    clsA A1, A2;

    cout << A1.Function1() << endl; // ✅ شغالة تمام (بس الأفضل تناديها باسم الكلاس)
    cout << A1.Function2() << endl; // ✅ دي لازم تتنادى بالأوبجيكت حصراً

```

---

<divider>قيود هامة جداً</divider>

بما إن الدالة الـ **Static** ممكن تشتغل من غير أوبجيكت، فهي عندها شوية "ممنوعات":

<defs>
<def term="١. لا تلمس المتغيرات العادية">

الدالة الـ <t color="teal">static</t> مقدرش تستخدم جواها أي متغير <b>غير ساكن</b> (Non-static variable)، لأن المتغيرات العادية محتاجة أوبجيكت وهي شغالة من غيره.

</def>
<def term="٢. الوصول للـ Static فقط">

الدالة الـ <t color="sky">static</t> تقدر تتعامل "فقط" مع متغيرات <t color="purple">static</t> تانية أو تنادي دوال <t color="rose">static</t> زيها.

</def>
</defs>

---

<divider>متى نستخدمها؟</divider>

بنستخدمها في الدوال "الخدمية" (Utility Functions) اللي مش محتاجة تخزن بيانات جوه الكلاس، زي:

* دالة بتجمع رقمين.
* دالة بتحول نص من صغير لكبير.
* تخيل عندك كلاس اسمه clsValidation وظيفته بس يتأكد هل الإيميل صح؟ هل الرقم بين 1 و 100؟ دي وظائف "خدمية" مش محتاجة تخزن بيانات جوه الكلاس.
```cpp
if (clsValidation::IsNumberBetween(50, 1, 100)) {
    // كود التنفيذ
}
```

<note type="success">✅ <b>الخلاصة:</b> الـ Static Method هي دالة "حرة" مرتبطة باسم الكلاس، بتوفر عليك زحمة إنشاء كائنات في الذاكرة لو كنت محتاج تنفذ وظيفة سريعة ومستقلة.</note>

<br-page></br-page>

</wrap>

<cover><cover-circle color="indigo">Inheritance — الوراثة</cover-circle></cover>

<br-page></br-page>


<wrap color="indigo">

<a id="l-third-principle-of-oop-inheritance"></a>
<lesson color="indigo">Third Principle of OOP: Inheritance</lesson>

<h4 style="text-align:center;font-size:20px">الدرس السادس عشر: الوراثة (Inheritance)</h4>

أمامك الآن مهمتين برمجيتين:

**المهمة الأولى:** عمل كلاس <t color="rose">clsPerson</t> يحتوي على الخصائص والدوال الأساسية لأي شخص.

**المهمة الثانية:** عمل كلاس <t color="amber">clsEmployee</t> يحتوي على الخصائص والدوال الخاصة بالموظف.

<cmp>
<good title="clsEmployee (الوريث)">

* <t>ID, FirstName, LastName, Email, Phone</t>
* <t>SendEmail(), SendSMS(), Print()</t>
* <t color=rose>Title, Department, Salary</t>


</good>
<good title="clsPerson (الأب)">

* <t>ID, FirstName, LastName, Email, Phone</t>
* <t>SendEmail(), SendSMS(), Print()</t>

</good>

</cmp>

من المقارنة السابقة، بنوضح حاجة مهمة وهي إن كل دوال <t color="lime">clsPerson</t> موجودة بالضرورة في الـ <t color="teal">clsEmployee</t>، لأن كل موظف هو في الأساس "شخص".
هنا بتبدأ فكرة **الوراثة (Inheritance)** في البرمجة. إيه اللي بنستفيده منها؟

1. هنعرّف بس الدوال الموجودة في الوريث ومش موجودة في الموروث (الأب).
2. لو عايز تعدل على كلاس <t color="sky">Person</t> والوريث بتاعه في دالة معينة (<t color="purple">Print</t> مثلاً)، ساعتها هتعدلها في الأب بس والتعديل هيسمع في الوريث.


---

دلوقتي هنكتب كود الـ <t color="rose">Person</t> القديم بتاعنا:

```cpp
#include <iostream>

using namespace std;

class clsPerson {
private:
    int _ID;
    string _FirstName;
    string _LastName;
    string _Email;
    string _Phone;
public:
   clsPerson(int ID, string FirstName, string LastName,string Email, string Phone){
        _ID = ID;
        _FirstName = FirstName;
        _LastName = LastName;
        _Email = Email;
        _Phone = Phone;
    }
    int ID() { return _ID; }

    //Property Set-Get
    void setFirstName(string FirstName) { _FirstName = FirstName; }
    string FirstName() { return _FirstName; }

    void setLastName(string LastName){_LastName = LastName;}
    string LastName(){ return _LastName; }

    void setEmail(string Email) { _Email = Email;}
    string Email(){return _Email;}

    void setPhone(string Phone){ _Phone = Phone;}
    string Phone() { return _Phone; }

    string FullName() { return _FirstName + " " + _LastName; }

    void Print(){
        cout << "\nInfo:";
        cout << "\n___________________";
        cout << "\nID       : " << _ID;
        cout << "\nFirstName: " << _FirstName;
        cout << "\nLastName : " << _LastName;
        cout << "\nFull Name: " << FullName();
        cout << "\nEmail    : " << _Email;
        cout << "\nPhone    : " << _Phone;
        cout << "\n___________________\n";
    }

    void SendEmail(string Subject, string Body) { ... }

    void SendSMS(string TextMessage) { ... }
};

```

وبعدها هنكتب كلاس الـ <t color="amber">Employee</t> فاضي خالص بدون أي شيء لكن مع عمل وراثة:

```cpp
class clsEmployee : public clsPerson{

};

```

وبعدين هتيجي في الـ <t color="lime">main</t> نجرب نعمل اوبجيكت من الوريث:

```cpp
int main()
{
    clsEmployee Employee1;
    return 0;
}

```
<note type=danger>

طبعاً السطر ده هيعمل إيرور بسبب الكونستراكتور بتاع الأب. لما بتعمل كائن من الوريث، أوتوماتيك بيحاول يستخدم الكونستراكتور الفاضي بتاع الأب، **وبما إننا عاملين كونستراكتور بباراميترات فالكونستراكتور الفاضي اتلغى**. هنحل المشكلة دي بشكل احترافي بعدين، ولكن حالياً عشان نعدي المشكلة عملنا Overloading لكونستراكتور مفيهوش أي باراميترات ولا محتويات في كلاس الأب عشان الوريث يستخدم الفاضي.

</note>

> هنحطه جمب الكونستراكتور القديم بتاعنا 

```cpp
public:
   clsPerson() {

   }
   clsPerson(int ID, string FirstName, string LastName,string Email, string Phone){ ... }
```
الآن وبما أن <t color="teal">Employee</t> ورث من <t color="sky">Person</t>، ننتقل للجزء الخاص فقط بالوريث وكتابته في كلاس الـ <t color="purple">clsEmployee</t>:

```cpp
class clsEmployee : public clsPerson
{
private:
    string _Title;
    string _Department;
    float _Salary;
public:
    //Property Set - Get
    void setTitle(string Title) {_Title = Title;}
    string Title(){return _Title;}

    //Property Set - Get
    void setDepartment(string Department) {_Department = Department;}
    string Department() {return _Department;}

    //Property Set - Get
    void setSalary(float Salary) {_Salary = Salary;}
    float Salary() {return _Salary;}
};
```

وأخيراً، هنكمل كتابة بقية الكود في الـ <t color="rose">main</t> لتجربة استخدام الموظف للخصائص الموروثة والخصائص الخاصة به:

```cpp
int main(){
    clsEmployee Employee1;

    Employee1.setFirstName("Mohammed");
    Employee1.setLastName("Abu-Hadhoud");
    Employee1.setEmail("a@a.com");
    Employee1.SendEmail("Hi", "How are you?");
    Employee1.setSalary(5000);

   cout << "Salary is: " << Employee1.Salary();
    
   //Calling the print will not print anything from derived class, only base class
   //therfore the print method will not serve me here, this is a problem will be solved in the next lecture. 
   Employee1.Print();
}
```
.
<out>
The following message sent successfully to email: a@a.com
Subject: Hi
Body: How are you?
Salary is: 5000
Info:
ID       : -858993460
FirstName: Mohammed
LastName : Abu-Hadhoud
Full Name: Mohammed Abu-Hadhoud
Email    : a@a.com
Phone    :
</out>

<note type=warn>

لاحظ في النهاية إن دالة <t color="amber">Print()</t> بتطبع بيانات الأب بس ومش بتطبع بيانات الوريث (المرتب والقسم)، ودي المشكلة اللي هنحلها في الدرس الجاي.

</note>


<br-page></br-page>

<a id="l-parameterized-constructor-of-the-base-class"></a>
<lesson color="indigo">Parameterized Constructor of the Base Class</lesson>

<h4 style="text-align:center;font-size:20px">الدرس السابع عشر: تمرير البيانات لكونستراكتور الأب</h4>

في الدرس السابق واجهتنا مشكلة وهي أن بمجرد إنشاء كائن من الوريث <t color="lime">clsEmployee</t>، كان البرنامج يحاول استدعاء الكونستراكتور الخاص بكلاس الاب  الخاص بكلاس الأب <t color="teal">clsPerson</t>، واضطرينا وقتها نعمل كونستراكتور فاضي كحل مؤقت.

في هذا الدرس سنعالج هذه المشكلة بالشكل الهندسي الصحيح. الحل يكمن في إنشاء كونستراكتور خاص بكلاس <t color="sky">clsEmployee</t>، ومن خلاله نقوم بتمرير (أو رمي) المتغيرات الأساسية مباشرة إلى الكونستراكتور الخاص بكلاس الأب (Base Class).

---

<divider>الخطوة الأولى: تمرير المتغيرات الأساسية للأب</divider>

لنفهم الفكرة، سنقوم بإنشاء كونستراكتور في كلاس الموظف يستقبل الـ 5 باراميترات الأساسية الخاصة بأي شخص، وبدلًا من مساواتها بالمتغيرات داخل كلاس الموظف، سنقوم بتمريرها لكونستراكتور الأب بهذا الشكل:

```cpp
class clsEmployee : public clsPerson
{
public:

    // نستقبل 5 باراميترات، ونقوم بتمريرها للأب بعد النقطتين الرأسيتين
    clsEmployee(int ID, string FirstName, string LastName,
     string Email, string Phone)
    : clsPerson(ID, FirstName, LastName, Email, Phone)
    {
    }

};

```

 بهذه الطريقة، الوريث يستقبل البيانات ويسلمها فوراً للأب ليتولى هو تعيينها في المتغيرات التي تم تعريفها هناك.

 > هذا يتم عن طريق وضع (<t>:</t>) بعد رأس الكونستراكتور , و من ثم استدعاء الكونستراكتور الخاص بكلاس الأب, ثم وضع الاقواس <t color="purple">{}</t> و كتابة كود الكونستراكتور داخلها

الآن في دالة <t color="rose">main</t>، سنجرب إنشاء الكائن <t color="amber">Employee1</t> وسنمرر له الـ 5 باراميترات التي قمنا بتعريفها، ثم نستدعي دالة <t color="lime">Print</t>:

```cpp
int main()
{
    clsEmployee Employee1(10, "Mohammed", "Abu-Hadhoud", "A@a.com",
     "8298982");
    Employee1.Print();
}
```

---

<divider>الخطوة الثانية: إضافة الباراميترات الخاصة بالوريث</divider>

الآن وقد تأكدنا أن البيانات الأساسية تمر بنجاح للأب، يمكننا زيادة الباراميترات الجديدة الخاصة بالـ <t color="teal">Employee</t> (مثل Title, Department, Salary) داخل نفس الكونستراكتور.

سنستقبل جميع الباراميترات الـ 8 معاً: نمرر الـ 5 الأولى للأب كما فعلنا، والـ 3 المتبقية نقوم بتعيينها داخل جسم الكونستراكتور الخاص بالموظف:

```cpp
class clsEmployee : public clsPerson
{
private:
    string _Title;
    string _Department;
    float _Salary;

public:

    clsEmployee(int ID, string FirstName, string LastName,
         string Email, string Phone, string Title,
         string Department, float Salary)
    : clsPerson(ID, FirstName, LastName, Email, Phone)
    {
        // المتغيرات الخاصة بالموظف يتم تعيينها هنا
        _Title = Title;
        _Department = Department;
        _Salary = Salary;
    }

    // دوال الخصائص (Properties) هنا ...
};

```

نعود الآن لدالة <t color="sky">main</t> لإنشاء الكائن وتمرير جميع الباراميترات الـ 8:

```cpp
int main()
{
    clsEmployee Employee1(10, "Mohammed", "Abu-Hadhoud", "A@a.com",
     "8298982", "CEO", "ProgrammingAdvices", 5000);
    
    Employee1.Print();

    system("pause>0");
    return 0;
}

```
<out>
Info:
ID       : 10
FirstName: Mohammed
LastName : Abu-Hadhoud
Full Name: Mohammed Abu-Hadhoud
Email    : A@a.com
Phone    : 8298982
</out>

---

إذا قمت بتشغيل الكود السابق، ستلاحظ مشكلة: دالة <t color="purple">Print</t> قامت بطباعة المتغيرات الخاصة بالـ <t color="rose">Person</t> فقط، ولم تقم بطباعة بيانات الـ <t color="amber">Employee</t> (المسمى الوظيفي، القسم، الراتب) رغم أننا مررناها بشكل صحيح!

السبب هو أن دالة <t color="lime">Print</t> التي استدعيناها هي الدالة الموروثة من الأب، وهي مصممة لطباعة بيانات الأب فقط. سنقوم بحل مشكلة دالة الطباعة بشكل جذري في الدرس القادم.

ولكن لكي نتأكد أن المتغيرات الثلاثة الخاصة بالموظف تم تخزينها بنجاح داخل الكائن، سنقوم بطباعتها يدوياً باستخدام دوال الـ Get (Properties) الخاصة بها:

```cpp
int main()
{
    clsEmployee Employee1(10, "Mohammed", "Abu-Hadhoud", "A@a.com",
     "8298982", "CEO", "ProgrammingAdvices", 5000);
    
    Employee1.Print(); // تطبع بيانات الشخص

    // نتحقق من البيانات الخاصة بالموظف
    cout << "\n" << Employee1.Title() << endl;
    cout << "\n" << Employee1.Department() << endl;
    cout << "\n" << Employee1.Salary() << endl;
}
```
<out>
Info:
ID       : 10
FirstName: Mohammed
LastName : Abu-Hadhoud
Full Name: Mohammed Abu-Hadhoud
Email    : A@a.com
Phone    : 8298982
CEO
ProgrammingAdvices
5000
</out>

> كدا زي الفل المتغيرات التمانية موجودين , و لكن المشكلة ان دالة الطباعة لا تطبع بيانات الموظف , و سنقوم بحل هذه المشكلة في الدرس القادم.

<br-page></br-page>
<a id="l-function-overriding"></a>
<lesson color="indigo">Function Overriding</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثامن عشر: إعادة كتابة الدوال (Function Overriding)</h4>

<divider>الربط بالدرس السابق والمشكلة</divider>

في الدرس اللي فات اتكلمنا عن الـ **Inheritance** (الوراثة)، وشوفنا إزاي كلاس الموظف <t color="teal">clsEmployee</t> ورث كل الخصائص من كلاس الشخص <t color="sky">clsPerson</t>.
لكن واجهتنا مشكلة: لما جينا نطبع بيانات الموظف عن طريق دالة <t color="purple">Print()</t>، طبعت البيانات الأساسية بس وتجاهلت البيانت الخاصة بالموظف (المسمى الوظيفي، القسم، الراتب). ليه؟ لأن الدالة اللي اشتغلت هي بتاعت الأب، واللي بطبيعة الحال ما تعرفش حاجة عن المتغيرات الجديدة بتاعة الوريث.

هنا بييجي دور المفهوم الجديد: **Function Overriding**.

<divider>أهمية ومفهوم الـ Function Overriding</divider>

الفكرة ببساطة إننا بنكتب دالة جوه **الوريث** (Child)، بس ليها نفس الاسم ونفس الشكل بالظبط بتاع دالة أصلاً موجودة في **الأب** (Parent).
الفايدة من ده إيه؟ إننا بنقول للكومبايلر: "أول ما حد يستدعي الدالة دي من الكائن بتاع الوريث، تجاهل دالة الأب وشغل النسخة الجديدة دي".

عشان نثبت ده، هنعمل دالة <t color="rose">Print</t> جديدة جوه <t color="amber">clsEmployee</t> بنفس الشكل بالظبط، بس هنسيبها فاضية مؤقتاً:

```cpp
class clsEmployee : public clsPerson
{
// ... بقية الكود

public:

    // الكونستراكتور
    clsEmployee(int ID, string FirstName, string LastName,
         string Email, string Phone, string Title,
         string Department, float Salary)
    : clsPerson(ID, FirstName, LastName, Email, Phone)
    {
        _Title = Title;
        _Department = Department;
        _Salary = Salary;
    }

    // دالة Print الجديدة الخاصة بالموظف (Overridden Method)
    void Print()
    {

    }

};
```

لو جينا شغلنا نفس الكود الأخير بتاع الـ <t color="lime">main</t> مرة تانية:

```cpp
int main()
{
    // عملنا الأوبجيكت ومررنا البيانات كلها
    clsEmployee Employee1(10, "Mohammed", "Abu-Hadhoud", "A@a.com",
     "8298982", "CEO", "ProgrammingAdvices", 5000);
    
    // استدعاء دالة الطباعة
    Employee1.Print(); 

    system("pause>0");
    return 0;
}
```

<out>
</out>

<note type="success">

الشاشة هتطلع فاضية تماماً! وده إثبات إن الكومبايلر شغل الدالة الجديدة (الفاضية) اللي إحنا لسة كاتبينها في الوريث، وتجاهل الدالة القديمة بتاعة الأب لأننا عملنالها <t>Overriding</t>.

</note>

---

<divider>البناء الصحيح للدالة واستدعاء الأب</divider>

دلوقتي إحنا محتاجين دالة <t color="teal">Print</t> بتاعة الوريث تطبع كل المتغيرات.
الطريقة الأذكى والموفرة للوقت هي إننا نستفيد من الدالة القديمة؛ نستدعي دالة الأب عشان تطبع الـ 5 متغيرات الأساسية، وبعدها نكمل إحنا طباعة الـ 3 متغيرات الجداد!

> بنعمل ده عن طريق كتابة <t color="teal">اسم الأب :: اسم الدالة ()</t>:

```cpp
    void Print()
    {
        // 1. استدعاء الدالة من كلاس الأب صراحةً
        clsPerson::Print();

        // 2. استكمال الطباعة الخاصة بالوريث
        cout << "\nTitle     : " << _Title;
        cout << "\nDepartment: " << _Department;
        cout << "\nSalary    : " << _Salary;
    }
```

لما نشغل البرنامج دلوقتي:

<out>
Info:
___________________
ID       : 10
FirstName: Mohammed
LastName : Abu-Hadhoud
Full Name: Mohammed Abu-Hadhoud
Email    : A@a.com
Phone    : 8298982
___________________
Title     : CEO
Department: ProgrammingAdvices
Salary    : 5000
</out>

---

طيب ماذا لو شيلت سطر <t color="sky">clsPerson::Print();</t> وحاولت أكتب كود الطباعة كله بنفسي جوه دالة الموظف الجديدة؟

```cpp
    void Print()
    {
        cout << "\nInfo:";
        cout << "\n___________________";
        cout << "\nID        : " << _ID;
        cout << "\nFirstName : " << _FirstName;
        cout << "\nLastName  : " << _LastName;
        cout << "\nFull Name : " << FullName();
        cout << "\nEmail     : " << _Email;
        cout << "\nPhone     : " << _Phone;
    }
```

<note type="warn">بمجرد ما تبني الكود ده هيحصل <b>إيرور (Error)</b> والبرنامج مش هيشتغل!</note>

**السبب:** المتغيرات دي (زي <t color="purple">_ID</t> و <t color="rose">_FirstName</t>) متعرفة في كلاس الأب <t color="teal">clsPerson</t> على إنها <t color="teal">private</t>. في مبادئ الـ OOP، المتغير الـ <t color="amber">private</t> ممنوع أي حد يشوفه أو يلمسه بره الكلاس بتاعه، **حتى لو كان كلاس وارث منه!** الوريث بيملك المتغيرات دي فعلياً، بس ملوش حق الوصول المباشر ليها في الكود.

---

<divider>حلول الوصول للمتغيرات المخفية</divider>

عشان نحل المشكلة دي ونقدر نتعامل مع بيانات الأب جوه الوريث، قدامنا حلين:

<cmp>
<good title="الحل الأول: تغيير Private إلى Protected">
ممكن نرجع لكلاس الأب <t color="amber">clsPerson</t> ونغير كلمة <t color="lime">private</t> ونخليها <t color="teal">protected</t>.
مفهوم <t color="sky">protected</t> معناه إن المتغيرات دي ما زالت مخفية عن الـ <t color="purple">main</t> والمستخدم الخارجي، بس <b>مسموح لأي كلاس وارث</b> إنه يوصلها ويستخدمها براحته مباشرة وكأنها بتاعته.
</good>
<good title="الحل الثاني: استخدام دوال الـ Get (الأفضل)">
ودا الحل الأفضل والمثالي! إننا نستخدم دوال الـ <t color="rose">Get</t> اللي عملناها أصلًا في الأب (زي <t color="amber">ID()</t> و <t color="lime">FirstName()</t>) لأن الدوال دي متعرفة كـ <t color="teal">public</t>، وبالتالي نقدر نقرأ البيانات بأمان بدون ما نكسر فكرة التغليف (Encapsulation).
</good>
</cmp>

تعال نطبق الحل التاني ونكتب الدالة كاملة بالاعتماد عليه بدون أي إيرور:

```cpp
    void Print()
    {
        cout << "\nInfo:";
        cout << "\n___________________";
        
        // استخدام دوال الـ Get للوصول لبيانات الأب
        cout << "\nID        : " << ID();
        cout << "\nFirstName : " << FirstName();
        cout << "\nLastName  : " << LastName();
        cout << "\nFull Name : " << FullName();
        cout << "\nEmail     : " << Email();
        cout << "\nPhone     : " << Phone();
        
        // بيانات الوريث متاحة وممكن نستخدم متغيراتها مباشرة
        cout << "\nTitle     : " << _Title;
        cout << "\nDepartment: " << _Department;
        cout << "\nSalary    : " << _Salary;
        
        cout << "\n___________________\n";
    }
```

<note type="success">

**الخلاصة:** الـ Function Overriding مفيد جداً لما تحب تغير شوية في سلوك دالة ورثتها من الأب عشان تناسب تفاصيل الوريث الجديد. وعشان تحافظ على حماية البيانات، إما تستخدم <t color="teal">protected</t> في كلاس الأب، أو تستخدم دوال <t color="teal">Get</t> المتاحة من الأب.

</note>

<br-page></br-page>
<a id="l-multi-level-inheritance"></a>
<lesson color="indigo">Multi Level Inheritance</lesson>

<h4 style="text-align:center;font-size:20px">الدرس التاسع عشر: الوراثة متعددة المستويات (Multi Level Inheritance)</h4>

<divider>فكرة الوراثة المتعددة وأهميتها</divider>

ماذا لو أردنا كتابة كلاس جديد اسمه <t color="purple">clsDeveloper</t> (المبرمج)؟ 
زي ما إنت عارف، المبرمج هو في الأساس موظف، وبالتالي هو كمان شخص! فبدل ما نكتب كل الخصائص من الصفر، هنخليه يورث من كلاس <t color="teal">clsEmployee</t>. 

خلينا نبص على تسلسل الوراثة (Hierarchy) زي ما هو موضح:

* <t color="rose">Person</t>: ده هو الـ **Super Class** أو **Base Class** (الكلاس الأب الأساسي)، اللي فيه الخصائص المشتركة لأي شخص (ID, First Name, Last Name, Email, Phone) ودوال زي <t color="lime">FullName()</t> و <t color="amber">Print()</t>.
* <t color="teal">Employee</t>: ده هو الـ **Sub Class** أو **Derived Class** (الكلاس الوريث) بالنسبة لـ <t color="rose">Person</t>، لأنه ورث منه كل حاجة وزود عليها حاجات خاصة بالموظف (Title, Department, Salary). وفي نفس الوقت هو **Super Class** بالنسبة للمبرمج!
* <t color="purple">Developer</t>: ده هو الـ **Sub Class** لكلاس <t color="teal">Employee</t>، هيورث كل خصائص الموظف (واللي بطبيعة الحال ورثها من الشخص) وهنزود عليه خاصية جديدة وهي <t color="sky">MainProgrammingLanguage</t>.

<note type="tip">

لو ضفنا، أو صلحنا، أو عدلنا أي دالة في الـ <b>Super Class</b> (زي الأب أو الجد)، التعديل ده هيتطبق أوتوماتيك على كل الـ <b>Derived Classes</b> اللي وارثين منه (في حالة إننا معملناش Overriding للدالة دي في الوريث).

</note>

طبعاً بنفس المنطق، إحنا نقدر نعمل كلاس لدكتور <t color="amber">clsDoctor</t> يورث من <t color="teal">clsEmployee</t> عادي جداً، وهيكون عنده خصائصه المميزة زي التخصص والمستشفى مثلاً.
<br-page></br-page>

---

<divider>التطبيق العملي وكتابة الكود</divider>

كده التسلسل بتاعنا هيكون بالشكل ده:

```cpp
class clsPerson { ... } ;

class clsEmployee : public clsPerson { ... } ; 
```

ودلوقتي هنبدأ نكتب كلاس الـ <t color="purple">clsDeveloper</t>:

### 1. إضافة المتغير الجديد المُمَيز

أول حاجة هنضيف المتغير الخاص بلغة البرمجة الأساسية في المنطقة الخاصة:

```cpp
class clsDeveloper : public clsEmployee 
{
private:
    string _MainProgrammingLanguage;
```

### 2. بناء الكونستراكتور (Constructor)

زي ما اتعلمنا في الدرس اللي فات، الكونستراكتور ده هيستلم كل البيانات، ياخد اللي يخصه منها، ويبعت الباقي للكونستراكتور بتاع الكلاس اللي قبله (اللي هو <t color="teal">clsEmployee</t>):

```cpp
public:
    clsDeveloper(int ID, string FirstName, string LastName, 
                 string Email, string Phone, string Title, 
                 string Department, float Salary, 
                 string MainProgrammingLanguage) 
        : clsEmployee(ID, FirstName, LastName, Email, Phone,
                      Title, Department, Salary) // المتغيرات الممررة
    {
        _MainProgrammingLanguage = MainProgrammingLanguage;
    }
```

ببساطة، إحنا استقبلنا 9 باراميترات. أخدنا الباراميتر الأخير بتاع لغة البرمجة وسجلناه في المتغير الخاص بالكلاس ده، وأما الـ 8 باراميترات الباقيين، رميناهم للـ <t color="teal">clsEmployee</t> عشان هو يتصرف فيهم (واللي بدوره هيرمي 5 منهم لـ <t color="rose">clsPerson</t>!). عملية تسليم وتسلم منظمة جداً.

### 3. بوابات التعديل والوصول (Set & Get)

طبعاً مننساش نحط الـ Set والـ Get الخاصين بالمتغير الجديد بتاعنا عشان نقدر نتعامل معاه بأمان من بره الكلاس:

```cpp
    // Property Set
    void setMainProgrammingLanguage(string MainProgrammingLanguage)
    {
        _MainProgrammingLanguage = MainProgrammingLanguage;
    }

    // Property Get
    string MainProgrammingLanguage()
    {
        return _MainProgrammingLanguage;
    }
```

### 4. إعادة كتابة دالة الطباعة (Function Overriding)

عشان دالة الطباعة تطلع كل البيانات صح، هنعملها Overriding عشان تطبع الجزء الجديد ورا شغل الدالة القديمة:

```cpp
    void Print()
    {
        clsEmployee::Print();
        cout << "\nPLanguage : " << MainProgrammingLanguage();
    }

}; // نهاية كلاس clsDeveloper
```

في الكود ده إحنا استدعينا دالة <t color="lime">Print()</t> بتاعة <t color="teal">clsEmployee</t> (واللي جواها بتستدعي بتاعة <t color="rose">clsPerson</t>)، وبعد ما تخلص، بنطبع السطر الجديد الخاص بلغة البرمجة.

<note type="success">
وبكده نكون عملنا تسلسل وراثة هرمي ممتاز ومترابط من غير ما نكرر أي سطر كود
</note>

<a id="l-access-specifiersmodifiers-review"></a>
<lesson color="indigo">Access Specifiers/Modifiers Review</lesson>

<h4 style="text-align:center;font-size:20px">الدرس العشرون: مراجعة مستويات الوصول (Access Specifiers)</h4>

<divider>مراجعة سريعة</divider>

في الدروس الأولى لـ OOP، اتكلمنا عن مستويات الوصول اللي بتتحكم مين يقدر يشوف ويستخدم المتغيرات والدوال اللي جوه الكلاس. خلينا نراجعهم بسرعة:

1. <t color="lime">private:</t> ده الخزنة المقفولة. أي حاجة تتعرف هنا، مستحيل حد يقدر يشوفها أو يستخدمها بره الكلاس، **ولا حتى الكلاسات اللي بتورث منه**.
2. <t color="rose">public:</t> ده الشارع العام. أي حاجة هنا، متاحة للكل. تقدر تستخدمها جوه الكلاس، في الـ الورثة، وحتى في الـ <t color="amber">main</t> براحتك.

<divider>الحل المنسي: الـ Protected</divider>

في درس الـ **Function Overriding** (الدرس 18)، واجهتنا مشكلة: لما جينا نكتب دالة <t color="teal">Print()</t> جوه الموظف عشان يحصل على بيانات الشخص (الأب)، المترجم اعترض لأن بيانات الشخص كانت <t color="lime">private</t>.
وقتها روحنا للحل المثالي وهو استخدام دوال الـ <t color="sky">Get</t>.

لكن كان في حل تاني إحنا ذكرناه وهو إننا نغير الـ <t color="lime">private</t> لـ <t color="purple">protected</t>. إيه هو الـ <t color="purple">protected</t> بالظبط؟

3. <t color="purple">protected:</t> ده مستوى وسط بين الاتنين. لو عرفت متغير أو دالة هنا، هتكون **مخفية** ومقفول عليها عن أي حد بره الكلاس (زي الـ <t color="purple">main</t>) مقدرش يشوفها. **لكن**، بتسمح لأي كلاس **وارث** (Derived Class) إنه يشوفها ويستخدمها مباشرة وكأنها بتاعته! هي "خزنة مقفولة للغرباء، بس مفتوحة لأهل البيت".

---

<br-page></br-page>
<divider>التطبيق العملي بالكود</divider>

عشان نفهم الفروق دي عملي، خلينا نبص على الكود ده ونحلله:

### 1. كلاس الأب (clsA) وتحديد الصلاحيات

في البداية هنعمل كلاس أب اسمه <t color="amber">clsA</t>، وهنقسم جواه المتغيرات والدوال لـ 3 أقسام عشان نشوف كل قسم فيهم مين هيقدر يوصله:

```cpp
#include <iostream>

using namespace std;

class clsA
{
private:
    int _Var1;
    void _Fun1(){
        cout << "Function 1";
    }
protected:
    int Var2;
    void Fun2(){
        cout << "Function 2";
    }
public:
    int Var3;
    void Fun3(){
        cout << "Function 3";
    }
};
```

* **القسم الأول (Private):** <t color="teal">_Var1</t> و <t color="sky">_Fun1()</t>، دول في الخزنة الخاصة. محدش هيقدر يستخدمهم غير جوه كلاس <t color="amber">clsA</t> نفسه فقط! الكلاسات الوارثة أو الدالة <t color="lime">main</t> مستحيل توصلهم.
* **القسم الثاني (Protected):** <t color="purple">Var2</t> و <t color="rose">Fun2()</t>، دول حصرية للعائلة. نقدر نستخدمهم جوه <t color="amber">clsA</t>، ونقدر كمان نستخدمهم جوه أي كلاس وارث منه. لكن الدالة <t color="lime">main</t> متعرفش عنهم حاجة.
* **القسم الثالث (Public):** <t color="teal">Var3</t> و <t color="sky">Fun3()</t>، دول متاحين للجميع. أي مكان في البرنامج يقدر يوصلهم.

### 2. كلاس الوريث (clsB) وتجربة الوصول

دلوقتي هنعمل كلاس جديد <t color="purple">clsB</t> يورث من <t color="amber">clsA</t>، ونجرب نوصل للبيانات من جواه:

```cpp
class clsB : public clsA
{
public:

    void Func1()
    {
        // [1] ✅ 
        cout << clsA::Var2; 
        
        // [2] cout << clsA::_Var1;  ❌
    }
};
```

<div dir="rtl">
<b>توضيحات الكود:</b>
<br>
[1] الوريث قدر يوصل لـ <t color="teal">Var2</t> لأنها protected في الأب.
<br>
[2] السطر ده هيديك إيرور لو شيلت التعليق لأن <t color="teal">_Var1</t> مخفية حتى عن الورثة (private).
</div>

الوريث قدر يشوف الـ <t color="rose">Var2</t> براحته لأنها <t color="teal">protected</t>، لكنه مقدرش يقرب من الـ <t color="sky">_Var1</t> لأنها <t color="lime">private</t>.

### 3. التجربة العملية في الدالة الرئيسية (main)

```cpp
int main()
{
    clsA A;

    A.Var3 = 10; // ✅ مسموح لأنها Public
    A.Fun3();    // ✅ مسموح لأنها Public

    // ❌ 
    // A.Var1 = 5; 
    // A.Var2 = 7; 
}
```

طبعاً الـ <t color="lime">main</t> قدرت تستخدم <t color="teal">Var3</t> لأنها <t color="sky">public</t>، لكنها اتمنعت تماماً من استخدام الباقي لأنهم محميين.

<note type="success">

**الخلاصة:**
استخدم <t color="lime">private</t> لما تكون عايز تحمي بياناتك من أي تلاعب سواء من المستخدمين أو حتى من الكلاسات اللي تورث منك.
استخدم <t color="purple">protected</t> لو أنت بتبني هيكل كبير وعايز تشارك البيانات بين الكلاسات اللي ورثة بعضها بمرونة، بس برضه تحميها من التدخلات الخارجية.

</note>

<br-page></br-page>
<a id="l-inheritance-visibility-modes"></a>
<lesson color="indigo">Inheritance Visibility Modes</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الحادي والعشرون: أوضاع الرؤية في الوراثة (Visibility Modes)</h4>

<divider>السؤال الأهم: إزاي بنورث؟</divider>

في كل الدروس اللي فاتت، لما كنا بنعمل كلاس يورث من كلاس تاني، كنا دايماً بنحط كلمة <t color="sky">public</t> قبل اسم الأب بالشكل ده:

```cpp
class DerivedClassName : public BaseClassName
{
    // ...
};
```

لكن الحقيقة إننا نقدر نغير الكلمة دي لـ <t color="lime">private</t> أو <t color="purple">protected</t>. الكلمة دي بتسمى **Inheritance Visibility Mode** (وضع الرؤية للوراثة)، وهي اللي بتحدد "قوة" الخصائص الموروثة جوه الكلاس الجديد. 

بمعنى تاني: الحاجات اللي الأب سامح بتوريثها (زي الـ <t color="sky">public</t> والـ <t color="purple">protected</t>)، هتنزل للوريث عاملة إزاي؟ هل هتفضل <t color="sky">public</t>؟ ولا الوريث هيقرر يخفيها عن الناس ويخليها <t color="lime">private</t> جواه؟

---

<divider>شرح الحالات الثلاثة للوراثة</divider>

عشان نفهم الجدول الجاي، لازم تحط قاعدة دهبية في دماغك: **أي حاجة <t color="lime">Private</t> في الأب، مستحيل تتورث للوريث تحت أي ظرف.**

تعالوا نشوف بقى اللي هيتورث للوريث، وضعه هيكون إيه بناءً على وضع الوراثة اللي هنختاره:

<defs>

<def term="1. الوراثة العامة (Public Inheritance)">

دي الحالة الطبيعية اللي إحنا متعودين عليها. الوريث بيورث كل حاجة زي ما هي:
<br> 1- الـ **Public** في الأب، بينزل **Public** في الوريث.
<br> 2- الـ **Protected** في الأب، بينزل **Protected** في الوريث.

</def>

<def term="2. الوراثة المحمية (Protected Inheritance)"> 

هنا الوريث بيقرر يقلل مستوى الرؤية شوية. بيعتبر كل حاجة ورثها وكأنها **Protected**:
<br> 1- الـ **Public** في الأب، **بينزل Protected في الوريث.**
<br> 2- الـ **Protected** في الأب، بيفضل **Protected** في الوريث.
<br> ده معناه إن الوريث هيقدر يستخدم الحاجات دي، ولو حد ورث منه هيقدر يستخدمها، بس الـ **main** بره مش هتشوف أي حاجة!

</def>

<def term="3. الوراثة الخاصة (Private Inheritance)">

دي أقصى درجات الإخفاء! الوريث بيقرر إنه يقفل على كل حاجة ورثها وتكون ملكه هو بس، وميسمحش لأي كلاس تاني يورث الأغراض دي منه:
<br> 1- الـ **Public** في الأب، **بينزل Private في الوريث.**
<br> 2- الـ **Protected** في الأب، **بينزل Private في الوريث.**

</def>

</defs>

<divider>جدول ملخص لأوضاع الوراثة</divider>

عشان الموضوع يثبت في دماغك، الجدول الجميل ده بيلخص كل الحالات اللي قولناها:

<br>
<div style="display: flex; justify-content: center; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; direction: ltr;">
  <table style="border-collapse: collapse; width: 90%; max-width: 800px; text-align: center; border-radius: 8px; overflow: hidden; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <thead>
      <tr style="background-color: #5c7cb1; color: white;">
        <th style="padding: 12px; border: 1px solid #ddd; background-color: #4a6797;">Visibility Mode</th>
        <th style="padding: 12px; border: 1px solid #ddd;">Private Members</th>
        <th style="padding: 12px; border: 1px solid #ddd;">Protected Members</th>
        <th style="padding: 12px; border: 1px solid #ddd;">Public Members</th>
      </tr>
    </thead>
    <tbody style="background-color: #ebeaf6; color: #333;">
      <tr style="transition: background-color 0.3s; border-bottom: 1px solid #d1d0e5;">
        <td style="padding: 12px; border: 1px solid #ddd; font-weight: bold; text-align: left; background-color: #d8d7ea;">Public Inheritance</td>
        <td style="padding: 12px; border: 1px solid #ddd;">Inaccessible</td>
        <td style="padding: 12px; border: 1px solid #ddd; color: #5a7d3c; font-weight: 600;">Protected</td>
        <td style="padding: 12px; border: 1px solid #ddd; color: #205c9e; font-weight: 600;">Public</td>
      </tr>
      <tr style="transition: background-color 0.3s; border-bottom: 1px solid #d1d0e5; background-color: #f2f1f9;">
        <td style="padding: 12px; border: 1px solid #ddd; font-weight: bold; text-align: left; background-color: #e2e1f2;">Private Inheritance</td>
        <td style="padding: 12px; border: 1px solid #ddd;">Inaccessible</td>
        <td style="padding: 12px; border: 1px solid #ddd; color: #c0392b; font-weight: 600;">Private</td>
        <td style="padding: 12px; border: 1px solid #ddd; color: #c0392b; font-weight: 600;">Private</td>
      </tr>
      <tr style="transition: background-color 0.3s;">
        <td style="padding: 12px; border: 1px solid #ddd; font-weight: bold; text-align: left; background-color: #d8d7ea;">Protected Inheritance</td>
        <td style="padding: 12px; border: 1px solid #ddd;">Inaccessible</td>
        <td style="padding: 12px; border: 1px solid #ddd; color: #5a7d3c; font-weight: 600;">Protected</td>
        <td style="padding: 12px; border: 1px solid #ddd; color: #5a7d3c; font-weight: 600;">Protected</td>
      </tr>
    </tbody>
  </table>
</div>
<br>

<br-page></br-page>

<divider>التطبيق العملي بالكود</divider>

دلوقتي هنطبق الكود عشان نفهم الجدول أكتر ونتخيل إيه اللي بيحصل. هنكتب كلاس أب <t color="amber">clsA</t> وثلاثة وراثة عشان نختبر الـ Visibility Modes.

### 1. الكلاس الأساسي أو الأب (clsA)

```cpp
#include <iostream>
using namespace std;

class clsA 
{
private: 
    int V1;
    int Fun1() { return 1; }

protected:
    int V2;
    int Fun2() { return 2; }

public:
    int V3;
    int Fun3() { return 3; }
};
```

زي ما إحنا شايفين، كلاس الأب فيه متغير ودالة لكل نوع من أنواع الرؤية عشان نختبرهم.

### 2. المستوى الأول للوراثة - وراثة خاصة (Private Inheritance)

دلوقتي هنعمل كلاس <t color="purple">clsB</t>، بس المرة دي الوريث طمّاع ومخفي! هيورث من <t color="amber">clsA</t> باستخدام وضع الـ <t color="lime">private</t>:

```cpp
class clsB : private clsA
{
public:
    int Fun4()
    {
        // [1] ❌ 
        // return V1; 
        
        // [2] ✅
        // return V2;
        // return V3;
        
        return 4;
    }
};
```

<div dir="rtl">
<b>توضيحات الكود:</b>
<br>
[1] السطر ده مرفوض لأن <t color="teal">V1</t> أصلاً مابتتورثش.
<br>
[2] الأسطر دي مسموحة لأن <t color="teal">V2</t> و <t color="teal">V3</t> اتورثوا، بس خد بالك هما نزلوا في كلاس B وبقوا private! يعنى B يقدر يستخدمهم داخلياً، بس ممنوع حد يورثهم منه بعد كدا.
</div>

* الـ <t color="purple">Protected</t> والـ <t color="sky">Public</t> بتوع كلاس الأب نزلوا في <t color="purple">clsB</t> وصاروا **<t color="lime">Private</t>**! 
* ده معناه إن كلاس <t color="purple">clsB</t> بس هو اللي يقدر يشوفهم، لكن مستحيل حد يورثهم منه أو يوصلهم في الـ <t color="teal">main</t>.

### 3. المستوى التاني للوراثة - محاولة توريث المخفي

عشان نتأكد إن كلامنا صح، هنعمل كلاس جديد <t color="rose">clsC</t> بيورث من <t color="purple">clsB</t> وراثة عامة (<t color="sky">public</t>).

```cpp
class clsC : public clsB
{
public:
    int Fun5()
    {
        // [1] ❌
        return 5;
    }
};
```

<div dir="rtl">
<b>توضيحات الكود:</b>
<br>
[1] مش هتقدر توصل لأي حاجة هنا خالص! لا <t color="teal">V2</t> ولا <t color="teal">V3</t> ولا أي دالة ورثها B، لأن B خباهم كلهم كـ Private. الدالة الوحيدة اللي المسموح C يشوفها هي دالة <t color="teal">Fun4()</t> لأنها Public في B.
</div>

بالرغم من إن <t color="rose">clsC</t> بيورث <t color="sky">public</t>، إلا إنه مقدرش يشوف حاجة من كلاس الجد الأكبر <t color="amber">clsA</t> لأن الكلاس الأب <t color="purple">clsB</t> عمل وراثة من الجد كـ <t color="lime">private</t>.

### 4. تجربة الوصول المتعدد في الـ Main

دلوقتي تعالوا نشوف الدنيا من وجهة نظر الـ <t color="teal">main</t>:

```cpp
int main()
{   
    clsB B1;
    // [1] ❌ 
    // B1.Fun3(); 
    
    clsC C1;
    // [2] ❌
    
    return 0;
}
```

<div dir="rtl">
<b>توضيحات الكود:</b>
<br>
[1] تقدر توصل لـ <t color="teal">Fun4()</t> بس! المترجم هيرفض ينده لدالة <t color="teal">Fun3()</t> لأنها في B أصبحت Private.
<br>
[2] تقدر توصل لـ <t color="teal">Fun5()</t> و <t color="teal">Fun4()</t> بس! ومفيش أي أثر لأي دالة من الكلاس الأساسي clsA.
</div>

<note type="success">
بهذا التسلسل البسيط، فهمنا إن وضع الوراثة (Visibility Mode) هو بوابة "تصفية" (Filter) بتسمح للمبرمج يتحكم بدقة في قدرات الكائنات والكلاسات اللي بتورث من شغله، ليضمن أقوى درجات الإخفاء (Encapsulation) لو احتاجها.
</note>

<br-page></br-page>
<a id="l-inheritance-types"></a>
<lesson color="indigo">Inheritance Types</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثاني والعشرون: أنواع الوراثة (Inheritance Types)</h4>

<divider>الأشكال المختلفة للوراثة</divider>

في لغة C++، الوراثة ليها أكتر من شكل أو نوع بناءً على طريقة تنظيم العلاقة بين الكلاسات (مين بيورث من مين). نقدر نقسمهم لـ 5 أنواع أساسية زي ما هو موضح في المخططات:

<defs>

<def term="1. الوراثة الفردية (Single Inheritance)">

دي أبسط وأشهر حالة، وفيها كلاس واحد (الوريث `B`) بيورث من كلاس أساسي واحد (الأب `A`).
<br><b>مثال:</b> كلاس `Employee` بيورث من كلاس `Person`.

</def>

<def term="2. الوراثة متعددة المستويات (Multi Level Inheritance)">

هنا الوراثة بتتم على مراحل متسلسلة (زي الجد، الأب، الابن). الكلاس `B` بيورث من `A`، وبعدين يجي كلاس `C` يورث من `B`، وبالتالي `C` بيكون واخد خصائص `B` و `A` مع بعض.
<br><b>مثال:</b> `Person` ⬅️ `Employee` ⬅️ `Developer`.

</def>

<def term="3. الوراثة الهرمية (Hierarchal Inheritance)">

في النوع ده بيكون عندنا كلاس أب واحد (`A`)، ولكن بيورث منه أكتر من كلاس (أبناء كتير زي `B, C, D`). كلهم بياخدوا نفس الخصائص الأساسية من نفس الأب المشترك.
<br><b>مثال:</b> `Employee` بيورث منه `Developer` و `Doctor` و `Teacher`.

</def>

</defs>

<br-page></br-page>

<divider>الأنواع المعقدة في C++</divider>

النوعين الجايين دول متاحين في لغة C++، بس هما <b>غير مستخدمين عملياً في معظم الأوقات</b> بسبب المشاكل والـ Errors الكتير اللي بيسببوها، وعشان كده <b>مش هندرسهم في الكورس ولا هنطبق عليهم بأكواد</b>، بس بنعرفهم لمجرد الثقافة البرمجية:

<defs>

<def term="4. الوراثة المتعددة (Multiple Inheritance)">

هنا الكلاس الواحد (`C`) بيورث من <b>أكتر من أب</b> في نفس الوقت (`A` و `B`).
<br><b>المشكلة:</b> لو الأب `A` والأب `B` عندهم دالة بنفس الاسم، الوريث `C` هيتلخبط ومش هيبقي عارف يستخدم دالة مين فيهم (بتحصل مشكلة اسمها Ambiguity). لغات كتير زي C# و Java منعت النوع ده تماماً من لغاتها بسبب تعقيده.

</def>

<def term="5. الوراثة الهجينة (Hybrid Inheritance)">

دي حرفياً "خليط" أو "هجين" بين أكتر من نوع وراثة (مثلاً دمج بين الهرمية والمتعددة).
زي إن كلاس `A` يورث منه `B` و `C`، وبعدين يجي كلاس `D` يورث من الـ `B` و `C` مع بعض!
<br><b>المشكلة:</b> بتعمل مشكلة شهيرة جداً في C++ اسمها <b>(Diamond Problem)</b>، لأن خصائص `A` هتروح لـ `D` مرتين (مرة عن طريق `B` ومرة عن طريق `C`)، وده بيدمر الذاكرة وبيعمل تداخلات معقدة جداً بتحتاج حلول متقدمة (Virtual Inheritance) عشان تتحل.

</def>

</defs>

<note type="success">

<b>الخلاصة:</b> ركز دايماً في شغلك على أول 3 أنواع (الفردية، متعددة المستويات، والهرمية) لأنهم بيمثلوا 99% من شغل الـ OOP الأساسي والنظيف.

</note>

<br-page></br-page>
<a id="l-up-casting-vs-down-casting"></a>
<lesson color="indigo">Up Casting vs Down Casting</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثالث والعشرون: تغيير النوع (Up Casting vs Down Casting)</h4>

<divider>يعني إيه Casting؟</divider>

خلينا نفتكر الأول مصطلح الـ **Casting** اللي أخدناه زمان في بدايات الكورس. الـ Casting ببساطة هو **عملية تغيير نوع المتغير (Data Type) لنوع تاني**. زي مثلاً لما كنا بنحول رقم `float` فيه كسور لرقم `int` صحيح، أو بنحول `string` لـ `int`.

النهارده بقا إحنا هنتكلم عن الـ Casting بس جوه عالم الـ **OOP** (البرمجة الكائنية). هنا إحنا مش بنغير أرقام ونصوص، إحنا بنحاول نغير نوع "الكائنات" (Objects)! وفي الـ OOP عندنا نوعين أساسيين من التحويل ده، ولازم نأكد على معلومة مهمة جداً قبل ما نبدأ:

<note type="warn">عملية الـ Casting بين الكلاسات بتتم في الغالب عن طريق استخدام الـ <b>Pointers (المؤشرات)</b>.</note>

<divider>أنواع الـ Casting في الـ OOP</divider>

عشان نفهم الفكرة اللي في الصورة، تخيل إن عندنا كلاس أب `Person` (شخص عادى) وكلاس وريث `Employee` (موظف).
هل ينفع أتعامل مع كائن الموظف على إنه مجرد شخص عادي؟ وهل ينفع العكس؟ ده اللي بيحدده النوعين دول:

<cmp>
<good title="⬆️ الـ Up Casting (التحويل للأعلى)">

* <b>معناه:</b> تحويل كائن من نوع "الوريث" (Employee) ليتصرف ككائن من نوع "الأب" (Person).
* <b>هل مسموح؟</b> <t color="lime">نعم (Valid) ✅</t>.
* <b>ليه؟</b> لأن أي "موظف" هو بالضرورة "شخص". فمن المنطقي جداً إني أقدر أشاور على الموظف بمؤشر من نوع شخص عادي، لأن الموظف جواه كل الخصائص الأساسية للشخص.

</good>
<bad title="⬇️ الـ Down Casting (التحويل للأسفل)">

* <b>معناه:</b> تحويل كائن من نوع "الأب" (Person) ليتصرف ككائن من نوع "الوريث" (Employee).
* <b>هل مسموح؟</b> <t color="rose">لا (Invalid) ❌</t>.
* <b>ليه؟</b> لأن مش كل "شخص" هو بالضرورة "موظف". الشخص العادي مفيش فيه متغيرات زي "الراتب" أو "القسم"، فلو حاولت أحوله لموظف، المترجم مش هيلاقي البيانات دي وهيرفض التحويل لأنه غير منطقي.

</bad>
</cmp>

---

<divider>تطبيق الـ Casting في الكود خطوة بخطوة</divider>

عشان نثبت الفكرة، هنطبقها عملي على الأكواد ونستخدم الـ Pointers (المؤشرات) زي ما اتفقنا.

<b>1. بناء الكلاسات الأساسية:</b>
عندنا كلاس الشخص (الأب) وفيه متغير `FullName`، وكلاس الموظف (الوريث) وفيه متغير `Title`.

```cpp
#include <iostream>
using namespace std;

class clsPerson
{
public:
    string FullName="Mohammed Abu-Hadhoud";
};

class clsEmployee : public clsPerson
{
public:
    string Title = "CEO";
};
```

<b>2. إنشاء كائن الموظف العادي:</b>
في دالة الـ `main`، هنعمل كائن موظف عادي ونطبع اسمه (واللي بطبيعة الحال ورثه من الأب):

```cpp
int main()
{
    clsEmployee Employee1;
    cout << Employee1.FullName << endl; // هتطبع: Mohammed Abu-Hadhoud
```

<b>3. عملية الـ Up Casting (الناجحة):</b>
هنا هنعمل مؤشر (Pointer) نوعه `clsPerson *` (الأب)، والمفاجأة إننا هنخليه يخزن عنوان الكائن `Employee1` (الوريث)!
العملية دي تمت بنجاح وبدون أي Error لأن كل موظف هو بالفعل شخص.

```cpp
    // This will convert employee to person.
    clsPerson * Person1 = &Employee1; 
```

دلوقتي، المؤشر `Person1` بيشاور على الموظف، بس هو "شايفه" كـ شخص عادي بس! 


يعني إيه؟ يعني لو طبعنا `Person1->FullName` هتطبع معاك عادي لأن الاسم خاصية للموظف وللشخص كمان. لكن لو حاولت تنادي على `Person1->Title` (اللي هو التايتل بتاع الموظف) هيديك Error، لأن المؤشر ده نوعه `Person` وميعرفش حاجة عن التايتل.

```cpp
    cout << Person1->FullName << endl; // ✅ عملية ناجحة، المؤشر بيقرا الخصائص المشتركة
```

<b>4. عملية الـ Down Casting (المرفوضة):</b>
لو حاولنا نعمل العكس: نكرييت شخص عادي، ونحاول نخلي مؤشر من نوع موظف يشاور عليه..

```cpp
    // clsEmployee* Employee2 = &Person2; // ❌ سطر هيدي إيرور يوقف البرنامج
```

 لغة C++ بترفض الـ Down Casting التلقائي للـ Pointers، لأنك بتحاول تفهمها إن الشخص العادي ده موظف وعنده Title، وده مش حقيقي (معندوش مساحة في الذاكرة لمتغير الـ Title).

<note type="success">

<b>الخلاصة:</b> هي إن (الابن يقدر يتصرف كأنه أب، لكن الأب مقدرش أعامله معاملة الابن)، والعملية دي بتتم عن طريق الـ Pointers <code>*</code> واللي بتخلي المؤشر يعاملك من منطلق هو (نوعه إيه)، مش من منطلق (هو بيشاور على إيه).

</note>


<br-page></br-page>
<a id="l-virtual-functions"></a>
<lesson color="indigo">Virtual Functions</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الرابع والعشرون: الدوال الافتراضية (Virtual Functions)</h4>

عندنا كلاس أب `clsPerson` وكلاسين ورثة (`clsEmployee` و `clsStudent`)، وكل واحد فيهم عنده نسخته الخاصة من دالة `Print()`:

```cpp
#include <iostream>
using namespace std;

class clsPerson {
public:
    void Print() { cout << "Hi, i'm a person!\n"; }
};

class clsEmployee : public clsPerson {
public:
    void Print() { cout << "Hi, I'm an Employee\n"; }
};

class clsStudent : public clsPerson {
public:
    void Print() { cout << "Hi, I'm a student\n"; }
};

int main() {
    clsEmployee Employee1;
    clsStudent Student1;
    Employee1.Print();
    Student1.Print();
}
```
<out>
Hi, I'm an Employee
Hi, I'm a student
</out>

ده سلوك طبيعي ومتوقع، وده الـ **Function Overriding** اللي اخدناه قبل كده. كل كائن بينادي الدالة الخاصة بالكلاس بتاعه.

<br-page></br-page>

<divider>المفاجأة: لما نعمل Up Casting</divider>

دلوقتي هنضيف سطرين في الـ `main`. زي ما اتعلمنا في الدرس الفائت (Up Casting)، هنعمل مؤشرين من نوع الأب `clsPerson *` ونخليهم يشاوروا على كائنات الورثة:

```cpp
    clsPerson * Person1 = &Employee1; // مؤشر أب بيشاور على موظف
    clsPerson * Person2 = &Student1;  // مؤشر أب بيشاور على طالب

    Person1->Print();
    Person2->Print();
```
<out>
Hi, i'm a person!
Hi, i'm a person!
</out>

مع إن `Person1` جاي من `Employee` و `Person2` جاي من `Student`، والاتنين عندهم دالة `Print()` خاصة بيهم عادي، **مع ذلك اللي اشتغل هي دالة الـ `Person` فقط!** لا دالة الموظف شغلت ولا دالة الطالب.

**السبب:** لأن المؤشر نوعه `clsPerson *`، والمؤشر العادي بيشغل الدالة حسب نوعه هو، مش حسب الكائن اللي بيشاور عليه. فالـ Overriding اللي عملناه ولا كأنه حصل!

---

<divider>الحل: كلمة virtual</divider>

عشان نخلي المؤشر يحترم الـ Overriding ويشغل الدالة الصح بتاعة الكائن الأصلي، كل اللي محتاجين نعمله هو إضافة كلمة `virtual` قبل الدالة **في كلاس الأب**:

```cpp
class clsPerson {
public:
    virtual void Print() { cout << "Hi, i'm a person!\n"; }
};
```

دلوقتي لو شغلنا نفس الكود بالظبط:

```cpp
    Person1->Print();
    Person2->Print();
```
<out>
Hi, I'm an Employee
Hi, I'm a student
</out>

كل مؤشر شغّل الدالة الصح بتاعة الكائن اللي بيشاور عليه!

---

<divider>يعني كلمة virtual بتعمل إيه بالظبط؟</divider>

كلمة `virtual` بتقول للمترجم: **"لما تيجي تشغل الدالة دي من خلال مؤشر، متبصش على نوع المؤشر، بص على نوع الكائن الفعلي اللي المؤشر بيشاور عليه، وشغل الدالة الخاصة بيه."**

* **بدون `virtual`:** المترجم بيبص على **نوع المؤشر** ← ولأنه `clsPerson *` بيشغل `clsPerson::Print()`.
* **مع `virtual`:** المترجم بيبص على **نوع الكائن الحقيقي** ← ولأنه `Employee` أو `Student` بيشغل الدالة بتاعتهم.

<note type="success">

<b>الخلاصة:</b> كلمة <code>virtual</code> بتضمن إن الـ Overriding يفضل شغال حتى لما نستخدم الـ Pointers والـ Up Casting. من غيرها، المؤشر بيتجاهل الدالة الجديدة ويرجع للأصل.

</note>

<br-page></br-page>
<a id="l-staticearly-binding-vs-dynamiclate-binding"></a>
<lesson color="indigo">Static/Early Binding vs Dynamic/Late Binding</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الخامس والعشرون: الربط المبكر والربط المتأخر</h4>

الدرس ده مبني على الدرس اللي فات (Virtual Functions) مباشرةً. كل اللي هنعمله هنا هو إننا **ندي أسماء علمية** للسلوكين اللي شوفناهم.

<divider>التسميتين</divider>

لما المترجم بيحدد أي دالة يشغلها، عنده طريقتين:

<defs>

<def term="1. الربط المبكر / الساكن (Static / Early Binding)">

المترجم بيحدد الدالة اللي هيشغلها **وقت الترجمة (Compilation Time)** — قبل ما البرنامج يشتغل أصلاً.
<br>ده اللي بيحصل لما بتنادي الدالة **من الكائن مباشرة** (بدون مؤشرات).

</def>

<def term="2. الربط المتأخر / الديناميكي (Dynamic / Late Binding)">

المترجم **مش بيحدد** الدالة وقت الترجمة، بل بيستنى لحد ما البرنامج **يشتغل فعلاً (Runtime)** ويشوف الكائن الحقيقي اللي المؤشر بيشاور عليه، وعلى أساسه يقرر يشغل أي دالة.
<br>ده اللي بيحصل لما بتستخدم **مؤشرات + كلمة `virtual`**.

</def>

</defs>

<divider>التطبيق على الكود</divider>

نفس الكلاسات بتاعة الدرس الفائت بالظبط (الدالة `Print` في الأب معمولة `virtual`):

```cpp
int main()
{
    clsEmployee Employee1;
    clsStudent Student1;

    // Early-Static Binding: at compilation time
    Employee1.Print();
    Student1.Print();

    clsPerson * Person1 = &Employee1;
    clsPerson * Person2 = &Student1;

    // Late-Dynamic Binding: at runtime
    Person1->Print();
    Person2->Print();
}
```
<out>
Hi, I'm an Employee
Hi, I'm a student
Hi, I'm an Employee
Hi, I'm a student
</out>

* **أول سطرين** (`Employee1.Print()` و `Student1.Print()`): المترجم عارف من البداية إن `Employee1` نوعه `clsEmployee` فبيقرر وقت الترجمة يشغل دالته ← ده اسمه **Early/Static Binding**.

* **آخر سطرين** (`Person1->Print()` و `Person2->Print()`): المترجم مش عارف وقت الترجمة المؤشر بيشاور على إيه بالظبط، فبيأجل القرار لوقت التشغيل ويبص على الكائن الفعلي ← ده اسمه **Late/Dynamic Binding** (وده بيحصل بسبب كلمة `virtual`).

<note type="success">

<b>الخلاصة:</b> الدرس ده مجرد تسميات علمية. الـ Static Binding هو السلوك العادي، والـ Dynamic Binding هو السلوك اللي بيحصل لما نستخدم `virtual` مع المؤشرات.

</note>

<br-page></br-page>

</wrap>

<cover><cover-circle color="fuchsia">Polymorphism</cover-circle></cover>

<br-page></br-page>


<wrap color="fuchsia">

<a id="l-fourth-principleconcept-of-oop-polymorphism"></a>
<lesson color="fuchsia">Fourth Principle/Concept of OOP: Polymorphism</lesson>

<h4 style="text-align:center;font-size:20px">الدرس السادس والعشرون: المبدأ الرابع — تعدد الأشكال (Polymorphism)</h4>

<divider>مقدمة</divider>

وصلنا أخيراً للمبدأ الرابع والأخير من مبادئ البرمجة الكائنية: **Polymorphism** (تعدد الأشكال).

كلمة Polymorphism أصلها يوناني ومعناها الحرفي "كثير الأشكال" — **Poly** (كثير) + **Morph** (شكل). والفكرة ببساطة شديدة: **إن الحاجة الواحدة (دالة، عملية، أو كائن) تقدر تتصرف بأشكال مختلفة حسب السياق اللي بتُستخدم فيه.**

مثال بسيط جداً: إنت كإنسان عندك "تعدد أشكال" في حياتك اليومية. في البيت إنت "ابن"، في الشغل إنت "موظف"، في الجامعة إنت "طالب". نفس الشخص (الكائن)، لكن بيتصرف بشكل مختلف حسب المكان والموقف.

والخبر الحلو إنك **أنت فعلاً طبقت المبدأ ده عملياً في الدروس اللي فاتت!** النهارده بس هنجمع الخيوط ونفهم إن كل اللي عملناه ده كان اسمه العلمي Polymorphism.

---

<divider>الأربع ركائز اللي بيقوم عليها الـ Polymorphism</divider>

الـ Polymorphism في C++ مبني على 4 أشياء أساسية، وكلهم اتشرحوا قبل كده:

<defs>

<def term="1. Function Overloading (تعدد الدوال)">

**الفكرة:** إنك تعمل أكتر من دالة **بنفس الاسم** بس بباراميترات مختلفة (عدد أو نوع)، والمترجم بيقرر يشغل أنهي واحدة حسب اللي إنت بعته.
<br>**ليه موجودة؟** عشان متضطرش تخترع أسماء مختلفة لدوال بتعمل نفس الوظيفة بس على أنواع بيانات مختلفة. بدل `AddIntegers()` و `AddFloats()` و `AddStrings()`، بتعمل دالة واحدة `Add()` والمترجم يتصرف.

</def>

<def term="2. Operator Overloading (تعدد العمليات)">

**الفكرة:** إن نفس العملية (الرمز) تشتغل بشكل مختلف حسب نوع البيانات اللي بتتعامل معاها.
<br>**مثال واضح:** علامة الجمع `+`:
<br>• لو استخدمتها مع أرقام: `5 + 3` ← بتجمعهم وتطلع `8`.
<br>• لو استخدمتها مع نصوص: `"Hello" + " World"` ← بتلزقهم وتطلع `"Hello World"`.
<br>نفس العلامة، لكن سلوك مختلف تماماً حسب السياق — ده تعدد أشكال!

</def>

<def term="3. Function Overriding (إعادة كتابة الدوال)">

**الفكرة:** إن الكلاس الوريث يكتب نسخة جديدة من دالة موجودة أصلاً في كلاس الأب بنفس الاسم ونفس الشكل، فالوريث يشغل نسخته هو بدل نسخة الأب.
<br>**ليه موجودة؟** عشان الوريث يقدر يعدل سلوك دالة ورثها من الأب عشان تناسب طبيعته الخاصة (زي ما الموظف عدل دالة `Print()` عشان تطبع الراتب كمان).

</def>

<def term="4. Virtual Functions (الدوال الافتراضية)">

**الفكرة:** لما نحط كلمة `virtual` قبل دالة في الأب، المترجم بيأجل قرار "أي دالة يشغل" لوقت التشغيل بدل وقت الترجمة، فالمؤشر بيشغل الدالة الصح بتاعة الكائن الفعلي مش بتاعة نوع المؤشر.
<br>**ليه موجودة؟** عشان الـ Overriding يفضل شغال حتى لما نستخدم الـ Pointers والـ Up Casting، ودي أقوى صورة من صور تعدد الأشكال لأن نفس السطر الواحد من الكود بيطلع نتايج مختلفة حسب الكائن الحقيقي.

</def>

</defs>

<note type="success">

<b>الخلاصة:</b> الـ Polymorphism مش حاجة جديدة هتتعلمها، هو مصطلح بيوصف قدرة الكود إنه يتصرف بأشكال متعددة حسب السياق. وإنت أصلاً بتطبقه كل ما بتعمل Overloading أو Overriding أو تستخدم Virtual Functions.

</note>

<br-page></br-page>
<a id="l-interfaces-pure-virtual-functions-and-abstract-classes"></a>
<lesson color="fuchsia">Interfaces: Pure Virtual Functions and Abstract Classes</lesson>

<h4 style="text-align:center;font-size:20px">الدرس السابع والعشرون: الكلاسات المجردة والدوال الافتراضية النقية</h4>

<divider>المفاهيم الجديدة</divider>

قبل ما ندخل في الكود، لازم نفهم 3 مصطلحات جديدة هنقابلهم في الدرس ده:

<defs>

<def term="1. Pure Virtual Function (دالة افتراضية نقية)">

دي دالة `virtual` عادية زي اللي أخدناها، بس الفرق إنها **مفيهاش أي كود جواها**. بنكتبها وبنحط في آخرها `= 0` بدل ما نكتب جسم الدالة. معنى كده إننا بنقول: "الدالة دي **لازم تتكتب** في أي كلاس يورث مني، أنا مش هكتبها هنا".

</def>

<def term="2. Abstract Class (كلاس مجرد)">

أي كلاس فيه **دالة Pure Virtual واحدة على الأقل** بيتحول أوتوماتيك لكلاس مجرد. الكلاس المجرد ده **مستحيل تعمل منه Object**. هو مجرد "قالب إجباري" بيفرض على اللي يورث منه إنه يكتب كود لكل الدوال النقية.

</def>

<def term="3. Interface / Contract (واجهة / عقد)">

دي مجرد تسمية تانية للـ Abstract Class لما يكون كله دوال نقية وبس بدون أي كود فعلي. بنسميه "عقد" لأنه بيقول: "لو عايز تورث مني، لازم تلتزم بكل البنود (الدوال) دي وتكتب كودها بنفسك".

</def>

</defs>

---

<divider>مثال توضيحي قبل الكود</divider>

تخيل إن وزارة الاتصالات أصدرت قانون بيقول: **"أي موبايل هيتباع في السوق لازم يكون فيه 3 وظائف: يعمل مكالمات، يبعت رسائل، ويصور."**

القانون ده **مش موبايل** — ده مجرد ورقة شروط. مينفعش تمسك القانون وتتصل بيه! لكن أي شركة (Apple, Samsung) عايزة تنزل موبايل **مُجبرة** تلتزم بالشروط دي وتنفذها بطريقتها الخاصة.

في الكود: القانون = الـ **Abstract Class**، والشركات = الـ **كلاسات الوارثة**.

---

<divider>شرح الكود خطوة بخطوة</divider>

### 1. تعريف الـ Abstract Class (العقد)

أول حاجة هنعرف الكلاس المجرد `clsMobile` اللي فيه 3 دوال نقية. لاحظ إن كل دالة مكتوب في آخرها `= 0` وده اللي بيخليها Pure:

```cpp
#include <iostream>
using namespace std;

// Abstract Class / Interface / Contract.
class clsMobile
{
    virtual void Dial(string PhoneNumber) = 0;
    virtual void SendSMS(string PhoneNumber, string Text) = 0;
    virtual void TakePicture() = 0;
};
```

الكلاس ده دلوقتي يعتبر **عقد**. مينفعش تكتب `clsMobile M1;` لأنه مفيهوش كود فعلي — هو مجرد "قائمة مطالب".

### 2. أول كلاس وارث: الآيفون

دلوقتي Apple عايزة تنزل موبايل. لازم **تورث** من `clsMobile` وتكتب **كود فعلي** لكل دالة من الـ 3 دوال النقية:

```cpp
class clsiPhone : public clsMobile
{
public:
    void Dial(string PhoneNumber)
    {
        // كود الاتصال بطريقة Apple
    };
  
    void SendSMS(string PhoneNumber, string Text)
    {
        // كود إرسال الرسائل بطريقة Apple
    };

    void TakePicture()
    {
        // كود التصوير بطريقة Apple
    };

    // ممكن تضيف دوال خاصة بيها زيادة عادي
    void MyOwnMethod()
    {

    }
};
```

لاحظ إن `clsiPhone` كتب كود لكل الـ 3 دوال (حتى لو فاضيين دلوقتي)، **وده إجباري**. لو نسي واحدة، المترجم هيرفض يبني البرنامج. وممكن كمان يضيف دوال خاصة بيه زي `MyOwnMethod()` بدون مشاكل.

<br-page></br-page>

### 3. تاني كلاس وارث: سامسونج

نفس الفكرة بالظبط، Samsung بتورث من نفس العقد وبتلتزم بنفس الشروط:

```cpp
class clsSamsungNote10 : public clsMobile
{
public:
    void Dial(string PhoneNumber)
    {
        // كود الاتصال بطريقة Samsung
    };

    void SendSMS(string PhoneNumber, string Text)
    {
        // كود إرسال الرسائل بطريقة Samsung
    };

    void TakePicture()
    {
        // كود التصوير بطريقة Samsung
    };
};
```

### 4. الاستخدام في الـ Main

دلوقتي نقدر نعمل Objects من الكلاسات الحقيقية (iPhone و Samsung) عادي جداً:

```cpp
int main()
{
    clsiPhone iPhone1;        // ✅ مسموح
    clsSamsungNote10 Note10;  // ✅ مسموح

    // clsMobile M1;          // ❌ ممنوع — ده كلاس مجرد مينفعش نعمل منه Object

    system("pause>0");
    return 0;
}
```

---

<divider>خلاصة سريعة</divider>

* لو حطيت `= 0` بعد دالة `virtual` ← بقت **Pure Virtual Function**.
* لو الكلاس فيه دالة Pure واحدة على الأقل ← بقى **Abstract Class** ومينفعش تعمل منه Object.
* أي كلاس يورث من الـ Abstract Class **مُجبر** يكتب كود لكل الدوال النقية، وإلا المترجم هيرفض.

<note type="success">

<b>الخلاصة:</b> الـ Abstract Class بيضمن إن كل الكلاسات اللي بتورث منه ملتزمة بنفس الهيكل. لو فريق من 20 مبرمج كل واحد بيعمل كلاس مختلف، العقد ده بيمنع حد ينسى دالة أو يسميها اسم غلط — المترجم نفسه هيوقفه.

</note>

</wrap>

<br-page></br-page>

<cover><cover-circle color="emerald">Friends</cover-circle></cover>

<br-page></br-page>

<wrap color="emerald">

<a id="l-friend-class"></a>
<lesson color="emerald">Friend Class</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثامن والعشرون: الكلاس الصديق (Friend Class)</h4>

<divider>مراجعة سريعة للصلاحيات</divider>

إحنا عرفنا إن كل كلاس بيبني حوالين نفسه جدار حماية (Access Specifiers) عشان يتحكم في مين يشوف بياناته:
- **Public:** متاح للجميع (جوه وبره الكلاس).
- **Protected:** متاح للكلاس نفسه ولأولاده (الورثة) فقط.
- **Private:** متاح للكلاس نفسه **حصراً**، وممنوع على أي حد بره يلمسه حتى لو كان ابنه الوريث.

<divider>مفهوم الـ Friend Class</divider>

طب ماذا لو عندنا كلاس تانية، لا هي الأب ولا هي ابنه الوريث، لكن عايزين نديها "صلاحيات استثنائية"؟ 

تخيل إن الكلاس التانية دي قدرت عن طريق "الرشوة" إنها تاخد الصلاحية الكاملة؛ يعني مش بس تشوف الـ <t color="lime">Public</t> والـ <t color="sky">Protected</t>، دي كمان تقدر تخترق الجدار وتوصل للـ <t color="rose">Private members</t>!

في C++ بنعمل الحركة دي عن طريق الـ Keyword اللي اسمها <hl color="emerald">friend</hl>. إنت هنا بتقول للمترجم: "الكلاس دي صاحبتي، افتحلها كل الأبواب".

<br-page></br-page>

بص على السطر السحري في <t color="amber">clsA</t> وهو بيدي الصلاحية لـ <t color="teal">clsB</t>:

```cpp
class clsA {
private:
    int _Var1 = 10;
protected:
    int _Var3 = 30;
public:
    int Var2 = 20;

    // السطر ده بيدي صلاحية مطلقة لـ clsB للوصول لكل شيء هنا
    friend class clsB; 
};

class clsB {
public:
    void display(clsA A1) {
        // لاحظ إن clsB قدرت توصل للـ Private والـ Protected بسهولة!
        cout << "\nVar1 (Private)   = " << A1._Var1;
        cout << "\nVar2 (Public)    = " << A1.Var2;
        cout << "\nVar3 (Protected) = " << A1._Var3;
    }
};

int main() {
    clsA A1;
    clsB B1;
    B1.display(A1);
    return 0;
}
```

<divider>النتيجة المترتبة</divider>

بمجرد ما كتبت <t color="emerald">friend class clsB;</t> جوه الكلاس الأولى:
1. أي دالة جوه <t color="teal">clsB</t> تقدر تقرأ وتعدل المتغيرات الـ <t color="rose">Private</t> بتاعة <t color="amber">clsA</t>.
2. كلاس <t color="teal">clsB</t> بقت بتمتلك "مفاتيح" الكلاس الأولى بالكامل.

<note type="warn">

⚠️ <b>تنبيه:</b> الصداقة في C++ <b>ليست متبادلة</b>. يعني لو A صديق لـ B، ده مش معناه إن B صديق لـ A أوتوماتيكياً. الصداقة لازم تُمنح من صاحب الشأن (صاحب البيانات الحساسة).

</note>

<a id="l-friend-functions"></a>
<lesson color="emerald">Friend Functions</lesson>

<h4 style="text-align:center;font-size:20px">الدرس التاسع والعشرون: الدوال الصديقة (Friend Functions)</h4>

<divider>الرشوة للدوال المستقلة</divider>

في الدرس اللي فات، عرفنا إننا ممكن ندّي صلاحية لكلاس تانية بالكامل. طب هل ممكن ندّي "الرشوة" دي لدالة واحدة بس؟ ودالة مش تابعة لأي كلاس كمان (Standalone Function)؟

الإجابة هي أيوة. لو عندك دالة عادية جداً بره أي كلاس، وعايز تخليها تقدر تدخل جوه "ممنوعات" الكلاس وتشوف الـ <t color="rose">Private</t> والـ <t color="sky">Protected</t>، بنستخدم نفس الـ Keyword وهي <hl color="emerald">friend</hl>.

---

<divider>تطبيق الكود</divider>

بص على الدالة <t color="purple">MySum</t>، هي دالة عادية خالص، بس الكلاس <t color="amber">clsA</t> "صاحبتها" ومدياها تصريح:

```cpp
class clsA {
private:
    int _Var1 = 10;
protected:
    int _Var3 = 30;
public:
    int Var2 = 20;

    // دي "شهادة صداقة" للدالة؛ بتقول للمترجم مسموح لـ MySum تشوف اللي جوه
    friend int MySum(clsA A1); 
};

// لاحظ إن الدالة دي "غريبة" ومش تابعة للكلاس (Normal Function)
int MySum(clsA A1) {
    // بفضل الصداقة، قدرت تجمع الـ Private والـ Protected بسهولة
    return A1._Var1 + A1.Var2 + A1._Var3;
}

int main() {
    clsA A1;
    cout << "Sum = " << MySum(A1); // 10 + 20 + 30 = 60
    return 0;
}
```

<divider>السطر المهم والنتيجة</divider>

السطر الأساسي هنا هو: <t color="emerald">friend int MySum(clsA A1);</t>
1. إنت هنا مش بتعرّف دالة جوه الكلاس، إنت بس بتسجل "اسم الدالة" وبتقول إنها صديقة ومسموح لها بالدخول.
2. النتيجة: الدالة <t color="purple">MySum</t> بتقدر تكسر حاجز الـ <t color="rose">Private</t> وتنفذ وظيفتها، رغم إن أي دالة تانية غريبة لو حاولت تعمل كدة هيطلع لها Error فوراً.

</wrap>

<br-page></br-page>

<cover><cover-circle color="lavender">Misc</cover-circle></cover>

<br-page></br-page>

<wrap color="lavender">

<a id="l-structure-inside-class"></a>
<lesson color="lavender">Structure Inside Class</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثلاثون: الستركتشر داخل الكلاس (Structure Inside Class)</h4>

ببساطة شديدة، زي ما إحنا عارفين إن الكلاس ممكن يحتوي على متغيرات ودوال، فمن حقنا كمان نعرّف جواها **Structure** كامل خاص بينا. بنستخدم الحركة دي لما نكون محتاجين نجمع مجموعة بيانات مرتبطة ببعضها جوه الكلاس بس مش مستاهلة نعملها كلاس مستقلة.

---

<divider>مثال سريع</divider>

```cpp
class clsPerson {
public:
    // تعريف ستركشر جوه الكلاس
    struct stAddress {
        string Street;
        string City;
    };

    string FullName;
    stAddress Address; // إنشاء متغير من نوع الستركشر اللي فوق
};

int main() {
    clsPerson Person1;
    Person1.FullName = "Mohammed Abu-Hadhoud";
    Person1.Address.Street = "Queen Rania Street";
    Person1.Address.City = "Amman";
}
```

<note type="success">
✅ <b>الخلاصة:</b> الـ Structure جوه الكلاس وسيلة ممتازة لتنظيم البيانات المتشابهة في "كتلة واحدة" لسهولة التعامل معاها.
</note>

<br-page></br-page>

<a id="l-nested-classes"></a>
<lesson color="lavender">Nested Classes</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الواحد والثلاثون: الكلاس المتداخل (Nested Classes)</h4>

بنفس منطق الستركتشر، إحنا نقدر نعرّف "كلاس جوه كلاس". المصطلح العلمي للموضوع ده هو **Nested Class** أو الأهم والأشهر: **Inner Class**.

الهدف منها هو التنظيم؛ يعني لو عندك كلاس وظيفته الوحيدة إنه يخدم على كلاس تانية، ممكن تخليه "عضو" جواها بدل ما تسيبه بره سايح في الكود.

---

<divider>تطبيق الكود</divider>

بص على كلاس <t color="amber">clsAddress</t> وهو مستخبي جوه <t color="teal">clsPerson</t>:

```cpp
class clsPerson {
    // Inner Class: كلاس داخل الكلاس الأساسي
    class clsAddress {
    public:
        string City, Country;
        void Print() {
            cout << "\nAddress: " << City << ", " << Country << endl;
        }
    };

public:
    string FullName;
    clsAddress Address; // بنستخدم الـ Inner Class كعضو عادي

    clsPerson() {
        FullName = "Mohammed Abu-Hadhoud";
        Address.City = "Amman";
        Address.Country = "Jordan";
    }
};

int main() {
    clsPerson Person1;
    Person1.Address.Print(); // وصول مباشر لبيانات الكلاس الداخلي
    return 0;
}
```

<note type="success">

 الـ <b>Inner Class</b> بيخلي الكود "أنضف" وأكثر تماسكاً، لأنك بتخبي التفاصيل اللي بتخص الكلاس ده بس جواه.
 
</note>


<br-page></br-page>

<a id="l-passing-objects-to-functions"></a>
<lesson color="lavender">Passing Objects to Functions (ByRef/ByVal)</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثاني والثلاثون: تمرير الكائنات للدوال</h4>

الفكرة هي إن الكائنات بيتم التعامل معاها زي أي متغير عادي لما نيجي نبعتها لدالة. بنقدر نبعتها بالقيمة (By Value) أو بالمرجع (By Reference).

---

<divider>تطبيق الكود</divider>

```cpp
class clsA {
public:
    int x;
};

// Passing By Value (Creates a copy)
void Fun1(clsA A1) {
    A1.x = 100;
}

// Passing By Reference (No copy, saves memory)
void Fun2(clsA &A1) {
    A1.x = 200;
}

int main() {
    clsA A1;
    A1.x = 10;

    Fun1(A1); // x will stay 10
    Fun2(A1); // x will become 200
}
```

<note type="success">
الـ <b>ByRef</b> أفضل دائماً مع الكائنات لأنه بيوفر استهلاك الذاكرة (مبيعملش نسخة تانية)، وبيدينا صلاحية نعدل على الكائن الحقيقي.
</note>

<br-page></br-page>

<a id="l-objects-and-vectors"></a>
<lesson color="lavender">Objects and Vectors</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الثالث والثلاثون: الكائنات والـ Vector</h4>

إحنا درسنا الـ Vector كطريقة لتخزين البيانات الديناميكية، وبنفس الطريقة بالظبط نقدر نخزن جواه مجموعة من الكائنات.

---

<divider>تطبيق الكود</divider>

```cpp
#include <vector>

class clsA {
public:
    int x;
    clsA(int val) { x = val; }
    void Print() { cout << "Value: " << x << endl; }
};

int main() {
    vector<clsA> vObjects;

    // Adding objects to vector
    vObjects.push_back(clsA(10));
    vObjects.push_back(clsA(20));

    // Accessing objects
    for (clsA &obj : vObjects) {
        obj.Print();
    }
}
```

<br-page></br-page>

<a id="l-objects-and-dynamic-array"></a>
<lesson color="lavender">Objects and Dynamic Array</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الرابع والثلاثون: الكائنات والمصفوفات الديناميكية</h4>

زي ما بنعمل مصفوفة أرقام ديناميكية باستخدام كلمة `new` ونوع البيانات، بنقدر نعمل مصفوفة من الأوبجيكتات بنفس الطريقة.

---

<divider>تطبيق الكود</divider>

```cpp
class clsA {
public:
    int x = 5;
};

int main() {
    // Creating dynamic array of 3 objects
    clsA* arr = new clsA[3]; 

    arr[0].x = 10;
    arr[1].x = 20;

    // Always remember to free memory
    delete[] arr;
}
```

<br-page></br-page>

<a id="l-objects-with-parameterized-constructor-and-array"></a>
<lesson color="lavender">Objects with Parameterized Constructor and Array</lesson>

<h4 style="text-align:center;font-size:20px">الدرس الخامس والثلاثون: الأوبجيكت بكونستراكتور ومصفوفة</h4>

التحدي هنا إن المصفوفة العادية بتنادي الـ Default Constructor. لو عايزين نبعت قيم للكونستراكتور وإحنا بنعمل مصفوفة، بنستخدم الـ **Initialization List**.

---

<divider>تطبيق الكود</divider>

```cpp
class clsA {
public:
    int x;
    clsA(int val) { x = val; }
};

int main() {
    // Array on stack with constructor values
    clsA arr[2] = { clsA(10), clsA(20) };

    // Dynamic array with constructor values
    clsA* arr2 = new clsA[2] { clsA(30), clsA(40) };

    delete[] arr2;
}
```

<note type="success">
الحركة دي بتخلينا نكون أكثر تحكماً في حالة كل أوبجيكت لحظة ولادته جوه المصفوفة.
</note>

</wrap>

</wrap>

<cover><cover-circle color="cyan">Other</cover-circle></cover>

<br-page></br-page>

<wrap color="cyan">

<a id="l-this-pointer"></a>
<lesson color="cyan">‘this’ pointer</lesson>

<h4 style="text-align:center;font-size:20px">الدرس السادس والثلاثون: مؤشر الكائن الحالي (this pointer)</h4>

كلمة **this** في C++ هي واحدة من أهم المفاهيم اللي بتنقل شغلك لمستوى المحترفين. ببساطة، هي "مؤشر مخفي" (Hidden Pointer) بيشاور على **الأوبجيكت اللي الكلام عليه دلوقتي**.

تخيل لو عندك 100 موظف (100 Objects)، لما تنادي دالة الطباعة لموظف معين، الكلاس بتبقى محتاجة تعرف هي بتطبع بيانات أنهي موظف فيهم؟ الـ <hl color="cyan">this</hl> هو اللي بيقولها: "اشتغلي على (أنا) شخصياً".

---

<divider>فلسفة الـ this وكيف تعمل؟</divider>

- **ليست كائناً بل مؤشرًا:** الـ `this` مش الأوبجيكت نفسه، هي **عنوانه** في الذاكرة. وعشان كدة إحنا بنتعامل معاها معاملة الـ Pointers.
- **داخل نطاق الكلاس فقط:** الـ `this` مسموح بها فقط داخل دوال الكلاس (Member Functions). لو حاولت تستخدمها بره (زي الـ main) المترجم هيرفض.
- **لماذا نستخدم السهم <t>-></t> ؟** لأن `this` مؤشر، والسهم هو الأداة اللي "بتدخلنا جوه" المؤشر عشان نوصل للمتغيرات (Members) بتاعته.

---

<divider>الحالة الأولى: فض الاشتباك (Shadowing)</divider>

ليه الغلبة دي؟ أوقات بنحب نسمي الباراميترز اللي داخلة للدالة بنفس اسم المتغيرات الأساسية جوه الكلاس (عشان الكود يكون مفهوم). هنا المترجم بيحصله حالة "ارتباك"، مبيعرفش مين ابن الكلاس ومين الضيف اللي جاي في الدالة.

بص على المثال ده:

```cpp
class clsEmployee {
public:
    int ID; // Member Variable

    clsEmployee (int ID) { // Parameter with same name
       // لو كتبت ID = ID; المترجم هيفتكرك بتساوي الباراميتر بنفسه!
       
       this->ID = ID; 
       // this->ID : دي الخاصة بالاوبجيكت
       // ID : الباراميتر اللي جاي من بره
    }
};
```

---

<divider>الحالة الثانية: فك المؤشر (Dereferencing) </divider>

دي النقطة اللي بتلخبط ناس كتير:
- **this:** هي العنوان (Address).
- **\*this:** هي الكيان نفسه أو البيت (The Object itself).

**ليه بنحتاجها؟**
ساعات بنبقى جوه دالة، وعايزين نبعت الأوبجيكت "بالكامل" لدالة تانية (عادةً بتكون دالة static أو دالة بره الكلاس) عشان تعمل عليه عمليات تانية. الدالة التانية دي مستنية "Object" مش مستنية "Address".

بص على تقسيم الكود ده عشان تفهم الحركة دي:

```cpp
class clsEmployee {
public:
    int ID; string Name; float Salary;

    clsEmployee(int ID, string Name, float Salary) {
        this->ID = ID;
        this->Name = Name;
        this->Salary = Salary;
    }

    // دالة static بتستقبل "أوبجيكت كامل" وتطبعه
    static void Func1(clsEmployee Employee) {
        Employee.Print();
    }

    // دالة عادية جوه الكلاس
    void Func2() {
        // هنا "أنا" (this) عايز أبعت "نفسي" كأوبجيكت لـ Func1
        // بما إن this مؤشر (عنوان)، لازم "أفكه" بعلامة الـ * عشان تطلع قيمته (الأوبجيكت)
        Func1(*this); 
    }

    void Print() {
        cout << ID << "  " << Name << "  " << Salary << endl;
    }
};
```

<note type="warn">
⚠️  لو بعت `this` بس، إنت بتبعت "رقم العنوان". لو بعت `*this` إنت بتبعت "الأوبجيكت بكل بياناته".
</note>

<note type="success">
 الـ <b>this</b> هو "ضمير المتكلم" للكلاس. بنستخدمه عشان نفصل بين المتغيرات المتشابهة في الأسامي، أو عشان نبعت الأوبجيكت اللي إحنا واقفين عليه لدالة تانية محتاجة تتعامل معاه ككيان كامل.
</note>

<br-page></br-page>

<a id="l-separate-classes-in-libraries"></a>
<lesson color="cyan">Separate Classes In Libraries</lesson>

<h4 style="text-align:center;font-size:20px">الدرس السابع والثلاثون: فصل الكلاسات في مكتبات مستقلة</h4>

بدل ما نكتب كل الكلاسات جوه الكود الرئيسي (Main Code)، الأحسن والأنضف إننا نفصل كل كلاس في "ملف لوحده". ده بيخلي الكود منظم جداً، سهل الصيانة، ومتقسم بشكل احترافي.

---

<divider>خطوات العمل في Visual Studio</divider>

<steps>

1. من القائمة فوق اختار **View** ثم **Solution Explorer**.
2. كليك يمين على فولدر **Header Files** واختار **Add** ثم **Class**.
3. سمي الكلاس بنفس الاسم (مثلاً `clsPerson`).
4. هتلاقي ملف جديد اتفتح باسم `clsPerson.h`.
5. امسح كل اللي فيه وحط الكلاس بتاعك اللي إنت "قصيته" من الكود الرئيسي.

</steps>

---

<divider>تجهيز ملف الـ Header</divider>

لازم تتأكد إن ملف الـ Header (`.h`) بيبدأ بالأساسيات دي عشان الأكواد اللي جواه تشتغل:

```cpp
#pragma once  // أهم سطر (هنشرحه تحت)

#include <iostream>
using namespace std;

class clsPerson {
    // Your class code here
};
```

وبعد كدة، في الملف اللي فيه الـ **main**، كل اللي عليك تعمله هو إنك تنادي الملف ده:

```cpp
#include "clsPerson.h" // بنستخدم علامات التنصيص للملفات اللي إحنا صانعينها

int main() {
    clsPerson Person1; // شغال تمام!
}
```

---

<divider>التعامل مع الوراثة والمشكلة الكبري</divider>

لو عندك كلاس `clsEmployee` وريث من `clsPerson` وكل واحد في ملف منفصل، لازم تروح لملف الموظف وتعمل Header لملف الشخص عشان يشوفه:

```cpp
// Inside clsEmployee.h
#include "clsPerson.h"

class clsEmployee : public clsPerson { ... };
```

**المشكلة:** كدة ملف `clsPerson.h` تم استدعاؤه مرتين؛ مرة في الـ main ومرة جوه ملف الـ Employee. المترجم هيطلع Error ويقولك الكلاس ده "متعرف مرتين"!

<divider>الحل السحري: #pragma once</divider>

السطر ده بنكتبه في **أول سطر** في أي ملف Header بنعمله:

```cpp
#pragma once
```

**فايدته:** بيقول للمترجم: "يا معلم، لو الملف ده تم استدعاؤه أكتر من مرة في البرنامج، اعتبر المرة الأولى بس وتجاهل أي مرة تانية". كدة المشاكل هتتحل والكود هيشتغل زي الفل.

<note type="success">

 الـ <b>Library Separation</b> هي الطريقة اللي بيشتغل بيها المبرمجين في المشاريع العملاقة. كل "Concept" في ملف لوحده، وكله مربوط ببعضه عن طريق الـ <b>Header Files</b> والـ <b>#pragma once</b>.

</note>

</wrap>

#### انتهى بفضل الله فقط
## للي بيسأل : ازاي تم كتابة الملخص ؟
الملخص ده مكتوب فقط بالكود من اللغتين الوصفيتين : **Html** , **CSS** 

و بما الملف مجرد كود html + css فنا استخدمت أداة بتشتغل بالبايثون منزلها من جيت هاب عشان استخدمها في تحويل الملف ل pdf , بالمناسبة في مليون طريقة تانية للتحويل


<a href="https://github.com/aboda-0100011/C10" download>اتفضل الملف قبل الحتويل لو انت عايز تشغله عندك في المتصفح كـ **Localhost** 
</a>

بالمناسبة الملف كان في الاول مارك داون بعدين حولته html , بس لو هتعمل بنفسك متعملش كده

---

عموما نيجي للجزء المهم : كتبت كل ده بنفسك ؟ 
لا 

جزء الcss مكتوب تماما باستخدام موديلات ai طيب هتقولي ايه الموديل القوي اللي عرف يعمل كل ده أو ايه البرومبيت القوي اللي قدر يوصف كل ده

مفيش واحد معين , الملف ده عبارة عن موديلات ذكاء اصطناعي كتير اوي اشتغلو مع بعض باستخدام برومبتات كتير اوي اوي قعدت اوصفها علي مدار اسبوعين متواصلين 

فضلت شوية بشتغل علي كلاود في الاول بعدها بشوية حولت ل جيميناي برو و بعدها بشوية حولت من استخدم VS code لاستخدام Antigravity و من الAntigravity استخدمت موديلات جيميناي برضو و كلاود بس عموما الcss كان نتاج تعب وصفي دقيق جدا

طب بالنسبة للhtml كتبته بنفسك؟ نوعا ما

انا كتبت شوية دروس بنفسي ولكن معظم الدروس برضو كانت نتاج وصف دقيق للموضوع اللي هيتم شرحه و ازاي هيتم شرحه باظبط و ايه النقاط اللي هيتم شرحها 

انا وصفت كل حاجة وراجعت كل كلمة تم كتابتها و عدلت كل الدروس بنسب متفاوتة بحيث يكون الكلام أوضح أو يكون طالع من انسان مش من آلة 

#### و بس كدا يباشا و أسألك الدعاء