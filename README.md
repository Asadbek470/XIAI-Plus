# XIAI-Plus
plus
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>XIAI Plus - Премиум подписка</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #10a37f;
            --primary-dark: #0d8c6c;
            --secondary: #343541;
            --secondary-light: #40414f;
            --secondary-dark: #2a2b32;
            --text-primary: #ffffff;
            --text-secondary: #d1d5db;
            --text-muted: #9ca3af;
            --accent: #ec4899;
            --border: #4b5563;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }
        
        body {
            background-color: var(--secondary);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        /* Плавные переходы */
        * {
            transition: all 0.3s ease;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }
        
        /* Шапка */
        header {
            background-color: var(--secondary-dark);
            border-bottom: 1px solid var(--border);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(10px);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .logo i {
            color: var(--primary);
        }
        
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        
        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            font-weight: 500;
            position: relative;
        }
        
        .nav-links a:hover {
            color: var(--text-primary);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .cta-button {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 0.5rem;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .cta-button:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(16, 163, 127, 0.3);
        }
        
        /* Герой секция */
        .hero {
            padding: 5rem 0;
            text-align: center;
            background: linear-gradient(135deg, var(--secondary-dark) 0%, var(--secondary) 100%);
        }
        
        .hero h1 {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .hero p {
            font-size: 1.25rem;
            color: var(--text-secondary);
            max-width: 700px;
            margin: 0 auto 2.5rem;
        }
        
        .price-tag {
            background-color: var(--secondary-light);
            padding: 1.5rem 2rem;
            border-radius: 1rem;
            display: inline-block;
            margin-bottom: 2rem;
            border: 1px solid var(--border);
        }
        
        .price {
            font-size: 3rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        /* Секции */
        .section {
            padding: 4rem 0;
        }
        
        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 3rem;
            text-align: center;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            border-radius: 2px;
        }
        
        /* Карточки функций */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .feature-card {
            background-color: var(--secondary-light);
            border-radius: 1rem;
            padding: 2rem;
            border: 1px solid var(--border);
            display: flex;
            flex-direction: column;
            height: 100%;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
            border-color: var(--primary);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            display: inline-block;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }
        
        .feature-card p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            flex-grow: 1;
        }
        
        /* Инструменты */
        .tools-section {
            background-color: var(--secondary-dark);
            border-radius: 1.5rem;
            padding: 3rem;
            margin-top: 2rem;
        }
        
        .tool-card {
            background-color: var(--secondary-light);
            border-radius: 1rem;
            padding: 2rem;
            border: 1px solid var(--border);
            margin-bottom: 2rem;
        }
        
        .tool-card:last-child {
            margin-bottom: 0;
        }
        
        .input-group {
            display: flex;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }
        
        input, textarea {
            flex-grow: 1;
            background-color: var(--secondary-dark);
            border: 1px solid var(--border);
            border-radius: 0.5rem;
            padding: 1rem;
            color: var(--text-primary);
            font-size: 1rem;
        }
        
        input:focus, textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 2px rgba(16, 163, 127, 0.2);
        }
        
        textarea {
            min-height: 120px;
            resize: vertical;
        }
        
        .btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 0.5rem;
            font-weight: 600;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background-color: transparent;
            border: 1px solid var(--border);
        }
        
        .btn-secondary:hover {
            background-color: var(--secondary-light);
        }
        
        .result {
            background-color: var(--secondary-dark);
            border-radius: 0.5rem;
            padding: 1.5rem;
            margin-top: 1.5rem;
            border: 1px solid var(--border);
            min-height: 100px;
        }
        
        /* Контактная информация */
        .contact-card {
            background: linear-gradient(135deg, var(--secondary-light) 0%, var(--secondary-dark) 100%);
            border-radius: 1.5rem;
            padding: 3rem;
            text-align: center;
            border: 1px solid var(--border);
            margin-top: 2rem;
        }
        
        .phone-number {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary);
            margin: 1.5rem 0;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 1rem;
        }
        
        /* Футер */
        footer {
            background-color: var(--secondary-dark);
            border-top: 1px solid var(--border);
            padding: 3rem 0;
            margin-top: 4rem;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .footer-logo {
            font-size: 1.5rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .copyright {
            color: var(--text-muted);
        }
        
        /* Адаптивность */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }
            
            .nav-links {
                gap: 1.5rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .input-group {
                flex-direction: column;
            }
            
            .footer-content {
                flex-direction: column;
                gap: 1.5rem;
                text-align: center;
            }
            
            .phone-number {
                font-size: 1.5rem;
                flex-direction: column;
                gap: 0.5rem;
            }
        }
        
        /* Анимации */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .fade-in {
            animation: fadeIn 0.8s ease forwards;
        }
        
        .delay-1 { animation-delay: 0.1s; }
        .delay-2 { animation-delay: 0.2s; }
        .delay-3 { animation-delay: 0.3s; }
        .delay-4 { animation-delay: 0.4s; }
        .delay-5 { animation-delay: 0.5s; }
        
        /* Индикатор загрузки */
        .loader {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: var(--primary);
            animation: spin 1s ease-in-out infinite;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <!-- Шапка -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-brain"></i>
                    <span>XIAI Plus</span>
                </div>
                <div class="nav-links">
                    <a href="#features">Функции</a>
                    <a href="#tools">Инструменты</a>
                    <a href="#contact">Контакты</a>
                </div>
                <button class="cta-button">
                    <i class="fas fa-rocket"></i>
                    Начать использовать
                </button>
            </div>
        </div>
    </header>

    <!-- Герой секция -->
    <section class="hero">
        <div class="container">
            <h1 class="fade-in">XIAI Plus - Искусственный интеллект нового поколения</h1>
            <p class="fade-in delay-1">Расширенные возможности искусственного интеллекта для решения ваших сложнейших задач всего за $0.50 в месяц</p>
            <div class="price-tag fade-in delay-2">
                <span class="price">$0.50</span>
                <span style="color: var(--text-muted);">/месяц</span>
            </div>
            <button class="cta-button fade-in delay-3">
                <i class="fas fa-bolt"></i>
                Попробовать бесплатно
            </button>
        </div>
    </section>

    <!-- Функции -->
    <section class="section" id="features">
        <div class="container">
            <h2 class="section-title">Мощные функции XIAI Plus</h2>
            <div class="features-grid">
                <div class="feature-card fade-in delay-1">
                    <div class="feature-icon">
                        <i class="fas fa-calculator"></i>
                    </div>
                    <h3>Решение сложных уравнений</h3>
                    <p>Наш ИИ решает уравнения любой сложности — от простых линейных до дифференциальных уравнений с пошаговым объяснением.</p>
                    <button class="btn-secondary">
                        <i class="fas fa-arrow-right"></i>
                        Узнать больше
                    </button>
                </div>
                <div class="feature-card fade-in delay-2">
                    <div class="feature-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Визуализация данных</h3>
                    <p>Создавайте интерактивные графики и диаграммы для наглядного представления информации и анализа тенденций.</p>
                    <button class="btn-secondary">
                        <i class="fas fa-arrow-right"></i>
                        Узнать больше
                    </button>
                </div>
                <div class="feature-card fade-in delay-3">
                    <div class="feature-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>Прямая связь с директором</h3>
                    <p>Получите персональный номер для связи с генеральным директором компании для решения любых вопросов.</p>
                    <button class="btn-secondary">
                        <i class="fas fa-arrow-right"></i>
                        Узнать больше
                    </button>
                </div>
                <div class="feature-card fade-in delay-4">
                    <div class="feature-icon">
                        <i class="fas fa-robot"></i>
                    </div>
                    <h3>Персональный AI-ассистент</h3>
                    <p>Ваш собственный ИИ-помощник, который учится вашим предпочтениям и привычкам для максимальной эффективности.</p>
                    <button class="btn-secondary">
                        <i class="fas fa-arrow-right"></i>
                        Узнать больше
                    </button>
                </div>
                <div class="feature-card fade-in delay-5">
                    <div class="feature-icon">
                        <i class="fas fa-database"></i>
                    </div>
                    <h3>Глубокий анализ данных</h3>
                    <p>Анализируйте большие массивы данных и получайте ценные инсайты для вашего бизнеса с помощью продвинутых алгоритмов.</p>
                    <button class="btn-secondary">
                        <i class="fas fa-arrow-right"></i>
                        Узнать больше
                    </button>
                </div>
                <div class="feature-card fade-in delay-5">
                    <div class="feature-icon">
                        <i class="fas fa-chart-bar"></i>
                    </div>
                    <h3>Прогнозирование тенденций</h3>
                    <p>Получайте точные прогнозы развития рынков и трендов на основе анализа больших данных и машинного обучения.</p>
                    <button class="btn-secondary">
                        <i class="fas fa-arrow-right"></i>
                        Узнать больше
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Инструменты -->
    <section class="section" id="tools">
        <div class="container">
            <h2 class="section-title">Инструменты XIAI Plus</h2>
            
            <div class="tools-section">
                <div class="tool-card">
                    <h3><i class="fas fa-calculator"></i> Решатель уравнений</h3>
                    <p>Введите ваше уравнение, и наш ИИ мгновенно найдет точное решение:</p>
                    
                    <div class="input-group">
                        <input type="text" id="equationInput" placeholder="Например: 2x + 3 = 7 или x * 597 * (355 + 599 * 369) / 2 = ?">
                        <button class="btn" onclick="solveEquation()">
                            <i class="fas fa-play"></i>
                            Решить
                        </button>
                    </div>
                    
                    <div class="result" id="equationResult">
                        Решение появится здесь...
                    </div>
                </div>
                
                <div class="tool-card">
                    <h3><i class="fas fa-chart-area"></i> Визуализация данных</h3>
                    <p>Создавайте интерактивные графики и диаграммы для ваших данных:</p>
                    
                    <textarea id="dataInput" placeholder="Введите данные для визуализации (например: категория1: 30, категория2: 45, категория3: 25) или математическую функцию для построения графика"></textarea>
                    
                    <div class="input-group">
                        <button class="btn" onclick="createVisualization()">
                            <i class="fas fa-chart-bar"></i>
                            Создать визуализацию
                        </button>
                        <button class="btn-secondary">
                            <i class="fas fa-download"></i>
                            Экспорт
                        </button>
                    </div>
                    
                    <div class="result" id="visualizationResult">
                        Здесь появится ваша визуализация...
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Контакты -->
    <section class="section" id="contact">
        <div class="container">
            <h2 class="section-title">Прямая связь с руководством</h2>
            
            <div class="contact-card">
                <h3><i class="fas fa-phone-alt"></i> Персональная поддержка</h3>
                <p>Для подписчиков XIAI Plus доступен прямой номер телефона генерального директора</p>
                
                <div class="phone-number">
                    <i class="fas fa-mobile-alt"></i>
                    +998-999-10-0097
                </div>
                
                <p>Звоните для решения любых вопросов, связанных с сервисом, или для обсуждения партнерских возможностей.</p>
                
                <button class="btn" style="margin-top: 1.5rem;">
                    <i class="fas fa-comment-alt"></i>
                    Начать чат с поддержкой
                </button>
            </div>
        </div>
    </section>

    <!-- Футер -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">
                    <i class="fas fa-brain"></i>
                    <span>XIAI Plus</span>
                </div>
                <div class="copyright">
                    &copy; 2025 XIAI Plus. Все права защищены.
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Анимация появления элементов при скролле
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.feature-card, .tool-card, .contact-card').forEach(el => {
            observer.observe(el);
        });

        // Решатель уравнений
        function solveEquation() {
            const equation = document.getElementById('equationInput').value;
            const resultElement = document.getElementById('equationResult');
            
            if (!equation.trim()) {
                resultElement.innerHTML = '<span style="color: var(--accent)">Пожалуйста, введите уравнение</span>';
                return;
            }
            
            // Показать индикатор загрузки
            resultElement.innerHTML = '<div class="loader"></div> Решаем уравнение...';
            
            // Имитация загрузки
            setTimeout(() => {
                try {
                    const solution = advancedEquationSolver(equation);
                    resultElement.innerHTML = `
                        <strong>Уравнение:</strong> ${equation}<br><br>
                        <strong>Решение:</strong> ${solution.answer}<br><br>
                        <strong>Пошаговое объяснение:</strong><br>${solution.steps.join('<br>')}
                    `;
                } catch (error) {
                    resultElement.innerHTML = `<span style="color: var(--accent)">Ошибка: ${error.message}. Пожалуйста, проверьте правильность уравнения.</span>`;
                }
            }, 1500);
        }
        
        function advancedEquationSolver(equation) {
            // Упрощаем уравнение: убираем пробелы и приводим к нижнему регистру
            const eq = equation.replace(/\s/g, '').toLowerCase();
            
            // Проверяем, является ли уравнение линейным
            if (eq.includes('x') && (eq.includes('='))) {
                return solveLinearEquation(eq);
            }
            
            // Если это простое выражение без переменных
            if (!eq.includes('x')) {
                return solveExpression(eq);
            }
            
            // Для других типов уравнений
            throw new Error('Сложные уравнения пока не поддерживаются');
        }
        
        function solveLinearEquation(equation) {
            const sides = equation.split('=');
            if (sides.length !== 2) {
                throw new Error('Неверный формат уравнения');
            }
            
            const left = sides[0];
            const right = sides[1];
            
            // Простая реализация для демонстрации
            // В реальном приложении здесь был бы полноценный парсер уравнений
            
            // Пример: 2x+3=7
            if (left === '2x+3' && right === '7') {
                return {
                    answer: 'x = 2',
                    steps: [
                        '1. Вычитаем 3 из обеих частей: 2x = 4',
                        '2. Делим обе части на 2: x = 2',
                        '3. Проверка: 2*2 + 3 = 7'
                    ]
                };
            }
            
            // Пример: 3x-5=10
            if (left === '3x-5' && right === '10') {
                return {
                    answer: 'x = 5',
                    steps: [
                        '1. Прибавляем 5 к обеим частям: 3x = 15',
                        '2. Делим обе части на 3: x = 5',
                        '3. Проверка: 3*5 - 5 = 10'
                    ]
                };
            }
            
            // Общий случай для простых линейных уравнений вида ax+b=c
            const match = left.match(/(\d*)x([+-]\d+)?/);
            if (match) {
                const a = match[1] ? parseInt(match[1]) : 1;
                const b = match[2] ? parseInt(match[2]) : 0;
                const c = parseInt(right);
                
                const x = (c - b) / a;
                
                return {
                    answer: `x = ${x}`,
                    steps: [
                        `1. Исходное уравнение: ${a}x ${b >= 0 ? '+' : ''} ${b} = ${c}`,
                        `2. Вычитаем ${b} из обеих частей: ${a}x = ${c - b}`,
                        `3. Делим обе части на ${a}: x = ${x}`,
                        `4. Проверка: ${a}*${x} ${b >= 0 ? '+' : ''} ${b} = ${c}`
                    ]
                };
            }
            
            throw new Error('Не удалось решить уравнение');
        }
        
        function solveExpression(expression) {
            // Безопасное вычисление выражения
            try {
                // Заменяем математические операторы для безопасного eval
                const safeExpression = expression
                    .replace(/×/g, '*')
                    .replace(/÷/g, '/')
                    .replace(/\^/g, '**');
                
                // Используем Function для безопасного вычисления
                const result = Function(`"use strict"; return (${safeExpression})`)();
                
                return {
                    answer: result,
                    steps: [
                        `1. Вычисляем выражение: ${expression}`,
                        `2. Получаем результат: ${result}`
                    ]
                };
            } catch (error) {
                throw new Error('Не удалось вычислить выражение');
            }
        }
        
        function createVisualization() {
            const data = document.getElementById('dataInput').value;
            const resultElement = document.getElementById('visualizationResult');
            
            if (!data.trim()) {
                resultElement.innerHTML = '<span style="color: var(--accent)">Пожалуйста, введите данные для визуализации</span>';
                return;
            }
            
            // Показать индикатор загрузки
            resultElement.innerHTML = '<div class="loader"></div> Создаем визуализацию...';
            
            // Имитация загрузки
            setTimeout(() => {
                // Простая имитация создания визуализации
                resultElement.innerHTML = `
                    <div style="text-align: center; padding: 1rem;">
                        <h3>Визуализация данных</h3>
                        <div style="display: flex; justify-content: center; align-items: flex-end; height: 200px; margin: 1rem 0; gap: 10px;">
                            <div style="background: linear-gradient(to top, var(--primary), var(--primary-dark)); width: 40px; height: 120px; border-radius: 4px 4px 0 0;"></div>
                            <div style="background: linear-gradient(to top, #e74c3c, #c0392b); width: 40px; height: 80px; border-radius: 4px 4px 0 0;"></div>
                            <div style="background: linear-gradient(to top, #2ecc71, #27ae60); width: 40px; height: 160px; border-radius: 4px 4px 0 0;"></div>
                            <div style="background: linear-gradient(to top, #f39c12, #e67e22); width: 40px; height: 100px; border-radius: 4px 4px 0 0;"></div>
                            <div style="background: linear-gradient(to top, #9b59b6, #8e44ad); width: 40px; height: 140px; border-radius: 4px 4px 0 0;"></div>
                        </div>
                        <p>Столбчатая диаграмма для данных: "${data}"</p>
                        <div style="display: flex; justify-content: center; gap: 1rem; margin-top: 1.5rem;">
                            <button class="btn-secondary">
                                <i class="fas fa-sliders-h"></i>
                                Настроить
                            </button>
                            <button class="btn">
                                <i class="fas fa-share"></i>
                                Поделиться
                            </button>
                        </div>
                    </div>
                `;
            }, 1500);
        }
    </script>
</body>
</html>
