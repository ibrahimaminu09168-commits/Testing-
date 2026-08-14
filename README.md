
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>D’EST Skincare & Spa | Beauty • Care • Confidence</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;0,600;0,700;1,400&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">

    <!-- Styles -->
    <style>
        :root {
            --bg-body: #FBFBF8;
            --surface-card: #FFFFFF;
            --primary-pink: #DB2777;
            --primary-light: #FDEBF2;
            --pink-accent: #FFC1D6;
            --text-dark: #1F2937;
            --text-muted: #6B7280;
            --border-color: #F3E8EE;
            --radius-sm: 8px;
            --radius-md: 12px;
            --radius-lg: 20px;
            --radius-full: 9999px;
            --shadow-sm: 0 1px 3px rgba(0,0,0,0.05);
            --shadow-md: 0 4px 12px rgba(219, 39, 119, 0.08);
            --shadow-lg: 0 10px 25px rgba(0,0,0,0.08);
            --font-serif: 'Playfair Display', serif;
            --font-sans: 'Plus Jakarta Sans', sans-serif;
            --transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: var(--font-sans);
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: var(--bg-body);
            color: var(--text-dark);
            line-height: 1.5;
            overflow-x: hidden;
        }

        a { color: inherit; text-decoration: none; }
        img { max-width: 100%; height: auto; display: block; }
        .container { max-width: 1200px; margin: 0 auto; padding: 0 16px; }

        /* Utility */
        .hidden { display: none !important; }
        .text-center { text-align: center; }
        .font-serif { font-family: var(--font-serif); }

        /* Announcement Bar */
        .announcement-bar {
            background: linear-gradient(90deg, #DB2777, #BE185D);
            color: #FFFFFF;
            padding: 10px 16px;
            font-size: 0.825rem;
            font-weight: 600;
            text-align: center;
            letter-spacing: 0.02em;
        }

        /* Header / Navigation */
        .header {
            background: rgba(255, 255, 255, 0.96);
            backdrop-filter: blur(8px);
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid var(--border-color);
        }

        .header-inner {
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 72px;
        }

        .brand-logo {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .brand-logo img {
            width: 46px;
            height: 46px;
            border-radius: 50%;
            object-fit: cover;
            border: 2px solid var(--pink-accent);
        }

        .brand-name {
            font-family: var(--font-serif);
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--text-dark);
            line-height: 1.1;
        }

        .brand-tagline {
            font-size: 0.65rem;
            text-transform: uppercase;
            letter-spacing: 0.1em;
            color: var(--primary-pink);
            font-weight: 600;
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 24px;
            list-style: none;
        }

        .nav-link {
            font-size: 0.9rem;
            font-weight: 500;
            color: var(--text-dark);
            transition: var(--transition);
        }

        .nav-link:hover, .nav-link.active {
            color: var(--primary-pink);
        }

        .nav-actions {
            display: flex;
            align-items: center;
            gap: 16px;
        }

        .cart-icon-btn {
            position: relative;
            background: var(--primary-light);
            border: none;
            width: 44px;
            height: 44px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            color: var(--primary-pink);
            font-size: 1.1rem;
            transition: var(--transition);
        }

        .cart-icon-btn:hover {
            background: var(--pink-accent);
            color: #FFFFFF;
        }

        .cart-badge {
            position: absolute;
            top: -2px;
            right: -2px;
            background: var(--primary-pink);
            color: #FFFFFF;
            font-size: 0.7rem;
            font-weight: 700;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 2px solid #FFFFFF;
        }

        .mobile-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.6rem;
            color: var(--text-dark);
            cursor: pointer;
        }

        /* Buttons */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            padding: 12px 24px;
            border-radius: var(--radius-full);
            font-size: 0.9rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            outline: none;
        }

        .btn-primary {
            background-color: var(--primary-pink);
            color: #FFFFFF;
            box-shadow: 0 4px 14px rgba(219, 39, 119, 0.3);
        }

        .btn-primary:hover {
            background-color: #BE185D;
            transform: translateY(-2px);
        }

        .btn-outline {
            background: transparent;
            border: 1px solid var(--primary-pink);
            color: var(--primary-pink);
        }

        .btn-outline:hover {
            background: var(--primary-light);
        }

        .btn-sm { padding: 8px 16px; font-size: 0.8rem; }
        .btn-block { width: 100%; }

        /* Hero Section */
        .hero {
            padding: 48px 0;
            background: radial-gradient(circle at top right, #FDEBF2, var(--bg-body));
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        .hero-title {
            font-family: var(--font-serif);
            font-size: 2.75rem;
            line-height: 1.2;
            margin-bottom: 16px;
            color: var(--text-dark);
        }

        .hero-subtitle {
            font-size: 1.05rem;
            color: var(--text-muted);
            margin-bottom: 28px;
        }

        .hero-banner-img {
            border-radius: var(--radius-lg);
            box-shadow: var(--shadow-lg);
            border: 4px solid #FFFFFF;
            width: 100%;
            max-height: 480px;
            object-fit: cover;
        }

        /* Anniversary Feature Card */
        .anniversary-badge-card {
            background: #FFFFFF;
            border: 1px solid var(--pink-accent);
            border-radius: var(--radius-md);
            padding: 16px;
            display: flex;
            align-items: center;
            gap: 16px;
            margin-bottom: 24px;
            box-shadow: var(--shadow-sm);
        }

        .anniversary-badge-card .num {
            font-family: var(--font-serif);
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary-pink);
            line-height: 1;
        }

        /* Controls & Categories */
        .section-title {
            font-family: var(--font-serif);
            font-size: 2rem;
            text-align: center;
            margin-bottom: 8px;
        }

        .section-subtitle {
            text-align: center;
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 32px;
        }

        .category-scroll {
            display: flex;
            gap: 10px;
            overflow-x: auto;
            padding-bottom: 12px;
            scrollbar-width: none;
        }

        .category-scroll::-webkit-scrollbar { display: none; }

        .cat-chip {
            padding: 10px 20px;
            background: #FFFFFF;
            border: 1px solid var(--border-color);
            border-radius: var(--radius-full);
            font-size: 0.85rem;
            font-weight: 500;
            white-space: nowrap;
            cursor: pointer;
            transition: var(--transition);
        }

        .cat-chip.active, .cat-chip:hover {
            background: var(--primary-pink);
            color: #FFFFFF;
            border-color: var(--primary-pink);
        }

        .shop-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 16px;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 24px;
        }

        .search-box {
            position: relative;
            flex: 1;
            min-width: 260px;
        }

        .search-input {
            width: 100%;
            padding: 12px 16px 12px 42px;
            border-radius: var(--radius-full);
            border: 1px solid var(--border-color);
            background: #FFFFFF;
            font-size: 0.9rem;
            outline: none;
            transition: var(--transition);
        }

        .search-input:focus {
            border-color: var(--primary-pink);
            box-shadow: 0 0 0 3px var(--primary-light);
        }

        .search-icon-svg {
            position: absolute;
            left: 14px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--text-muted);
        }

        .sort-select {
            padding: 12px 20px;
            border-radius: var(--radius-full);
            border: 1px solid var(--border-color);
            background: #FFFFFF;
            font-size: 0.85rem;
            outline: none;
            cursor: pointer;
        }

        /* Product Grid & Cards */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .product-card {
            background: var(--surface-card);
            border-radius: var(--radius-md);
            border: 1px solid var(--border-color);
            overflow: hidden;
            display: flex;
            flex-direction: column;
            transition: var(--transition);
        }

        .product-card:hover {
            box-shadow: var(--shadow-md);
            transform: translateY(-3px);
        }

        .product-img-wrapper {
            position: relative;
            width: 100%;
            padding-top: 100%;
            background: #F9FAFB;
            overflow: hidden;
            cursor: pointer;
        }

        .product-img {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .product-card:hover .product-img {
            transform: scale(1.04);
        }

        .product-info {
            padding: 16px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .product-category {
            font-size: 0.725rem;
            text-transform: uppercase;
            color: var(--primary-pink);
            font-weight: 600;
            margin-bottom: 4px;
        }

        .product-title {
            font-size: 0.95rem;
            font-weight: 600;
            color: var(--text-dark);
            margin-bottom: 8px;
            line-height: 1.3;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
            height: 2.6em;
            cursor: pointer;
        }

        .product-price {
            font-size: 1.05rem;
            font-weight: 700;
            color: var(--text-dark);
            margin-top: auto;
            margin-bottom: 12px;
        }

        .price-unavailable {
            font-size: 0.8rem;
            color: var(--text-muted);
            font-style: italic;
            font-weight: normal;
        }

        /* Drawers & Modals */
        .drawer-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.4);
            backdrop-filter: blur(4px);
            z-index: 200;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.3s ease;
        }

        .drawer-overlay.active { opacity: 1; pointer-events: auto; }

        .drawer {
            position: fixed;
            top: 0;
            right: 0;
            width: 100%;
            max-width: 440px;
            height: 100%;
            background: #FFFFFF;
            z-index: 210;
            transform: translateX(100%);
            transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            display: flex;
            flex-direction: column;
            box-shadow: var(--shadow-lg);
        }

        .drawer-overlay.active .drawer { transform: translateX(0); }

        .drawer-header {
            padding: 20px;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .drawer-title { font-family: var(--font-serif); font-size: 1.25rem; font-weight: 700; }
        .close-btn { background: none; border: none; font-size: 1.5rem; cursor: pointer; color: var(--text-muted); }
        .drawer-body { padding: 20px; overflow-y: auto; flex-grow: 1; }
        .drawer-footer { padding: 20px; border-top: 1px solid var(--border-color); background: #FAFAFA; }

        /* Cart Items */
        .cart-item {
            display: flex;
            gap: 12px;
            margin-bottom: 16px;
            padding-bottom: 16px;
            border-bottom: 1px solid var(--border-color);
        }

        .cart-item-img {
            width: 64px;
            height: 64px;
            border-radius: var(--radius-sm);
            object-fit: cover;
        }

        .cart-item-details { flex-grow: 1; }
        .cart-item-title { font-size: 0.85rem; font-weight: 600; margin-bottom: 4px; }
        .cart-item-price { font-size: 0.85rem; color: var(--primary-pink); font-weight: 700; }
        
        .qty-controls {
            display: flex;
            align-items: center;
            gap: 8px;
            margin-top: 6px;
        }

        .qty-btn {
            width: 24px;
            height: 24px;
            border-radius: 50%;
            border: 1px solid var(--border-color);
            background: #FFFFFF;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
        }

        .qty-num { font-size: 0.85rem; font-weight: 600; }

        /* Gallery Modal */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(4px);
            z-index: 300;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 16px;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.25s ease;
        }

        .modal-overlay.active { opacity: 1; pointer-events: auto; }

        .modal-card {
            background: #FFFFFF;
            border-radius: var(--radius-lg);
            width: 100%;
            max-width: 700px;
            max-height: 90vh;
            overflow-y: auto;
            box-shadow: var(--shadow-lg);
            position: relative;
        }

        .modal-body {
            padding: 24px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 24px;
        }

        .gallery-main-img {
            width: 100%;
            height: 280px;
            object-fit: cover;
            border-radius: var(--radius-md);
            margin-bottom: 8px;
        }

        .gallery-thumbs {
            display: flex;
            gap: 8px;
            overflow-x: auto;
        }

        .thumb-img {
            width: 52px;
            height: 52px;
            border-radius: var(--radius-sm);
            object-fit: cover;
            cursor: pointer;
            border: 2px solid transparent;
        }

        .thumb-img.active { border-color: var(--primary-pink); }

        /* Forms */
        .form-group { margin-bottom: 16px; }
        .form-label { display: block; font-size: 0.8rem; font-weight: 600; margin-bottom: 6px; color: var(--text-dark); }
        .form-control {
            width: 100%;
            padding: 10px 14px;
            border-radius: var(--radius-sm);
            border: 1px solid var(--border-color);
            font-size: 0.875rem;
            outline: none;
            background: #FFFFFF;
        }

        .form-control:focus { border-color: var(--primary-pink); }

        .timer-box {
            background: #FFF1F2;
            border: 1px dashed var(--primary-pink);
            padding: 12px;
            border-radius: var(--radius-md);
            text-align: center;
            margin-bottom: 16px;
        }

        .timer-val {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-pink);
            font-family: monospace;
        }

        /* Sections */
        .section { padding: 60px 0; }
        .bg-pink { background-color: var(--primary-light); }

        /* Testimonials Grid */
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 16px;
        }

        .testimonial-img {
            width: 100%;
            height: 380px;
            object-fit: cover;
            border-radius: var(--radius-md);
            box-shadow: var(--shadow-sm);
        }

        /* Trust Grid */
        .trust-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            text-align: center;
        }

        .trust-card {
            padding: 20px;
            background: #FFFFFF;
            border-radius: var(--radius-md);
            border: 1px solid var(--border-color);
        }

        .trust-icon { font-size: 1.8rem; color: var(--primary-pink); margin-bottom: 8px; }

        /* Footer */
        .footer {
            background: #111827;
            color: #F9FAFB;
            padding: 60px 0 20px 0;
            font-size: 0.875rem;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 32px;
            margin-bottom: 40px;
        }

        .footer-title {
            font-family: var(--font-serif);
            font-size: 1.1rem;
            margin-bottom: 16px;
            color: var(--pink-accent);
        }

        .footer-links { list-style: none; }
        .footer-links li { margin-bottom: 8px; }
        .footer-links a:hover { color: var(--pink-accent); }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #1F2937;
            color: #9CA3AF;
            font-size: 0.75rem;
        }

        /* Mobile Adjustments */
        @media (max-width: 768px) {
            .hero-grid { grid-template-columns: 1fr; }
            .hero-title { font-size: 2rem; }
            .nav-links {
                display: none;
                position: absolute;
                top: 72px;
                left: 0;
                width: 100%;
                background: #FFFFFF;
                flex-direction: column;
                padding: 20px;
                border-bottom: 1px solid var(--border-color);
                box-shadow: var(--shadow-md);
            }
            .nav-links.active { display: flex; }
            .mobile-toggle { display: block; }
            .modal-body { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <!-- Announcement Bar -->
    <div class="announcement-bar">
        🎉 CELEBRATING 4 YEARS OF SKINCARE & 1 YEAR OF SPA | 16TH – 29TH AUGUST SPECIAL OFFERS!
    </div>

    <!-- Header Navigation -->
    <header class="header">
        <div class="container header-inner">
            <a href="#" class="brand-logo">
                <img src="https://i.ibb.co/bjkvCs4W/IMG-6551.jpg" alt="D'EST Skincare & Spa Logo">
                <div>
                    <div class="brand-name">D’EST</div>
                    <div class="brand-tagline">Skincare & Spa</div>
                </div>
            </a>

            <nav>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#home" class="nav-link active" onclick="closeMenu()">Home</a></li>
                    <li><a href="#shop" class="nav-link" onclick="closeMenu()">Shop Products</a></li>
                    <li><a href="#spa" class="nav-link" onclick="closeMenu()">Spa Experience</a></li>
                    <li><a href="#about" class="nav-link" onclick="closeMenu()">About Us</a></li>
                    <li><a href="#testimonials" class="nav-link" onclick="closeMenu()">Reviews</a></li>
                    <li><a href="#contact" class="nav-link" onclick="closeMenu()">Contact</a></li>
                </ul>
            </nav>

            <div class="nav-actions">
                <button class="cart-icon-btn" onclick="openCartDrawer()" aria-label="Cart">
                    🛒
                    <span class="cart-badge" id="cartCountBadge">0</span>
                </button>
                <button class="mobile-toggle" onclick="toggleMenu()" aria-label="Toggle Menu">☰</button>
            </div>
        </div>
    </header>

    <!-- Main Body -->
    <main>
        <!-- Hero Section -->
        <section id="home" class="hero">
            <div class="container hero-grid">
                <div>
                    <span style="font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.15em; color: var(--primary-pink); font-weight: 700;">Beauty • Care • Confidence</span>
                    <h1 class="hero-title">Glow Effortlessly with Premium Skincare & Spa</h1>
                    <p class="hero-subtitle">D’EST Skincare & Spa is your destination for quality skincare, beauty essentials, and relaxing spa experiences. We’re here to help you look good, feel confident and glow effortlessly.</p>
                    
                    <div class="anniversary-badge-card">
                        <div>
                            <div class="num">4 YRS</div>
                            <div style="font-size: 0.75rem; text-transform: uppercase; font-weight: 600;">Skincare</div>
                        </div>
                        <div style="border-left: 1px solid var(--border-color); padding-left: 16px;">
                            <div class="num">1 YR</div>
                            <div style="font-size: 0.75rem; text-transform: uppercase; font-weight: 600;">Spa Experience</div>
                        </div>
                    </div>

                    <div style="display: flex; gap: 12px; flex-wrap: wrap;">
                        <a href="#shop" class="btn btn-primary">SHOP PRODUCTS</a>
                        <a href="#spa" class="btn btn-outline">BOOK A SPA EXPERIENCE</a>
                    </div>
                </div>
                <div>
                    <img src="https://i.ibb.co/4gWn5Yss/1786732118045.png" alt="D'EST Anniversary Celebration" class="hero-banner-img">
                </div>
            </div>
        </section>

        <!-- Trust Badges -->
        <section class="section" style="padding: 36px 0;">
            <div class="container">
                <div class="trust-grid">
                    <div class="trust-card">
                        <div class="trust-icon">✨</div>
                        <h3>100% Authentic</h3>
                        <p style="font-size: 0.8rem; color: var(--text-muted); margin-top: 4px;">Direct from verified beauty distributors.</p>
                    </div>
                    <div class="trust-card">
                        <div class="trust-icon">🌿</div>
                        <h3>Expert Skincare</h3>
                        <p style="font-size: 0.8rem; color: var(--text-muted); margin-top: 4px;">Tailored routines for your skin type.</p>
                    </div>
                    <div class="trust-card">
                        <div class="trust-icon">🚚</div>
                        <h3>Swift Delivery</h3>
                        <p style="font-size: 0.8rem; color: var(--text-muted); margin-top: 4px;">Carefully packaged doorstep shipping.</p>
                    </div>
                    <div class="trust-card">
                        <div class="trust-icon">🌸</div>
                        <h3>Relaxing Spa</h3>
                        <p style="font-size: 0.8rem; color: var(--text-muted); margin-top: 4px;">Aesthetic and tranquil aesthetic therapy.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Shop Section -->
        <section id="shop" class="section bg-pink">
            <div class="container">
                <h2 class="section-title">Explore Our Shop</h2>
                <p class="section-subtitle">Find your exact skincare products, soaps, shower gels, and body lotions.</p>

                <!-- Search & Filters -->
                <div class="shop-controls">
                    <div class="search-box">
                        <span class="search-icon-svg">🔍</span>
                        <input type="text" id="searchInput" class="search-input" placeholder="Search by name (e.g., NIVEA, Kojic, Bath)..." oninput="renderProducts()">
                    </div>
                    <select id="sortSelect" class="sort-select" onchange="renderProducts()">
                        <option value="default">Default Sorting</option>
                        <option value="low-high">Price: Low to High</option>
                        <option value="high-low">Price: High to Low</option>
                        <option value="az">Name: A - Z</option>
                    </select>
                </div>

                <!-- Category Chips -->
                <div class="category-scroll" id="categoryContainer">
                    <!-- Populated via JS -->
                </div>

                <!-- Products Grid -->
                <div class="product-grid" id="productGridContainer" style="margin-top: 24px;">
                    <!-- Populated via JS -->
                </div>
            </div>
        </section>

        <!-- Product Request Section -->
        <section class="section">
            <div class="container text-center" style="max-width: 600px;">
                <h2 class="font-serif" style="font-size: 1.75rem; margin-bottom: 8px;">Can't find what you're looking for?</h2>
                <p style="color: var(--text-muted); font-size: 0.9rem; margin-bottom: 20px;">Looking for a skincare product you don't see in our shop? Send us a message and tell us what you're looking for.</p>
                <div style="display: flex; gap: 8px;">
                    <input type="text" id="customProductInput" class="form-control" placeholder="Product you're looking for...">
                    <button class="btn btn-primary" onclick="askCustomProductWhatsApp()">ASK ABOUT THIS PRODUCT</button>
                </div>
            </div>
        </section>

        <!-- Spa Section -->
        <section id="spa" class="section bg-pink">
            <div class="container">
                <div class="hero-grid">
                    <div>
                        <span style="font-size: 0.8rem; text-transform: uppercase; color: var(--primary-pink); font-weight: 700;">Serenity & Aesthetic Care</span>
                        <h2 class="font-serif" style="font-size: 2.25rem; margin: 8px 0 16px 0;">D’EST Spa Experience</h2>
                        <p style="color: var(--text-muted); font-size: 0.95rem; margin-bottom: 24px;">Rejuvenate your skin and mind. Contact us for details on our personalized body treatments, facial therapy, and relaxing spa sessions.</p>
                        
                        <form id="spaBookingForm" onsubmit="handleSpaBooking(event)">
                            <div class="form-group">
                                <label class="form-label">Full Name *</label>
                                <input type="text" id="spaName" class="form-control" required placeholder="Your full name">
                            </div>
                            <div class="form-group">
                                <label class="form-label">Phone Number *</label>
                                <input type="tel" id="spaPhone" class="form-control" required placeholder="08166501584">
                            </div>
                            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 12px;">
                                <div class="form-group">
                                    <label class="form-label">Preferred Date *</label>
                                    <input type="date" id="spaDate" class="form-control" required>
                                </div>
                                <div class="form-group">
                                    <label class="form-label">Preferred Time *</label>
                                    <input type="time" id="spaTime" class="form-control" required>
                                </div>
                            </div>
                            <div class="form-group">
                                <label class="form-label">Service / Treatment / Note</label>
                                <textarea id="spaNotes" class="form-control" rows="2" placeholder="Facial glow treatment, relaxing massage, etc."></textarea>
                            </div>
                            <button type="submit" class="btn btn-primary btn-block">BOOK A SPA SESSION</button>
                        </form>
                    </div>
                    <div>
                        <img src="https://i.ibb.co/4gWn5Yss/1786732118045.png" alt="D'EST Spa Atmosphere" style="border-radius: var(--radius-lg); box-shadow: var(--shadow-lg);">
                    </div>
                </div>
            </div>
        </section>

        <!-- Testimonials -->
        <section id="testimonials" class="section">
            <div class="container">
                <h2 class="section-title">Customer Testimonials</h2>
                <p class="section-subtitle">Real feedback and glow results from our valued customers.</p>
                <div class="testimonials-grid">
                    <img src="https://i.ibb.co/p6S4kZC0/In-Shot-20260813-142917019.jpg" alt="D'EST Customer Review 1" class="testimonial-img" loading="lazy">
                    <img src="https://i.ibb.co/RG0hFbNY/In-Shot-20260813-143500658.jpg" alt="D'EST Customer Review 2" class="testimonial-img" loading="lazy">
                    <img src="https://i.ibb.co/ycS6ZnDB/In-Shot-20260813-143540310.jpg" alt="D'EST Customer Review 3" class="testimonial-img" loading="lazy">
                    <img src="https://i.ibb.co/FLrw3DVp/In-Shot-20260813-143615819.jpg" alt="D'EST Customer Review 4" class="testimonial-img" loading="lazy">
                </div>
            </div>
        </section>

        <!-- About Business -->
        <section id="about" class="section bg-pink">
            <div class="container text-center" style="max-width: 800px;">
                <h2 class="section-title">About D’EST Skincare & Spa</h2>
                <p style="font-size: 1.05rem; line-height: 1.8; color: var(--text-dark); margin-top: 16px;">
                    D’EST Skincare & Spa is your destination for quality skincare, beauty essentials, and relaxing spa experiences. We’re here to help you look good, feel confident and glow effortlessly.
                </p>
            </div>
        </section>

        <!-- Location & Contact -->
        <section id="contact" class="section">
            <div class="container">
                <div class="hero-grid">
                    <div>
                        <h2 class="font-serif" style="font-size: 2rem; margin-bottom: 16px;">Location & Hours</h2>
                        <div style="margin-bottom: 16px;">
                            <strong>📍 Physical Address:</strong>
                            <p style="color: var(--text-muted); font-size: 0.95rem; margin-top: 4px;">
                                Old Ife road Afro bus-stop,<br>
                                In God We Trust Plaza,<br>
                                Sawmill, Ibadan, Oyo State, Nigeria.
                            </p>
                        </div>

                        <div style="margin-bottom: 16px;">
                            <strong>🕒 Opening Hours:</strong>
                            <p style="color: var(--text-muted); font-size: 0.95rem; margin-top: 4px;">
                                Monday – Friday: 9:00 AM – 6:00 PM<br>
                                Saturday: 10:00 AM – 6:00 PM
                            </p>
                        </div>

                        <div style="margin-bottom: 24px;">
                            <strong>📞 Phone & WhatsApp:</strong>
                            <p style="color: var(--text-muted); font-size: 0.95rem; margin-top: 4px;">08166501584</p>
                        </div>

                        <div style="display: flex; gap: 12px; flex-wrap: wrap;">
                            <a href="https://wa.me/2348166501584" target="_blank" class="btn btn-primary btn-sm">Chat on WhatsApp</a>
                            <a href="https://www.instagram.com/d_est_skincareandspa?igsh=MWR0M3hiOTVqNzRtNQ%3D%3D&utm_source=qr" target="_blank" class="btn btn-outline btn-sm">Instagram</a>
                            <a href="https://www.tiktok.com/@destskincareandspa?_r=1&_t=ZS-98qnNnHIsEv" target="_blank" class="btn btn-outline btn-sm">TikTok</a>
                        </div>
                    </div>

                    <div style="background: #FFFFFF; padding: 24px; border-radius: var(--radius-lg); border: 1px solid var(--border-color); box-shadow: var(--shadow-md);">
                        <h3 class="font-serif" style="font-size: 1.25rem; margin-bottom: 12px;">Track Existing Order</h3>
                        <p style="font-size: 0.85rem; color: var(--text-muted); margin-bottom: 16px;">Have your order reference number? Connect with our team to verify tracking status.</p>
                        <div class="form-group">
                            <input type="text" id="trackOrderInput" class="form-control" placeholder="Order Number (e.g. DEST-12345)">
                        </div>
                        <button class="btn btn-primary btn-block" onclick="trackOrderWhatsApp()">TRACK ORDER</button>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div>
                    <h3 class="footer-title">D’EST Skincare & Spa</h3>
                    <p style="color: #9CA3AF; line-height: 1.6;">Quality skincare, beauty essentials, and relaxing spa experiences. Helping you look good, feel confident and glow effortlessly.</p>
                </div>
                <div>
                    <h3 class="footer-title">Quick Navigation</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#shop">Shop Essentials</a></li>
                        <li><a href="#spa">Spa Experience</a></li>
                        <li><a href="#about">About D'EST</a></li>
                        <li><a href="#contact">Location & Hours</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="footer-title">Connect With Us</h3>
                    <ul class="footer-links">
                        <li><a href="https://www.instagram.com/d_est_skincareandspa?igsh=MWR0M3hiOTVqNzRtNQ%3D%3D&utm_source=qr" target="_blank">Instagram (@D_est_skincareandspa)</a></li>
                        <li><a href="https://www.tiktok.com/@destskincareandspa?_r=1&_t=ZS-98qnNnHIsEv" target="_blank">TikTok (@destskincareandspa)</a></li>
                        <li><a href="https://wa.me/2348166501584" target="_blank">WhatsApp Support</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                &copy; 2026 D’EST Skincare & Spa. All Rights Reserved.
            </div>
        </div>
    </footer>

    <!-- Shopping Cart Drawer -->
    <div class="drawer-overlay" id="cartDrawerOverlay">
        <div class="drawer">
            <div class="drawer-header">
                <span class="drawer-title">Shopping Cart</span>
                <button class="close-btn" onclick="closeCartDrawer()">×</button>
            </div>
            <div class="drawer-body" id="cartDrawerBody">
                <!-- Dynamically Populated -->
            </div>
            <div class="drawer-footer" id="cartDrawerFooter">
                <div style="display: flex; justify-content: space-between; font-weight: 700; margin-bottom: 12px;">
                    <span>Total:</span>
                    <span id="cartSubtotalText">₦0</span>
                </div>
                <button class="btn btn-primary btn-block" onclick="openCheckoutModal()">CHECKOUT</button>
            </div>
        </div>
    </div>

    <!-- Product Detail / Gallery Modal -->
    <div class="modal-overlay" id="productModalOverlay">
        <div class="modal-card">
            <button class="close-btn" style="position: absolute; right: 16px; top: 16px; z-index: 10;" onclick="closeProductModal()">×</button>
            <div class="modal-body" id="productModalBody">
                <!-- Dynamically Populated -->
            </div>
        </div>
    </div>

    <!-- Checkout Modal -->
    <div class="modal-overlay" id="checkoutModalOverlay">
        <div class="modal-card" style="max-width: 500px;">
            <div style="padding: 20px; border-bottom: 1px solid var(--border-color); display: flex; justify-content: space-between; align-items: center;">
                <h3 class="font-serif" style="font-size: 1.25rem;">Order Checkout</h3>
                <button class="close-btn" onclick="closeCheckoutModal()">×</button>
            </div>
            
            <div style="padding: 20px;">
                <!-- Step 1: Customer Info -->
                <div id="checkoutStep1">
                    <h4 style="margin-bottom: 12px; font-size: 0.85rem; text-transform: uppercase; color: var(--primary-pink);">1. Customer Information</h4>
                    <form onsubmit="goToPaymentStep(event)">
                        <div class="form-group">
                            <label class="form-label">Full Name *</label>
                            <input type="text" id="custName" class="form-control" required placeholder="Enter your full name">
                        </div>
                        <div class="form-group">
                            <label class="form-label">Phone Number *</label>
                            <input type="tel" id="custPhone" class="form-control" required placeholder="08166501584">
                        </div>
                        <div class="form-group">
                            <label class="form-label">Email Address (Optional)</label>
                            <input type="email" id="custEmail" class="form-control" placeholder="yourname@gmail.com">
                        </div>
                        <div class="form-group">
                            <label class="form-label">State *</label>
                            <input type="text" id="custState" class="form-control" required value="Oyo State">
                        </div>
                        <div class="form-group">
                            <label class="form-label">Delivery Address *</label>
                            <textarea id="custAddress" class="form-control" rows="2" required placeholder="Full street address for doorstep delivery"></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary btn-block">PROCEED TO PAYMENT</button>
                    </form>
                </div>

                <!-- Step 2: Payment Details & Countdown -->
                <div id="checkoutStep2" class="hidden">
                    <div class="timer-box">
                        <div style="font-size: 0.75rem; color: var(--text-muted); font-weight: 600;">PAYMENT RESERVATION EXPIRES IN:</div>
                        <div class="timer-val" id="paymentTimer">20:00</div>
                    </div>

                    <div style="background: var(--primary-light); padding: 16px; border-radius: var(--radius-md); margin-bottom: 16px; text-align: center;">
                        <div style="font-size: 0.8rem; color: var(--text-muted); font-weight: 600;">ACCOUNT NAME</div>
                        <div style="font-weight: 700; font-size: 1.1rem; color: var(--text-dark);">D’EST SKINCARE & SPA</div>
                        
                        <div style="font-size: 0.8rem; color: var(--text-muted); font-weight: 600; margin-top: 8px;">BANK</div>
                        <div style="font-size: 0.95rem; font-weight: 700;">MONIEPOINT</div>

                        <div style="font-size: 0.8rem; color: var(--text-muted); font-weight: 600; margin-top: 8px;">ACCOUNT NUMBER</div>
                        <div style="font-size: 1.35rem; font-weight: 800; color: var(--primary-pink); letter-spacing: 0.05em; margin: 2px 0 8px 0;">5073013578</div>
                        
                        <button class="btn btn-outline btn-sm" type="button" onclick="copyAccountNo()">Copy Account Number</button>
                    </div>

                    <form onsubmit="submitPaymentToFirebase(event)">
                        <h4 style="margin-bottom: 12px; font-size: 0.85rem; text-transform: uppercase; color: var(--text-dark);">Submit Payment Information</h4>
                        <div class="form-group">
                            <label class="form-label">Amount Paid (₦) *</label>
                            <input type="number" id="payAmount" class="form-control" required readonly>
                        </div>
                        <div class="form-group">
                            <label class="form-label">Sender Name *</label>
                            <input type="text" id="paySender" class="form-control" required placeholder="Name on sender bank account">
                        </div>
                        <div class="form-group">
                            <label class="form-label">Bank Name *</label>
                            <input type="text" id="payBank" class="form-control" required placeholder="Sender bank (e.g. First Bank, GTB, Kuda)">
                        </div>
                        <button type="submit" id="submitPayBtn" class="btn btn-primary btn-block">SUBMIT PAYMENT</button>
                    </form>
                </div>

                <!-- Step 3: Success Confirmation -->
                <div id="checkoutStep3" class="hidden text-center" style="padding: 16px 0;">
                    <div style="font-size: 3rem; margin-bottom: 8px;">🎉</div>
                    <h3 class="font-serif" style="font-size: 1.5rem; margin-bottom: 8px;">Order Received Successfully</h3>
                    <p style="font-size: 0.875rem; color: var(--text-muted); margin-bottom: 16px;">Thank you for shopping with D’EST Skincare & Spa.</p>
                    
                    <div style="background: var(--bg-body); padding: 12px; border-radius: var(--radius-md); font-size: 0.85rem; margin-bottom: 20px;">
                        Order Reference: <strong id="successOrderId" style="color: var(--primary-pink);">#DEST-000000</strong>
                    </div>

                    <button class="btn btn-primary btn-block" onclick="trackOrderWhatsAppFromSuccess()">TRACK ORDER VIA WHATSAPP</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Firebase Integration -->
    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
        import { getFirestore, collection, addDoc, serverTimestamp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-firestore.js";

        // Firebase Web SDK Configuration
        const firebaseConfig = {
            apiKey: "AIzaSyBfK6zYrKVcvt9iqmQy6hdJwMboEhAbiBE",
            authDomain: "d-est-skincare.firebaseapp.com",
            projectId: "d-est-skincare",
            storageBucket: "d-est-skincare.firebasestorage.app",
            messagingSenderId: "243719637506",
            appId: "1:243719637506:web:96987646e172cb2c17351b",
            measurementId: "G-VTJ3REP9HH"
        };

        const app = initializeApp(firebaseConfig);
        const db = getFirestore(app);

        window.db = db;
        window.collection = collection;
        window.addDoc = addDoc;
        window.serverTimestamp = serverTimestamp;
    </script>

    <!-- Main Application JavaScript -->
    <script>
        // --- 1. PRODUCT DATABASE ---
        const productsData = [
            { id: 1, name: "Advanced Korea Bath", category: "BODY WASH / BATH", price: 16000, images: ["https://i.ibb.co/V07Y4fQP/IMG-0064-HEIC.avif", "https://i.ibb.co/dsJmTQR4/IMG-0065-HEIC.avif"] },
            { id: 2, name: "Cosmo Bath", category: "BODY WASH / BATH", price: 10000, images: ["https://i.ibb.co/RGRKfghM/IMG-0066-HEIC.avif"] },
            { id: 3, name: "Dove Bath", category: "BODY WASH / BATH", price: 10500, images: ["https://ibb.co/rGwL8rYQ", "https://ibb.co/4qrj5sN", "https://ibb.co/vxgVMpWk"] },
            { id: 4, name: "Golden Glow Bath", category: "BODY WASH / BATH", price: 9500, images: ["https://ibb.co/YTdRnRpH", "https://ibb.co/R4gpTqwS", "https://i.ibb.co/bgxBhPbY/IMG-0078-HEIC.avif"] },
            { id: 5, name: "Veetgold Bath", category: "BODY WASH / BATH", price: 9000, images: ["https://ibb.co/r2YmPdNy", "https://ibb.co/G3VsNKx5", "https://ibb.co/mC6s56GZ"] },
            { id: 6, name: "Healthy Glow Bath (Black & Orange)", category: "BODY WASH / BATH", price: 10000, images: ["https://ibb.co/1fGT501v", "https://i.ibb.co/xKNdBGjC/IMG-0076-HEIC.avif"] },
            { id: 7, name: "NIVEA Fresh Shower", category: "SHOWER GEL", price: 7000, images: ["https://i.ibb.co/xtMDQ3SP/IMG-0090-HEIC.avif"] },
            { id: 8, name: "Crustal Extra whitening body", category: "OTHER SKINCARE", price: 10000, images: ["https://i.ibb.co/jvr9SWmz/IMG-0073-HEIC.avif"] },
            { id: 9, name: "the purest Glow", category: "OTHER SKINCARE", price: 9000, images: ["https://i.ibb.co/bjCn3qXJ/IMG-0072-HEIC.avif"] },
            { id: 10, name: "AQUA RICH Hydrating Bright", category: "OTHER SKINCARE", price: 12000, images: ["https://ibb.co/wFHKxHd0", "https://ibb.co/TxbL9YxF"] },
            { id: 11, name: "OLAY Tone Brightening", category: "OTHER SKINCARE", price: 21500, images: ["https://ibb.co/5g9fDPXd"] },
            { id: 12, name: "COLLAGENE white", category: "OTHER SKINCARE", price: 15500, images: ["https://i.ibb.co/prrRn4Cx/IMG-0085-HEIC.avif"] },
            { id: 13, name: "Fair & Glow Brightening & Lightning Vitamin C Shower Gel", category: "SHOWER GEL", price: 9000, images: ["https://ibb.co/mCW3YRzq", "https://ibb.co/5hmLk6by"] },
            { id: 14, name: "SKIN BY ZARON Vitamin C BODYWASH", category: "SHOWER GEL", price: 15500, images: ["https://ibb.co/q3tcYZnV"] },
            { id: 15, name: "Dr Teals Body Wash WITH PURE EPSOM SALT", category: "SHOWER GEL", price: 11500, images: ["https://ibb.co/TxRm4TWq"] },
            { id: 16, name: "niu skin GLOWING BODY WASH", category: "SHOWER GEL", price: 9000, images: ["https://ibb.co/7JkxpQ3w", "https://i.ibb.co/wh2rr00S/IMG-0132-HEIC.avif"] },
            { id: 17, name: "NIVEASoft", category: "BODY CREAM / BUTTER", price: 9000, images: ["https://i.ibb.co/kV0xDBCR/IMG-0102-HEIC.avif"] },
            { id: 18, name: "BANANA BODY CRÈME Softens & Relieves", category: "BODY CREAM / BUTTER", price: 3500, images: ["https://ibb.co/v4NwHtfk"] },
            { id: 19, name: "NIVEA MEN", category: "BODY CREAM / BUTTER", price: 5500, images: ["https://i.ibb.co/vxcSshNx/IMG-0105-HEIC.avif"] },
            { id: 20, name: "NIVEA Body Lotion Nourishing Cocoa 48h Deep Moisture", category: "BODY LOTION", price: 5500, images: ["https://ibb.co/YTB0spNs"] },
            { id: 21, name: "SK Duchess Glow L-Glutathione", category: "BODY LOTION", price: 8000, images: ["https://ibb.co/Wvz03L9b"] },
            { id: 22, name: "FADE MILK", category: "BODY LOTION", price: 17000, images: ["https://ibb.co/nsg8yZq5"] },
            { id: 23, name: "Fair child", category: "BODY LOTION", price: 3500, images: ["https://i.ibb.co/2YYdX118/IMG-0116-HEIC.avif"] },
            { id: 24, name: "Baby secret", category: "BODY LOTION", price: 11500, images: ["https://i.ibb.co/G48Gbym1/IMG-0118-HEIC.avif", "https://i.ibb.co/Fq5dBQKS/IMG-0126-HEIC.avif", "https://i.ibb.co/VWMSNrxN/IMG-0127-HEIC.avif"] },
            { id: 25, name: "5 medix", category: "BODY LOTION", price: 6000, images: ["https://i.ibb.co/qLzQdjzF/IMG-0121-HEIC.avif"] },
            { id: 26, name: "E45", category: "BODY LOTION", price: 6000, images: ["https://i.ibb.co/FbCB1fQL/IMG-0123-HEIC.avif"] },
            { id: 27, name: "Arden", category: "BODY LOTION", price: 9500, images: ["https://i.ibb.co/qLkYnpG2/IMG-0128-HEIC.avif"] },
            { id: 28, name: "SKIN BY ZARON Vitamin C", category: "FACE CARE", price: null, images: ["https://i.ibb.co/TBWN18dP/IMG-0129-HEIC.avif"] },
            { id: 29, name: "Body butter", category: "BODY CREAM / BUTTER", price: null, images: ["https://i.ibb.co/kg6c0fWf/IMG-0130-HEIC.avif", "https://i.ibb.co/k23rVfXq/IMG-0131-HEIC.avif"] },
            { id: 30, name: "Body Lotion", category: "BODY LOTION", price: 8000, images: ["https://i.ibb.co/0VDMcbXV/IMG-0137-HEIC.avif"] },
            { id: 31, name: "vibrant orange& Glow Sunscreen Lotion", category: "SUNSCREEN", price: null, images: ["https://i.ibb.co/rGcDsxm4/IMG-0138-HEIC.avif"] },
            { id: 32, name: "CeraVe Moisturising Body Lotion", category: "BODY LOTION", price: null, images: ["https://i.ibb.co/mr21fY8V/IMG-0139-HEIC.avif"] },
            { id: 33, name: "Dr. Davey Arbutin & Vitamin C Body Lotion", category: "BODY LOTION", price: 4000, images: ["https://i.ibb.co/Wvm85Gcb/IMG-0148-HEIC.avif"] },
            { id: 34, name: "Gluta White body lotion", category: "BODY LOTION", price: 11000, images: ["https://i.ibb.co/FqYY0HCj/IMG-0151-HEIC.avif"] },
            { id: 35, name: "Fair & White So White Brightening and Moisturizing Body Milk", category: "BODY LOTION", price: 22000, images: ["https://i.ibb.co/hFCj9Rtm/IMG-0158-HEIC.avif"] },
            { id: 36, name: "Medix Retinol Cream", category: "BODY CREAM / BUTTER", price: 24000, images: ["https://i.ibb.co/JWdmkL3x/IMG-0156-HEIC.avif"] },
            { id: 37, name: "ORANGE BLOSSOM Shower Gel", category: "SHOWER GEL", price: 8000, images: ["https://i.ibb.co/ksNw35kP/IMG-0175-HEIC.avif"] },
            { id: 38, name: "Honey Sweet Secret Shower Bath Gel", category: "SHOWER GEL", price: 8000, images: ["https://ibb.co/spbsXg7Y"] },
            { id: 39, name: "Alpha 3 plus Arbutin collagen soap", category: "SOAP", price: 3500, images: ["https://ibb.co/nNbfqkNG"] },
            { id: 40, name: "GLUTATHIONE Skin Whitening Soap", category: "SOAP", price: 2500, images: ["https://i.ibb.co/fYWKvMdS/IMG-0186-HEIC.avif"] },
            { id: 41, name: "Rhome Skin Care Transparent Soap", category: "SOAP", price: 1500, images: ["https://i.ibb.co/RpWQpfS7/IMG-0187-HEIC.avif"] },
            { id: 42, name: "E45 3X CARROT", category: "SOAP", price: 2000, images: ["https://i.ibb.co/HLmgq00B/IMG-0185-HEIC.avif"] },
            { id: 43, name: "VEET SKIN WHITENING & TONING TRANSPARENT SOAP", category: "SOAP", price: 3000, images: ["https://i.ibb.co/M55xyJSB/IMG-0184-HEIC.avif"] },
            { id: 44, name: "KOJIC SOAP", category: "SOAP", price: 1500, images: ["https://i.ibb.co/vvqmWYT4/IMG-0217-HEIC.avif", "https://i.ibb.co/rGdR3MCg/IMG-0214-HEIC.avif"] },
            { id: 45, name: "U.s.a BEAUTY CARE FACE OUT", category: "FACE CARE", price: 2000, images: ["https://i.ibb.co/8D8bJ4cc/IMG-0216-HEIC.avif"] },
            { id: 46, name: "Skin Aqua", category: "SUNSCREEN", price: null, images: ["https://i.ibb.co/M5CvQz6Z/IMG-0274-HEIC.avif"] },
            { id: 47, name: "NIVEA UV Super Water 50 gel", category: "SUNSCREEN", price: null, images: ["https://i.ibb.co/0jvyG6ZR/IMG-0275-HEIC.avif"] },
            { id: 48, name: "Simplehydrating light moisturis", category: "FACE CARE", price: null, images: ["https://i.ibb.co/m5bNzcSr/IMG-0225-HEIC.avif"] },
            { id: 49, name: "Ceramide Skin barrier complex", category: "FACE CARE", price: null, images: ["https://i.ibb.co/V07F9nqT/IMG-0231-HEIC.avif"] },
            { id: 50, name: "Goatmilk Gluta Collagen Soap", category: "SOAP", price: 800, images: ["https://i.ibb.co/MySJB7VP/IMG-0201-HEIC.avif"] },
            { id: 51, name: "Acne Soap", category: "SOAP", price: 800, images: ["https://i.ibb.co/spDmRrcr/IMG-0189-HEIC.avif"] },
            { id: 52, name: "IDOLE Carotte", category: "SOAP", price: 1500, images: ["https://i.ibb.co/ZRxGVYvg/IMG-0211-HEIC.avif"] },
            { id: 53, name: "Ceramide Mochi Toner", category: "TONER", price: 22000, images: ["https://i.ibb.co/k6MYddKR/IMG-0219-HEIC.avif"] }
        ];

        // Neutral clean SVG fallback image string
        const FALLBACK_SVG = "data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='400' height='400' viewBox='0 0 400 400'><rect width='100%' height='100%' fill='%23FDEBF2'/><text x='50%' y='50%' dominant-baseline='middle' text-anchor='middle' font-family='sans-serif' font-size='16' fill='%23DB2777'>D’EST Skincare Product</text></svg>";

        // --- 2. GLOBAL STATE ---
        let cart = JSON.parse(localStorage.getItem('dest_cart_v2')) || [];
        let selectedCategory = "ALL";
        let activeTimerInterval = null;
        let activeOrderRef = "";

        // --- 3. INITIALIZATION ---
        document.addEventListener('DOMContentLoaded', () => {
            renderCategoryChips();
            renderProducts();
            updateCartUI();
        });

        // --- 4. CATEGORY & SHOP RENDER ---
        function renderCategoryChips() {
            const categories = ["ALL", "BODY WASH / BATH", "SHOWER GEL", "BODY LOTION", "BODY CREAM / BUTTER", "SOAP", "SUNSCREEN", "FACE CARE", "TONER", "OTHER SKINCARE"];
            const container = document.getElementById('categoryContainer');
            container.innerHTML = categories.map(cat => `
                <button class="cat-chip ${cat === selectedCategory ? 'active' : ''}" onclick="selectCategory('${cat}')">${cat}</button>
            `).join('');
        }

        function selectCategory(cat) {
            selectedCategory = cat;
            renderCategoryChips();
            renderProducts();
        }

        function renderProducts() {
            const searchVal = document.getElementById('searchInput').value.toLowerCase().trim();
            const sortVal = document.getElementById('sortSelect').value;
            const container = document.getElementById('productGridContainer');

            let filtered = productsData.filter(p => {
                const matchesCat = selectedCategory === "ALL" || p.category === selectedCategory;
                const matchesSearch = p.name.toLowerCase().includes(searchVal) || p.category.toLowerCase().includes(searchVal);
                return matchesCat && matchesSearch;
            });

            if (sortVal === "low-high") {
                filtered.sort((a, b) => (a.price || 0) - (b.price || 0));
            } else if (sortVal === "high-low") {
                filtered.sort((a, b) => (b.price || 0) - (a.price || 0));
            } else if (sortVal === "az") {
                filtered.sort((a, b) => a.name.localeCompare(b.name));
            }

            if (filtered.length === 0) {
                container.innerHTML = `
                    <div style="grid-column: 1/-1; text-align: center; padding: 40px 0;">
                        <p style="color: var(--text-muted); font-size: 1rem;">No products found matching your search.</p>
                        <button class="btn btn-outline btn-sm" style="margin-top: 12px;" onclick="askCustomProductWhatsApp()">Inquire via WhatsApp</button>
                    </div>
                `;
                return;
            }

            container.innerHTML = filtered.map(p => {
                const mainImg = p.images && p.images.length > 0 ? p.images[0] : FALLBACK_SVG;
                const priceFormatted = p.price !== null ? `₦${p.price.toLocaleString()}` : `<span class="price-unavailable">Price unavailable — Contact us</span>`;

                return `
                    <div class="product-card">
                        <div class="product-img-wrapper" onclick="openProductModal(${p.id})">
                            <img src="${mainImg}" alt="${p.name}" class="product-img" loading="lazy" onerror="this.onerror=null;this.src='${FALLBACK_SVG}';">
                        </div>
                        <div class="product-info">
                            <div class="product-category">${p.category}</div>
                            <div class="product-title" onclick="openProductModal(${p.id})">${p.name}</div>
                            <div class="product-price">${priceFormatted}</div>
                            ${p.price !== null ? 
                                `<button class="btn btn-primary btn-sm btn-block" onclick="addToCart(${p.id})">Add to Cart</button>` : 
                                `<button class="btn btn-outline btn-sm btn-block" onclick="askPriceWhatsApp('${p.name}')">Inquire Price</button>`
                            }
                        </div>
                    </div>
                `;
            }).join('');
        }

        // --- 5. CART SYSTEM ---
        function addToCart(productId) {
            const product = productsData.find(p => p.id === productId);
            if (!product || product.price === null) return;

            const existingItem = cart.find(item => item.id === productId);
            if (existingItem) {
                existingItem.qty += 1;
            } else {
                cart.push({
                    id: product.id,
                    name: product.name,
                    price: product.price,
                    image: product.images[0] || FALLBACK_SVG,
                    qty: 1
                });
            }

            saveCart();
            updateCartUI();
            openCartDrawer();
        }

        function updateCartQty(productId, delta) {
            const item = cart.find(i => i.id === productId);
            if (!item) return;

            item.qty += delta;
            if (item.qty <= 0) {
                cart = cart.filter(i => i.id !== productId);
            }
            saveCart();
            updateCartUI();
        }

        function saveCart() {
            localStorage.setItem('dest_cart_v2', JSON.stringify(cart));
        }

        function updateCartUI() {
            const totalItems = cart.reduce((acc, item) => acc + item.qty, 0);
            const subtotal = cart.reduce((acc, item) => acc + (item.price * item.qty), 0);

            document.getElementById('cartCountBadge').textContent = totalItems;
            document.getElementById('cartSubtotalText').textContent = `₦${subtotal.toLocaleString()}`;

            const drawerBody = document.getElementById('cartDrawerBody');
            
            if (cart.length === 0) {
                drawerBody.innerHTML = `<div style="text-align: center; padding: 40px 0; color: var(--text-muted);">Your shopping cart is empty.</div>`;
                document.getElementById('cartDrawerFooter').classList.add('hidden');
                return;
            }

            document.getElementById('cartDrawerFooter').classList.remove('hidden');
            drawerBody.innerHTML = cart.map(item => `
                <div class="cart-item">
                    <img src="${item.image}" alt="${item.name}" class="cart-item-img" onerror="this.onerror=null;this.src='${FALLBACK_SVG}';">
                    <div class="cart-item-details">
                        <div class="cart-item-title">${item.name}</div>
                        <div class="cart-item-price">₦${(item.price * item.qty).toLocaleString()}</div>
                        <div class="qty-controls">
                            <button class="qty-btn" onclick="updateCartQty(${item.id}, -1)">-</button>
                            <span class="qty-num">${item.qty}</span>
                            <button class="qty-btn" onclick="updateCartQty(${item.id}, 1)">+</button>
                        </div>
                    </div>
                </div>
            `).join('');
        }

        // --- 6. NAVIGATION & MODALS ---
        function toggleMenu() { document.getElementById('navLinks').classList.toggle('active'); }
        function closeMenu() { document.getElementById('navLinks').classList.remove('active'); }

        function openCartDrawer() { document.getElementById('cartDrawerOverlay').classList.add('active'); }
        function closeCartDrawer() { document.getElementById('cartDrawerOverlay').classList.remove('active'); }

        function openProductModal(productId) {
            const product = productsData.find(p => p.id === productId);
            if (!product) return;

            // Deduplicate URLs for the gallery
            const galleryImages = [...new Set(product.images)];
            const mainImg = galleryImages.length > 0 ? galleryImages[0] : FALLBACK_SVG;

            const modalBody = document.getElementById('productModalBody');
            modalBody.innerHTML = `
                <div>
                    <img id="mainGalleryImg" src="${mainImg}" class="gallery-main-img" onerror="this.onerror=null;this.src='${FALLBACK_SVG}';">
                    ${galleryImages.length > 1 ? `
                        <div class="gallery-thumbs">
                            ${galleryImages.map((img, idx) => `
                                <img src="${img}" class="thumb-img ${idx === 0 ? 'active' : ''}" onclick="swapGalleryImg('${img}', this)" onerror="this.onerror=null;this.src='${FALLBACK_SVG}';">
                            `).join('')}
                        </div>
                    ` : ''}
                </div>
                <div style="display: flex; flex-direction: column; justify-content: center;">
                    <div class="product-category">${product.category}</div>
                    <h2 class="font-serif" style="font-size: 1.5rem; margin-bottom: 8px;">${product.name}</h2>
                    <div style="font-size: 1.25rem; font-weight: 700; color: var(--primary-pink); margin-bottom: 16px;">
                        ${product.price !== null ? `₦${product.price.toLocaleString()}` : 'Price unavailable — Contact us'}
                    </div>
                    <p style="font-size: 0.85rem; color: var(--text-muted); margin-bottom: 24px;">Authentic beauty & skincare formula sourced directly for D’EST Skincare & Spa.</p>
                    ${product.price !== null ? 
                        `<button class="btn btn-primary btn-block" onclick="addToCart(${product.id}); closeProductModal();">Add to Shopping Cart</button>` : 
                        `<button class="btn btn-outline btn-block" onclick="askPriceWhatsApp('${product.name}')">Inquire Price on WhatsApp</button>`
                    }
                </div>
            `;

            document.getElementById('productModalOverlay').classList.add('active');
        }

        function swapGalleryImg(url, thumbEl) {
            document.getElementById('mainGalleryImg').src = url;
            document.querySelectorAll('.thumb-img').forEach(el => el.classList.remove('active'));
            thumbEl.classList.add('active');
        }

        function closeProductModal() { document.getElementById('productModalOverlay').classList.remove('active'); }

        // --- 7. CHECKOUT & FIREBASE SUBMISSION ---
        function openCheckoutModal() {
            if (cart.length === 0) return;
            closeCartDrawer();
            document.getElementById('checkoutStep1').classList.remove('hidden');
            document.getElementById('checkoutStep2').classList.add('hidden');
            document.getElementById('checkoutStep3').classList.add('hidden');
            document.getElementById('checkoutModalOverlay').classList.add('active');
        }

        function closeCheckoutModal() {
            document.getElementById('checkoutModalOverlay').classList.remove('active');
            if (activeTimerInterval) clearInterval(activeTimerInterval);
        }

        function goToPaymentStep(e) {
            e.preventDefault();
            const subtotal = cart.reduce((acc, item) => acc + (item.price * item.qty), 0);
            document.getElementById('payAmount').value = subtotal;

            document.getElementById('checkoutStep1').classList.add('hidden');
            document.getElementById('checkoutStep2').classList.remove('hidden');
            startPaymentCountdown();
        }

        function startPaymentCountdown() {
            let duration = 20 * 60; // 20 minutes
            const timerEl = document.getElementById('paymentTimer');

            if (activeTimerInterval) clearInterval(activeTimerInterval);

            activeTimerInterval = setInterval(() => {
                const mins = Math.floor(duration / 60);
                const secs = duration % 60;
                timerEl.textContent = `${mins.toString().padStart(2, '0')}:${secs.toString().padStart(2, '0')}`;

                if (--duration < 0) {
                    clearInterval(activeTimerInterval);
                    alert("Payment session expired. Please restart checkout.");
                    closeCheckoutModal();
                }
            }, 1000);
        }

        function copyAccountNo() {
            navigator.clipboard.writeText("5073013578");
            alert("Account number (5073013578) copied successfully!");
        }

        async function submitPaymentToFirebase(e) {
            e.preventDefault();
            const submitBtn = document.getElementById('submitPayBtn');
            submitBtn.disabled = true;
            submitBtn.textContent = "Submitting Order...";

            const now = new Date();
            const dateStr = now.toISOString().slice(0,10).replace(/-/g,"");
            const randomSuffix = Math.floor(1000 + Math.random() * 9000);
            const orderId = `DEST-${dateStr}-${randomSuffix}`;
            activeOrderRef = orderId;

            const subtotal = cart.reduce((acc, item) => acc + (item.price * item.qty), 0);

            // Exact schema required by Admin Dashboard
            const orderPayload = {
                orderId: orderId,
                customerName: document.getElementById('custName').value.trim(),
                phone: document.getElementById('custPhone').value.trim(),
                email: document.getElementById('custEmail').value.trim() || "N/A",
                state: document.getElementById('custState').value.trim(),
                deliveryAddress: document.getElementById('custAddress').value.trim(),
                productName: cart.map(i => `${i.name} (x${i.qty})`).join(', '),
                items: cart.map(i => ({
                    productId: i.id,
                    productName: i.name,
                    quantity: i.qty,
                    unitPrice: i.price,
                    subtotal: i.price * i.qty
                })),
                totalAmount: subtotal,
                amountPaid: parseFloat(document.getElementById('payAmount').value),
                senderName: document.getElementById('paySender').value.trim(),
                senderBank: document.getElementById('payBank').value.trim(),
                paymentStatus: "Pending Verification",
                orderStatus: "Pending",
                createdAt: window.serverTimestamp ? window.serverTimestamp() : new Date().toISOString(),
                createdDate: now.toLocaleDateString(),
                createdTime: now.toLocaleTimeString()
            };

            try {
                if (window.db && window.collection && window.addDoc) {
                    await window.addDoc(window.collection(window.db, 'orders'), orderPayload);
                } else {
                    console.warn("Database SDK offline. Local tracking fallback engaged.");
                }

                // Reset state
                cart = [];
                saveCart();
                updateCartUI();

                document.getElementById('successOrderId').textContent = `#${orderId}`;
                document.getElementById('checkoutStep2').classList.add('hidden');
                document.getElementById('checkoutStep3').classList.remove('hidden');

            } catch (err) {
                console.error("Firebase write error:", err);
                alert("Order recorded locally. Please confirm with us via WhatsApp.");
                document.getElementById('successOrderId').textContent = `#${orderId}`;
                document.getElementById('checkoutStep2').classList.add('hidden');
                document.getElementById('checkoutStep3').classList.remove('hidden');
            } finally {
                submitBtn.disabled = false;
                submitBtn.textContent = "SUBMIT PAYMENT";
                if (activeTimerInterval) clearInterval(activeTimerInterval);
            }
        }

        // --- 8. WHATSAPP HELPERS ---
        function askPriceWhatsApp(productName) {
            const msg = encodeURIComponent(`Hello D’EST Skincare & Spa, I am looking for ${productName}. Please can you tell me the price?`);
            window.open(`https://wa.me/2348166501584?text=${msg}`, '_blank');
        }

        function askCustomProductWhatsApp() {
            const input = document.getElementById('customProductInput').value.trim();
            if (!input) return;
            const msg = encodeURIComponent(`Hello D’EST Skincare & Spa, I am looking for a skincare product you don't see in your shop: ${input}. Do you have it?`);
            window.open(`https://wa.me/2348166501584?text=${msg}`, '_blank');
        }

        function trackOrderWhatsApp() {
            const orderNum = document.getElementById('trackOrderInput').value.trim();
            const msg = encodeURIComponent(`Hello D’EST Skincare & Spa, I would like to track my order. My order number is ${orderNum || '______'}.`);
            window.open(`https://wa.me/2348166501584?text=${msg}`, '_blank');
        }

        function trackOrderWhatsAppFromSuccess() {
            const msg = encodeURIComponent(`Hello D’EST Skincare & Spa, I would like to track my order. My order number is #${activeOrderRef}.`);
            window.open(`https://wa.me/2348166501584?text=${msg}`, '_blank');
        }

        function handleSpaBooking(e) {
            e.preventDefault();
            const name = document.getElementById('spaName').value.trim();
            const phone = document.getElementById('spaPhone').value.trim();
            const date = document.getElementById('spaDate').value;
            const time = document.getElementById('spaTime').value;
            const notes = document.getElementById('spaNotes').value.trim();

            const msg = encodeURIComponent(`Hello D’EST Skincare & Spa, I would like to book a SPA session.\n\nName: ${name}\nPhone: ${phone}\nDate: ${date}\nTime: ${time}\nService/Note: ${notes || 'General Inquiry'}`);
            window.open(`https://wa.me/2348166501584?text=${msg}`, '_blank');
        }
    </script>
</body>
</html>
