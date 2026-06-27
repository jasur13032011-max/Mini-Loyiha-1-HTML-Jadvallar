# Mini-Loyiha-1-HTML-Jadvallar
1. HTML Kod (index.html)
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Grid Kartochkalar</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="grid-container">
        
        <div class="card">
            <div class="profile-wrapper">
                <img src="https://picsum.photos/150?random=1" alt="Profil" class="profile-img">
            </div>
            <h3>Anvar Alimov</h3>
            <p class="role">Frontend Dasturchi</p>
            <p class="desc">HTML, CSS va JavaScript yordamida zamonaviy va mukammal veb-saytlar yaratadi.</p>
            <button class="btn">Bog'lanish</button>
        </div>

        <div class="card">
            <div class="profile-wrapper">
                <img src="https://picsum.photos/150?random=2" alt="Profil" class="profile-img">
            </div>
            <h3>Zarina Karimova</h3>
            <p class="role">UI/UX Dizayner</p>
            <p class="desc">Figma va Adobe XD orqali foydalanuvchilarga qulay va chiroyli interfeyslar chizadi.</p>
            <button class="btn">Ko'rish</button>
        </div>

        <div class="card">
            <div class="profile-wrapper">
                <img src="https://picsum.photos/150?random=3" alt="Profil" class="profile-img">
            </div>
            <h3>Jasur Axmedov</h3>
            <p class="role">Project Manager</p>
            <p class="desc">Loyihalarni o'z vaqtida, sifatli va jamoa bilan hamjihatlikda bajarilishini ta'minlaydi.</p>
            <button class="btn">Bog'lanish</button>
        </div>

    </div>

</body>
</html>
2. CSS Kod (style.css)
CSS
/* Umumiy sozlamalar */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #f4f7f6;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 40px 20px;
}

/* 1. CSS Grid orqali kartochkalarni joylashtirish */
.grid-container {
    display: grid;
    /* Ekran o'lchamiga qarab avtomatik ustunlar sonini moslashtiradi (Responsive) */
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 30px;
    width: 100%;
    max-width: 1000px;
}

/* Kartochka stillari */
.card {
    background-color: #ffffff;
    padding: 30px 20px;
    text-align: center;
    
    /* 2. Border-radius va Box-shadow */
    border-radius: 16px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.05);
    
    /* 6. Silliq animatsiya uchun transition */
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

/* 3. Hover: transform: translateY(-8px) */
.card:hover {
    transform: translateY(-8px); /* Kartochka 8px tepaga ko'tariladi */
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15); /* Soya ham quyuqlashadi */
}

/* 4. Profil rasmini doira shakliga keltirish */
.profile-wrapper {
    margin-bottom: 20px;
}

.profile-img {
    width: 100px;
    height: 100px;
    border-radius: 50%; /* Mukammal doira shakli */
    object-fit: cover; /* Rasm cho'zilib ketmasligi uchun */
    border: 3px solid #667eea; /* Rasm atrofiga chiroyli hoshiya */
    padding: 3px;
}

/* Matnlar stillari */
.card h3 {
    color: #333;
    font-size: 1.3rem;
    margin-bottom: 5px;
}

.role {
    color: #667eea;
    font-weight: 600;
    font-size: 0.9rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 15px;
}

.desc {
    color: #666;
    font-size: 0.95rem;
    line-height: 1.5;
    margin-bottom: 25px;
}

/* 5. Tugma stillari */
.btn {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    border: none;
    padding: 10px 24px;
    font-size: 0.95rem;
    font-weight: 500;
    border-radius: 25px; /* Dumaloq burchakli tugma */
    cursor: pointer;
    box-shadow: 0 4px 10px rgba(102, 126, 234, 0.3);
    transition: all 0.2s ease;
}

/* Tugma hover effekti */
.btn:hover {
    box-shadow: 0 6px 15px rgba(102, 126, 234, 0.5);
    opacity: 0.9;
}
Kodning asosiy xususiyatlari:
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)) — Bu qator yordamida media-so'rovlarsiz (@media) mutlaqo responsive dizayn yaratildi. Katta ekranda 3 ta kartochka yonma-yon turadi, telefonlarda esa avtomatik bittadan bo'lib joylashadi.

border-radius: 50% — Kvadrat shaklidagi rasmni silliq aylana shakliga keltirib beradi.

translateY(-8px) — Kartochka ustiga sichqoncha kelganda uning Y o'qi (tepa-past) bo'ylab yuqoriga ohista siljishini ta'minlaydi.

transition: ... 0.3s ease — Hover bo'lgandagi sakrashni yumshatib,
