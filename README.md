САЙТ В РАЗРАБОТКЕ
Элитные бани собственного производства
Создаем уникальные бани премиум-класса из отборных пород дерева с полным комплектом аксессуаров для вашего комфорта

<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Банный Лист - Бани премиум-класса собственного производства</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2A6B3F;
            --primary-dark: #1E4E2C;
            --accent: #D8A556;
            --dark: #1A1A1A;
            --light: #F8F5F0;
            --gray: #6B7280;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
            background-color: var(--light);
        }
        
        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
            margin-bottom: 1rem;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .btn {
            display: inline-block;
            padding: 15px 30px;
            background-color: var(--primary);
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .btn-accent {
            background-color: var(--accent);
            color: var(--dark);
        }
        
        .btn-accent:hover {
            background-color: #c69348;
        }
        
        /* Header */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 20px 0;
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            transition: var(--transition);
        }
        
        header.scrolled {
            padding: 15px 0;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        
        .logo span {
            color: var(--accent);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: var(--transition);
        }
        
        nav ul li a:hover {
            color: var(--primary);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            padding: 160px 0 100px;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://images.unsplash.com/photo-1595877244574-e90ce41ce089?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        /* Features */
        .features {
            padding: 80px 0;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.5rem;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            text-align: center;
            padding: 30px;
            border-radius: 10px;
            transition: var(--transition);
            background-color: var(--light);
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            font-size: 48px;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        /* Products */
        .products {
            padding: 80px 0;
            background-color: var(--light);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .product-image {
            height: 250px;
            overflow: hidden;
        }
        
        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
        
        .product-card:hover .product-image img {
            transform: scale(1.1);
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-title {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }
        
        .product-price {
            font-weight: 600;
            color: var(--primary);
            font-size: 1.2rem;
            margin-bottom: 15px;
        }
        
        /* Accessories */
        .accessories {
            padding: 80px 0;
            background-color: white;
        }
        
        .accessories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .accessory-card {
            display: flex;
            align-items: center;
            background-color: var(--light);
            padding: 20px;
            border-radius: 10px;
            transition: var(--transition);
        }
        
        .accessory-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .accessory-icon {
            font-size: 36px;
            margin-right: 15px;
            color: var(--primary);
        }
        
        /* Gallery */
        .gallery {
            padding: 80px 0;
            background-color: var(--light);
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 15px;
        }
        
        .gallery-item {
            height: 250px;
            overflow: hidden;
            border-radius: 10px;
            position: relative;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        /* About */
        .about {
            padding: 80px 0;
            background-color: white;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .about-image {
            border-radius: 10px;
            overflow: hidden;
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Contact */
        .contact {
            padding: 80px 0;
            background-color: var(--light);
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
        }
        
        .contact-icon {
            font-size: 24px;
            margin-right: 15px;
            color: var(--primary);
        }
        
        .contact-form {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: inherit;
            font-size: 16px;
            transition: var(--transition);
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 2px rgba(42, 107, 63, 0.2);
        }
        
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-logo {
            font-family: 'Playfair Display', serif;
            font-size: 24px;
            font-weight: 700;
            color: white;
            margin-bottom: 15px;
            display: block;
        }
        
        .footer-logo span {
            color: var(--accent);
        }
        
        .footer-links h4 {
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links ul li {
            margin-bottom: 10px;
        }
        
        .footer-links ul li a {
            color: #ddd;
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-links ul li a:hover {
            color: var(--accent);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            .about-content,
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 768px) {
            nav {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background-color: white;
                transition: var(--transition);
                padding: 30px;
            }
            
            nav.active {
                left: 0;
            }
            
            nav ul {
                flex-direction: column;
            }
            
            nav ul li {
                margin: 15px 0;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero {
                padding: 140px 0 80px;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .btn {
                padding: 12px 25px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container header-container">
            <a href="#" class="logo">Банный <span>Лист</span></a>
            <button class="mobile-menu-btn">☰</button>
            <nav id="nav">
                <ul>
                    <li><a href="#hero">Главная</a></li>
                    <li><a href="#products">Наши бани</a></li>
                    <li><a href="#accessories">Аксессуары</a></li>
                    <li><a href="#gallery">Галерея</a></li>
                    <li><a href="#about">О нас</a></li>
                    <li><a href="#contact">Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="hero">
        <div class="container">
            <h1>Элитные бани собственного производства</h1>
            <p>Создаем уникальные бани премиум-класса из отборных пород дерева с полным комплектом аксессуаров для вашего комфорта</p>
            <a href="#products" class="btn">Смотреть каталог</a>
            <a href="#contact" class="btn btn-accent">Получить консультацию</a>
        </div>
    </section>

    <!-- Features -->
    <section class="features">
        <div class="container">
            <h2 class="section-title">Почему выбирают нас</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">✓</div>
                    <h3>Качество материалов</h3>
                    <p>Используем только отборную древесину северных пород с собственных лесных угодий</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">✓</div>
                    <h3>Собственное производство</h3>
                    <p>Полный контроль качества на всех этапах производства от заготовки до сборки</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">✓</div>
                    <h3>Индивидуальный подход</h3>
                    <p>Проектируем и строим бани согласно вашим пожеланиям и особенностям участка</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">✓</div>
                    <h3>Гарантия 5 лет</h3>
                    <p>Предоставляем расширенную гарантию на все наши изделия и выполняем сервисное обслуживание</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Products -->
    <section class="products" id="products">
        <div class="container">
            <h2 class="section-title">Наши бани</h2>
            <div class="products-grid">
                <div class="product-card">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1577495508326-19a1b3cf65b7?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Баня Русская Классика">
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Русская Классика</h3>
                        <p>Традиционная баня из сруба с предбанником и парной на 3-4 человека</p>
                        <p class="product-price">от 350 000 руб.</p>
                        <a href="#contact" class="btn">Заказать</a>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1593085260707-5377ba37f868?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Баня Современная">
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Современная</h3>
                        <p>Баня с панорамным остеклением, современной печью и зоной отдыха</p>
                        <p class="product-price">от 550 000 руб.</p>
                        <a href="#contact" class="btn">Заказать</a>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-image">
                        <img src="https://images.unsplash.com/photo-1577495508045-aa6fd43d1830?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Баня Премиум">
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Премиум</h3>
                        <p>Просторная баня с бассейном, комнатой отдыха и бильярдной</p>
                        <p class="product-price">от 950 000 руб.</p>
                        <a href="#contact" class="btn">Заказать</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Accessories -->
    <section class="accessories" id="accessories">
        <div class="container">
            <h2 class="section-title">Аксессуары и принадлежности</h2>
            <div class="accessories-grid">
                <div class="accessory-card">
                    <div class="accessory-icon">♨️</div>
                    <div>
                        <h3>Печи банные</h3>
                        <p>Каменные и металлические печи от проверенных производителей</p>
                    </div>
                </div>
                <div class="accessory-card">
                    <div class="accessory-icon">🪑</div>
                    <div>
                        <h3>Мебель для бани</h3>
                        <p>Полки, лежаки, столы и табуреты из липы и кедра</p>
                    </div>
                </div>
                <div class="accessory-card">
                    <div class="accessory-icon">🍶</div>
                    <div>
                        <h3>Аксессуары</h3>
                        <p>Веники, ковши, шапочки и прочие банные принадлежности</p>
                    </div>
                </div>
                <div class="accessory-card">
                    <div class="accessory-icon">💡</div>
                    <div>
                        <h3>Освещение</h3>
                        <p>Влагозащищенные светильники и подсветка для создания атмосферы</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery -->
    <section class="gallery" id="gallery">
        <div class="container">
            <h2 class="section-title">Галерея выполненных работ</h2>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1577495508045-aa6fd43d1830?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Готовая баня 1">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1593085260707-5377ba37f868?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Готовая баня 2">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1577495508326-19a1b3cf65b7?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Готовая баня 3">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1595877244574-e90ce41ce089?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Готовая баня 4">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1542353427-5a2c874afc6d?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Готовая баня 5">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1565538810649-32b9c5b61c0d?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Готовая баня 6">
                </div>
            </div>
        </div>
    </section>

    <!-- About -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">О нашей компании</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Банный Двор - семейная компания с 15-летней историей, специализирующаяся на создании элитных бань из отборных пород дерева.</p>
                    <p>Мы контролируем весь процесс производства: от заготовки древесины на собственных лесных угодьях до финальной сборки на вашем участке.</p>
                    <p>Наши мастера - потомственные плотники, знающие все тонкости работы с деревом и создания идеального микроклимата в бане.</p>
                    <p>Каждое наше изделие - это уникальный проект, созданный с учетом пожеланий заказчика и особенностей места установки.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1586023492125-27a5df90a570?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Наше производство">
                </div>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Свяжитесь с нами</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">📞</div>
                        <div>
                            <h3>Телефон</h3>
                            <p>+7 (495) 123-45-67</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">✉️</div>
                        <div>
                            <h3>Email</h3>
                            <p>info@banniy-dvor.ru</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">🏢</div>
                        <div>
                            <h3>Адрес производства</h3>
                            <p>Оренбургская область, г. Оренбург</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">🕒</div>
                        <div>
                            <h3>Время работы</h3>
                            <p>Пн-Пт: 9:00 - 18:00<br>Сб: 10:00 - 16:00<br>Вс: выходной</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="consultation-form">
                        <div class="form-group">
                            <label for="name">Ваше имя</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Телефон</label>
                            <input type="tel" id="phone" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Сообщение</label>
                            <textarea id="message" class="form-control" placeholder="Расскажите о вашем проекте"></textarea>
                        </div>
                        <button type="submit" class="btn btn-accent">Отправить заявку</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-about">
                    <a href="#" class="footer-logo">Банный <span>Лист</span></a>
                    <p>Создаем элитные бани из отборных пород дерева с 2008 года. Собственное производство, гарантия качества.</p>
                </div>
                <div class="footer-links">
                    <h4>Продукция</h4>
                    <ul>
                        <li><a href="#products">Бани</a></li>
                        <li><a href="#accessories">Аксессуары</a></li>
                        <li><a href="#gallery">Галерея работ</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Компания</h4>
                    <ul>
                        <li><a href="#about">О нас</a></li>
                        <li><a href="#contact">Контакты</a></li>
                        <li><a href="#">Доставка и оплата</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Контакты</h4>
                    <ul>
                        <li>+7 (495) 123-45-67</li>
                        <li>info@banniy-dvor.ru</li>
                        <li>Оренбургская обл., г. Оренбург</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>© 2025 Банный Двор. ИП Рахметов А.К. ИНН 561902398552. Все права защищены.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const nav = document.querySelector('#nav');
        
        mobileMenuBtn.addEventListener('click', () => {
            nav.classList.toggle('active');
        });
        
        // Header scroll effect
        const header = document.querySelector('#header');
        
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Smooth scroll for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    // Close mobile menu if open
                    nav.classList.remove('active');
                    
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Form submission
        const contactForm = document.getElementById('consultation-form');
        
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Here would be the code to send the form data to the server
            alert('Спасибо за вашу заявку! Мы свяжемся с вами в ближайшее время.');
            contactForm.reset();
        });
    </script>
</body>
</html>
