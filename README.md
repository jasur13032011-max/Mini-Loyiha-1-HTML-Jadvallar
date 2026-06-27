# Mini-Loyiha-1-HTML-Jadvallar
1. HTML Kod (index.html)
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sticky Navbar Proyekti</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <nav class="navbar">
        <div class="logo">MyBrand</div>
        <ul class="nav-links">
            <li><a href="#home">Bosh sahifa</a></li>
            <li><a href="#services">Xizmatlar</a></li>
            <li><a href="#portfolio">Portfolio</a></li>
            <li><a href="#contact">Aloqa</a></li>
        </ul>
    </nav>

    <div class="content">
        <section id="home">
            <h1>Xush kelibsiz!</h1>
            <p>Sahifani pastga scroll qilib (aylantirib), navbarning yopishib qolishini va orqa fon xiralashishini ko'ring.</p>
        </section>
        <section id="services">
            <h2>Xizmatlarimiz</h2>
            <p>Zamonaviy va mukammal veb-saytlar yaratish.</p>
        </section>
        <section id="portfolio">
            <h2>Ijodiy ishlar</h2>
            <p>Bizning oxirgi loyihalarimiz bilan tanishing.</p>
        </section>
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
    /* Orqa fonga chiroyli gradient beramiz (scroll effekti bilinishi uchun) */
    background: linear-gradient(135deg, #1e3c72, #2a5298, #667eea, #764ba2);
    background-size: cover;
    background-attachment: fixed;
    color: #fff;
}

/* ==========================================
   NAVBAR SOZLAMALARI
   ========================================== */
.navbar {
    /* 1. Sahifa pastga scroll bo'lganda tepada qolishi uchun */
    position: sticky;
    top: 0;
    z-index: 1000; /* Har doim boshqa elementlardan ustida turishi uchun */

    /* 2. Flexbox orqali Logo va Havolalarni ikki chetga surish */
    display: flex;
    justify-content: space-between;
    align-items: center;
    
    padding: 20px 10%;
    background: rgba(255, 255, 255, 0.1); /* Shaffof fon */
    border-bottom: 1px solid rgba(255, 255, 255, 0.2);

    /* 3. Backdrop-filter blur effekti (Oyna effekti) */
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px); /* Safari brauzeri uchun */
}

.logo {
    font-size: 1.5rem;
    font-weight: bold;
    letter-spacing: 1px;
}

/* 4. Flexbox orqali havolalarni yonma-yon joylashtirish */
.nav-links {
    display: flex;
    list-style: none;
    gap: 30px; /* Havolalar orasidagi masofa */
}

/* Havolalarning standart ko'rinishi */
.nav-links a {
    /* 5. Ostidagi chiziqni olib tashlash */
    text-decoration: none;
    
    color: rgba(255, 255, 255, 0.8);
    font-size: 1.1rem;
    font-weight: 500;
    transition: color 0.3s ease, transform 0.3s ease;
    display: inline-block;
}

/* 6. a:hover rangini o'zgartirish */
.nav-links a:hover {
    color: #00f2fe; /* Yorqin neon firuza rangi */
    transform: translateY(-2px); /* Biroz tepaga ko'tarilish effekti */
}

/* ==========================================
   KONTENT SOZLAMALARI (Scroll seziyishi uchun)
   ========================================== */
.content {
    padding: 40px 10%;
}

section {
    min-height: 60vh; /* Har bir bo'lim yetarlicha katta bo'lishi uchun */
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

section h1, section h2 {
    font-size: 2.5rem;
    margin-bottom: 15px;
}

section p {
    font-size: 1.2rem;
    color: #e0e0e0;
}

/* Responsive dizayn (Mobil qurilmalar uchun) */
@media (max-width: 768px) {
    .navbar {
        padding: 15px 5%;
    }
    
    .nav-links {
        gap: 15px;
    }
    
    .nav-links a {
        font-size: 0.95rem;
    }
}
Kod qanday ishlaydi?
position: sticky; top: 0; — Element brauzer oynasining eng tepasiga (top: 0) yetganda yopishib qoladi va scroll bo'lganda ham joyidan qimirlamaydi.

display: flex (Navbarda) — Logo chap tomonda, havolalar bloki esa o'ng tomonda chiroyli joylashishini ta'minlaydi (justify-content: space-between).

display: flex (Ro'yxatda) — <ul> ichidagi <li> elementlarini vertikal emas, yonma-yon (gorizontal) qilib tizib beradi.

backdrop-filter: blur(10px) — Navbar ostidan o'tayotgan matn va ranglarni xiralashtirib, juda zamonaviy "muzlagan oyna" effektini beradi.

text-decoration: none; — Havolalarning (<a> tegi) tagidagi standart chiziqni olib tashlaydi.

a:hover — Sichqoncha havola ustiga kelganda rang silliq ravishda firuza (#00f2fe) rangiga o'zgaradi.
