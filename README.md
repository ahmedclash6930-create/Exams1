# Exams1
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة الاختبارات الذكية - Ahmed Hatem Asaad</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #3498db;
            --secondary: #2ecc71;
            --accent: #e74c3c;
            --dark: #2c3e50;
            --light: #ecf0f1;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
            direction: rtl;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, var(--dark), #34495e);
            color: white;
            padding: 40px;
            text-align: center;
            position: relative;
        }

        .creator-signature {
            background: linear-gradient(135deg, var(--accent), #c0392b);
            color: white;
            padding: 15px 30px;
            border-radius: 50px;
            display: inline-block;
            font-size: 1.3em;
            font-weight: bold;
            margin-bottom: 20px;
            box-shadow: 0 5px 15px rgba(231, 76, 60, 0.3);
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .ai-badge {
            background: linear-gradient(135deg, #9b59b6, #8e44ad);
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            display: inline-block;
            margin: 10px 0;
            font-weight: bold;
        }

        /* Tab Navigation */
        .tabs {
            display: flex;
            background: var(--dark);
            border-bottom: 3px solid var(--primary);
        }

        .tab {
            flex: 1;
            padding: 20px;
            text-align: center;
            background: var(--dark);
            color: white;
            border: none;
            cursor: pointer;
            font-size: 1.1em;
            font-weight: bold;
            transition: all 0.3s ease;
            border-bottom: 3px solid transparent;
        }

        .tab.active {
            background: var(--primary);
            border-bottom: 3px solid var(--secondary);
        }

        .tab:hover:not(.disabled) {
            background: var(--primary);
        }

        .tab.disabled {
            opacity: 0.5;
            cursor: not-allowed;
            background: var(--dark) !important;
        }

        /* Tab Content */
        .tab-content {
            display: none;
            padding: 40px;
        }

        .tab-content.active {
            display: block;
        }

        /* Upload Section */
        .upload-section {
            background: var(--light);
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 30px;
            border: 3px dashed var(--primary);
            text-align: center;
        }

        .upload-area {
            border: 2px dashed #bdc3c7;
            border-radius: 10px;
            padding: 50px;
            text-align: center;
            margin: 20px 0;
            cursor: pointer;
            transition: all 0.3s ease;
            background: white;
        }

        .upload-area.dragover {
            border-color: var(--primary);
            background: #ebf5fb;
            transform: scale(1.02);
        }

        .upload-icon {
            font-size: 4em;
            margin-bottom: 20px;
            color: var(--primary);
        }

        .file-input {
            display: none;
        }

        .upload-button {
            background: var(--primary);
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1.2em;
            font-weight: bold;
            margin: 15px;
            transition: all 0.3s ease;
        }

        .upload-button:hover {
            background: #2980b9;
            transform: translateY(-2px);
        }

        /* Exam Settings */
        .exam-settings {
            background: white;
            padding: 30px;
            border-radius: 15px;
            border: 2px solid var(--light);
            margin: 20px 0;
        }

        .setting-group {
            margin: 20px 0;
        }

        .setting-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: var(--dark);
        }

        .setting-group select, .setting-group input {
            width: 100%;
            padding: 12px;
            border: 2px solid #bdc3c7;
            border-radius: 8px;
            font-size: 1em;
            transition: all 0.3s ease;
        }

        .setting-group select:focus, .setting-group input:focus {
            border-color: var(--primary);
            outline: none;
        }

        .generate-btn {
            background: linear-gradient(135deg, var(--secondary), #27ae60);
            color: white;
            padding: 18px 50px;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1.3em;
            font-weight: bold;
            margin: 30px auto;
            display: block;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(46, 204, 113, 0.3);
        }

        .generate-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(46, 204, 113, 0.4);
        }

        /* Exam Section */
        .exam-header {
            background: linear-gradient(135deg, var(--dark), #34495e);
            color: white;
            padding: 30px;
            text-align: center;
            border-radius: 15px;
            margin-bottom: 30px;
        }

        .timer {
            background: var(--accent);
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            font-size: 1.2em;
            font-weight: bold;
            margin: 10px 0;
            display: inline-block;
        }

        .question {
            background: #f8f9fa;
            padding: 30px;
            border-radius: 15px;
            margin: 20px 0;
            border: 2px solid #e9ecef;
        }

        .question-number {
            background: var(--primary);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-bottom: 15px;
        }

        .options {
            margin: 20px 0;
        }

        .option {
            background: white;
            padding: 15px;
            margin: 10px 0;
            border: 2px solid #bdc3c7;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .option:hover {
            border-color: var(--primary);
            background: #ebf5fb;
        }

        .option.selected {
            border-color: var(--secondary);
            background: #d5f4e6;
        }

        .navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 30px;
        }

        .nav-btn {
            background: var(--primary);
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .nav-btn:hover {
            background: #2980b9;
            transform: translateY(-2px);
        }

        .nav-btn:disabled {
            background: #bdc3c7;
            cursor: not-allowed;
            transform: none;
        }

        .submit-btn {
            background: linear-gradient(135deg, var(--secondary), #27ae60);
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1.2em;
            font-weight: bold;
            margin: 20px auto;
            display: block;
            transition: all 0.3s ease;
        }

        .submit-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(46, 204, 113, 0.4);
        }

        .progress-bar {
            width: 100%;
            height: 10px;
            background: #ecf0f1;
            border-radius: 5px;
            margin: 20px 0;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            width: 0%;
            transition: width 0.3s ease;
        }

        /* Notification */
        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            background: var(--secondary);
            color: white;
            padding: 15px 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            display: none;
            z-index: 1000;
        }

        .notification.error {
            background: var(--accent);
        }

        .file-preview {
            margin: 20px 0;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 10px;
            display: none;
        }

        .file-info {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .file-icon {
            font-size: 2em;
        }

        .no-exam-message {
            text-align: center;
            padding: 60px;
            color: #7f8c8d;
        }

        .no-exam-message .icon {
            font-size: 4em;
            margin-bottom: 20px;
        }

        .exam-active {
            display: block !important;
        }

        .exam-hidden {
            display: none !important;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="creator-signature">
                🎯 منصة الاختبارات الذكية - أحمد حاتم أسعد
            </div>
            <h1>اختبارات ذكية مدعومة بالذكاء الاصطناعي</h1>
            <div class="ai-badge">🤖 مدعوم بواسطة DeepSeek AI</div>
            <p>ارفع ملفك الدراسي وسأقوم بإنشاء اختبار مخصص لك!</p>
        </div>

        <!-- Tab Navigation -->
        <div class="tabs">
            <button class="tab active" onclick="switchTab('upload')">📤 رفع الملف وإنشاء الاختبار</button>
            <button class="tab disabled" id="examTab" onclick="switchTab('exam')">📝 أداء الاختبار</button>
        </div>

        <!-- Upload Tab -->
        <div class="tab-content active" id="uploadTab">
            <div class="upload-section">
                <h2>📤 ارفع ملفك الدراسي</h2>
                <p>يمكنك رفع ملفات PDF، Word، PowerPoint، أو حتى نص عادي</p>
                
                <div class="upload-area" id="uploadArea">
                    <div class="upload-icon">📁</div>
                    <h3>اسحب الملف هنا أو انقر للاختيار</h3>
                    <p>يدعم: PDF, DOC, DOCX, PPT, PPTX, TXT</p>
                    <p style="color: var(--accent); margin-top: 10px;" id="fileInfo">لم يتم اختيار أي ملف</p>
                </div>

                <input type="file" id="fileInput" class="file-input" 
                       accept=".pdf,.doc,.docx,.ppt,.pptx,.txt,.md">

                <div class="file-preview" id="filePreview">
                    <div class="file-info">
                        <div class="file-icon" id="fileIcon">📄</div>
                        <div>
                            <div id="fileName" style="font-weight: bold;"></div>
                            <div id="fileSize" style="color: #7f8c8d;"></div>
                        </div>
                    </div>
                </div>

                <button class="upload-button" onclick="processFile()">
                    📝 معالجة الملف بواسطة الذكاء الاصطناعي
                </button>
            </div>

            <div class="exam-settings">
                <h2>⚙️ إعدادات الاختبار</h2>
                
                <div class="setting-group">
                    <label>📊 نوع الاختبار:</label>
                    <select id="examType">
                        <option value="mcq">اختيار من متعدد</option>
                        <option value="truefalse">صح أم خطأ</option>
                        <option value="mixed">مختلط</option>
                    </select>
                </div>

                <div class="setting-group">
                    <label>🔢 عدد الأسئلة:</label>
                    <select id="questionCount">
                        <option value="5">5 أسئلة</option>
                        <option value="10" selected>10 أسئلة</option>
                        <option value="15">15 أسئلة</option>
                        <option value="20">20 أسئلة</option>
                    </select>
                </div>

                <div class="setting-group">
                    <label>⏱️ وقت الاختبار (دقائق):</label>
                    <select id="examTime">
                        <option value="10">10 دقائق</option>
                        <option value="20">20 دقائق</option>
                        <option value="30" selected>30 دقائق</option>
                        <option value="45">45 دقائق</option>
                        <option value="60">60 دقائق</option>
                    </select>
                </div>

                <div class="setting-group">
                    <label>🎯 مستوى الصعوبة:</label>
                    <select id="difficulty">
                        <option value="easy">سهل</option>
                        <option value="medium" selected>متوسط</option>
                        <option value="hard">صعب</option>
                    </select>
                </div>

                <div class="setting-group">
                    <label>📚 التركيز على:</label>
                    <input type="text" id="focusArea" placeholder="مثال: التفاضل، الكيمياء العضوية، التاريخ الإسلامي...">
                </div>
            </div>

            <button class="generate-btn" onclick="generateExam()">
                🚀 إنشاء الاختبار الذكي
            </button>
        </div>

        <!-- Exam Tab -->
        <div class="tab-content" id="examTab">
            <div class="exam-header">
                <h1>📝 الاختبار الذكي</h1>
                <div class="timer" id="timer">⏱️ --:--</div>
                <p id="examInfo">لم يتم إنشاء اختبار بعد</p>
            </div>

            <div class="progress-bar">
                <div class="progress-fill" id="progressFill"></div>
            </div>

            <div id="questionsContainer">
                <div class="no-exam-message">
                    <div class="icon">📝</div>
                    <h3>لا يوجد اختبار جاهز بعد</h3>
                    <p>يرجى العودة إلى تبويب "رفع الملف" وإنشاء اختبار أولاً</p>
                    <button class="upload-button" onclick="switchTab('upload')" style="margin-top: 20px;">
                        العودة لإنشاء الاختبار
                    </button>
                </div>
            </div>

            <div class="navigation exam-hidden" id="examNavigation">
                <button class="nav-btn" id="prevBtn" onclick="previousQuestion()">السابق</button>
                <button class="nav-btn" id="nextBtn" onclick="nextQuestion()">التالي</button>
            </div>

            <button class="submit-btn exam-hidden" onclick="submitExam()" id="submitBtn">✅ إنهاء الاختبار</button>
        </div>
    </div>

    <div class="notification" id="notification"></div>

    <script>
        // البيانات المشتركة
        let currentFile = null;
        let examQuestions = [];
        let currentQuestion = 0;
        let userAnswers = [];
        let timeLeft = 0;
        let timerInterval;
        let examGenerated = false;

        // عناصر DOM
        const uploadArea = document.getElementById('uploadArea');
        const fileInput = document.getElementById('fileInput');
        const filePreview = document.getElementById('filePreview');
        const fileName = document.getElementById('fileName');
        const fileSize = document.getElementById('fileSize');
        const fileIcon = document.getElementById('fileIcon');
        const fileInfo = document.getElementById('fileInfo');
        const notification = document.getElementById('notification');
        const examTab = document.getElementById('examTab');
        const examInfo = document.getElementById('examInfo');
        const examNavigation = document.getElementById('examNavigation');
        const submitBtn = document.getElementById('submitBtn');
        const questionsContainer = document.getElementById('questionsContainer');

        // دوال التبويب
        function switchTab(tabName) {
            // إخفاء كل المحتويات
            document.querySelectorAll('.tab-content').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // إلغاء تفعيل كل الأزرار
            document.querySelectorAll('.tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // إظهار المحتوى المطلوب
            document.getElementById(tabName + 'Tab').classList.add('active');
            
            // تفعيل الزر المطلوب
            document.querySelector(`.tab[onclick="switchTab('${tabName}')"]`).classList.add('active');

            // إذا كان التبويب هو الاختبار وكان هناك اختبار مولد، عرضه
            if (tabName === 'exam' && examGenerated) {
                startExam(); // ✅ هذا هو التصحيح المهم
            }
        }

        // أحداث سحب وإفلات الملفات
        uploadArea.addEventListener('click', () => fileInput.click());
        
        uploadArea.addEventListener('dragover', (e) => {
            e.preventDefault();
            uploadArea.classList.add('dragover');
        });

        uploadArea.addEventListener('dragleave', () => {
            uploadArea.classList.remove('dragover');
        });

        uploadArea.addEventListener('drop', (e) => {
            e.preventDefault();
            uploadArea.classList.remove('dragover');
            fileInput.files = e.dataTransfer.files;
            handleFileSelect();
        });

        fileInput.addEventListener('change', handleFileSelect);

        function handleFileSelect() {
            const file = fileInput.files[0];
            if (!file) return;

            currentFile = file;
            
            // عرض معلومات الملف
            fileName.textContent = file.name;
            fileSize.textContent = formatFileSize(file.size);
            fileInfo.textContent = `تم اختيار: ${file.name}`;
            fileInfo.style.color = '#27ae60';
            
            // تعيين الأيقونة المناسبة
            const icon = getFileIcon(file.name);
            fileIcon.textContent = icon;
            
            filePreview.style.display = 'block';
            
            showNotification('تم تحميل الملف بنجاح!');
        }

        function processFile() {
            if (!currentFile) {
                showNotification('يرجى اختيار ملف أولاً', 'error');
                return;
            }

            showNotification('🤖 جاري تحليل الملف بواسطة الذكاء الاصطناعي...');

            // محاكاة معالجة الملف
            setTimeout(() => {
                showNotification('تم تحليل الملف بنجاح! يمكنك الآن إنشاء الاختبار');
            }, 2000);
        }

        function generateExam() {
            if (!currentFile) {
                showNotification('يرجى رفع ملف أولاً', 'error');
                return;
            }

            const examType = document.getElementById('examType').value;
            const questionCount = parseInt(document.getElementById('questionCount').value);
            const examTime = parseInt(document.getElementById('examTime').value);
            const difficulty = document.getElementById('difficulty').value;
            const focusArea = document.getElementById('focusArea').value;

            showNotification('🤖 جاري إنشاء الاختبار الذكي...');

            // محاكاة إنشاء الأسئلة بواسطة الذكاء الاصطناعي
            setTimeout(() => {
                // توليد أسئلة مثال
                examQuestions = generateSampleQuestions(questionCount);
                timeLeft = examTime * 60;
                
                // تمكين تبويب الاختبار
                examTab.classList.remove('disabled');
                examTab.disabled = false;
                
                // تعيين علامة أن الاختبار تم إنشاؤه
                examGenerated = true;
                
                // تحديث معلومات الاختبار
                examInfo.textContent = `تم إنشاء اختبار ${questionCount} أسئلة - ${examTime} دقيقة - مستوى ${difficulty}`;
                
                showNotification(`✅ تم إنشاء الاختبار بنجاح! ${questionCount} أسئلة جاهزة`);
                
                // الانتقال تلقائياً لتبويب الاختبار
                switchTab('exam');
                
            }, 2000);
        }

        function generateSampleQuestions(count) {
            const questions = [];
            const topics = ['الرياضيات', 'الفيزياء', 'الكيمياء', 'الأحياء', 'التاريخ', 'الجغرافيا'];
            const questionTexts = {
                'الرياضيات': [
                    'ما هو ناتج جمع 15 + 27؟',
                    'ما هو محيط الدائرة التي نصف قطرها 7 سم؟',
                    'ما هو حل المعادلة: 2س + 5 = 15؟',
                    'ما هو مساحة المربع الذي طول ضلعه 5 سم؟',
                    'ما هو الجذر التربيعي للعدد 64؟'
                ],
                'الفيزياء': [
                    'ما هي وحدة قياس القوة في النظام الدولي؟',
                    'ما هو قانون نيوتن الأول؟',
                    'كيف تحسب السرعة المتوسطة؟',
                    'ما هي أنواع الطاقة؟',
                    'ما هو الفرق بين الكتلة والوزن؟'
                ],
                'الكيمياء': [
                    'ما هو الرمز الكيميائي للذهب؟',
                    'ما هو عدد الإلكترونات في ذرة الأكسجين؟',
                    'ما هو الغاز النبيل الأكثر انتشاراً في الغلاف الجوي؟',
                    'ما هو الرقم الهيدروجيني للماء النقي؟',
                    'ما هي أنواع الروابط الكيميائية؟'
                ],
                'الأحياء': [
                    'ما هو العضو المسؤول عن ضخ الدم في الجسم؟',
                    'ما هي عملية البناء الضوئي؟',
                    'كم عدد الكروموسومات في الإنسان؟',
                    'ما هو الفرق بين الخلية النباتية والحيوانية؟',
                    'ما هي وظيفة الميتوكوندريا؟'
                ]
            };
            
            for (let i = 0; i < count; i++) {
                const topic = topics[Math.floor(Math.random() * topics.length)];
                const questionList = questionTexts[topic] || ['ما هو ...؟'];
                const questionText = questionList[Math.floor(Math.random() * questionList.length)];
                
                // إنشاء خيارات متنوعة
                const options = [
                    'الإجابة الصحيحة',
                    'إجابة خاطئة 1',
                    'إجابة خاطئة 2', 
                    'إجابة خاطئة 3'
                ];
                
                // خلط الخيارات عشوائياً
                for (let j = options.length - 1; j > 0; j--) {
                    const k = Math.floor(Math.random() * (j + 1));
                    [options[j], options[k]] = [options[k], options[j]];
                }
                
                questions.push({
                    id: i + 1,
                    question: `سؤال ${i + 1}: ${questionText}`,
                    type: Math.random() > 0.3 ? 'mcq' : 'truefalse',
                    options: options,
                    correctAnswer: options.indexOf('الإجابة الصحيحة'),
                    explanation: `شرح الإجابة الصحيحة للسؤال ${i + 1}`
                });
            }
            return questions;
        }

        // ✅ دوال الاختبار - هذه هي الدوال الأساسية
        function startExam() {
            console.log('بدء الاختبار - عدد الأسئلة:', examQuestions.length); // للتتبع
            currentQuestion = 0;
            userAnswers = new Array(examQuestions.length).fill(null);
            
            // إظهار عناصر التحكم
            examNavigation.classList.remove('exam-hidden');
            examNavigation.classList.add('exam-active');
            submitBtn.classList.remove('exam-hidden');
            submitBtn.classList.add('exam-active');
            
            startTimer();
            displayQuestion();
        }

        function startTimer() {
            clearInterval(timerInterval);
            updateTimer(); // التحديث الأولي
            
            timerInterval = setInterval(() => {
                timeLeft--;
                updateTimer();
                
                if (timeLeft <= 0) {
                    clearInterval(timerInterval);
                    submitExam();
                }
            }, 1000);
        }

        function updateTimer() {
            const minutes = Math.floor(timeLeft / 60);
            const seconds = timeLeft % 60;
            document.getElementById('timer').textContent = 
                `⏱️ ${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        }

        function displayQuestion() {
            console.log('عرض السؤال:', currentQuestion + 1); // للتتبع
            
            if (!examGenerated || examQuestions.length === 0) {
                questionsContainer.innerHTML = `
                    <div class="no-exam-message">
                        <div class="icon">📝</div>
                        <h3>لا يوجد اختبار جاهز بعد</h3>
                        <p>يرجى العودة إلى تبويب "رفع الملف" وإنشاء اختبار أولاً</p>
                        <button class="upload-button" onclick="switchTab('upload')" style="margin-top: 20px;">
                            العودة لإنشاء الاختبار
                        </button>
                    </div>
                `;
                return;
            }

            const question = examQuestions[currentQuestion];
            
            let questionHTML = `
                <div class="question">
                    <div class="question-number">${currentQuestion + 1}</div>
                    <h3>${question.question}</h3>
                    <div class="options">
            `;

            if (question.type === 'mcq') {
                question.options.forEach((option, index) => {
                    const isSelected = userAnswers[currentQuestion] === index;
                    questionHTML += `
                        <div class="option ${isSelected ? 'selected' : ''}" 
                             onclick="selectAnswer(${index})">
                            ${String.fromCharCode(1570 + index)}) ${option}
                        </div>
                    `;
                });
            } else if (question.type === 'truefalse') {
                questionHTML += `
                    <div class="option ${userAnswers[currentQuestion] === true ? 'selected' : ''}" 
                         onclick="selectAnswer(true)">
                        ✅ صح
                    </div>
                    <div class="option ${userAnswers[currentQuestion] === false ? 'selected' : ''}" 
                         onclick="selectAnswer(false)">
                        ❌ خطأ
                    </div>
                `;
            }

            questionHTML += `</div></div>`;
            questionsContainer.innerHTML = questionHTML;
            
            updateProgress();
            updateNavigation();
        }

        function selectAnswer(answer) {
            userAnswers[currentQuestion] = answer;
            displayQuestion();
        }

        function nextQuestion() {
            if (currentQuestion < examQuestions.length - 1) {
                currentQuestion++;
                displayQuestion();
            }
        }

        function previousQuestion() {
            if (currentQuestion > 0) {
                currentQuestion--;
                displayQuestion();
            }
        }

        function updateProgress() {
            const progress = ((currentQuestion + 1) / examQuestions.length) * 100;
            document.getElementById('progressFill').style.width = progress + '%';
        }

        function updateNavigation() {
            document.getElementById('prevBtn').disabled = currentQuestion === 0;
            document.getElementById('nextBtn').disabled = currentQuestion === examQuestions.length - 1;
        }

        function submitExam() {
            clearInterval(timerInterval);
            
            // حساب النتيجة
            let score = 0;
            examQuestions.forEach((question, index) => {
                if (userAnswers[index] === question.correctAnswer) {
                    score++;
                }
            });

            const percentage = (score / examQuestions.length) * 100;
            const timeSpent = Math.round((parseInt(document.getElementById('examTime').value) * 60 - timeLeft) / 60);
            
            showNotification(`🎉 تم إنهاء الاختبار! نتيجتك: ${score}/${examQuestions.length} (${Math.round(percentage)}%)`);
            
            // عرض النتائج في نافذة منبثقة
            setTimeout(() => {
                alert(`🎊 نتيجة الاختبار:\n\n✅ الإجابات الصحيحة: ${score}\n❌ الإجابات الخاطئة: ${examQuestions.length - score}\n📊 النسبة: ${Math.round(percentage)}%\n⏱️ الوقت المستغرق: ${timeSpent} دقيقة\n\n💡 يمكنك إنشاء اختبار جديد من تبويب رفع الملف`);
            }, 1000);
        }

        // دوال مساعدة
        function getFileIcon(filename) {
            const ext = filename.split('.').pop().toLowerCase();
            const icons = {
                pdf: '📕',
                doc: '📘', docx: '📘',
                ppt: '📊', pptx: '📊',
                txt: '📄', md: '📄'
            };
            return icons[ext] || '📄';
        }

        function formatFileSize(bytes) {
            if (bytes < 1024) return bytes + ' Bytes';
            else if (bytes < 1048576) return (bytes / 1024).toFixed(1) + ' KB';
            else return (bytes / 1048576).toFixed(1) + ' MB';
        }

        function showNotification(message, type = 'success') {
            notification.textContent = message;
            notification.className = 'notification ' + (type === 'error' ? 'error' : '');
            notification.style.display = 'block';
            
            setTimeout(() => {
                notification.style.display = 'none';
            }, 4000);
        }
    </script>
</body>
</html>
