<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>صلاتي خلاصي - أجبية الأطفال</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&family=Amiri:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --baby-blue: #E3F2FD;
            --main-blue: #B3E5FC;
            --dark-blue: #0288D1;
            --white: #ffffff;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--baby-blue);
            background-image: url('https://www.transparenttextures.com/patterns/clouds.png');
            margin: 0; padding: 0; color: #333;
        }

        header {
            background: linear-gradient(to bottom, var(--dark-blue), var(--main-blue));
            color: white; padding: 40px 20px; text-align: center;
            border-bottom-left-radius: 50px; border-bottom-right-radius: 50px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .container { max-width: 900px; margin: auto; padding: 20px; }

        .tabs {
            display: flex; flex-wrap: wrap; justify-content: center;
            gap: 10px; margin-bottom: 20px; margin-top: -30px;
        }

        .tab-btn {
            background: white; border: 2px solid var(--dark-blue);
            padding: 10px 20px; border-radius: 25px; cursor: pointer;
            font-weight: bold; color: var(--dark-blue); transition: 0.3s;
        }

        .tab-btn.active { background: var(--dark-blue); color: white; }

        .prayer-card {
            background: white; border-radius: 30px; padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05); border: 4px solid var(--main-blue);
            display: none; min-height: 400px;
        }

        .prayer-card.active { display: block; animation: fadeIn 0.5s; }

        .prayer-text {
            font-family: 'Amiri', serif; font-size: 1.4em; line-height: 1.8;
            color: #2c3e50; text-align: justify;
        }

        .prayer-text strong { color: var(--dark-blue); display: block; margin-top: 15px; }

        .notebook {
            background: white; border-radius: 30px; padding: 25px;
            margin-top: 40px; border: 5px dashed var(--main-blue);
        }

        input[type="text"] {
            width: 80%; padding: 12px; border-radius: 15px;
            border: 2px solid var(--main-blue); font-size: 1.1em; margin: 10px 0; text-align: center;
        }

        table { width: 100%; border-collapse: collapse; margin-top: 20px; }
        th, td { padding: 10px; border: 1px solid var(--baby-blue); text-align: center; }
        th { background: var(--main-blue); color: #000; }

        .btn-send {
            background: #4CAF50; color: white; border: none;
            padding: 15px 40px; border-radius: 50px; font-size: 1.2em;
            cursor: pointer; margin-top: 20px; width: 100%; transition: 0.3s;
        }

        .btn-send:hover { background: #388E3C; }

        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        .img-top { width: 100%; height: 200px; object-fit: cover; border-radius: 20px; margin-bottom: 20px; }
    </style>
</head>
<body>

<header>
    <h1>🕊️ صلاتي خلاصي 🕊️</h1>
    <p>أجبيتي الجميلة الملونة للأطفال</p>
</header>

<div class="container">
    
    <div class="tabs">
        <button class="tab-btn active" onclick="showPrayer('baker')">صلاة باكر</button>
        <button class="tab-btn" onclick="showPrayer('third')">الساعة الثالثة</button>
        <button class="tab-btn" onclick="showPrayer('sixth')">الساعة السادسة</button>
        <button class="tab-btn" onclick="showPrayer('ninth')">الساعة التاسعة</button>
        <button class="tab-btn" onclick="showPrayer('sunset')">صلاة الغروب</button>
        <button class="tab-btn" onclick="showPrayer('sleep')">صلاة النوم</button>
    </div>

    <div id="baker" class="prayer-card active">
        <img src="https://images.unsplash.com/photo-1470252649358-96962407e9d9?auto=format&fit=crop&q=80&w=500" class="img-top" alt="شروق">
        <h2>🌅 صلاة باكر</h2>
        <div class="prayer-text">
            <strong>باسم الآب والابن والروح القدس الإله الواحد آمين.</strong>
            يا رب ارحم، يا رب ارحم، يا رب بارك آمين.<br>
            <strong>صلاة الشكر:</strong> فلنشكر صانع الخيرات الرحوم الله أب ربنا وإلهنا ومخلصنا يسوع المسيح، لأنه سترنا وأعاننا وحفظنا.. <br>
            <strong>المزمور الخمسون:</strong> ارحمني يا الله كعظيم رحمتك، ومثل كثرة رأفتك امح إثمي.. <br>
            <strong>المزمور الأول:</strong> طوبى للرجل الذي لم يسلك في مشورة الأشرار.. يكون كشجرة مغروسة على مجاري المياه.
        </div>
    </div>

    <div id="third" class="prayer-card">
        <h2>🕒 صلاة الساعة الثالثة</h2>
        <div class="prayer-text">
            <strong>باسم الآب والابن والروح القدس..</strong>
            يا روحك القدوس يارب الذي أرسلته على تلاميذك القديسين ورسلك المكرمين في الساعة الثالثة، هذا لا تنزعه منا أيها الصالح لكن جدده في أحشائنا.<br>
            <strong>المزمور التاسع عشر:</strong> يستجيب لك الرب في يوم شدتك، ينصرك اسم إله يعقوب. يرسل لك عوناً من قدسه ومن صهيون يعضدك.
        </div>
    </div>

    <div id="sixth" class="prayer-card">
        <h2>🌞 صلاة الساعة السادسة</h2>
        <div class="prayer-text">
            <strong>باسم الآب والابن والروح القدس..</strong>
            يا من في اليوم السادس وفي الساعة السادسة سُمرت على الصليب من أجل الخطية التي تجرأ عليها أبونا آدم في الفردوس، مزق صك خطايانا أيها المسيح إلهنا وخلصنا.<br>
            <strong>المزمور الثالث والخمسون:</strong> اللهم باسمك خلصني وبقوتك احكم لي. استمع يا الله صلاتي وأنصت إلى كلام فمي.
        </div>
    </div>

    <div id="ninth" class="prayer-card">
        <h2>⛪ صلاة الساعة التاسعة</h2>
        <div class="prayer-text">
            <strong>باسم الآب والابن والروح القدس..</strong>
            يا من ذاق الموت بالجسد في الساعة التاسعة من أجلنا نحن الخطاة، أمت حواسنا الجسدية أيها المسيح إلهنا ونجنا.<br>
            <strong>المزمور الخامس والتسعون:</strong> سبحوا الرب تسبيحاً جديداً، سبحي الرب يا كل الأرض. سبحوا الرب وباركوا اسمه.
        </div>
    </div>

    <div id="sunset" class="prayer-card">
        <h2>🌇 صلاة الغروب</h2>
        <div class="prayer-text">
            <strong>باسم الآب والابن والروح القدس..</strong>
            نشكرك يا ملكنا الرحوم، لأنك منحتنا أن نعبر هذا اليوم بسلام، وأتيت بنا إلى المساء شاكرين، وجعلتنا مستحقين أن ننظر النور إلى المساء.<br>
            <strong>المزمور المئة السادس عشر:</strong> سبحوا الرب يا جميع الأمم، ولتباركه كافة الشعوب، لأن رحمته قد ثبتت علينا وحق الرب يدوم إلى الأبد.
        </div>
    </div>

    <div id="sleep" class="prayer-card">
        <img src="https://images.unsplash.com/photo-1532767153582-b1a0e5145009?auto=format&fit=crop&q=80&w=500" class="img-top" alt="نجوم">
        <h2>🌙 صلاة النوم</h2>
        <div class="prayer-text">
            <strong>باسم الآب والابن والروح القدس..</strong>
            تفضل يا رب أن تحفظنا في هذه الليلة بغير خطية. مبارك أنت أيها الرب إله آبائنا، ومتزايد بركة واسمك القدوس مملوء مجداً إلى الأبد آمين.<br>
            <strong>الإنجيل (لوقا ٢):</strong> يا سيد تطلق عبدك بسلام حسب قولك، لأن عيني قد أبصرتا خلاصك الذي أعددته قدام جميع الشعوب.
        </div>
    </div>

    <div class="notebook">
        <h2 style="text-align: center; color: var(--dark-blue);">📝 نوته "صلاتي خلاصي" الأسبوعية</h2>
        <center>
            <label>اكتب اسمك:</label><br>
            <input type="text" id="childName" placeholder="اكتب الاسم هنا">
        </center>
        <table>
            <thead>
                <tr>
                    <th>اليوم</th>
                    <th>باكر</th>
                    <th>3/6/9</th>
                    <th>غروب/نوم</th>
                    <th>إنجيل</th>
                </tr>
            </thead>
            <tbody id="weeklyTable"></tbody>
        </table>
        <button class="btn-send" onclick="sendToParents()">إرسال النوته لماما وبابا ✨</button>
    </div>
</div>

<script>
    function showPrayer(prayerId) {
        document.querySelectorAll('.prayer-card').forEach(card => card.classList.remove('active'));
        document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
        
        document.getElementById(prayerId).classList.add('active');
        event.currentTarget.classList.add('active');
    }

    const days = ["الأحد", "الاثنين", "الثلاثاء", "الأربعاء", "الخميس", "الجمعة", "السبت"];
    const tableBody = document.getElementById('weeklyTable');
    days.forEach(day => {
        tableBody.innerHTML += `<tr>
            <td><strong>${day}</strong></td>
            <td><input type="checkbox"></td>
            <td><input type="checkbox"></td>
            <td><input type="checkbox"></td>
            <td><input type="checkbox"></td>
        </tr>`;
    });

    function sendToParents() {
        const name = document.getElementById('childName').value;
        if(!name) {
            alert("من فضلك اكتب اسمك أولاً");
        } else {
            alert("أحسنت يا " + name + "! تم حفظ نوتتك الروحية بنجاح.");
        }
    }
</script>

</body>
</html>
