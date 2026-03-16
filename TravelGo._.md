<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TravelGo — Твій гід у світі пригод</title>
    
    <style>
        /* Базові налаштування */
        :root {
            --primary-color: #ff6b6b;
            --dark-color: #2d3436;
            --light-bg: #f9f9f9;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            color: #333;
            scroll-behavior: smooth; /* Плавна прокрутка до секцій */
        }

        /* Шапка сайту */
        header {
            background: #fff;
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        header h1 {
            margin: 0;
            color: var(--primary-color);
            font-size: 1.8rem;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 20px;
            margin: 0;
            padding: 0;
        }

        nav a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 500;
            transition: 0.3s;
        }

        nav a:hover {
            color: var(--primary-color);
        }

        /* Головний банер (Hero) */
        #hero {
            height: 70vh;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                        url('https://pexels.com');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: #fff;
            text-align: center;
            padding: 0 20px;
        }

        #hero h2 { font-size: 3.5rem; margin-bottom: 1rem; }
        #hero p { font-size: 1.3rem; margin-bottom: 2rem; }

        .btn-main {
            background: var(--primary-color);
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 30px;
            font-size: 1.1rem;
            cursor: pointer;
            text-decoration: none;
            transition: 0.3s;
        }

        .btn-main:hover { background: #ee5253; transform: scale(1.05); }

        /* Основний контент */
        main {
            max-width: 1200px;
            margin: auto;
            padding: 40px 20px;
        }

        h2 { text-align: center; margin-bottom: 40px; font-size: 2.2rem; }

        /* Картки напрямків */
        .card-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background: #fff;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: 0.3s;
        }

        .card:hover { transform: translateY(-10px); }

        .card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }

        .card-content { padding: 25px; }
        .card h3 { margin: 0 0 10px 0; color: var(--dark-color); }
        .card p { color: #666; margin-bottom: 20px; }

        .btn-card {
            display: inline-block;
            width: 100%;
            text-align: center;
            padding: 10px;
            background: #f1f2f6;
            color: var(--dark-color);
            text-decoration: none;
            border-radius: 8px;
            font-weight: bold;
            transition: 0.3s;
        }

        .btn-card:hover { background: var(--primary-color); color: white; }

        /* Поради та FAQ */
        .info-section {
            background: var(--light-bg);
            padding: 40px;
            border-radius: 15px;
            margin: 40px 0;
        }

        details {
            background: #fff;
            padding: 15px;
            margin-bottom: 10px;
            border-radius: 8px;
            cursor: pointer;
            border: 1px solid #eee;
        }

        summary { font-weight: bold; }

        aside {
            border-left: 4px solid var(--primary-color);
            padding: 20px;
            background: #fff5f5;
            margin: 30px 0;
            font-style: italic;
        }

        /* Футер */
        footer {
            background: var(--dark-color);
            color: #dfe6e9;
            padding: 50px 20px;
            text-align: center;
        }

        footer nav { margin-top: 20px; }
        footer nav a { color: #fab1a0; margin: 0 15px; text-decoration: none; }
    </style>
</head>
<body>

    <header>
        <h1>TravelGo</h1>
        <nav>
            <ul>
                <li><a href="#hero">Головна</a></li>
                <li><a href="#destinations">Напрямки</a></li>
                <li><a href="#tips">Поради</a></li>
                <li><a href="#faq">FAQ</a></li>
            </ul>
        </nav>
    </header>

    <section id="hero">
        <h2>Відкрий світ з нами</h2>
        <p>Ваша ідеальна подорож починається тут</p>
        <a href="#destinations" class="btn-main">Обрати тур</a>
    </section>

    <main>
        
        <section id="destinations">
            <h2>Популярні напрямки</h2>
            <div class="card-container">
                
                <article class="card">
                    <img src="https://pexels.com" alt="Париж">
                    <div class="card-content">
                        <h3>Париж, Франція</h3>
                        <p>Відкрийте для себе чарівність Парижа: від Ейфелевої вежі до затишних кафе на березі Сени.</p>
                        <a href="#" class="btn-card">Дізнатися більше</a>
                    </div>
                </article>

                <article class="card">
                    <img src="https://pexels.com" alt="Кіото">
                    <div class="card-content">
                        <h3>Кіото, Японія</h3>
                        <p>Пориньте в атмосферу самураїв та квітучої сакури у культурному серці Японії.</p>
                        <a href="#" class="btn-card">Забронювати тур</a>
                    </div>
                </article>

                <article class="card">
                    <img src="https://pexels.com" alt="Мачу-Пікчу">
                    <div class="card-content">
                        <h3>Мачу-Пікчу, Перу</h3>
                        <p>Досліджуйте таємниці давніх інків на вершинах величних Андських гір.</p>
                        <a href="#" class="btn-card">Переглянути маршрут</a>
                    </div>
                </article>

            </div>
        </section>

        <section id="tips" class="info-section">
            <h2>Поради для мандрівників</h2>
            <article>
                <h3>Як зібрати ідеальну валізу?</h3>
                <p>Використовуйте техніку "ролів" для одягу — це зекономить місце. Не забудьте павербанк та міні-аптечку. Подорожуйте легко!</p>
            </article>

            <aside>
                <strong>💡 Цікаво знати:</strong> Японія налічує понад 6800 островів, хоча більшість туристів відвідують лише 4 найбільші.
            </aside>
        </section>

        <section id="faq">
            <h2>Часті запитання</h2>
            <details>
                <summary>Чи потрібна віза для поїздки?</summary>
                <p>Це залежить від вашого громадянства та обраної країни. Ми надаємо безкоштовні консультації щодо документів після бронювання.</p>
            </details>
            <details>
                <summary>Які методи оплати ви приймаєте?</summary>
                <p>Ми приймаємо всі основні кредитні картки, Apple Pay, Google Pay та банківські перекази.</p>
            </details>
        </section>

    </main>

    <footer>
        <p>© 2026 TravelGo — Проєкт виконано згідно з інструкцією Етапу 1</p>
        <nav>
            <a href="#">Instagram</a>
            <a href="#">Facebook</a>
            <a href="#">YouTube</a>
        </nav>
    </footer>

</body>
</html>
