# Mini-Loyiha-1-HTML-Jadvallar
Mana, barcha so'ralgan talablar (list-style, fon rasmi, backdrop-filter, Flexbox, Hover effekti va Responsive dizayn) mukammal jamlangan kod namunasi.

Bu loyihada chiroyli, orqa foni xiralashgan (glassmorphism effekti) va harakatlanuvchi ro'yxat elementlari yaratilgan.

1. HTML Kod (index.html)
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zamonaviy Flexbox Loyihasi</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <h2>Kardlar Ro'yxati</h2>
        <ul class="card-list">
            <li class="card-item">CSS Grid & Flexbox darslari</li>
            <li class="card-item">Responsive veb-dizayn asoslari</li>
            <li class="card-item">Backdrop-filter va vizual effektlar</li>
            <li class="card-item">Zamonaviy CSS Hover effektlari</li>
        </ul>
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

/* 1. Fon rasmi va uning fiksatsiyasi */
body {
    min-height: 100vh;
    background-image: url('https://picsum.photos/1920/1080'); /* Sifatli ixtiyoriy rasm */
    background-size: cover;
    background-position: center;
    background-attachment: fixed; /* Sahifa aylantirilganda fon joyida qoladi */
    
    /* 2. Flexbox yordamida konteynerni markazga joylashtirish */
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

/* Konteyner va Glassmorphic (Oyna) effekti */
.container {
    background: rgba(255, 255, 255, 0.15);
    padding: 40px;
    border-radius: 16px;
    border: 1px solid rgba(255, 255, 255, 0.25);
    width: 100%;
    max-width: 600px;
    box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
    
    /* 3. Backdrop-filter effekti */
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px); /* Safari uchun */
    
    text-align: center;
}

h2 {
    color: #fff;
    margin-bottom: 25px;
    font-size: 2rem;
    text-shadow: 0 2px 4px rgba(0,0,0,0.2);
}

/* 4. Flexbox orqali ro'yxat elementlarini tekislash */
.card-list {
    display: flex;
    flex-direction: column;
    gap: 15px; /* Elementlar orasidagi masofa */
    
    /* 5. List-style bilan markerlarni o'zgartirish */
    list-style: "🔥 "; /* Standart nuqtani ixtiyoriy emoji yoki belgiga almashtirish */
    padding-left: 20px;
}

/* Ro'yxat elementlarining ko'rinishi */
.card-item {
    background: rgba(255, 255, 255, 0.2);
    color: #fff;
    padding: 15px 20px;
    border-radius: 8px;
    font-size: 1.1rem;
    text-align: left;
    font-weight: 500;
    transition: all 0.3s ease; /* Silliq effekt uchun */
    cursor: pointer;
}

/* 6. Hover effekti */
.card-item:hover {
    background: #fff;
    color: #333;
    transform: translateX(10px) scale(1.02); /* O'ngga surilish va biroz kattalashish */
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

/* 7. Responsive ko'rinish (Media so'rovlar) */
@media (max-width: 480px) {
    .container {
        padding: 20px;
    }
    
    h2 {
        font-size: 1.5rem;
    }

    .card-item {
        font-size: 0.95rem;
        padding: 12px 15px;
    }
    
    .card-item:hover {
        transform: translateY(-5px); /* Mobil qurilmada chetga emas, tepaga ko'tariladi */
    }
}
Kodda bajarilgan vazifalar qisqacha:
list-style: "🔥 " — Ro'yxat boshidagi zerikarli qora nuqtalarni olov emojisi bilan almashtirdi.

background-attachment: fixed — Fon rasmini qotirib qo'ydi, kontent uning ustida suzib yurgandek ko'rinadi.

backdrop-filter: blur(12px) — Konteyner orqasidagi fonni xiralashtirib, oyna (glassmorphism) effektini berdi.

display: flex — Ham butun sahifani o'rtaga keltirishda, ham ro'yxat elementlarini chiroyli ketma-ket joylashtirishda ishlatildi.

:hover — Element ustiga sichqoncha kelganda rang o'zgarishi, o'ngga surilishi va soya paydo bo'lishini ta'minladi.

@media (max-width: 480px) — Ekran kichrayganda (mobil telefonlarda) shriftlar va paddinglar avtomatik kichrayib, moslashuvchan (responsive) bo'lishini ta'minladi.
