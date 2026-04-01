<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>قهوتي - نظام نقطة البيع الاحترافي</title>
  <meta name="description" content="نظام نقاط بيع احترافي لإدارة مقاهيك ومطاعمك - قهوتي">
  <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;900&display=swap" rel="stylesheet">
  <style>
    :root {
      --gold: #c8a96e;
      --gold-light: #e8c98e;
      --gold-dark: #a07840;
      --dark: #0e0e0e;
      --surface: #161616;
      --surface2: #1e1e1e;
      --text: #e8e8e8;
      --text-sec: #888;
    }
    
    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body {
      font-family: 'Tajawal', sans-serif;
      background: var(--dark);
      color: var(--text);
      line-height: 1.8;
    }
    
    header {
      background: linear-gradient(135deg, var(--surface) 0%, var(--dark) 100%);
      padding: 20px 5%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid rgba(200, 169, 110, 0.2);
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 100;
    }
    
    .logo {
      font-size: 1.8rem;
      font-weight: 900;
      color: var(--gold);
      display: flex;
      align-items: center;
      gap: 10px;
    }
    
    nav a {
      color: var(--text);
      text-decoration: none;
      margin-right: 30px;
      font-weight: 500;
      transition: color 0.3s;
    }
    
    nav a:hover { color: var(--gold); }
    
    .btn {
      background: linear-gradient(135deg, var(--gold), var(--gold-light));
      color: #1a1a1a;
      padding: 12px 30px;
      border: none;
      border-radius: 8px;
      font-family: 'Tajawal', sans-serif;
      font-size: 1rem;
      font-weight: 700;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    
    .btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 30px rgba(200, 169, 110, 0.3);
    }
    
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 120px 5% 80px;
      background: linear-gradient(180deg, var(--dark) 0%, var(--surface) 50%, var(--dark) 100%);
      position: relative;
      overflow: hidden;
    }
    
    .hero::before {
      content: '';
      position: absolute;
      top: 20%;
      left: 10%;
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, rgba(200, 169, 110, 0.1) 0%, transparent 70%);
      border-radius: 50%;
    }
    
    .hero-content {
      max-width: 600px;
      z-index: 1;
    }
    
    .hero h1 {
      font-size: 3.5rem;
      font-weight: 900;
      color: var(--gold);
      margin-bottom: 20px;
      line-height: 1.2;
    }
    
    .hero p {
      font-size: 1.3rem;
      color: var(--text-sec);
      margin-bottom: 30px;
    }
    
    .hero-btns {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }
    
    .hero-img {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      width: 600px;
      height: 400px;
      background: linear-gradient(135deg, var(--surface2), var(--surface));
      border-radius: 20px;
      border: 2px solid var(--gold);
      opacity: 0.3;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 5rem;
    }
    
    .features {
      padding: 100px 5%;
      background: var(--surface);
    }
    
    .section-title {
      text-align: center;
      font-size: 2.5rem;
      font-weight: 900;
      color: var(--gold);
      margin-bottom: 15px;
    }
    
    .section-subtitle {
      text-align: center;
      color: var(--text-sec);
      margin-bottom: 60px;
      font-size: 1.1rem;
    }
    
    .features-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .feature-card {
      background: var(--surface2);
      border: 1px solid rgba(200, 169, 110, 0.1);
      border-radius: 15px;
      padding: 30px;
      transition: transform 0.3s, border-color 0.3s;
    }
    
    .feature-card:hover {
      transform: translateY(-5px);
      border-color: var(--gold);
    }
    
    .feature-icon {
      font-size: 3rem;
      margin-bottom: 15px;
    }
    
    .feature-card h3 {
      color: var(--gold-light);
      margin-bottom: 10px;
      font-size: 1.2rem;
    }
    
    .feature-card p {
      color: var(--text-sec);
      font-size: 0.95rem;
    }
    
    .screenshots {
      padding: 100px 5%;
      background: var(--dark);
    }
    
    .screenshots-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
      gap: 30px;
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .screenshot {
      background: var(--surface);
      border-radius: 15px;
      overflow: hidden;
      border: 1px solid rgba(200, 169, 110, 0.2);
    }
    
    .screenshot-header {
      background: var(--surface2);
      padding: 10px 15px;
      display: flex;
      gap: 8px;
    }
    
    .screenshot-dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
    }
    
    .dot-red { background: #ff5f57; }
    .dot-yellow { background: #febc2e; }
    .dot-green { background: #28c840; }
    
    .screenshot-body {
      padding: 20px;
      min-height: 250px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--text-sec);
      font-size: 0.9rem;
    }
    
    .pricing {
      padding: 100px 5%;
      background: var(--surface);
    }
    
    .pricing-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
      max-width: 1000px;
      margin: 0 auto;
    }
    
    .price-card {
      background: var(--surface2);
      border: 2px solid rgba(200, 169, 110, 0.2);
      border-radius: 20px;
      padding: 40px;
      text-align: center;
      transition: border-color 0.3s;
    }
    
    .price-card.featured {
      border-color: var(--gold);
      position: relative;
    }
    
    .price-card.featured::before {
      content: 'الأكثر طلباً';
      position: absolute;
      top: -12px;
      right: 50%;
      transform: translateX(50%);
      background: var(--gold);
      color: #1a1a1a;
      padding: 5px 15px;
      border-radius: 20px;
      font-size: 0.8rem;
      font-weight: 700;
    }
    
    .price-card h3 {
      font-size: 1.5rem;
      color: var(--gold);
      margin-bottom: 10px;
    }
    
    .price {
      font-size: 2.5rem;
      font-weight: 900;
      color: var(--gold-light);
      margin-bottom: 5px;
    }
    
    .price span {
      font-size: 1rem;
      color: var(--text-sec);
    }
    
    .price-features {
      list-style: none;
      margin: 20px 0;
      text-align: right;
    }
    
    .price-features li {
      padding: 8px 0;
      border-bottom: 1px solid rgba(255,255,255,0.05);
    }
    
    .price-features li::before {
      content: '✓';
      color: var(--gold);
      margin-left: 10px;
    }
    
    .download {
      padding: 100px 5%;
      background: linear-gradient(180deg, var(--dark) 0%, var(--surface) 100%);
      text-align: center;
    }
    
    .download h2 {
      font-size: 2.5rem;
      color: var(--gold);
      margin-bottom: 15px;
    }
    
    .download p {
      color: var(--text-sec);
      margin-bottom: 40px;
      font-size: 1.1rem;
    }
    
    .download-btns {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }
    
    .download-btn {
      background: var(--surface2);
      border: 2px solid var(--gold);
      border-radius: 15px;
      padding: 20px 40px;
      display: flex;
      align-items: center;
      gap: 15px;
      transition: background 0.3s, transform 0.3s;
    }
    
    .download-btn:hover {
      background: var(--surface);
      transform: translateY(-3px);
    }
    
    .download-btn-icon {
      font-size: 2.5rem;
    }
    
    .download-btn-text {
      text-align: right;
    }
    
    .download-btn-text span {
      display: block;
      color: var(--text-sec);
      font-size: 0.85rem;
    }
    
    footer {
      background: var(--surface);
      padding: 50px 5%;
      border-top: 1px solid rgba(200, 169, 110, 0.1);
    }
    
    .footer-content {
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 40px;
    }
    
    .footer-col h4 {
      color: var(--gold);
      margin-bottom: 15px;
    }
    
    .footer-col a {
      display: block;
      color: var(--text-sec);
      text-decoration: none;
      margin-bottom: 10px;
      transition: color 0.3s;
    }
    
    .footer-col a:hover { color: var(--gold); }
    
    .footer-bottom {
      text-align: center;
      padding-top: 30px;
      margin-top: 30px;
      border-top: 1px solid rgba(255,255,255,0.05);
      color: var(--text-sec);
    }
    
    @media (max-width: 768px) {
      header {
        flex-direction: column;
        gap: 15px;
        padding: 15px 5%;
      }
      
      nav { display: none; }
      
      .hero {
        flex-direction: column;
        text-align: center;
        padding-top: 150px;
      }
      
      .hero h1 { font-size: 2.5rem; }
      
      .hero-btns { justify-content: center; }
      
      .hero-img { display: none; }
      
      .section-title { font-size: 2rem; }
      
      .features-grid,
      .pricing-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>

  <header>
    <div class="logo">☕ قهوتي</div>
    <nav>
      <a href="#features">المميزات</a>
      <a href="#screenshots">الصور</a>
      <a href="#pricing">الأسعار</a>
      <a href="#download">التحميل</a>
    </nav>
    <a href="#download" class="btn">حمّل الآن</a>
  </header>

  <section class="hero">
    <div class="hero-content">
      <h1>نظام نقطة بيع احترافي لمقاهيك ومطاعمك</h1>
      <p>قهوتي يساعدك على إدارة مبيعاتك ومخزونك بسهولة، مع تصميم عربي أنيق وواجهة سهلة الاستخدام.</p>
      <div class="hero-btns">
        <a href="#download" class="btn">🚀 ابدأ مجاناً</a>
        <a href="#features" class="btn" style="background: transparent; border: 2px solid var(--gold); color: var(--gold);">تعرف على المزيد</a>
      </div>
    </div>
    <div class="hero-img">☕</div>
  </section>

  <section class="features" id="features">
    <h2 class="section-title">لماذا قهوتي؟</h2>
    <p class="section-subtitle">كل ما تحتاجه لإدارة مقهاك في مكان واحد</p>
    
    <div class="features-grid">
      <div class="feature-card">
        <div class="feature-icon">💰</div>
        <h3>نقاط البيع</h3>
        <p>سجل المبيعات بسرعة مع واجهة سحب وإفلات سهلة. دعم الدفع النقدي والبطاقة.</p>
      </div>
      
      <div class="feature-card">
        <div class="feature-icon">📦</div>
        <h3>إدارة المخزون</h3>
        <p>تتبع المواد الخام والمنتجات. تنبيهات عند انخفاض المخزون تلقائياً.</p>
      </div>
      
      <div class="feature-card">
        <div class="feature-icon">📊</div>
        <h3>تقارير وإحصائيات</h3>
        <p>تقارير مفصلة عن المبيعات والأرباح. تصدير البيانات بسهولة.</p>
      </div>
      
      <div class="feature-card">
        <div class="feature-icon">🔐</div>
        <h3>نظام التراخيص</h3>
        <p>تراخيص مرتبطة بالجهاز. حماية قوية من النسخ غير المرخص.</p>
      </div>
      
      <div class="feature-card">
        <div class="feature-icon">📱</div>
        <h3>تصميم متجاوب</h3>
        <p>يعمل على جميع الأجهزة: كمبيوتر، تابلت، وهاتف.</p>
      </div>
      
      <div class="feature-card">
        <div class="feature-icon">🎨</div>
        <h3>واجهة عربية</h3>
        <p>تصميم أنيق يدعم اللغة العربية بالكامل مع خط Tajawal.</p>
      </div>
      
      <div class="feature-card">
        <div class="feature-icon">☁️</div>
        <h3>سحابة آمنة</h3>
        <p>بياناتك محفوظة بأمان مع دعم Supabase للتخزين السحابي.</p>
      </div>
      
      <div class="feature-card">
        <div class="feature-icon">🔄</div>
        <h3>تحديثات مجانية</h3>
        <p>احصل على آخر التحديثات والمميزات الجديدة بدون تكلفة إضافية.</p>
      </div>
    </div>
  </section>

  <section class="screenshots" id="screenshots">
    <h2 class="section-title">لقطات من التطبيق</h2>
    <p class="section-subtitle">شاهد واجهة التطبيق الأنيقة</p>
    
    <div class="screenshots-grid">
      <div class="screenshot">
        <div class="screenshot-header">
          <div class="screenshot-dot dot-red"></div>
          <div class="screenshot-dot dot-yellow"></div>
          <div class="screenshot-dot dot-green"></div>
        </div>
        <div class="screenshot-body">📋 شاشة نقاط البيع - سلة البيع والمنتجات</div>
      </div>
      
      <div class="screenshot">
        <div class="screenshot-header">
          <div class="screenshot-dot dot-red"></div>
          <div class="screenshot-dot dot-yellow"></div>
          <div class="screenshot-dot dot-green"></div>
        </div>
        <div class="screenshot-body">📦 إدارة المخزون - تتبع المواد الخام</div>
      </div>
      
      <div class="screenshot">
        <div class="screenshot-header">
          <div class="screenshot-dot dot-red"></div>
          <div class="screenshot-dot dot-yellow"></div>
          <div class="screenshot-dot dot-green"></div>
        </div>
        <div class="screenshot-body">📊 التقارير - إحصائيات المبيعات والأرباح</div>
      </div>
      
      <div class="screenshot">
        <div class="screenshot-header">
          <div class="screenshot-dot dot-red"></div>
          <div class="screenshot-dot dot-yellow"></div>
          <div class="screenshot-dot dot-green"></div>
        </div>
        <div class="screenshot-body">🔐 شاشة الترخيص - تفعيل ومتابعة الاشتراك</div>
      </div>
    </div>
  </section>

  <section class="pricing" id="pricing">
    <h2 class="section-title">خطط الأسعار</h2>
    <p class="section-subtitle">اختر الباقة المناسبة لمقهاك</p>
    
    <div class="pricing-grid">
      <div class="price-card">
        <h3>شهري</h3>
        <div class="price">49 <span>ريال/شهر</span></div>
        <ul class="price-features">
          <li>نقاط بيع غير محدودة</li>
          <li>إدارة المخزون</li>
          <li>التقارير الأساسية</li>
          <li>دعم فني</li>
        </ul>
        <a href="#download" class="btn">اشترك الآن</a>
      </div>
      
      <div class="price-card featured">
        <h3>نصف سنوي</h3>
        <div class="price">249 <span>ريال/6 أشهر</span></div>
        <ul class="price-features">
          <li>كل مميزات الشهري</li>
          <li>توفير 15%</li>
          <li>تدريب مجاني</li>
          <li>أولويات الدعم</li>
        </ul>
        <a href="#download" class="btn">اشترك الآن</a>
      </div>
      
      <div class="price-card">
        <h3>سنوي</h3>
        <div class="price">399 <span>ريال/سنة</span></div>
        <ul class="price-features">
          <li>كل المميزات</li>
          <li>توفير 33%</li>
          <li>تدريب متقدم</li>
          <li>دعم VIP</li>
        </ul>
        <a href="#download" class="btn">اشترك الآن</a>
      </div>
    </div>
  </section>

  <section class="download" id="download">
    <h2>حمّل تطبيق قهوتي الآن</h2>
    <p>ابدأ فترة تجريبية مجانية لمدة 15 يوم</p>
    
    <div class="download-btns">
      <a href="#" class="download-btn">
        <div class="download-btn-icon">🪟</div>
        <div class="download-btn-text">Windows<span>exe - 85 MB</span></div>
      </a>
      
      <a href="https://wa.me/966570347437" target="_blank" class="download-btn">
        <div class="download-btn-icon">💬</div>
        <div class="download-btn-text">واتساب<span>تواصل معنا</span></div>
      </a>
    </div>
    
    <div style="margin-top: 40px; padding: 25px; background: var(--surface2); border-radius: 15px; display: inline-block;">
      <p style="margin-bottom: 10px;"><strong style="color: var(--gold);">📱 هاتف:</strong> <span dir="ltr" style="color: var(--text);">+966 57 034 7437</span></p>
      <p><strong style="color: var(--gold);">✉️ بريد:</strong> <a href="mailto:morfeuse71@gmail.com" style="color: var(--text); text-decoration: none;">morfeuse71@gmail.com</a></p>
    </div>
  </section>

  <footer>
    <div class="footer-content">
      <div class="footer-col">
        <h4>☕ قهوتي</h4>
        <p style="color: var(--text-sec); font-size: 0.9rem;">نظام نقطة بيع احترافي لإدارة مقاهيك ومطاعمك.</p>
      </div>
      
      <div class="footer-col">
        <h4>روابط سريعة</h4>
        <a href="#features">المميزات</a>
        <a href="#pricing">الأسعار</a>
        <a href="#download">التحميل</a>
      </div>
      
      <div class="footer-col">
        <h4>الدعم</h4>
        <a href="#">تواصل معنا</a>
        <a href="#">الأسئلة الشائعة</a>
        <a href="#">وثائق API</a>
      </div>
      
      <div class="footer-col">
        <h4>تواصل معنا</h4>
        <a href="tel:+966570347437">📱 +966 57 034 7437</a>
        <a href="https://wa.me/966570347437" target="_blank">💬 واتساب</a>
        <a href="mailto:morfeuse71@gmail.com">✉️ morfeuse71@gmail.com</a>
      </div>
    </div>
    
    <div class="footer-bottom">
      <p>© 2024 قهوتي. جميع الحقوق محفوظة.</p>
    </div>
  </footer>

</body>
</html>
