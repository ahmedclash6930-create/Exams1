<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>طلاب علوم - المنصة التعليمية المتكاملة</title>
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
            --transition: all 0.3s ease;
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
            transition: var(--transition);
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
            transition: var(--transition);
            text-decoration: none;
            display: inline-block;
            text-align: center;
            border: none;
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
            transition: var(--transition);
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
            transition: var(--transition);
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
            transition: var(--transition);
        }
        
        .course-card:hover {
            transform: translateY(-5px);
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
        
        /* Interactive Elements */
        .interactive-section {
            padding: 80px 0;
            background: linear-gradient(135deg, var(--primary-blue) 0%, #1a2530 100%);
            color: var(--white);
            text-align: center;
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .stat-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 10px;
            backdrop-filter: blur(10px);
        }
        
        .stat-number {
            font-size: 42px;
            font-weight: 800;
            margin-bottom: 10px;
            color: var(--secondary-green);
        }
        
        /* Login Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }
        
        .modal-content {
            background: var(--white);
            border-radius: 10px;
            width: 90%;
            max-width: 500px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .close-modal {
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
            color: var(--text-light);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-group input {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }
        
        /* User Dashboard */
        .dashboard {
            display: none;
            margin-top: 80px;
            padding: 40px 0;
        }
        
        .dashboard-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
        }
        
        .user-info {
            display: flex;
            align-items: center;
        }
        
        .user-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: var(--secondary-green);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 24px;
            margin-left: 15px;
        }
        
        .dashboard-nav {
            display: flex;
            margin-bottom: 30px;
            border-bottom: 1px solid #ddd;
        }
        
        .dashboard-nav button {
            padding: 12px 20px;
            background: none;
            border: none;
            cursor: pointer;
            font-size: 16px;
            border-bottom: 3px solid transparent;
            transition: var(--transition);
        }
        
        .dashboard-nav button.active {
            border-bottom: 3px solid var(--secondary-green);
            color: var(--secondary-green);
        }
        
        .dashboard-content {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
        }
        
        .my-courses, .progress-tracker, .upcoming-classes {
            background: var(--white);
            border-radius: 10px;
            padding: 20px;
            box-shadow: var(--shadow);
        }
        
        .course-item {
            display: flex;
            align-items: center;
            padding: 15px 0;
            border-bottom: 1px solid #eee;
        }
        
        .course-item:last-child {
            border-bottom: none;
        }
        
        .course-thumb {
            width: 80px;
            height: 60px;
            background: #ddd;
            border-radius: 5px;
            margin-left: 15px;
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
            transition: var(--transition);
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
            transition: var(--transition);
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
            
            .dashboard-content {
                grid-template-columns: 1fr;
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
            
            nav ul {
                display: none;
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
                    <button id="loginBtn" class="btn btn-outline">تسجيل الدخول</button>
                    <button id="signupBtn" class="btn btn-filled">انضم إلينا</button>
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

    <!-- Interactive Stats Section -->
    <section class="interactive-section">
        <div class="container">
            <div class="section-title">
                <h2>إحصائيات حية</h2>
                <p>انضم إلى مجتمعنا المتنامي من الطلاب والمدرسين</p>
            </div>
            <div class="stats">
                <div class="stat-item">
                    <div class="stat-number" id="studentsCount">0</div>
                    <div class="stat-label">طالب مسجل</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number" id="coursesCount">0</div>
                    <div class="stat-label">دورة تعليمية</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number" id="teachersCount">0</div>
                    <div class="stat-label">مدرس معتمد</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number" id="successRate">0%</div>
                    <div class="stat-label">نسبة النجاح</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Login Modal -->
    <div id="loginModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>تسجيل الدخول</h2>
                <button class="close-modal">&times;</button>
            </div>
            <form id="loginForm">
                <div class="form-group">
                    <label for="email">البريد الإلكتروني</label>
                    <input type="email" id="email" required>
                </div>
                <div class="form-group">
                    <label for="password">كلمة المرور</label>
                    <input type="password" id="password" required>
                </div>
                <button type="submit" class="btn btn-filled" style="width: 100%;">تسجيل الدخول</button>
            </form>
            <p style="text-align: center; margin-top: 15px;">ليس لديك حساب؟ <a href="#" id="switchToSignup">سجل الآن</a></p>
        </div>
    </div>

    <!-- Signup Modal -->
    <div id="signupModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>إنشاء حساب جديد</h2>
                <button class="close-modal">&times;</button>
            </div>
            <form id="signupForm">
                <div class="form-group">
                    <label for="fullName">الاسم الكامل</label>
                    <input type="text" id="fullName" required>
                </div>
                <div class="form-group">
                    <label for="signupEmail">البريد الإلكتروني</label>
                    <input type="email" id="signupEmail" required>
                </div>
                <div class="form-group">
                    <label for="signupPassword">كلمة المرور</label>
                    <input type="password" id="signupPassword" required>
                </div>
                <div class="form-group">
                    <label for="confirmPassword">تأكيد كلمة المرور</label>
                    <input type="password" id="confirmPassword" required>
                </div>
                <button type="submit" class="btn btn-filled" style="width: 100%;">إنشاء الحساب</button>
            </form>
            <p style="text-align: center; margin-top: 15px;">لديك حساب بالفعل؟ <a href="#" id="switchToLogin">سجل الدخول</a></p>
        </div>
    </div>

    <!-- User Dashboard -->
    <div id="userDashboard" class="dashboard">
        <div class="container">
            <div class="dashboard-header">
                <div class="user-info">
                    <div class="user-avatar">
                        <i class="fas fa-user"></i>
                    </div>
                    <div>
                        <h2 id="userWelcome">مرحباً، أحمد!</h2>
                        <p>طالب في الصف الثالث الثانوي</p>
                    </div>
                </div>
                <button id="logoutBtn" class="btn btn-outline">تسجيل الخروج</button>
            </div>
            
            <div class="dashboard-nav">
                <button class="active" data-tab="courses">دوراتي</button>
                <button data-tab="progress">تقدمي</button>
                <button data-tab="schedule">جدولي</button>
                <button data-tab="profile">ملفي الشخصي</button>
            </div>
            
            <div class="dashboard-content">
                <div class="my-courses">
                    <h3>دوراتي النشطة</h3>
                    <div class="course-item">
                        <div class="course-thumb" style="background: linear-gradient(135deg, #8E44AD, #9B59B6);"></div>
                        <div>
                            <h4>الكيمياء العضوية المتقدمة</h4>
                            <p>الأستاذ أحمد محمد</p>
                            <div class="progress-bar">
                                <div class="progress" style="width: 75%;"></div>
                            </div>
                            <p>75% مكتمل</p>
                        </div>
                    </div>
                    <div class="course-item">
                        <div class="course-thumb" style="background: linear-gradient(135deg, #3498DB, #5DADE2);"></div>
                        <div>
                            <h4>الفيزياء الحديثة</h4>
                            <p>الأستاذ يوسف خالد</p>
                            <div class="progress-bar">
                                <div class="progress" style="width: 40%;"></div>
                            </div>
                            <p>40% مكتمل</p>
                        </div>
                    </div>
                </div>
                
                <div>
                    <div class="progress-tracker">
                        <h3>تقدمي العام</h3>
                        <div style="margin: 20px 0;">
                            <div style="display: flex; justify-content: space-between; margin-bottom: 10px;">
                                <span>الكيمياء</span>
                                <span>75%</span>
                            </div>
                            <div class="progress-bar">
                                <div class="progress" style="width: 75%;"></div>
                            </div>
                        </div>
                        <div style="margin: 20px 0;">
                            <div style="display: flex; justify-content: space-between; margin-bottom: 10px;">
                                <span>الفيزياء</span>
                                <span>40%</span>
                            </div>
                            <div class="progress-bar">
                                <div class="progress" style="width: 40%;"></div>
                            </div>
                        </div>
                        <div style="margin: 20px 0;">
                            <div style="display: flex; justify-content: space-between; margin-bottom: 10px;">
                                <span>الأحياء</span>
                                <span>20%</span>
                            </div>
                            <div class="progress-bar">
                                <div class="progress" style="width: 20%;"></div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="upcoming-classes">
                        <h3>الحصص القادمة</h3>
                        <div style="margin: 15px 0; padding: 10px; background: #f5f5f5; border-radius: 5px;">
                            <p><strong>الكيمياء العضوية</strong></p>
                            <p>غداً، 10:00 صباحاً</p>
                        </div>
                        <div style="margin: 15px 0; padding: 10px; background: #f5f5f5; border-radius: 5px;">
                            <p><strong>الفيزياء الحديثة</strong></p>
                            <p>بعد غد، 2:00 مساءً</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

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
        // عناصر DOM
        const loginBtn = document.getElementById('loginBtn');
        const signupBtn = document.getElementById('signupBtn');
        const loginModal = document.getElementById('loginModal');
        const signupModal = document.getElementById('signupModal');
        const closeModalButtons = document.querySelectorAll('.close-modal');
        const switchToSignup = document.getElementById('switchToSignup');
        const switchToLogin = document.getElementById('switchToLogin');
        const loginForm = document.getElementById('loginForm');
        const signupForm = document.getElementById('signupForm');
        const userDashboard = document.getElementById('userDashboard');
        const logoutBtn = document.getElementById('logoutBtn');
        const dashboardNavButtons = document.querySelectorAll('.dashboard-nav button');
        
        // فتح نافذة تسجيل الدخول
        loginBtn.addEventListener('click', () => {
            loginModal.style.display = 'flex';
        });
        
        // فتح نافذة إنشاء حساب
        signupBtn.addEventListener('click', () => {
            signupModal.style.display = 'flex';
        });
        
        // إغلاق النوافذ
        closeModalButtons.forEach(button => {
            button.addEventListener('click', () => {
                loginModal.style.display = 'none';
                signupModal.style.display = 'none';
            });
        });
        
        // التبديل بين نافذتي تسجيل الدخول وإنشاء حساب
        switchToSignup.addEventListener('click', (e) => {
            e.preventDefault();
            loginModal.style.display = 'none';
            signupModal.style.display = 'flex';
        });
        
        switchToLogin.addEventListener('click', (e) => {
            e.preventDefault();
            signupModal.style.display = 'none';
            loginModal.style.display = 'flex';
        });
        
        // معالجة تسجيل الدخول
        loginForm.addEventListener('submit', (e) => {
            e.preventDefault();
            // في التطبيق الحقيقي، هنا سيتم التحقق من بيانات المستخدم
            loginModal.style.display = 'none';
            userDashboard.style.display = 'block';
            document.querySelector('header').style.display = 'none';
            document.querySelector('.hero').style.display = 'none';
            document.querySelector('.features').style.display = 'none';
            document.querySelector('.subjects').style.display = 'none';
            document.querySelector('.interactive-section').style.display = 'none';
            document.querySelector('footer').style.marginTop = '0';
        });
        
        // معالجة إنشاء حساب
        signupForm.addEventListener('submit', (e) => {
            e.preventDefault();
            // في التطبيق الحقيقي، هنا سيتم إنشاء حساب جديد
            signupModal.style.display = 'none';
            userDashboard.style.display = 'block';
            document.querySelector('header').style.display = 'none';
            document.querySelector('.hero').style.display = 'none';
            document.querySelector('.features').style.display = 'none';
            document.querySelector('.subjects').style.display = 'none';
            document.querySelector('.interactive-section').style.display = 'none';
            document.querySelector('footer').style.marginTop = '0';
            
            // تعيين اسم المستخدم
            const fullName = document.getElementById('fullName').value;
            document.getElementById('userWelcome').textContent = `مرحباً، ${fullName}!`;
        });
        
        // تسجيل الخروج
        logoutBtn.addEventListener('click', () => {
            userDashboard.style.display = 'none';
            document.querySelector('header').style.display = 'block';
            document.querySelector('.hero').style.display = 'block';
            document.querySelector('.features').style.display = 'block';
            document.querySelector('.subjects').style.display = 'block';
            document.querySelector('.interactive-section').style.display = 'block';
            document.querySelector('footer').style.marginTop = '';
        });
        
        // التنقل في لوحة التحكم
        dashboardNavButtons.forEach(button => {
            button.addEventListener('click', () => {
                dashboardNavButtons.forEach(btn => btn.classList.remove('active'));
                button.classList.add('active');
                // في التطبيق الحقيقي، هنا سيتم تغيير محتوى لوحة التحكم
            });
        });
        
        // إحصائيات متحركة
        function animateCounter(element, target, duration) {
            let start = 0;
            const increment = target / (duration / 16);
            const timer = setInterval(() => {
                start += increment;
                if (start >= target) {
                    element.textContent = target;
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(start);
                }
            }, 16);
        }
        
        // تشغيل العدادات عند التمرير للقسم
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    animateCounter(document.getElementById('studentsCount'), 1250, 2000);
                    animateCounter(document.getElementById('coursesCount'), 48, 1500);
                    animateCounter(document.getElementById('teachersCount'), 32, 1500);
                    
                    let rate = 0;
                    const rateInterval = setInterval(() => {
                        rate += 1;
                        document.getElementById('successRate').textContent = `${rate}%`;
                        if (rate >= 94) clearInterval(rateInterval);
                    }, 20);
                    
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.5 });
        
        observer.observe(document.querySelector('.interactive-section'));
        
        // إضافة تأثيرات للبطاقات عند التمرير
        const cards = document.querySelectorAll('.feature-card, .subject-card, .course-card');
        const cardObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, { threshold: 0.1 });
        
        cards.forEach(card => {
            card.style.opacity = 0;
            card.style.transform = 'translateY(20px)';
            card.style.transition = 'opacity 0.5s, transform 0.5s';
            cardObserver.observe(card);
        });
    </script>
</body>
</html>
