<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>طلاب علوم - منصة التعليم الطلابية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-blue: #2C3E50;
            --secondary-green: #27AE60;
            --accent-orange: #E67E22;
            --light-bg: #F8F9FA;
            --text-dark: #2D3748;
            --text-light: #718096;
            --white: #FFFFFF;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tajawal', sans-serif;
        }
        
        body {
            background-color: var(--light-bg);
            color: var(--text-dark);
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: var(--white);
            box-shadow: var(--shadow);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo i {
            font-size: 28px;
            color: var(--secondary-green);
            margin-left: 10px;
        }
        
        .logo h1 {
            font-size: 24px;
            font-weight: 800;
            color: var(--primary-blue);
        }
        
        .logo span {
            color: var(--secondary-green);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin: 0 15px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--secondary-green);
        }
        
        .auth-buttons {
            display: flex;
        }
        
        .btn {
            padding: 10px 20px;
            border-radius: 5px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
            text-align: center;
        }
        
        .btn-outline {
            border: 2px solid var(--secondary-green);
            color: var(--secondary-green);
            background: transparent;
            margin-left: 10px;
        }
        
        .btn-filled {
            background-color: var(--secondary-green);
            color: var(--white);
            border: 2px solid var(--secondary-green);
        }
        
        .btn-outline:hover {
            background-color: var(--secondary-green);
            color: var(--white);
        }
        
        .btn-filled:hover {
            background-color: #219653;
            border-color: #219653;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-blue) 0%, #1a2530 100%);
            color: var(--white);
            padding: 150px 0 100px;
            margin-top: 70px;
        }
        
        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .hero-text {
            flex: 1;
            padding-left: 40px;
        }
        
        .hero-text h2 {
            font-size: 42px;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero-text p {
            font-size: 18px;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .hero-buttons {
            display: flex;
            gap: 15px;
        }
        
        .hero-image {
            flex: 1;
            text-align: center;
        }
        
        .hero-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        /* Features Section */
        .features {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 36px;
            color: var(--primary-blue);
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: var(--text-light);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            background: var(--white);
            border-radius: 10px;
            padding: 30px;
            box-shadow: var(--shadow);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            width: 70px;
            height: 70px;
            background: rgba(39, 174, 96, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
        }
        
        .feature-icon i {
            font-size: 30px;
            color: var(--secondary-green);
        }
        
        .feature-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--primary-blue);
        }
        
        /* Subjects Section */
        .subjects {
            padding: 80px 0;
            background-color: var(--white);
        }
        
        .subjects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }
        
        .subject-card {
            background: var(--light-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
        }
        
        .subject-card:hover {
            transform: translateY(-5px);
        }
        
        .subject-icon {
            height: 120px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 50px;
        }
        
        .chemistry .subject-icon {
            background: linear-gradient(135deg, #8E44AD, #9B59B6);
        }
        
        .physics .subject-icon {
            background: linear-gradient(135deg, #3498DB, #5DADE2);
        }
        
        .biology .subject-icon {
            background: linear-gradient(135deg, #27AE60, #58D68D);
        }
        
        .math .subject-icon {
            background: linear-gradient(135deg, #E67E22, #F39C12);
        }
        
        .subject-content {
            padding: 20px;
        }
        
        .subject-content h3 {
            font-size: 22px;
            margin-bottom: 10px;
            color: var(--primary-blue);
        }
        
        .subject-content p {
            color: var(--text-light);
            margin-bottom: 15px;
        }
        
        /* Teachers Section */
        .teachers {
            padding: 80px 0;
        }
        
        .teachers-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .teacher-card {
            background: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            text-align: center;
        }
        
        .teacher-image {
            height: 200px;
            background-size: cover;
            background-position: center;
        }
        
        .teacher-info {
            padding: 20px;
        }
        
        .teacher-info h3 {
            font-size: 22px;
            margin-bottom: 5px;
            color: var(--primary-blue);
        }
        
        .teacher-info p {
            color: var(--text-light);
            margin-bottom: 10px;
        }
        
        .rating {
            color: #F1C40F;
            margin-bottom: 15px;
        }
        
        /* Courses Section */
        .courses {
            padding: 80px 0;
            background-color: var(--white);
        }
        
        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .course-card {
            background: var(--light-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }
        
        .course-image {
            height: 180px;
            background-size: cover;
            background-position: center;
        }
        
        .course-content {
            padding: 20px;
        }
        
        .course-content h3 {
            font-size: 22px;
            margin-bottom: 10px;
            color: var(--primary-blue);
        }
        
        .course-meta {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
            color: var(--text-light);
        }
        
        .progress-bar {
            height: 8px;
            background: #E0E0E0;
            border-radius: 4px;
            margin-bottom: 15px;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            background: var(--secondary-green);
            border-radius: 4px;
        }
        
        /* Footer */
        footer {
            background: var(--primary-blue);
            color: var(--white);
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 22px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            right: 0;
            width: 50px;
            height: 3px;
            background: var(--secondary-green);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #CBD5E0;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: var(--secondary-green);
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-icons a {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .social-icons a:hover {
            background: var(--secondary-green);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #CBD5E0;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
            }
            
            .hero-text {
                padding-left: 0;
                margin-bottom: 40px;
                text-align: center;
            }
            
            nav ul {
                display: none;
            }
            
            .mobile-menu {
                display: block;
            }
        }
        
        @media (max-width: 768px) {
            .hero-text h2 {
                font-size: 32px;
            }
            
            .section-title h2 {
                font-size: 28px;
            }
            
            .hero-buttons {
                flex-direction: column;
                gap: 10px;
            }
            
            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-graduation-cap"></i>
                    <h1>طلاب <span>علوم</span></h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#">الرئيسية</a></li>
                        <li><a href="#">المواد الدراسية</a></li>
                        <li><a href="#">المدرسون</a></li>
                        <li><a href="#">الدورات</a></li>
                        <li><a href="#">المجتمع</a></li>
                        <li><a href="#">اتصل بنا</a></li>
                    </ul>
                </nav>
                <div class="auth-buttons">
                    <a href="#" class="btn btn-outline">تسجيل الدخول</a>
                    <a href="#" class="btn btn-filled">انضم إلينا</a>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h2>منصة طلابية تشاركية لتعليم المواد العلمية</h2>
                    <p>بالعلم نرتقي.. وبالتعاون ننتصر. انضم إلى آلاف الطلاب الذين يحققون تفوقهم الأكاديمي من خلال منصتنا التعليمية المبتكرة.</p>
                    <div class="hero-buttons">
                        <a href="#" class="btn btn-filled">ابدأ رحلتك التعليمية</a>
                        <a href="#" class="btn btn-outline">استكشف المواد الدراسية</a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1523240795612-9a054b0db644?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="طلاب يدرسون معًا">
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <div class="section-title">
                <h2>لماذا تختار منصة طلاب علوم؟</h2>
                <p>نقدم تجربة تعليمية فريدة تجمع بين الجودة العالية والأسعار المناسبة</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>شرح بلغة طلابية</h3>
                    <p>مدرسون من خريجي كليات القمة يشرحون بلغة بسيطة وسهلة الفهم</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-tags"></i>
                    </div>
                    <h3>أسعار مناسبة</h3>
                    <p>أسعارنا تبدأ من 50% أقل من المنصات التجارية الأخرى</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-chalkboard-teacher"></i>
                    </div>
                    <h3>مدرسون متميزون</h3>
                    <p>فريق من الطلاب المتفوقين والخريجين من كليات الطب والهندسة والعلوم</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-file-alt"></i>
                    </div>
                    <h3>مراجعات نهائية مجانية</h3>
                    <p>نوفر مراجعات نهائية مجانية قبل الامتحانات لجميع الطلاب</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Subjects Section -->
    <section class="subjects">
        <div class="container">
            <div class="section-title">
                <h2>المواد الدراسية</h2>
                <p>نغطي جميع المواد العلمية الأساسية بمحتوى تعليمي متكامل</p>
            </div>
            <div class="subjects-grid">
                <div class="subject-card chemistry">
                    <div class="subject-icon">
                        <i class="fas fa-flask"></i>
                    </div>
                    <div class="subject-content">
                        <h3>الكيمياء</h3>
                        <p>شرح منهج الكيمياء بجميع فروعه من الصفر إلى الاحتراف</p>
                        <a href="#" class="btn btn-outline">استكشف الدروس</a>
                    </div>
                </div>
                <div class="subject-card physics">
                    <div class="subject-icon">
                        <i class="fas fa-atom"></i>
                    </div>
                    <div class="subject-content">
                        <h3>الفيزياء</h3>
                        <p>فهم قوانين الفيزياء وتطبيقاتها العملية في الحياة اليومية</p>
                        <a href="#" class="btn btn-outline">استكشف الدروس</a>
                    </div>
                </div>
                <div class="subject-card biology">
                    <div class="subject-icon">
                        <i class="fas fa-dna"></i>
                    </div>
                    <div class="subject-content">
                        <h3>الأحياء</h3>
                        <p>دراسة الكائنات الحية ووظائفها من الخلية إلى الأنظمة البيئية</p>
                        <a href="#" class="btn btn-outline">استكشف الدروس</a>
                    </div>
                </div>
                <div class="subject-card math">
                    <div class="subject-icon">
                        <i class="fas fa-square-root-alt"></i>
                    </div>
                    <div class="subject-content">
                        <h3>الرياضيات</h3>
                        <p>تطوير مهارات حل المسائل الرياضية بمختلف أنواعها</p>
                        <a href="#" class="btn btn-outline">استكشف الدروس</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Teachers Section -->
    <section class="teachers">
        <div class="container">
            <div class="section-title">
                <h2>مدرسون متميزون</h2>
                <p>تعلم من أفضل الطلاب والخريجين المتفوقين في تخصصاتهم</p>
            </div>
            <div class="teachers-grid">
                <div class="teacher-card">
                    <div class="teacher-image" style="background-image: url('https://images.unsplash.com/photo-1568602471122-7832951cc4c5?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80');"></div>
                    <div class="teacher-info">
                        <h3>أحمد محمد</h3>
                        <p>خريج كلية الطب - متخصص في الكيمياء</p>
                        <div class="rating">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star-half-alt"></i>
                        </div>
                        <p>عدد الطلاب: 350+</p>
                    </div>
                </div>
                <div class="teacher-card">
                    <div class="teacher-image" style="background-image: url('https://images.unsplash.com/photo-1544717305-2782549b5136?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80');"></div>
                    <div class="teacher-info">
                        <h3>سارة أحمد</h3>
                        <p>طالبة صيدلة - متخصصة في الأحياء</p>
                        <div class="rating">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                        <p>عدد الطلاب: 280+</p>
                    </div>
                </div>
                <div class="teacher-card">
                    <div class="teacher-image" style="background-image: url('https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80');"></div>
                    <div class="teacher-info">
                        <h3>يوسف خالد</h3>
                        <p>خريج هندسة - متخصص في الفيزياء</p>
                        <div class="rating">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="far fa-star"></i>
                        </div>
                        <p>عدد الطلاب: 420+</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Courses Section -->
    <section class="courses">
        <div class="container">
            <div class="section-title">
                <h2>الدورات الأكثر شيوعًا</h2>
                <p>انضم إلى آلاف الطلاب الذين يستفيدون من دوراتنا التعليمية</p>
            </div>
            <div class="courses-grid">
                <div class="course-card">
                    <div class="course-image" style="background-image: url('https://images.unsplash.com/photo-1532094349884-543bc11b234d?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80');"></div>
                    <div class="course-content">
                        <h3>الكيمياء العضوية المتقدمة</h3>
                        <div class="course-meta">
                            <span><i class="far fa-clock"></i> 24 ساعة</span>
                            <span><i class="far fa-user"></i> 340 طالب</span>
                        </div>
                        <div class="progress-bar">
                            <div class="progress" style="width: 75%;"></div>
                        </div>
                        <p>شامل لجميع أساسيات الكيمياء العضوية وتطبيقاتها</p>
                        <a href="#" class="btn btn-filled">استمر في التعلم</a>
                    </div>
                </div>
                <div class="course-card">
                    <div class="course-image" style="background-image: url('https://images.unsplash.com/photo-1635070041078-e363dbe005cb?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80');"></div>
                    <div class="course-content">
                        <h3>الفيزياء الحديثة</h3>
                        <div class="course-meta">
                            <span><i class="far fa-clock"></i> 18 ساعة</span>
                            <span><i class="far fa-user"></i> 290 طالب</span>
                        </div>
                        <div class="progress-bar">
                            <div class="progress" style="width: 40%;"></div>
                        </div>
                        <p>استكشاف النظريات الفيزيائية الحديثة وتطبيقاتها</p>
                        <a href="#" class="btn btn-filled">استمر في التعلم</a>
                    </div>
                </div>
                <div class="course-card">
                    <div class="course-image" style="background-image: url('https://images.unsplash.com/photo-1536922246289-88c42f957773?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80');"></div>
                    <div class="course-content">
                        <h3>الوراثة والأحياء الجزيئية</h3>
                        <div class="course-meta">
                            <span><i class="far fa-clock"></i> 30 ساعة</span>
                            <span><i class="far fa-user"></i> 510 طالب</span>
                        </div>
                        <div class="progress-bar">
                            <div class="progress" style="width: 90%;"></div>
                        </div>
                        <p>فهم أساسيات الوراثة وتطبيقاتها في العلوم الطبية</p>
                        <a href="#" class="btn btn-filled">استمر في التعلم</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>طلاب علوم</h3>
                    <p>منصة طلابية تشاركية لتعليم المواد العلمية، نهدف إلى تقديم تعليم عالي الجودة بأسعار مناسبة للجميع.</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>روابط سريعة</h3>
                    <ul>
                        <li><a href="#">الرئيسية</a></li>
                        <li><a href="#">من نحن</a></li>
                        <li><a href="#">المواد الدراسية</a></li>
                        <li><a href="#">المدرسون</a></li>
                        <li><a href="#">المدونة</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>المواد الدراسية</h3>
                    <ul>
                        <li><a href="#">الكيمياء</a></li>
                        <li><a href="#">الفيزياء</a></li>
                        <li><a href="#">الأحياء</a></li>
                        <li><a href="#">الرياضيات</a></li>
                        <li><a href="#">المسارات المتقدمة</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>اتصل بنا</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> القاهرة، مصر</li>
                        <li><i class="fas fa-phone"></i> +20 123 456 7890</li>
                        <li><i class="fas fa-envelope"></i> info@tullab-ulum.com</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>جميع الحقوق محفوظة &copy; 2023 منصة طلاب علوم</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple JavaScript for interactive elements
        document.addEventListener('DOMContentLoaded', function() {
            // Add animation to feature cards on scroll
            const featureCards = document.querySelectorAll('.feature-card');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = 1;
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, { threshold: 0.1 });
            
            featureCards.forEach(card => {
                card.style.opacity = 0;
                card.style.transform = 'translateY(20px)';
                card.style.transition = 'opacity 0.5s, transform 0.5s';
                observer.observe(card);
            });
        });
    </script>
</body>
</html>
