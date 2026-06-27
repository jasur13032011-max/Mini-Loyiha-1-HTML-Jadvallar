# Mini-Loyiha-1-HTML-Jadvallar
stillari keltirilgan.

Kodni brauzerda ochib tekshirishingiz mumkin:

HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Jadvallar va CSS Stillari</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f7f6;
            padding: 20px;
            color: #333;
        }

        /* Umumiy jadval stillari */
        table {
            width: 100%;
            max-width: 800px;
            margin: 20px auto 40px auto;
            border-collapse: collapse; /* Chegara chiziqlarini birlashtirish */
            background-color: #ffffff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
            border-radius: 8px;
            overflow: hidden;
        }

        /* Caption (Jadval nomi) stili */
        caption {
            font-size: 1.4rem;
            font-weight: bold;
            margin-bottom: 10px;
            color: #2c3e50;
            caption-side: top;
        }

        /* th (Sarlavha) uchun alohida stil */
        th {
            background-color: #34495e;
            color: #ffffff;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.9rem;
            padding: 12px 15px;
            text-align: left;
            border-bottom: 3px solid #2c3e50;
        }

        /* td (Katakcha) uchun alohida stil */
        td {
            padding: 12px 15px;
            border-bottom: 1px solid #e0e0e0;
            color: #555;
            font-size: 0.95rem;
        }

        /* Alternativ ranglar (Zebra effekti) */
        tr:nth-child(even) {
            background-color: #f8f9fa;
        }

        /* Hover effekti (Sichqoncha ustiga kelganda) */
        tr:hover {
            background-color: #e8f4fd;
            cursor: pointer;
            transition: background-color 0.2s ease;
        }

        /* Murakkab jadvaldagi birlashtirilgan umumiy natija qatori uchun maxsus uslub */
        .total-row {
            font-weight: bold;
            background-color: #eaeded !important;
        }
    </style>
</head>
<body>

    <table>
        <caption>1-jadval: Foydalanuvchilar ro'yxati (Oddiy jadval)</caption>
        <thead>
            <tr>
                <th>ID</th>
                <th>Ism</th>
                <th>Familiya</th>
                <th>Kasbi</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td>Anvar</td>
                <td>Aliyev</td>
                <td>Dasturchi</td>
            </tr>
            <tr>
                <td>2</td>
                <td>Dilnoza</td>
                <td>Karimova</td>
                <td>Dizayner</td>
            </tr>
            <tr>
                <td>3</td>
                <td>Jasur</td>
                <td>Tojirov</td>
                <td>Menejer</td>
            </tr>
            <tr>
                <td>4</td>
                <td>Shahnoza</td>
                <td>Umarova</td>
                <td>SMM mutaxassis</td>
            </tr>
        </tbody>
    </table>


    <table>
        <caption>2-jadval: Oylik savdo hisoboti (Murakkab jadval)</caption>
        <thead>
            <tr>
                <th rowspan="2">Kategoriya</th>
                <th rowspan="2">Mahsulot</th>
                <th colspan="2">Savdo hajmi (Haftalar kesimida)</th>
            </tr>
            <tr>
                <th>1-Hafta</th>
                <th>2-Hafta</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td rowspan="2">Elektronika</td>
                <td>Smartfon</td>
                <td>$5,000</td>
                <td>$6,200</td>
            </tr>
            <tr>
                <td>Noutbuk</td>
                <td>$8,500</td>
                <td>$7,900</td>
            </tr>
            <tr>
                <td rowspan="2">Kiyim-kechak</td>
                <td>Kurtka</td>
                <td>$1,200</td>
                <td>$1,500</td>
            </tr>
            <tr>
                <td>Oyoq kiyim</td>
                <td>$2,100</td>
                <td>$2,400</td>
            </tr>
            <tr class="total-row">
                <td colspan="2">Umumiy hisob</td>
                <td>$16,800</td>
                <td>$18,000</td>
            </tr>
        </tbody>
    </table>

</body>
</html>
Kod qanday topshiriqlarni bajardi?
2 ta jadval: Birinchisi oddiy tuzilishga ega, ikkinchisida esa rowspan va colspan yordamida murakkab tuzilma hosil qilingan.

border-collapse: collapse;: Har ikki jadval chekkalari bir-biriga yopishgan va chiroyli ko'rinishda.

Alohida stillar: th uchun to'q rangli fon va oq matn, td uchun esa ochroq rang va ingichka chiziqlar berildi.

tr:nth-child(even): Jadvallarning har ikkinchi qatori avtomatik ravishda och kulrang (#f8f9fa) tusga kiradi.

tr:hover: Sichqoncha ko'rsatkichi qator ustiga kelganda qator rangi mayin ko'k (#e8f4fd) rangga o'zgaradi.

caption: Har bir jadvalning tepasida uning nomi joylashtirildi.
