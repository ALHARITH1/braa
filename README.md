<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Editable CV</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f4f8;
            color: #333;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1, h2, h3 {
            color: #007BFF; /* اللون الأزرق */
        }
        .editable {
            background-color: #f9f9f9;
            padding: 5px;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-bottom: 10px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input[type="text"], textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-bottom: 10px;
        }
        button {
            background-color: #007BFF;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        img {
            border-radius: 50%;
            width: 150px;
            height: 150px;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Editable CV</h1>
    
    <!-- صورة قابلة للتعديل -->
    <div>
        <img id="profile-pic" src="path_to_your_image.png" alt="Profile Picture">
        <br><br>
        <input type="file" id="imageUpload" accept="image/*">
    </div>
    
    <!-- الاسم -->
    <h2 id="name-display">الحارث محمد عباس</h2>
    <label for="name">Name:</label>
    <input type="text" id="name" value="الحارث محمد عباس">
    
    <!-- الملخص المهني -->
    <h3>Professional Summary</h3>
    <p id="summary-display">With 11 years of experience in Human Resources and Accounting...</p>
    <label for="summary">Summary:</label>
    <textarea id="summary">With 11 years of experience in Human Resources and Accounting...</textarea>
    
    <!-- الخبرة العملية -->
    <h3>Work Experience</h3>
    <p id="experience-display">Third Layer Wireless Communications Company, Riyadh, Saudi Oct 2022 – Oct 2024...</p>
    <label for="experience">Experience:</label>
    <textarea id="experience">Third Layer Wireless Communications Company, Riyadh, Saudi Oct 2022 – Oct 2024...</textarea>
    
    <!-- زر حفظ التعديلات -->
    <button onclick="saveChanges()">Save Changes</button>
</div>

<script>
    // تحميل الصورة الجديدة
    const imageInput = document.getElementById('imageUpload');
    imageInput.addEventListener('change', function() {
        const reader = new FileReader();
        reader.onload = function() {
            document.getElementById('profile-pic').src = reader.result;
        };
        reader.readAsDataURL(this.files[0]);
    });

    // حفظ التعديلات
    function saveChanges() {
        const name = document.getElementById('name').value;
        const summary = document.getElementById('summary').value;
        const experience = document.getElementById('experience').value;

        document.getElementById('name-display').innerText = name;
        document.getElementById('summary-display').innerText = summary;
        document.getElementById('experience-display').innerText = experience;
    }
</script>

</body>
</html>
