<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>السيرة الذاتية - الحارث محمد عباس</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f8ff;
            color: #333;
            margin: 0;
            padding: 0;
            direction: rtl;
        }

        .container {
            width: 90%;
            margin: auto;
            padding: 20px;
            background-color: #ffffff;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            border-radius: 15px;
            margin-top: 30px;
        }

        header {
            text-align: center;
            margin-bottom: 20px;
            background-color: #1e90ff;
            padding: 20px;
            border-radius: 15px 15px 0 0;
        }

        header img {
            border-radius: 50%;
            width: 150px;
            height: 150px;
            object-fit: cover;
            border: 5px solid #ffffff;
            background-color: #fff;
        }

        h1 {
            color: #ffffff;
            margin: 15px 0;
            font-size: 28px;
        }

        .contact-info {
            margin-bottom: 20px;
            text-align: center;
            color: #fff;
        }

        .contact-info a {
            color: #ffffff;
            text-decoration: none;
        }

        .contact-info a:hover {
            text-decoration: underline;
        }

        h2 {
            color: #1e90ff;
            border-bottom: 2px solid #1e90ff;
            padding-bottom: 10px;
            margin-bottom: 20px;
        }

        .section {
            margin-bottom: 30px;
        }

        .section ul {
            list-style-type: none;
            padding: 0;
        }

        .section ul li {
            background-color: #f0f8ff;
            margin: 8px 0;
            padding: 10px;
            border-radius: 8px;
            border-left: 5px solid #1e90ff;
            transition: background-color 0.3s ease, box-shadow 0.3s ease;
        }

        .section ul li:hover {
            background-color: #e6f7ff;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        footer {
            text-align: center;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid #ccc;
        }

        footer p {
            font-size: 0.9em;
            color: #666;
        }

        /* زر لتحميل الصورة */
        .image-upload {
            display: none;
        }

        .upload-btn {
            margin-top: 10px;
            padding: 10px 20px;
            background-color: #1e90ff;
            color: #ffffff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .upload-btn:hover {
            background-color: #1c7ed6;
        }
    </style>
</head>
<body>

    <div class="container">
        <header>
            <!-- الصورة الشخصية -->
            <img id="profile-pic" src="تنزيل.png" alt="الحارث محمد عباس">
            <h1>الحارث محمد عباس</h1>
            <div class="contact-info">
                <p>اتصال: +966543756069 | البريد الإلكتروني: <a href="mailto:alharith.moh@gmail.com">alharith.moh@gmail.com</a></p>
                <p>العنوان: الرياض، السعودية | <a href="https://www.linkedin.com/in/الحارث-محمد-elharith-abas-77598a11a/" target="_blank">LinkedIn</a></p>
            </div>
            <!-- زر تغيير الصورة -->
            <input type="file" id="image-upload" class="image-upload" accept="image/*" onchange="changeProfilePic(event)">
            <br>
            <button class="upload-btn" onclick="document.getElementById('image-upload').click()">تغيير الصورة</button>
        </header>

        <section class="section">
            <h2>الملخص المهني</h2>
            <p>أكثر من 11 عامًا من الخبرة في إدارة الموارد البشرية والمحاسبة، بما في ذلك العلاقات الحكومية والتخطيط الاستراتيجي. يحمل درجة ماجستير في إدارة الأعمال (HR) وبكالوريوس في المحاسبة. خبرة في تحسين العمليات الإدارية والمالية، وتطوير استراتيجيات الامتثال، وتحليل البيانات لدعم اتخاذ القرارات.</p>
        </section>

        <section class="section">
            <h2>الخبرة العملية</h2>
            <ul>
                <li>
                    <strong>Third Layer Wireless Communications Company</strong> - الرياض، السعودية<br>
                    <em>أكتوبر 2022 – أكتوبر 2024</em><br>
                    أخصائي موارد بشرية: أشرفت على عمليات الموارد البشرية، إدارة التوظيف، العلاقات الحكومية، وتطوير الإجراءات التنظيمية.
                </li>
                <li>
                    <strong>جمعية الدعوة والإرشاد وتوعية الجاليات</strong> - المزاحمية، السعودية<br>
                    <em>مارس 2013 – يناير 2022</em><br>
                    محاسب وأخصائي موارد بشرية: إدارة الحسابات، الرواتب، وميزانية الجمعية بشكل احترافي، وتحسين نظم الحوكمة.
                </li>
                <li>
                    <strong>مؤسسة الخيال للمقاولات</strong> - الرياض، السعودية<br>
                    <em>أغسطس 2012 – فبراير 2013</em><br>
                    مسؤول حسابات: إدارة التعاملات اليومية وإعداد التقارير المالية.
                </li>
            </ul>
        </section>

        <section class="section">
            <h2>المهارات</h2>
            <ul>
                <li>إدارة الموارد البشرية</li>
                <li>التقارير المالية</li>
                <li>إعداد الميزانية والتنبؤ المالي</li>
                <li>الامتثال واللوائح</li>
                <li>التدريب والتطوير</li>
                <li>إدارة الموردين</li>
                <li>التوظيف وإدارة الأداء</li>
                <li>نظم الـ ERP</li>
                <li>التحليل المالي وإدارة البيانات</li>
                <li>استخدام برامج Microsoft Office</li>
                <li>إدارة العلاقات الحكومية</li>
            </ul>
        </section>

        <section class="section">
            <h2>التعليم</h2>
            <ul>
                <li>ماجستير في إدارة الأعمال (HR) - جامعة ريادة الأعمال والأعمال، السعودية - 2024</li>
                <li>بكالوريوس في المحاسبة - الأكاديمية العربية الدولية، السعودية - 2022</li>
                <li>دبلوم في المحاسبة المالية - جامعة الخرطوم، السودان - 2012</li>
            </ul>
        </section>

        <footer>
            <p>© 2024 الحارث محمد عباس. جميع الحقوق محفوظة.</p>
        </footer>
    </div>

    <script>
        function changeProfilePic(event) {
            var reader = new FileReader();
            reader.onload = function(){
                var output = document.getElementById('profile-pic');
                output.src = reader.result;
            };
            reader.readAsDataURL(event.target.files[0]);
        }
    </script>

</body>
</html>
