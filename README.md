<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Иван Петров — веб-разработчик</title>
    <meta name="description" content="Персональная страница-визитка">

    <!-- Шрифты (не обязательны, но улучшают типографику) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">

    <style>
        /* ===== БАЗОВЫЕ НАСТРОЙКИ ===== */
        :root {
            --bg: #fafafa;           /* цвет фона */
            --text: #1a1a1a;         /* основной цвет текста */
            --muted: #6b6b6b;        /* приглушённый текст */
            --accent: #1a1a1a;       /* цвет акцентов (ссылки, линии) */
            --border: #e5e5e5;       /* цвет тонких линий */
            --max-width: 640px;      /* максимальная ширина контента */
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        html { scroll-behavior: smooth; }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            font-weight: 400;
        }

        /* ===== КОНТЕЙНЕР ===== */
        .container {
            max-width: var(--max-width);
            margin: 0 auto;
            padding: 0 24px;
        }

        /* ===== ШАПКА / ВЕРХНИЙ БЛОК ===== */
        .hero {
            padding: 120px 0 80px;
        }

        .hero .label {
            font-size: 14px;
            color: var(--muted);
            letter-spacing: 0.05em;
            text-transform: uppercase;
            margin-bottom: 24px;
        }

        .hero h1 {
            font-size: clamp(36px, 6vw, 56px);
            font-weight: 600;
            line-height: 1.1;
            letter-spacing: -0.02em;
            margin-bottom: 20px;
        }

        .hero .subtitle {
            font-size: clamp(18px, 2.5vw, 22px);
            color: var(--muted);
            font-weight: 300;
            max-width: 480px;
        }

        /* ===== СЕКЦИИ ===== */
        section {
            padding: 48px 0;
            border-top: 1px solid var(--border);
        }

        .section-title {
            font-size: 13px;
            font-weight: 500;
            color: var(--muted);
            letter-spacing: 0.08em;
            text-transform: uppercase;
            margin-bottom: 28px;
        }

        .about-text {
            font-size: 17px;
            line-height: 1.7;
            color: var(--text);
            max-width: 560px;
        }

        .about-text p + p { margin-top: 16px; }

        /* ===== ССЫЛКИ / КОНТАКТЫ ===== */
        .links {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 4px;
        }

        .links li { border-bottom: 1px solid var(--border); }
        .links li:last-child { border-bottom: none; }

        .links a {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 18px 0;
            color: var(--text);
            text-decoration: none;
            font-size: 16px;
            transition: opacity 0.2s ease, padding-left 0.2s ease;
        }

        .links a:hover {
            opacity: 0.6;
            padding-left: 8px;
        }

        .links .arrow {
            color: var(--muted);
            font-size: 18px;
            transition: transform 0.2s ease;
        }

        .links a:hover .arrow { transform: translateX(4px); }

        /* ===== ПОДВАЛ ===== */
        footer {
            padding: 48px 0 64px;
            font-size: 14px;
            color: var(--muted);
        }

        /* ===== АДАПТИВНОСТЬ ===== */
        @media (max-width: 600px) {
            .hero { padding: 80px 0 56px; }
            section { padding: 36px 0; }
            .links a { padding: 16px 0; font-size: 15px; }
        }

        /* ===== УВАЖЕНИЕ К ПОЛЬЗОВАТЕЛЮ (prefers-reduced-motion) ===== */
        @media (prefers-reduced-motion: reduce) {
            html { scroll-behavior: auto; }
            * { transition: none !important; }
        }
    </style>
</head>
<body>

    <!-- ===== ГЛАВНЫЙ БЛОК ===== -->
    <!-- Замените имя, должность и короткое описание на свои -->
    <header class="hero container">
        <div class="label">Личная страница</div>
        <h1>Иван Петров</h1>
        <p class="subtitle">Веб-разработчик и дизайнер. Создаю быстрые, чистые и удобные сайты.</p>
    </header>

    <!-- ===== О СЕБЕ ===== -->
    <!-- Расскажите о себе в 2–3 абзацах -->
    <section class="container" id="about">
        <h2 class="section-title">О себе</h2>
        <div class="about-text">
            <p>Привет! Меня зовут Иван. Уже более пяти лет я помогаю компаниям и частным специалистам переносить их идеи в цифровую среду — от простых визиток до полноценных веб-сервисов.</p>
            <p>Ценю минимализм, скорость и внимание к деталям. Каждый проект начинаю с вопроса «зачем это нужно пользователю?» — и строю всё вокруг ответа.</p>
        </div>
    </section>

    <!-- ===== КОНТАКТЫ ===== -->
    <!-- Замените ссылки и подписи на свои -->
    <section class="container" id="contact">
        <h2 class="section-title">Связаться</h2>
        <ul class="links">
            <li>
                <a href="mailto:hello@example.com">
                    <span>Email — hello@example.com</span>
                    <span class="arrow">→</span>
                </a>
            </li>
            <li>
                <a href="https://t.me/username" target="_blank" rel="noopener">
                    <span>Telegram — @username</span>
                    <span class="arrow">→</span>
                </a>
            </li>
            <li>
                <a href="https://github.com/username" target="_blank" rel="noopener">
                    <span>GitHub — /username</span>
                    <span class="arrow">→</span>
                </a>
            </li>
            <li>
                <a href="https://linkedin.com/in/username" target="_blank" rel="noopener">
                    <span>LinkedIn — /in/username</span>
                    <span class="arrow">→</span>
                </a>
            </li>
        </ul>
    </section>

    <!-- ===== ПОДВАЛ ===== -->
    <footer class="container">
        <p>© 2026 Иван Петров. Сделано вручную.</p>
    </footer>

</body>
</html>
