78<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مي فور الكترومكنيكال | خدمات مكيفات الهواء</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f0f9ff;
            color: #333;
            overflow-x: hidden;
        }
        
        /* الشريط العلوي */
        .top-bar {
            background: linear-gradient(90deg, #003366, #0066cc);
            color: white;
            padding: 10px 0;
            text-align: center;
            font-size: 0.9rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        /* شريط التنقل */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
            background-color: white;
            box-shadow: 0 2px 15px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 50px;
            margin-left: 10px;
        }
        
        .logo h1 {
            font-size: 1.6rem;
            color: #0066cc;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin: 0 15px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: #003366;
            font-weight: 600;
            font-size: 1.1rem;
            transition: color 0.3s;
            position: relative;
        }
        
        .nav-links a:hover {
            color: #00a8ff;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: #00a8ff;
            transition: width 0.3s;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .contact-btn {
            background: linear-gradient(90deg, #00a8ff, #0066cc);
            color: white;
            border: none;
            padding: 10px 25px;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            font-size: 1rem;
        }
        
        .contact-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 104, 255, 0.4);
        }
        
        /* قسم الهيرو */
        .hero {
            background: linear-gradient(rgba(0, 60, 120, 0.8), rgba(0, 100, 200, 0.8)), url('https://images.unsplash.com/photo-1631146711666-7d6e6c1f0a8b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            height: 80vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 0 20px;
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            max-width: 900px;
            z-index: 2;
        }
        
        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
            animation: fadeInDown 1s ease;
        }
        
        .hero p {
            font-size: 1.4rem;
            margin-bottom: 30px;
            animation: fadeInUp 1s ease;
        }
        
        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 20px;
            animation: fadeIn 1.5s ease;
        }
        
        .service-btn {
            background: transparent;
            border: 2px solid white;
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .service-btn:hover {
            background-color: white;
            color: #0066cc;
        }
        
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
        
        /* قسم الخدمات */
        .services {
            padding: 80px 5%;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: #003366;
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, #00a8ff, #0066cc);
            border-radius: 2px;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background: #f9f9f9;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
            transition: transform 0.4s, box-shadow 0.4s;
            position: relative;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 104, 255, 0.2);
        }
        
        .service-icon {
            height: 200px;
            background: linear-gradient(135deg, #00a8ff, #0066cc);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 5rem;
            color: white;
        }
        
        .service-content {
            padding: 25px;
        }
        
        .service-content h3 {
            font-size: 1.8rem;
            color: #003366;
            margin-bottom: 15px;
        }
        
        .service-content p {
            color: #555;
            line-height: 1.8;
            margin-bottom: 20px;
        }
        
        .service-list {
            list-style: none;
            margin-bottom: 20px;
        }
        
        .service-list li {
            padding: 8px 0;
            border-bottom: 1px dashed #ddd;
            display: flex;
            align-items: center;
        }
        
        .service-list li i {
            color: #00a8ff;
            margin-left: 10px;
        }
        
        /* قسم عن الشركة */
        .about {
            padding: 80px 5%;
            background: linear-gradient(135deg, #e6f4ff, #f0f9ff);
            display: flex;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
            height: 500px;
            background: url('https://images.unsplash.com/photo-1581092580497-e0d23cbdf1dc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80') center/cover;
            border-radius: 15px;
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .about-content {
            flex: 1;
            min-width: 300px;
            padding: 0 50px;
        }
        
        .about-content h2 {
            font-size: 2.5rem;
            color: #003366;
            margin-bottom: 25px;
        }
        
        .about-content p {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #444;
            margin-bottom: 20px;
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 40px;
        }
        
        .stat-box {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .stat-box:hover {
            transform: translateY(-5px);
        }
        
        .stat-box i {
            font-size: 2.5rem;
            color: #00a8ff;
            margin-bottom: 15px;
        }
        
        .stat-box h3 {
            font-size: 2.5rem;
            color: #0066cc;
            margin-bottom: 10px;
        }
        
        .stat-box p {
            font-size: 1.1rem;
            color: #555;
            margin: 0;
        }
        
        /* قسم العملاء */
        .testimonials {
            padding: 80px 5%;
            background-color: white;
            text-align: center;
        }
        
        .clients {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
            margin: 50px 0;
        }
        
        .client-logo {
            width: 150px;
            height: 100px;
            background: #f5f5f5;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }
        
        .client-logo:hover {
            transform: scale(1.1);
        }
        
        .client-logo img {
            max-width: 80%;
            max-height: 70%;
        }
        
        /* الفوتر */
        .footer {
            background: linear-gradient(135deg, #003366, #001a33);
            color: white;
            padding: 60px 5% 30px;
        }
        
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-col h3 {
            font-size: 1.5rem;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-col h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: #00a8ff;
        }
        
        .footer-col p {
            line-height: 1.8;
            margin-bottom: 20px;
            color: #ccc;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
            display: flex;
            align-items: center;
        }
        
        .footer-links a i {
            margin-left: 8px;
            color: #00a8ff;
        }
        
        .footer-links a:hover {
            color: #00a8ff;
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s;
        }
        
        .social-icons a:hover {
            background: #00a8ff;
            transform: translateY(-5px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* تأثيرات الفقاعات */
        .bubble {
            position: absolute;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            animation: float 6s infinite ease-in-out;
            z-index: 1;
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0) translateX(0);
            }
            50% {
                transform: translateY(-50px) translateX(20px);
            }
        }
        
        /* التجاوبية */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 2.8rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .about-content {
                padding: 50px 0 0 0;
            }
        }
        
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                padding: 15px;
            }
            
            .logo {
                margin-bottom: 15px;
            }
            
            .nav-links {
                margin-bottom: 15px;
            }
            
            .hero {
                height: 70vh;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: center;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 480px) {
            .nav-links {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .nav-links li {
                margin: 5px 10px;
            }
            
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .service-card {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- شريط أعلى -->
    <div class="top-bar">
        <p><i class="fas fa-phone"></i> اتصل بنا الآن: 0123456789 | <i class="fas fa-map-marker-alt"></i> الرياض، المملكة العربية السعودية</p>
    </div>
    
    <!-- شريط التنقل -->
    <nav class="navbar">
        <div class="logo">
            <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNTAgMjUwIj48cGF0aCBmaWxsPSIjMDA2NmNjIiBkPSJNMTI1IDMwTDE4Ny4xMjUgMjE4Ljc1SDYyLjg3NUwxMjUgMzBaIi8+PHBhdGggZmlsbD0iIzAwYThmZiIgZD0iTTEyNSA4NUwxNjIuNSA2My43NUw4Ny41IDYzLjc1TDEyNSA4NVoiLz48cGF0aCBmaWxsPSIjMDAzMzY2IiBkPSJNMTI1IDg1TDE2Mi41IDE1Ni4yNUw4Ny41IDE1Ni4yNUwxMjUgODVaIi8+PC9zdmc+" alt="Logo">
            <h1>مي فور الكترومكنيكال</h1>
        </div>
        
        <ul class="nav-links">
            <li><a href="#home">الرئيسية</a></li>
            <li><a href="#services">خدماتنا</a></li>
            <li><a href="#about">من نحن</a></li>
            <li><a href="#clients">عملائنا</a></li>
            <li><a href="#contact">اتصل بنا</a></li>
        </ul>
        
        <button class="contact-btn">
            <i class="fas fa-phone"></i> طلب خدمة
        </button>
    </nav>
    
    <!-- قسم الهيرو -->
    <section class="hero" id="home">
        <!-- فقاعات متحركة -->
        <div class="bubble" style="width: 80px; height: 80px; top: 20%; left: 10%;"></div>
        <div class="bubble" style="width: 60px; height: 60px; top: 50%; left: 20%; animation-delay: -2s;"></div>
        <div class="bubble" style="width: 100px; height: 100px; top: 70%; left: 80%; animation-delay: -4s;"></div>
        <div class="bubble" style="width: 40px; height: 40px; top: 40%; left: 85%; animation-delay: -1s;"></div>
        
        <div class="hero-content">
            <h2>الخبرة والتميز في عالم التكييف والتبريد</h2>
            <p>نقدم حلولاً متكاملة لصيانة وتركيب وتنظيف مكيفات الهواء مع فريق محترف وضمان على الخدمة</p>
            <div class="hero-btns">
                <button class="service-btn">خدماتنا</button>
                <button class="service-btn">اتصل بنا</button>
            </div>
        </div>
    </section>
    
    <!-- قسم الخدمات -->
    <section class="services" id="services">
        <div class="section-title">
            <h2>خدماتنا المتكاملة</h2>
        </div>
        
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-tools"></i>
                </div>
                <div class="service-content">
                    <h3>صيانة المكيفات</h3>
                    <p>خدمات صيانة شاملة ومتخصصة لجميع أنواع المكيفات المركزية والسبليت والنوافذ</p>
                    <ul class="service-list">
                        <li><i class="fas fa-check-circle"></i> صيانة دورية وقائية</li>
                        <li><i class="fas fa-check-circle"></i> إصلاح الأعطال الفنية</li>
                        <li><i class="fas fa-check-circle"></i> استبدال القطع التالفة</li>
                        <li><i class="fas fa-check-circle"></i> تشخيص دقيق للأعطال</li>
                    </ul>
                </div>
            </div>
            
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-wind"></i>
                </div>
                <div class="service-content">
                    <h3>تنظيف المكيفات</h3>
                    <p>خدمات تنظيف احترافية تعيد كفاءة المكيف وتضمن جودة الهواء في مساحتك</p>
                    <ul class="service-list">
                        <li><i class="fas fa-check-circle"></i> تنظيف فلتر المكيف</li>
                        <li><i class="fas fa-check-circle"></i> تعقيم المكيف بالكامل</li>
                        <li><i class="fas fa-check-circle"></i> إزالة الأتربة والغبار</li>
                        <li><i class="fas fa-check-circle"></i> تنظيف الوحدة الخارجية</li>
                    </ul>
                </div>
            </div>
            
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-gas-pump"></i>
                </div>
                <div class="service-content">
                    <h3>تعبئة غاز الفريون</h3>
                    <p>خدمات تعبئة غاز الفريون بأنواعه المختلفة بأسعار تنافسية وضمان الجودة</p>
                    <ul class="service-list">
                        <li><i class="fas fa-check-circle"></i> فحص تسريب الغاز</li>
                        <li><i class="fas fa-check-circle"></i> تعبئة الغاز بأنواعه</li>
                        <li><i class="fas fa-check-circle"></i> صيانة دورة التبريد</li>
                        <li><i class="fas fa-check-circle"></i> استبدال الضواغط</li>
                    </ul>
                </div>
            </div>
            
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-hammer"></i>
                </div>
                <div class="service-content">
                    <h3>تركيب المكيفات</h3>
                    <p>خدمات تركيب احترافية لمختلف أنواع المكيفات مع ضمان التوصيلات الصحيحة</p>
                    <ul class="service-list">
                        <li><i class="fas fa-check-circle"></i> تركيب مكيفات سبليت</li>
                        <li><i class="fas fa-check-circle"></i> تركيب مكيفات مركزية</li>
                        <li><i class="fas fa-check-circle"></i> تركيب أنظمة VRV/VRF</li>
                        <li><i class="fas fa-check-circle"></i> تركيب المكيفات الطابقية</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
    
    <!-- قسم عن الشركة -->
    <section class="about" id="about">
        <div class="about-image"></div>
        <div class="about-content">
            <h2>من نحن</h2>
            <p>شركة "مي فور الكترومكنيكال" هي شركة رائدة في مجال خدمات التكييف والتبريد، تأسست عام 2010 بهدف تقديم خدمات عالية الجودة في مجال صيانة وتركيب وتنظيف المكيفات بأنواعها.</p>
            <p>نحن نتميز بفريق فني مؤهل ومدرب على أعلى مستوى، قادر على التعامل مع كافة أنواع المكيفات ومشاكلها. نستخدم أحدث المعدات والتقنيات لضمان تقديم خدمة مميزة تلبي تطلعات عملائنا الكرام.</p>
            <p>نسعى دائماً لتحقيق رضا العملاء من خلال تقديم خدمات سريعة وبأسعار تنافسية مع ضمان على جميع أعمالنا.</p>
            
            <div class="stats">
                <div class="stat-box">
                    <i class="fas fa-users"></i>
                    <h3>500+</h3>
                    <p>عميل راضٍ</p>
                </div>
                <div class="stat-box">
                    <i class="fas fa-tools"></i>
                    <h3>2000+</h3>
                    <p>خدمة مقدمة</p>
                </div>
                <div class="stat-box">
                    <i class="fas fa-user-cog"></i>
                    <h3>25+</h3>
                    <p>فني محترف</p>
                </div>
                <div class="stat-box">
                    <i class="fas fa-building"></i>
                    <h3>12+</h3>
                    <p>سنة خبرة</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- قسم العملاء -->
    <section class="testimonials" id="clients">
        <div class="section-title">
            <h2>عملاؤنا</h2>
        </div>
        
        <div class="clients">
            <div class="client-logo">شركة 1</div>
            <div class="client-logo">شركة 2</div>
            <div class="client-logo">شركة 3</div>
            <div class="client-logo">شركة 4</div>
            <div class="client-logo">شركة 5</div>
            <div class="client-logo">شركة 6</div>
        </div>
    </section>
    
    <!-- الفوتر -->
    <footer class="footer" id="contact">
        <div class="footer-grid">
            <div class="footer-col">
                <h3>مي فور الكترومكنيكال</h3>
                <p>شركة متخصصة في خدمات صيانة وتركيب وتنظيف وتعبئة غاز مكيفات الفريون، نقدم خدماتنا باحترافية وجودة عالية.</p>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
            
            <div class="footer-col">
                <h3>روابط سريعة</h3>
                <ul class="footer-links">
                    <li><a href="#home"><i class="fas fa-chevron-left"></i> الرئيسية</a></li>
                    <li><a href="#services"><i class="fas fa-chevron-left"></i> خدماتنا</a></li>
                    <li><a href="#about"><i class="fas fa-chevron-left"></i> من نحن</a></li>
                    <li><a href="#clients"><i class="fas fa-chevron-left"></i> عملاؤنا</a></li>
                    <li><a href="#contact"><i class="fas fa-chevron-left"></i> اتصل بنا</a></li>
                </ul>
            </div>
            
            <div class="footer-col">
                <h3>خدماتنا</h3>
                <ul class="footer-links">
                    <li><a href="#"><i class="fas fa-chevron-left"></i> صيانة المكيفات</a></li>
                    <li><a href="#"><i class="fas fa-chevron-left"></i> تنظيف المكيفات</a></li>
                    <li><a href="#"><i class="fas fa-chevron-left"></i> تعبئة غاز الفريون</a></li>
                    <li><a href="#"><i class="fas fa-chevron-left"></i> تركيب المكيفات</a></li>
                    <li><a href="#"><i class="fas fa-chevron-left"></i> خدمات الطوارئ</a></li>
                </ul>
            </div>
            
            <div class="footer-col">
                <h3>اتصل بنا</h3>
                <ul class="footer-links">
                    <li><a href="#"><i class="fas fa-map-marker-alt"></i> الرياض، المملكة العربية السعودية</a></li>
                    <li><a href="tel:0123456789"><i class="fas fa-phone"></i> 0123456789</a></li>
                    <li><a href="tel:0987654321"><i class="fas fa-mobile-alt"></i> 0987654321</a></li>
                    <li><a href="mailto:info@me4-electromechanical.com"><i class="fas fa-envelope"></i> info@me4-electromechanical.com</a></li>
                    <li><a href="#"><i class="fas fa-clock"></i> الأحد - الخميس: 8 صباحاً - 6 مساءً</a></li>
                </ul>
            </div>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023 مي فور الكترومكنيكال. جميع الحقوق محفوظة.</p>
        </div>
    </footer>
    
    <script>
        // إنشاء فقاعات عشوائية
        function createBubbles() {
            const hero = document.querySelector('.hero');
            const bubbleCount = 8;
            
            for (let i = 0; i < bubbleCount; i++) {
                const bubble = document.createElement('div');
                bubble.classList.add('bubble');
                
                const size = Math.random() * 80 + 20;
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                const delay = Math.random() * 5;
                
                bubble.style.width = `${size}px`;
                bubble.style.height = `${size}px`;
                bubble.style.left = `${posX}%`;
                bubble.style.top = `${posY}%`;
                bubble.style.animationDelay = `-${delay}s`;
                
                hero.appendChild(bubble);
            }
        }
        
        // تأثير التمرير السلس
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // تأثير ظهور العناصر عند التمرير
        function animateOnScroll() {
            const elements = document.querySelectorAll('.service-card, .stat-box, .client-logo');
            
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.3;
                
                if (elementPosition < screenPosition) {
                    element.style.opacity = 1;
                    element.style.transform = 'translateY(0)';
                }
            });
        }
        
        // تهيئة تأثيرات الخدمات
        document.querySelectorAll('.service-card').forEach(card => {
            card.style.opacity = 0;
            card.style.transform = 'translateY(50px)';
            card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
        });
        
        // تهيئة تأثيرات إحصاءات الشركة
        document.querySelectorAll('.stat-box').forEach(box => {
            box.style.opacity = 0;
            box.style.transform = 'translateY(30px)';
            box.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
        });
        
        // تهيئة تأثيرات شعارات العملاء
        document.querySelectorAll('.client-logo').forEach(logo => {
            logo.style.opacity = 0;
            logo.style.transform = 'scale(0.8)';
            logo.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
        });
        
        // عند تحميل الصفحة
        window.addEventListener('load', () => {
            createBubbles();
            
            // إظهار العناصر فور التحميل
            setTimeout(() => {
                document.querySelectorAll('.service-card, .stat-box, .client-logo').forEach(el => {
                    el.style.opacity = 1;
                    el.style.transform = 'translateY(0) scale(1)';
                });
            }, 500);
        });
        
        // عند التمرير
        window.addEventListener('scroll', animateOnScroll);
    </script>
</body>
</html>