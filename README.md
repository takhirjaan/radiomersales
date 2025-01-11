# radiomersales
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RadioMer Vending Machine Sales</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #eef2f5;
            line-height: 1.6;
        }
        header {
            background: #1a1a2e;
            color: #ffffff;
            padding: 1rem 0;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        nav {
            display: flex;
            justify-content: center;
            background: #162447;
            padding: 0.5rem 0;
        }
        nav a {
            color: #ffffff;
            text-decoration: none;
            padding: 0.5rem 1rem;
            transition: background 0.3s;
        }
        nav a:hover {
            background: #1f4068;
        }
        .language-selector {
            margin-left: auto;
            display: flex;
            align-items: center;
        }
        .language-selector select {
            padding: 0.5rem;
            margin: 0 1rem;
            border: none;
            background: #1f4068;
            color: #ffffff;
            border-radius: 4px;
        }
        main {
            padding: 2rem;
            text-align: center;
            color: #162447;
        }
        footer {
            background: #1a1a2e;
            color: #ffffff;
            text-align: center;
            padding: 1rem 0;
        }
        .location, .contact-info p {
            font-size: 1.1rem;
            margin: 1rem 0;
            color: #1f4068;
        }
        .contact-info {
            margin-top: 20px;
            font-size: 1.2rem;
            display: flex;
            justify-content: center;
            flex-direction: column;
            align-items: center;
        }
        .contact-info a {
            color: #1f4068;
            text-decoration: none;
            margin: 5px 0;
        }
        .contact-info i {
            margin-right: 8px;
        }
        .social-media {
            margin-top: 20px;
        }
        .social-media a {
            margin: 0 10px;
            color: #1f4068;
            font-size: 1.5rem;
        }
        .order-button {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #1f4068;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1 id="header-title">RadioMer Vending Machine Sales</h1>
    </header>
    <nav>
        <a href="#home">Home</a>
        <a href="#about" id="about-menu">About</a>
        <a href="#contact" id="contact-menu">Contact</a>
        <div class="language-selector">
            <select id="language" onchange="changeLanguage()">
                <option value="en">English</option>
                <option value="ru">Русский</option>
                <option value="uz">O'zbekcha</option>
            </select>
            <i class="fas fa-globe"></i>
        </div>
    </nav>
    <main>
        <h2 id="about-header">About Us</h2>
        <p id="greeting">Hello, my name is Zokirov Toxirjon.</p>
        <p>My Telegram Username: <strong>t.me/zokirovtoxir</strong></p>

        <div class="order-info">
            <button class="order-button" onclick="showUsername()">Order Here</button>
            <p id="username" style="display:none;">t.me/zokirovtoxir</p>
        </div>

        <p class="location" id="location">Our Location: Andijon Viloyati, Oltinko'l Tumani, Sportchilar 43</p>
        
        <!-- Contact Information -->
        <div class="contact-info">
            <p>If you want to order, contact me:</p>
            <a href="tel:+998332052602"><i class="fas fa-phone"></i> +998 33 205 2602</a>
            <a href="mailto:radiomerdirectsales@gmail.com"><i class="fas fa-envelope"></i> radiomerdirectsales@gmail.com</a>
        </div>

        <!-- Social Media Links -->
        <div class="social-media">
            <p>Follow us on:</p>
            <a href="https://www.instagram.com/radiomer.official" target="_blank"><i class="fab fa-instagram"></i></a>
            <a href="https://www.facebook.com/radiomer.official" target="_blank"><i class="fab fa-facebook"></i></a>
            <a href="https://www.youtube.com/RadioMerOffcial" target="_blank"><i class="fab fa-youtube"></i></a>
        </div>
    </main>
    <footer>
        <p>&copy; 2025 RadioMer. All rights reserved.</p>
    </footer>

    <script>
        function changeLanguage() {
            const lang = document.getElementById('language').value;

            const texts = {
                en: {
                    header: "RadioMer Vending Machine Sales",
                    about: "About Us",
                    greeting: "Hello, my name is Zokirov Toxirjon.",
                    location: "Our Location: Andijon Viloyati, Oltinko'l Tumani, Sportchilar 43",
                    contact: "If you want to order, contact me:"
                },
                ru: {
                    header: "РадиоМер Продажа Торговых Автоматов",
                    about: "О нас",
                    greeting: "Здравствуйте, меня зовут Зокиров Тохиржон.",
                    location: "Наше местоположение: Андижанская область, Олтункульский район, Спортчилар 43",
                    contact: "Если хотите заказать, свяжитесь со мной:"
                },
                uz: {
                    header: "RadioMer Savdo Avtomati Sotishi",
                    about: "Biz Haqimizda",
                    greeting: "Salom, mening ismim Zokirov Toxirjon.",
                    location: "Bizning Manzilimiz: Andijon Viloyati, Oltinko'l Tumani, Sportchilar 43",
                    contact: "Agar buyurtma bermoqchi bo'lsangiz, menga bog'laning:"
                }
            };

            document.getElementById('header-title').textContent = texts[lang].header;
            document.getElementById('about-header').textContent = texts[lang].about;
            document.getElementById('greeting').textContent = texts[lang].greeting;
            document.getElementById('location').textContent = texts[lang].location;
            document.querySelector('.contact-info p').textContent = texts[lang].contact;
        }

        function showUsername() {
            const username = document.getElementById('username');
            username.style.display = username.style.display === 'none' ? 'block' : 'none';
        }
    </script>
</body>
</html>
