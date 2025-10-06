<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Магазин банных аксессуаров и печей. Качественные товары для бани и сауны с доставкой по России.">
    <title>Банный Двор - магазин банных аксессуаров и печей</title>
    <style>
        :root {
            --primary-color: #8B4513;
            --secondary-color: #D2691E;
            --accent-color: #F4A460;
            --light-color: #FFF8DC;
            --dark-color: #4A2C2A;
            --text-color: #333;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background-color: #f9f5f0;
            color: var(--text-color);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header styles */
        header {
            background-color: var(--primary-color);
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            color: white;
            font-size: 24px;
            font-weight: bold;
            display: flex;
            align-items: center;
        }
        
        .logo span {
            color: var(--accent-color);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }
        
        nav ul li a:hover {
            color: var(--accent-color);
        }
        
        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent-color);
            transition: width 0.3s;
        }
        
        nav ul li a:hover::after {
            width: 100%;
        }
        
        .header-buttons {
            display: flex;
            align-items: center;
        }
        
        .btn {
            padding: 8px 15px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
            cursor: pointer;
            border: none;
            display: inline-block;
            text-align: center;
        }
        
        .btn-outline {
            border: 1px solid white;
            color: white;
            margin-right: 10px;
            background: transparent;
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--primary-color);
        }
        
        .btn-primary {
            background-color: var(--accent-color);
            color: var(--dark-color);
        }
        
        .btn-primary:hover {
            background-color: #e5944a;
            transform: translateY(-2px);
        }
        
        /* Hero section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%238B4513"/><path d="M0 0L100 100" stroke="%23D2691E" stroke-width="2"/><path d="M100 0L0 100" stroke="%23D2691E" stroke-width="2"/></svg>');
            background-size: cover;
            padding: 100px 0;
            text-align: center;
            color: white;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        /* Categories section */
        .section-title {
            text-align: center;
            margin: 50px 0 30px;
            color: var(--dark-color);
            position: relative;
        }
        
        .section-title:after {
            content: "";
            display: block;
            width: 80px;
            height: 3px;
            background-color: var(--secondary-color);
            margin: 10px auto;
        }
        
        .categories {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 50px;
        }
        
        .category-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .category-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
        }
        
        .category-img {
            height: 200px;
            background-color: var(--light-color);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary-color);
            font-size: 3rem;
        }
        
        .category-content {
            padding: 20px;
            text-align: center;
        }
        
        .category-content h3 {
            margin-bottom: 10px;
            color: var(--dark-color);
        }
        
        /* Products section */
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 50px;
        }
        
        .product-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
        }
        
        .product-img {
            height: 200px;
            background-color: var(--light-color);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary-color);
            font-size: 2rem;
        }
        
        .product-content {
            padding: 20px;
        }
        
        .product-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--dark-color);
            min-height: 56px;
        }
        
        .product-price {
            font-weight: bold;
            color: var(--primary-color);
            font-size: 1.2rem;
            margin-bottom: 15px;
        }
        
        .product-btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            padding: 8px 15px;
            border-radius: 4px;
            text-decoration: none;
            transition: background-color 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .product-btn:hover {
            background-color: var(--secondary-color);
        }
        
        /* About section */
        .about {
            background-color: var(--light-color);
            padding: 50px 0;
            margin: 50px 0;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
            padding-right: 30px;
        }
        
        .about-text p {
            margin-bottom: 15px;
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
            height: 300px;
            background-color: var(--accent-color);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-column h3 {
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3:after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background-color: var(--accent-color);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: var(--accent-color);
        }
        
        .contact-info {
            color: #ccc;
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Responsive design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin: 20px 0;
                justify-content: center;
                flex-wrap: wrap;
            }
            
            nav ul li {
                margin: 5px 10px;
            }
            
            .hero {
                padding: 60px 0;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .about-text {
                padding-right: 0;
                margin-bottom: 30px;
            }
            
            .header-buttons {
                margin-top: 15px;
            }
        }
        
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .btn {
                padding: 10px 15px;
                font-size: 0.9rem;
            }
            
            .categories, .products {
                grid-template-columns: 1fr;
            }
        }
        
        /* Skip link for accessibility */
        .skip-link {
            position: absolute;
            top: -40px;
            left: 0;
            background: var(--primary-color);
            color: white;
            padding: 8px;
            z-index: 1000;
            transition: top 0.3s;
        }
        
        .skip-link:focus {
            top: 0;
        }
    </style>
</head>
<body>
    <!-- Skip link for accessibility -->
    <a href="#main-content" class="skip-link">Перейти к основному содержимому</a>
    
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <span>Банный</span>Двор
            </div>
            <nav aria-label="Основная навигация">
                <ul>
                    <li><a href="#">Главная</a></li>
                    <li><a href="#">Каталог</a></li>
                    <li><a href="#">Печи</a></li>
                    <li><a href="#">Аксессуары</a></li>
                    <li><a href="#">О нас</a></li>
                    <li><a href="#">Контакты</a></li>
                </ul>
            </nav>
            <div class="header-buttons">
                <a href="#" class="btn btn-outline">Войти</a>
                <a href="#" class="btn btn-primary">Корзина (0)</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="main-content">
        <div class="container">
            <h1>Всё для вашей бани и сауны</h1>
            <p>Качественные печи, аксессуары и банные принадлежности для настоящих ценителей русской бани и финской сауны</p>
            <a href="#" class="btn btn-primary">Перейти в каталог</a>
        </div>
    </section>

    <!-- Categories Section -->
    <section class="container" aria-labelledby="categories-title">
        <h2 class="section-title" id="categories-title">Категории товаров</h2>
        <div class="categories">
            <div class="category-card">
                <div class="category-img" aria-hidden="true">🔥</div>
                <div class="category-content">
                    <h3>Банные печи</h3>
                    <p>Печи для русской бани и финской сауны</p>
                </div>
            </div>
            <div class="category-card">
                <div class="category-img" aria-hidden="true">👕</div>
                <div class="category-content">
                    <h3>Банная одежда</h3>
                    <p>Шапки, рукавицы и халаты</p>
                </div>
            </div>
            <div class="category-card">
                <div class="category-img" aria-hidden="true">🌿</div>
                <div class="category-content">
                    <h3>Аксессуары</h3>
                    <p>Веники, ковши, термометры</p>
                </div>
            </div>
            <div class="category-card">
                <div class="category-img" aria-hidden="true">♨️</div>
                <div class="category-content">
                    <h3>Парогенераторы</h3>
                    <p>Оборудование для создания пара</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Popular Products -->
    <section class="container" aria-labelledby="products-title">
        <h2 class="section-title" id="products-title">Популярные товары</h2>
        <div class="products">
            <div class="product-card">
                <div class="product-img" aria-hidden="true">🔥</div>
                <div class="product-content">
                    <h3 class="product-title">Печь банная "Вулкан"</h3>
                    <p class="product-price">25 990 ₽</p>
                    <button class="product-btn">В корзину</button>
                </div>
            </div>
            <div class="product-card">
                <div class="product-img" aria-hidden="true">👒</div>
                <div class="product-content">
                    <h3 class="product-title">Шапка банная войлочная</h3>
                    <p class="product-price">890 ₽</p>
                    <button class="product-btn">В корзину</button>
                </div>
            </div>
            <div class="product-card">
                <div class="product-img" aria-hidden="true">🌿</div>
                <div class="product-content">
                    <h3 class="product-title">Веник банный березовый</h3>
                    <p class="product-price">450 ₽</p>
                    <button class="product-btn">В корзину</button>
                </div>
            </div>
            <div class="product-card">
                <div class="product-img" aria-hidden="true">🥤</div>
                <div class="product-content">
                    <h3 class="product-title">Ковш деревянный резной</h3>
                    <p class="product-price">1 250 ₽</p>
                    <button class="product-btn">В корзину</button>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" aria-labelledby="about-title">
        <div class="container">
            <h2 class="section-title" id="about-title">О нашем магазине</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Мы специализируемся на продаже качественных банных аксессуаров и печей уже более 10 лет. Наша продукция изготовлена из натуральных материалов и прошла строгий контроль качества.</p>
                    <p>В нашем ассортименте вы найдете всё необходимое для обустройства бани или сауны: от традиционных банных печей до аксессуаров, которые создадут неповторимую атмосферу и помогут вам полностью расслабиться.</p>
                    <p>Мы сотрудничаем с проверенными производителями и гарантируем высокое качество всей нашей продукции.</p>
                </div>
                <div class="about-image" aria-hidden="true">
                    Наш магазин
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Магазин</h3>
                    <ul>
                        <li><a href="#">О нас</a></li>
                        <li><a href="#">Доставка и оплата</a></li>
                        <li><a href="#">Возврат товара</a></li>
                        <li><a href="#">Акции</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Каталог</h3>
                    <ul>
                        <li><a href="#">Банные печи</a></li>
                        <li><a href="#">Аксессуары для бани</a></li>
                        <li><a href="#">Банная одежда</a></li>
                        <li><a href="#">Парогенераторы</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Контакты</h3>
                    <ul>
                        <li class="contact-info">г. Москва, ул. Банная, д. 1</li>
                        <li class="contact-info">+7 (495) 123-45-67</li>
                        <li class="contact-info">info@bannyidvor.ru</li>
                        <li class="contact-info">Ежедневно с 9:00 до 21:00</li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 Банный Двор. Все права защищены.</p>
            </div>
        </div>
    </footer>

    <script>
        // Простой скрипт для демонстрации работы корзины
        document.addEventListener('DOMContentLoaded', function() {
            const cartButtons = document.querySelectorAll('.product-btn');
            const cartCounter = document.querySelector('.btn-primary');
            let cartCount = 0;
            
            cartButtons.forEach(button => {
                button.addEventListener('click', function() {
                    cartCount++;
                    cartCounter.textContent = `Корзина (${cartCount})`;
                    
                    // Анимация добавления в корзину
                    this.textContent = 'Добавлено!';
                    this.style.backgroundColor = '#4CAF50';
                    
                    setTimeout(() => {
                        this.textContent = 'В корзину';
                        this.style.backgroundColor = '';
                    }, 1500);
                });
            });
        });
    </script>
</body>
</html>
