 <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>صلاتي خلاصي - الأجبية الكاملة</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&family=Amiri:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root { --main-blue: #0288D1; --light-blue: #E1F5FE; --gold: #FFD700; }
        body { font-family: 'Cairo', sans-serif; background: var(--light-blue); margin: 0; padding: 0; }
        
        nav { background: var(--main-blue); padding: 10px; text-align: center; position: sticky; top: 0; z-index: 1000; display: flex; justify-content: center; gap: 8px; flex-wrap: wrap; }
        .nav-btn { background: white; border: none; padding: 10px 15px; border-radius: 20px; font-weight: bold; cursor: pointer; font-size: 0.9em; }
        .nav-btn.active { background: var(--gold); color: black; }

        .container { max-width: 800px; margin: auto; padding: 15px; }
        .page { display: none; background: white; border-radius: 25px; padding: 25px; border: 5px solid var(--main-blue); box-shadow: 0 5px 15px rgba(0,0,0,0.1); margin-top: 20px; }
        .page.active { display: block; }

        h1 { color: var(--main-blue); text-align: center; border-bottom: 2px solid #eee; padding-bottom: 10px; }
        
        /* إطار عرض الصلوات */
        .prayer-frame { width: 100%; height: 70vh; border: none; border-radius: 15px; }

        .note-content { text-align: center; }
        table { width: 100%; border-collapse: collapse; margin: 20px 0; }
        th, td { padding: 10px; border: 1px solid #ddd; text-align: center; }
        th { background: #f5f5f5; }
        .send-btn { background: #4CAF50; color: white; border: none; padding: 15px 40px; border-radius: 30px; font-size: 1.2em; cursor: pointer; }
    </style>
</head>
<body>

<nav>
    <button class="nav-btn active" onclick="loadPrayer('https://st-takla.org/Agpeya/Coptic-Service-Prayers-Agpia-01-Morning-Prime.html', this)">🌅 باكر</button>
    <button class="nav-btn" onclick="loadPrayer('https://st-takla.org/Agpeya/Coptic-Service-Prayers-Agpia-03-Third-Hour.html', this)">🕒 الثالثة</button>
    <button class="nav-btn" onclick="loadPrayer('https://st-takla.org/Agpeya/Coptic-Service-Prayers-Agpia-06-Sixth-Hour.html', this)">🕕 السادسة</button>
    <button class="nav-btn" onclick="loadPrayer('https://st-takla.org/Agpeya/Coptic-Service-Prayers-Agpia-09-Ninth-Hour.html', this)">🕘 التاسعة</button>
    <button class="nav-btn" onclick="showNote(this)" style="background: var(--gold); color: black;">📝 النوته</button>
</nav>

<div class="container">
    <div id="prayerPage" class="page active">
        <h1 id="pTitle">صلاة باكر كاملة</h1>
        <iframe id="prayerFrame" src="https://st-takla.org/Agpeya/Coptic-Service-Prayers-Agpia-01-Morning-Prime.html" class="prayer-frame"></iframe>
    </div>

    <div id="notePage" class="page">
        <div class="note-content">
            <h1>📝 نوتتي الروحية</h1>
            <input type="text" id="cName" placeholder="اكتب اسمك هنا" style="width: 80%; padding: 12px; border-radius: 15px; border: 1px solid #ccc; text-align: center; margin-bottom: 15px;">
            <table>
                <thead><tr><th>اليوم</th><th>صليت</th><th>إنجيل</th></tr></thead>
                <tbody id="weekBody"></tbody>
            </table>
            <button class="send-btn" onclick="alert('تم الإرسال يا بطل!')">إرسال النوته ✨</button>
        </div>
    </div>
</div>

<script>
    function loadPrayer(url, btn) {
        document.getElementById('notePage').classList.remove('active');
        document.getElementById('prayerPage').classList.add('active');
        document.getElementById('prayerFrame').src = url;
        document.getElementById('pTitle').innerText = btn.innerText + " كاملة";
        updateActiveBtn(btn);
    }

    function showNote(btn) {
        document.getElementById('prayerPage').classList.remove('active');
        document.getElementById('notePage').classList.add('active');
        updateActiveBtn(btn);
    }

    function updateActiveBtn(btn) {
        document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
    }

    const days = ["الأحد", "الاثنين", "الثلاثاء", "الأربعاء", "الخميس", "الجمعة", "السبت"];
    const tbody = document.getElementById('weekBody');
    days.forEach(day => {
        tbody.innerHTML += `<tr><td>${day}</td><td><input type="checkbox"></td><td><input type="checkbox"></td></tr>`;
    });
</script>

</body>
</html>
