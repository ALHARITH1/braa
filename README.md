<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive CV</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f4f8;
            color: #333;
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
        }

        h1, h2, h3 {
            color: #007BFF;
        }

        .editable {
            display: inline-block;
            border-bottom: 1px dashed #007BFF;
            cursor: pointer;
        }

        .editable:hover {
            background-color: #eef6ff;
        }

        img {
            border-radius: 50%;
            width: 150px;
            height: 150px;
            object-fit: cover;
        }

        .profile-pic {
            display: block;
            margin: 0 auto 20px;
            text-align: center;
        }

        .save-btn {
            background-color: #007BFF;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            display: inline-block;
        }

        .save-btn:hover {
            background-color: #0056b3;
        }

        label {
            font-weight: bold;
            margin-bottom: 5px;
            display: block;
        }

        input[type="file"] {
            display: block;
            margin: 10px auto;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Editable CV</h1>

    <!-- صورة قابلة للتعديل -->
    <div class="profile-pic">
        <img id="profile-pic" src="path_to_your_image.png" alt="Profile Picture">
        <input type="file" id="imageUpload" accept="image/*">
    </div>

    <!-- الاسم -->
    <h2>Name: <span id="name" class="editable">الحارث محمد عباس</span></h2>

    <!-- الملخص المهني -->
    <h3>Professional Summary:</h3>
    <p id="summary" class="editable">
        With 11 years of experience in Human Resources and Accounting, including expertise in government relations. 
        Major skills encompass HR management, financial reporting, budgeting and forecasting, compliance, and strategic planning.
        Holds a Master’s in Business Administration (HR), a Bachelor’s in Accounting, and a Diploma in Financial Accounting. 
        Demonstrates a proven track record in enhancing HR operations, optimizing payroll and benefits administration, 
        improving financial accuracy, and managing government interactions.
    </p>

    <!-- الخبرة العملية -->
    <h3>Work Experience:</h3>

    <h4>Third Layer Wireless Communications Company, Riyadh, Saudi Oct 2022 – Oct 2024</h4>
    <p id="experience1" class="editable">
        Human Resources Officer<br>
        - Oversaw HR operations for a large workforce, managing recruitment, onboarding, and employee relations.<br>
        - Implemented HR policies and procedures, improving regulatory compliance and reducing employee grievances.<br>
        - Conducted annual training programs for staff, leading to enhanced overall employee competency.<br>
        - Administered employee benefits and compensation, achieving better cost management while ensuring accurate and timely payroll.<br>
        - Analyzed HR metrics and produced monthly reports, supporting better decision-making and strategic planning.
    </p>

    <h4>Dawah and Guidance Association, Al-Muzahimiyah, Saudi Arabia Mar 2013 – Jan 2022</h4>
    <p id="experience2" class="editable">
        Accountant and HR Specialist<br>
        - Managed the financial transactions and accounts of the association, ensuring the accuracy of financial records and reports.<br>
        - Coordinated with various departments to implement financial and HR systems that enhanced overall efficiency.<br>
        - Handled employee relations, recruitment, and benefits administration, ensuring smooth HR operations.<br>
        - Supported strategic planning and governance initiatives by providing financial and human resource insights to leadership.
    </p>

    <h4>Al-Khayal Contracting Est, Riyadh, Saudi Arabia Aug 2012 – Feb 2013</h4>
    <p id="experience3" class="editable">
        Accounting Officer<br>
        - Processed and recorded daily transactions, ensuring 100% accuracy and compliance with financial regulations.<br>
        - Assisted in the preparation of financial statements and reports, contributing to on-time financial audits and reviews with a 98% compliance rate.<br>
        - Managed vendor accounts and resolved discrepancies, improving supplier payment processes and relationships by 20%.<br>
        - Monitored and analyzed financial data to support budgeting and forecasting, enhancing planning accuracy by 15%.
    </p>

    <!-- المهارات -->
    <h3>Skills:</h3>
    <ul id="skills" class="editable">
        <li>HR Management</li>
        <li>Financial Reporting</li>
        <li>Budgeting and Forecasting</li>
        <li>Compliance and Regulation</li>
        <li>Employee Training and Development</li>
        <li>Vendor Management</li>
        <li>Recruitment and Onboarding</li>
        <li>Employee Benefits and Compensation Administration</li>
        <li>Payroll Processing</li>
        <li>Accounting Software</li>
        <li>ERP Systems</li>
        <li>ClickUp Program</li>
        <li>Government Systems Platforms (Saudi Arabia)</li>
        <li>Microsoft Office Programs</li>
        <li>Data Analysis</li>
        <li>Strategic Planning</li>
    </ul>

    <!-- اللغات -->
    <h3>Languages:</h3>
    <p id="languages" class="editable">
        Arabic: Native<br>
        English: Intermediate
    </p>

    <!-- التعليم -->
    <h3>Education:</h3>
    <h4>Entrepreneurship & Business University, Saudi Arabia Mar 2022 – May 2024</h4>
    <p id="education1" class="editable">
        Master of Business Administration (MBA – HR)
    </p>

    <h4>Arab International Academy, Saudi Arabia Jul 2019 – Sep 2022</h4>
    <p id="education2" class="editable">
        Bachelor of Accounting
    </p>

    <h4>University of Khartoum, Khartoum, Sudan Apr 2009 – Jan 2012</h4>
    <p id="education3" class="editable">
        Diploma in Financial Accounting
    </p>

    <!-- زر حفظ التعديلات -->
    <button class="save-btn" onclick="saveChanges()">Save Changes</button>
</div>

<script>
    // تحميل صورة جديدة
    const imageInput = document.getElementById('imageUpload');
    imageInput.addEventListener('change', function() {
        const reader = new FileReader();
        reader.onload = function() {
            document.getElementById('profile-pic').src = reader.result;
        };
        reader.readAsDataURL(this.files[0]);
    });

    // التفاعل مع الحقول القابلة للتعديل
    const editableElements = document.querySelectorAll('.editable');

    editableElements.forEach(function(element) {
        element.addEventListener('click', function() {
            const currentText = element.innerText;
            const input = document.createElement('input');
            input.type = 'text';
            input.value = currentText;
            input.style.width = '100%';
            element.innerHTML = '';
            element.appendChild(input);

            // استعادة النص عند فقدان التركيز (blur)
            input.addEventListener('blur', function() {
                element.innerHTML = input.value;
            });

            // حفظ النص عند الضغط على Enter
            input.addEventListener('keydown', function(event) {
                if (event.key === 'Enter') {
                    element.innerHTML = input.value;
                }
            });
        });
    });

    // حفظ التعديلات
    function saveChanges() {
        alert('Changes saved successfully!');
    }
</script>

</body>
</html>
