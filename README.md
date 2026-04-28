<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARCA ENERGIES S.A. | Distribuidor Autorizado Invertek • Schrack • Murr en Ecuador</title>
    <meta name="description" content="ARCA ENERGIES S.A. - Distribuidor autorizado de variadores de frecuencia Invertek, protecciones Schrack Technik y automatización Murr Elektronik en Ecuador. Ahorro energético hasta 30%.">
    <meta name="keywords" content="variadores de frecuencia Ecuador, Invertek Drives distribuidor, protecciones eléctricas Schrack Ecuador, automatización industrial Quito, Murr Elektronik Ecuador, arrancadores suaves, relés industriales">
    <link href="https://cdn.jsdelivr.net/npm/fontsource-roboto@4.0.0/index.css" rel="stylesheet">
    <link href="https://cdn.jsdelivr.net/npm/fontsource-montserrat@4.0.0/index.css" rel="stylesheet">
    <style>
        :root {
            --gray: #656C70;
            --gray-light: #f0f2f3;
            --gray-lighter: #e8eaec;
            --gray-dark: #4a5053;
            --white: #FFFFFF;
            --green: #2EB72E;
            --green-light: #e6f9e6;
            --green-dark: #249a24;
            --blue: #084D9C;
            --blue-light: #e8f0fa;
            --blue-dark: #063d7e;
            --whatsapp: #25D366;
            --shadow-sm: 0 2px 8px rgba(8,77,156,0.08);
            --shadow-md: 0 4px 20px rgba(8,77,156,0.12);
            --shadow-lg: 0 8px 40px rgba(8,77,156,0.16);
        }
       * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        body {
            font-family: 'Roboto', sans-serif;
            background: var(--white);
            color: var(--gray);
            overflow-x: hidden;
            line-height: 1.7;
        }
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: var(--gray-light); }
        ::-webkit-scrollbar-thumb { background: var(--blue); border-radius: 4px; }
        /* ===== NAVIGATION ===== */
        .navbar {
            position: fixed;
            top: 0; left: 0; right: 0;
            z-index: 1000;
            padding: 0.8rem 2rem;
            transition: all 0.4s ease;
            background: rgba(255,255,255,0.97);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid transparent;
        }
        .navbar.scrolled {
            padding: 0.5rem 2rem;
            border-bottom: 1px solid var(--gray-lighter);
            box-shadow: var(--shadow-sm);
        }
        .nav-container {
            max-width: 1300px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .nav-logo {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            text-decoration: none;
        }
        .nav-logo-text {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.3rem;
            font-weight: 800;
            color: var(--blue);
            letter-spacing: 1px;
        }
        .nav-logo-text span { color: var(--green); }
        .nav-slogan {
            font-size: 0.65rem;
            color: var(--gray);
            font-style: italic;
            display: block;
            margin-top: -2px;
        }
        .nav-links {
            display: flex;
            list-style: none;
            gap: 1.8rem;
            align-items: center;
        }
        .nav-links a {
            color: var(--gray);
            text-decoration: none;
            font-size: 0.88rem;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -4px; left: 0;
            width: 0; height: 2px;
            background: var(--green);
            transition: width 0.3s;
        }
        .nav-links a:hover { color: var(--blue); }
        .nav-links a:hover::after { width: 100%; }
        .nav-cta {
            background: var(--blue) !important;
            color: var(--white) !important;
            padding: 0.6rem 1.5rem;
            border-radius: 50px;
            font-weight: 600 !important;
            border: none;
            cursor: pointer;
            transition: all 0.3s !important;
        }
        .nav-cta:hover {
            background: var(--blue-dark) !important;
            transform: translateY(-2px);
            box-shadow: var(--shadow-md);
        }
        .nav-cta::after { display: none !important; }
        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 5px;
        }
        .hamburger span {
            width: 28px; height: 2px;
            background: var(--gray);
            transition: all 0.3s;
        }
        .hamburger.active span:nth-child(1) { transform: rotate(45deg) translate(5px, 5px); }
        .hamburger.active span:nth-child(2) { opacity: 0; }
        .hamburger.active span:nth-child(3) { transform: rotate(-45deg) translate(5px, -5px); }
        /* ===== HERO SECTION ===== */
        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            overflow: hidden;
            background: linear-gradient(135deg, var(--white) 0%, var(--blue-light) 40%, var(--green-light) 100%);
        }
        #heroCanvas {
            position: absolute;
            top: 0; left: 0;
            width: 100%; height: 100%;
            z-index: 1;
        }
        .hero-content {
            position: relative;
            z-index: 3;
            max-width: 1300px;
            margin: 0 auto;
            padding: 7rem 2rem 3rem;
            display: grid;
            grid-template-columns: 1.1fr 0.9fr;
            gap: 4rem;
            align-items: center;
        }
        .hero-text { animation: slideInLeft 0.8s ease both; }
        @keyframes slideInLeft {
            from { opacity: 0; transform: translateX(-40px); }
            to { opacity: 1; transform: translateX(0); }
        }
        @keyframes slideInRight {
            from { opacity: 0; transform: translateX(40px); }
            to { opacity: 1; transform: translateX(0); }
        }
        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: var(--blue-light);
            border: 1px solid rgba(8,77,156,0.2);
            padding: 0.4rem 1.2rem;
            border-radius: 50px;
            font-size: 0.82rem;
            color: var(--blue);
            font-weight: 600;
            margin-bottom: 1.2rem;
        }
        .badge-dot {
            width: 8px; height: 8px;
            background: var(--green);
            border-radius: 50%;
            animation: pulse-dot 2s infinite;
        }
        @keyframes pulse-dot {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.5; transform: scale(1.5); }
        }
        .hero-title {
            font-family: 'Montserrat', sans-serif;
            font-size: clamp(2rem, 4.5vw, 3rem);
            font-weight: 800;
            line-height: 1.15;
            margin-bottom: 0.8rem;
            color: var(--gray-dark);
        }
        .hero-title .highlight { color: var(--blue); }
        .hero-title .highlight-green { color: var(--green); }
        .hero-slogan {
            font-size: 1.05rem;
            color: var(--blue);
            font-style: italic;
            font-weight: 500;
            margin-bottom: 0.8rem;
        }
        .hero-subtitle {
            font-size: 1rem;
            color: var(--gray);
            margin-bottom: 0.5rem;
        }
        .hero-brands {
            font-size: 0.9rem;
            color: var(--gray);
            margin-bottom: 2rem;
        }
        .hero-brands strong { color: var(--blue); }
        .hero-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            margin-bottom: 2rem;
        }
        .btn-primary {
            background: var(--blue);
            color: var(--white);
            padding: 0.9rem 2rem;
            border-radius: 50px;
            font-size: 0.95rem;
            font-weight: 600;
            text-decoration: none;
            border: none;
            cursor: pointer;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }
        .btn-primary:hover {
            background: var(--blue-dark);
            transform: translateY(-3px);
            box-shadow: var(--shadow-lg);
        }
        .btn-whatsapp {
            background: var(--green);
            color: var(--white);
            padding: 0.9rem 2rem;
            border-radius: 50px;
            font-size: 0.95rem;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        .btn-whatsapp:hover {
            background: var(--green-dark);
            transform: translateY(-3px);
            box-shadow: var(--shadow-md);
        }
        .hero-features {
            display: flex;
            gap: 1.5rem;
            flex-wrap: wrap;
        }
        .hero-feature-item {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-size: 0.88rem;
            color: var(--gray-dark);
            font-weight: 500;
        }
       .hero-feature-item svg { color: var(--green); flex-shrink: 0; }
        .hero-visual {
            animation: slideInRight 0.8s ease 0.2s both;
        }
        .hero-visual-card {
            background: var(--white);
            border-radius: 20px;
            box-shadow: var(--shadow-lg);
            padding: 1.5rem;
            border: 1px solid var(--gray-lighter);
            position: relative;
            overflow: hidden;
        }
        .hero-visual-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--blue), var(--green));
        }
        .hero-product-img {
            width: 100%;
            height: 280px;
            object-fit: contain;
            border-radius: 12px;
            background: #f8f9fa;
            margin-bottom: 1rem;
        }
        .hero-visual-card h3 {
            text-align: center;
            font-family: 'Montserrat', sans-serif;
            font-size: 1rem;
            color: var(--gray-dark);
            margin-bottom: 0.2rem;
        }
        .hero-visual-card > p {
            text-align: center;
            color: var(--gray);
            font-size: 0.82rem;
            margin-bottom: 1rem;
        }
        .visual-stats {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 0.6rem;
        }
        .visual-stat {
            text-align: center;
            padding: 0.7rem 0.4rem;
            background: var(--gray-light);
            border-radius: 10px;
        }
        .visual-stat-val {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.2rem;
            font-weight: 800;
            color: var(--blue);
        }
        .visual-stat-val.green { color: var(--green); }
        .visual-stat-label {
            font-size: 0.65rem;
            color: var(--gray);
            margin-top: 0.2rem;
        }
        /* ===== MARQUEE BRANDS ===== */
        .brands-marquee {
            background: var(--gray-light);
            padding: 1.5rem 0;
            overflow: hidden;
            border-top: 1px solid var(--gray-lighter);
            border-bottom: 1px solid var(--gray-lighter);
        }
        .marquee-track {
            display: flex;
            gap: 4rem;
            animation: marquee 25s linear infinite;
            width: max-content;
        }
        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }
        .marquee-item {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--gray);
            opacity: 0.4;
            white-space: nowrap;
            display: flex;
            align-items: center;
            gap: 0.8rem;
        }
        .marquee-item span {
            color: var(--blue);
            opacity: 0.6;
        }
        /* ===== SECTION STYLES ===== */
        .section {
            padding: 5rem 2rem;
            max-width: 1300px;
            margin: 0 auto;
        }
        .section-header {
            text-align: center;
            margin-bottom: 3.5rem;
        }
        .section-tag {
            font-family: 'Montserrat', sans-serif;
            font-size: 0.72rem;
            color: var(--blue);
            text-transform: uppercase;
            letter-spacing: 3px;
            font-weight: 700;
            margin-bottom: 0.8rem;
        }
        .section-title {
            font-family: 'Montserrat', sans-serif;
            font-size: clamp(1.8rem, 3.5vw, 2.4rem);
            font-weight: 800;
            color: var(--gray-dark);
            margin-bottom: 1rem;
        }
        .section-title .highlight { color: var(--blue); }
        .section-title .highlight-green { color: var(--green); }
        .section-desc {
            color: var(--gray);
            max-width: 650px;
            margin: 0 auto;
            font-size: 1rem;
        }
        /* ===== BENEFITS ===== */
        .benefits-section {
            background: var(--gray-light);
            padding: 5rem 2rem;
        }
        .benefits-container { max-width: 1300px; margin: 0 auto; }
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 1.5rem;
        }
        .benefit-card {
            background: var(--white);
            border-radius: 16px;
            padding: 2rem;
            transition: all 0.4s ease;
            border: 1px solid var(--gray-lighter);
            position: relative;
            overflow: hidden;
        }
        .benefit-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0;
            width: 4px; height: 0;
            background: var(--green);
            transition: height 0.4s ease;
        }
        .benefit-card:hover {
            transform: translateY(-6px);
            box-shadow: var(--shadow-md);
            border-color: rgba(46,183,46,0.2);
        }
        .benefit-card:hover::before { height: 100%; }
        .benefit-icon {
            width: 52px; height: 52px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1rem;
            background: var(--blue-light);
        }
        .benefit-icon.green-bg { background: var(--green-light); }
        .benefit-icon svg { width: 26px; height: 26px; }
        .benefit-icon svg.blue { color: var(--blue); }
        .benefit-icon svg.green { color: var(--green); }
        .benefit-card h3 {
            font-size: 1.05rem;
            font-weight: 700;
            color: var(--gray-dark);
            margin-bottom: 0.5rem;
        }
        .benefit-card p {
            color: var(--gray);
            font-size: 0.9rem;
            line-height: 1.6;
        }
        /* ===== PRODUCTS ===== */
        .products-section {
            padding: 5rem 2rem;
            max-width: 1300px;
            margin: 0 auto;
        }
        .products-tabs {
            display: flex;
            justify-content: center;
            gap: 0.5rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }
        .tab-btn {
            padding: 0.7rem 1.8rem;
            border: 2px solid var(--gray-lighter);
            background: var(--white);
            color: var(--gray);
            border-radius: 50px;
            cursor: pointer;
            font-size: 0.88rem;
            font-weight: 600;
            transition: all 0.3s;
            font-family: 'Montserrat', sans-serif;
        }
        .tab-btn.active, .tab-btn:hover {
            background: var(--blue);
            color: var(--white);
            border-color: var(--blue);
        }
        .product-showcase {
            display: none;
        }
        .product-showcase.active {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
            animation: fadeIn 0.5s ease;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .product-image-container {
            position: relative;
            border-radius: 20px;
            overflow: hidden;
            aspect-ratio: 4/3;
            background: var(--gray-light);
            border: 1px solid var(--gray-lighter);
       }
        .product-image-container img {
            width: 100%; height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        .product-image-container:hover img {
            transform: scale(1.05);
        }
        .product-brand-badge {
            display: inline-block;
            padding: 0.3rem 1rem;
            border-radius: 50px;
            font-size: 0.72rem;
            font-weight: 700;
        }
        .badge-invertek { background: var(--blue-light); color: var(--blue); }
        .badge-schrack { background: #f3e8ff; color: #7c3aed; }
        .badge-murr { background: var(--green-light); color: var(--green); }
        .product-info h3 {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--gray-dark);
            margin-bottom: 0.8rem;
        }
        .product-info p {
            color: var(--gray);
            margin-bottom: 1.5rem;
            line-height: 1.7;
        }
        .product-features-list {
            list-style: none;
            margin-bottom: 2rem;
        }
        .product-features-list li {
            display: flex;
            align-items: center;
            gap: 0.7rem;
            padding: 0.4rem 0;
            color: var(--gray-dark);
            font-size: 0.92rem;
        }
       .product-features-list li svg { color: var(--green); flex-shrink: 0; }
        .product-specs {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0.8rem;
            margin-bottom: 1.5rem;
        }
        .spec-item {
            background: var(--gray-light);
            border-radius: 10px;
            padding: 0.8rem 1rem;
        }
        .spec-label {
            font-size: 0.7rem;
            color: var(--gray);
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        .spec-value {
            font-weight: 700;
            color: var(--gray-dark);
            font-size: 0.95rem;
        }
        /* ===== CAROUSEL ===== */
        .carousel-section { margin-top: 4rem; }
        .carousel-wrapper {
            position: relative;
            overflow: hidden;
            border-radius: 16px;
        }
        .carousel-track {
            display: flex;
            transition: transform 0.5s ease;
            gap: 1.5rem;
        }
        .carousel-item {
            min-width: 280px;
            background: var(--white);
            border: 1px solid var(--gray-lighter);
            border-radius: 16px;
            overflow: hidden;
            transition: all 0.3s;
        }
        .carousel-item:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-md);
        }
        .carousel-img {
            width: 100%; height: 200px;
            background: var(--gray-light);
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }
        .carousel-img img {
            width: 100%; height: 100%;
            object-fit: cover;
        }
        .carousel-content { padding: 1.3rem; }
        .carousel-content h4 { font-size: 0.92rem; color: var(--gray-dark); margin-bottom: 0.3rem; font-weight: 700; }
        .carousel-content p { color: var(--gray); font-size: 0.82rem; }
        .carousel-controls {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 1.5rem;
        }
       .carousel-btn {
            width: 44px; height: 44px;
            border-radius: 50%;
            border: 2px solid var(--gray-lighter);
            background: var(--white);
            color: var(--gray);
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }
        .carousel-btn:hover {
            background: var(--blue);
            border-color: var(--blue);
            color: var(--white);
        }
        /* ===== STATS ===== */
        .stats-section {
            padding: 4rem 2rem;
            background: var(--blue);
            position: relative;
            overflow: hidden;
        }
       .stats-section::before {
            content: '';
            position: absolute;
            top: -50%; right: -20%;
            width: 500px; height: 500px;
            background: radial-gradient(circle, rgba(46,183,46,0.15) 0%, transparent 70%);
            border-radius: 50%;
        }
        .stats-container { max-width: 1300px; margin: 0 auto; position: relative; z-index: 1; }
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }
        .stat-card {
            text-align: center;
            padding: 2rem 1.5rem;
            background: rgba(255,255,255,0.1);
            border-radius: 16px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.15);
        }
        .stat-number {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--white);
        }

        .stat-label {
            color: rgba(255,255,255,0.8);
            font-size: 0.92rem;
            margin-top: 0.5rem;
        }

        /* ===== SERVICES ===== */
        .services-section {
            padding: 5rem 2rem;
            background: var(--gray-light);
        }

        .services-container { max-width: 1300px; margin: 0 auto; }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: var(--white);
            border-radius: 16px;
            overflow: hidden;
            border: 1px solid var(--gray-lighter);
            transition: all 0.3s;
        }

        .service-card:hover {
            box-shadow: var(--shadow-md);
            transform: translateY(-4px);
        }

        .service-img {
            width: 100%;
            height: 220px;
            object-fit: cover;
        }

        .service-content {
            padding: 1.5rem;
        }

        .service-content h3 {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.1rem;
            font-weight: 700;
            color: var(--gray-dark);
            margin-bottom: 0.5rem;
        }

        .service-content p {
            color: var(--gray);
            font-size: 0.9rem;
            line-height: 1.6;
        }

        /* ===== TESTIMONIALS ===== */
        .testimonials-section {
            padding: 5rem 2rem;
            background: var(--white);
        }

        .testimonials-container { max-width: 1300px; margin: 0 auto; }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(330px, 1fr));
            gap: 2rem;
        }

        .testimonial-card {
            background: var(--gray-light);
            border-radius: 16px;
            padding: 2rem;
            border: 1px solid var(--gray-lighter);
            transition: all 0.3s;
        }

        .testimonial-card:hover {
            box-shadow: var(--shadow-sm);
            transform: translateY(-4px);
        }

        .testimonial-quote {
            font-size: 3rem;
            color: var(--blue);
            opacity: 0.15;
            position: absolute;
            top: 0.8rem; right: 1.5rem;
            font-family: Georgia, serif;
        }

        .testimonial-card { position: relative; }

        .testimonial-stars { display: flex; gap: 0.2rem; margin-bottom: 1rem; }
        .testimonial-stars svg { color: #fbbf24; }

        .testimonial-text {
            color: var(--gray);
            font-style: italic;
            line-height: 1.7;
            margin-bottom: 1.5rem;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .testimonial-avatar {
            width: 48px; height: 48px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--blue), var(--green));
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 1.1rem;
            color: var(--white);
        }

        .testimonial-name { font-weight: 700; color: var(--gray-dark); }
        .testimonial-role { font-size: 0.82rem; color: var(--gray); }

        /* ===== ABOUT ===== */
        .about-section {
            padding: 5rem 2rem;
            max-width: 1300px;
            margin: 0 auto;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-image {
            position: relative;
            border-radius: 20px;
            overflow: hidden;
            aspect-ratio: 4/3;
            background: var(--gray-light);
            border: 1px solid var(--gray-lighter);
        }

        .about-image img {
            width: 100%; height: 100%;
            object-fit: cover;
        }

        .about-image::after {
            content: '';
            position: absolute;
            bottom: 0; left: 0; right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--blue), var(--green));
        }

        .about-content h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.9rem;
            font-weight: 800;
            color: var(--gray-dark);
            margin-bottom: 1.2rem;
        }

        .about-content h2 .highlight { color: var(--blue); }
        .about-content h2 .highlight-green { color: var(--green); }

        .about-content p {
            color: var(--gray);
            margin-bottom: 1rem;
            line-height: 1.7;
        }

        .about-highlights {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .about-highlight {
            display: flex;
            align-items: center;
            gap: 0.7rem;
            padding: 0.9rem;
            background: var(--gray-light);
            border-radius: 10px;
            border: 1px solid var(--gray-lighter);
        }

        .about-highlight svg { color: var(--green); flex-shrink: 0; }
        .about-highlight span { font-size: 0.88rem; font-weight: 600; color: var(--gray-dark); }

        /* ===== CTA BANNER ===== */
        .cta-banner {
            background: linear-gradient(135deg, var(--blue) 0%, var(--blue-dark) 100%);
            padding: 4rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .cta-banner::before {
            content: '';
            position: absolute;
            top: -50%; left: -20%;
            width: 400px; height: 400px;
            background: radial-gradient(circle, rgba(46,183,46,0.2) 0%, transparent 70%);
            border-radius: 50%;
        }

        .cta-banner h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: clamp(1.5rem, 3vw, 2.2rem);
            font-weight: 800;
            color: var(--white);
            margin-bottom: 0.8rem;
            position: relative;
            z-index: 1;
        }

        .cta-banner p {
            color: rgba(255,255,255,0.8);
            margin-bottom: 2rem;
            font-size: 1.05rem;
            position: relative;
            z-index: 1;
        }

        .cta-banner .btn-whatsapp {
            font-size: 1.05rem;
            padding: 1rem 2.5rem;
            position: relative;
            z-index: 1;
        }

        /* ===== CONTACT ===== */
        .contact-section {
            padding: 5rem 2rem;
            background: var(--gray-light);
        }

        .contact-container { max-width: 1300px; margin: 0 auto; }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .contact-form {
            background: var(--white);
            border-radius: 20px;
            padding: 2.5rem;
            border: 1px solid var(--gray-lighter);
            box-shadow: var(--shadow-sm);
        }

        .form-group { margin-bottom: 1.3rem; }

        .form-group label {
            display: block;
            margin-bottom: 0.4rem;
            font-weight: 600;
            font-size: 0.82rem;
            color: var(--gray-dark);
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem 1.1rem;
            background: var(--gray-light);
            border: 2px solid var(--gray-lighter);
            border-radius: 10px;
            color: var(--gray-dark);
            font-size: 0.92rem;
            font-family: 'Roboto', sans-serif;
            transition: border-color 0.3s, box-shadow 0.3s;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--blue);
            box-shadow: 0 0 0 3px rgba(8,77,156,0.1);
        }

        .form-group textarea {
            min-height: 110px;
            resize: vertical;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        .form-submit {
            width: 100%;
            padding: 1rem;
            background: var(--green);
            color: var(--white);
            border: none;
            border-radius: 10px;
            font-size: 1rem;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
            font-family: 'Montserrat', sans-serif;
        }

        .form-submit:hover {
            background: var(--green-dark);
            transform: translateY(-2px);
            box-shadow: var(--shadow-md);
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1.2rem;
        }

        .contact-info-card {
            display: flex;
            align-items: flex-start;
            gap: 1.2rem;
            padding: 1.3rem;
            background: var(--white);
            border: 1px solid var(--gray-lighter);
            border-radius: 14px;
            transition: all 0.3s;
        }

        .contact-info-card:hover {
            box-shadow: var(--shadow-sm);
            border-color: rgba(8,77,156,0.2);
        }

        .contact-icon {
            width: 44px; height: 44px;
            border-radius: 10px;
            background: var(--blue-light);
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
        }

        .contact-icon.green-bg { background: var(--green-light); }

        .contact-icon svg { color: var(--blue); }
        .contact-icon.green-bg svg { color: var(--green); }

        .contact-detail h4 {
            font-size: 0.92rem;
            color: var(--gray-dark);
            margin-bottom: 0.2rem;
        }

        .contact-detail p, .contact-detail a {
            color: var(--gray);
            font-size: 0.88rem;
            text-decoration: none;
            transition: color 0.3s;
        }

        .contact-detail a:hover { color: var(--blue); }

        .contact-map {
            border-radius: 14px;
            overflow: hidden;
            border: 1px solid var(--gray-lighter);
            height: 180px;
            background: var(--gray-light);
        }

        .contact-map iframe {
            width: 100%; height: 100%;
            border: none;
        }

        /* ===== FOOTER ===== */
        .footer {
            background: var(--gray-dark);
            padding: 4rem 2rem 2rem;
            color: rgba(255,255,255,0.7);
        }

        .footer-container { max-width: 1300px; margin: 0 auto; }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-brand .nav-logo-text { color: var(--white); }

        .footer-brand p {
            margin-top: 0.8rem;
            font-size: 0.88rem;
            line-height: 1.6;
            color: rgba(255,255,255,0.5);
        }

        .footer-social {
            display: flex;
            gap: 0.8rem;
            margin-top: 1.2rem;
        }

        .social-link {
            width: 36px; height: 36px;
            border-radius: 10px;
            background: rgba(255,255,255,0.08);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
            text-decoration: none;
        }

        .social-link:hover {
            background: var(--green);
            transform: translateY(-3px);
        }

        .social-link svg { color: rgba(255,255,255,0.6); transition: color 0.3s; }
        .social-link:hover svg { color: var(--white); }

        .footer-col h4 {
            font-size: 0.95rem;
            margin-bottom: 1rem;
            color: var(--white);
            position: relative;
            padding-bottom: 0.7rem;
        }

        .footer-col h4::after {
            content: '';
            position: absolute;
            bottom: 0; left: 0;
            width: 30px; height: 2px;
            background: var(--green);
        }

        .footer-col ul { list-style: none; }
        .footer-col ul li { margin-bottom: 0.5rem; }

        .footer-col ul a {
            color: rgba(255,255,255,0.5);
            text-decoration: none;
            font-size: 0.88rem;
            transition: color 0.3s;
        }

        .footer-col ul a:hover { color: var(--green); }

        .footer-bottom {
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .footer-bottom p {
            font-size: 0.82rem;
            color: rgba(255,255,255,0.4);
        }

        /* ===== WHATSAPP FLOAT ===== */
        .whatsapp-float {
            position: fixed;
            bottom: 2rem; right: 2rem;
            z-index: 999;
            width: 60px; height: 60px;
            border-radius: 50%;
            background: var(--whatsapp);
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 8px 25px rgba(37,211,102,0.4);
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            animation: pulse-wa 2s infinite;
        }

        .whatsapp-float:hover { transform: scale(1.1); }

        @keyframes pulse-wa {
            0% { box-shadow: 0 0 0 0 rgba(37,211,102,0.5); }
            70% { box-shadow: 0 0 0 20px rgba(37,211,102,0); }
            100% { box-shadow: 0 0 0 0 rgba(37,211,102,0); }
        }

        /* ===== TOAST ===== */
        .toast {
            position: fixed;
            top: 100px; right: 2rem;
            background: var(--white);
            border: 2px solid var(--green);
            border-radius: 12px;
            padding: 1rem 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.8rem;
            z-index: 9999;
            transform: translateX(120%);
            transition: transform 0.4s ease;
            box-shadow: var(--shadow-lg);
        }

        .toast.show { transform: translateX(0); }
        .toast svg { color: var(--green); }
        .toast span { color: var(--gray-dark); font-weight: 500; }

        /* ===== SCROLL REVEAL ===== */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.7s ease;
        }

        .reveal.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 1024px) {
            .hero-content { grid-template-columns: 1fr; text-align: center; }
            .hero-features { justify-content: center; }
            .hero-buttons { justify-content: center; }
            .hero-visual { order: -1; }
            .hero-visual-card { max-width: 400px; margin: 0 auto; }
            .product-showcase.active { grid-template-columns: 1fr; }
            .about-grid { grid-template-columns: 1fr; }
            .contact-grid { grid-template-columns: 1fr; }
            .footer-grid { grid-template-columns: 1fr 1fr; }
            .stats-grid { grid-template-columns: repeat(2, 1fr); }
        }

        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 0; right: -100%;
                width: 80%;
                max-width: 350px;
                height: 100vh;
                background: var(--white);
                flex-direction: column;
                justify-content: center;
                padding: 2rem;
                transition: right 0.4s ease;
                border-left: 1px solid var(--gray-lighter);
                box-shadow: var(--shadow-lg);
            }
            .nav-links.open { right: 0; }
            .hamburger { display: flex; }
            .form-row { grid-template-columns: 1fr; }
            .footer-grid { grid-template-columns: 1fr; }
            .testimonials-grid { grid-template-columns: 1fr; }
            .about-highlights { grid-template-columns: 1fr; }
            .carousel-item { min-width: 250px; }
            .footer-bottom { flex-direction: column; text-align: center; }
            .stats-grid { grid-template-columns: 1fr 1fr; }
            .product-specs { grid-template-columns: 1fr; }
        }

        @media (max-width: 480px) {
            .hero-buttons { flex-direction: column; align-items: center; }
            .btn-primary, .btn-whatsapp { width: 100%; justify-content: center; }
            .visual-stats { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <!-- ===== NAVIGATION ===== -->
    <nav class="navbar" id="navbar">
        <div class="nav-container">
            <a href="#" class="nav-logo">
                <svg viewBox="0 0 45 45" fill="none" width="42" height="42">
                    <rect x="2" y="2" width="41" height="41" rx="10" stroke="#084D9C" stroke-width="2.5"/>
                    <path d="M14 28L22.5 14L31 28H14Z" fill="none" stroke="#084D9C" stroke-width="2" stroke-linejoin="round"/>
                    <line x1="22.5" y1="20" x2="22.5" y2="26" stroke="#2EB72E" stroke-width="2.5" stroke-linecap="round"/>
                </svg>
                <div>
                    <span class="nav-logo-text">ARCA <span>ENERGIES</span></span>
                    <span class="nav-slogan">Navegamos hacia la innovación</span>
                </div>
            </a>
            <ul class="nav-links" id="navLinks">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#beneficios">Beneficios</a></li>
                <li><a href="#productos">Productos</a></li>
                <li><a href="#servicios">Servicios</a></li>
                <li><a href="#nosotros">Nosotros</a></li>
                <li><a href="#contacto">Contacto</a></li>
                <li><a href="#contacto" class="nav-cta">Cotizar Ahora</a></li>
            </ul>
            <div class="hamburger" id="hamburger" onclick="toggleMenu()">
                <span></span><span></span><span></span>
            </div>
        </div>
    </nav>

    <!-- ===== HERO SECTION ===== -->
    <section class="hero" id="inicio">
        <canvas id="heroCanvas"></canvas>
        <div class="hero-content">
            <div class="hero-text">
                <div class="hero-badge">
                    <span class="badge-dot"></span>
                    Distribuidor Autorizado Ecuador
                </div>
                <h1 class="hero-title">
                    Variadores de Frecuencia,<br>
                    <span class="highlight">Protección</span> y
                    <span class="highlight-green">Automatización</span>
                </h1>
                <p class="hero-slogan">"Protección europea para tu industria ecuatoriana"</p>
                <p class="hero-subtitle">Las mejores marcas europeas para optimizar tu producción industrial</p>
                <p class="hero-brands">Distribuidor Autorizado <strong>Invertek Drives</strong> • <strong>Schrack Technik</strong> • <strong>Murr Elektronik</strong></p>
                <div class="hero-buttons">
                    <a href="#contacto" class="btn-primary">
                        <svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"/></svg>
                        Cotiza tu Variador Ahora
                    </a>
                    <a href="https://wa.me/593992567537?text=Hola%20ARCA%20ENERGIES%2C%20deseo%20información%20sobre%20sus%20productos" target="_blank" class="btn-whatsapp">
                        <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
                        WhatsApp Directo
                    </a>
                </div>
                <div class="hero-features">
                    <div class="hero-feature-item">
                        <svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>
                        Ahorro energético hasta 30%
                    </div>
                    <div class="hero-feature-item">
                        <svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>
                        Mayor vida útil de motores
                    </div>
                    <div class="hero-feature-item">
                        <svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>
                        Arranque suave
                    </div>
                </div>
            </div>
            <div class="hero-visual">
                <div class="hero-visual-card">
                    <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/18a6a72e6-5c10-4465-9155-7daf2083b573.png" alt="Invertek OPTIDRIVE E3 Variador de Frecuencia" class="hero-product-img">
                    <h3>OPTIDRIVE E³ – Invertek Drives</h3>
                    <p>Variador de frecuencia trifásico de alto rendimiento</p>
                    <div class="visual-stats">
                        <div class="visual-stat">
                            <div class="visual-stat-val">30%</div>
                            <div class="visual-stat-label">Ahorro</div>
                        </div>
                        <div class="visual-stat">
                            <div class="visual-stat-val green">IP66</div>
                            <div class="visual-stat-label">Protección</div>
                        </div>
                        <div class="visual-stat">
                            <div class="visual-stat-val">CE</div>
                            <div class="visual-stat-label">Certificado</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== BRANDS MARQUEE ===== -->
    <div class="brands-marquee">
        <div class="marquee-track">
            <div class="marquee-item"><span>●</span> INVERTEK DRIVES</div>
            <div class="marquee-item"><span>●</span> SCHRACK TECHNIK</div>
            <div class="marquee-item"><span>●</span> MURR ELEKTRONIK</div>
            <div class="marquee-item"><span>●</span> VARIADORES DE FRECUENCIA</div>
            <div class="marquee-item"><span>●</span> PROTECCIONES ELÉCTRICAS</div>
            <div class="marquee-item"><span>●</span> AUTOMATIZACIÓN INDUSTRIAL</div>
            <div class="marquee-item"><span>●</span> INVERTEK DRIVES</div>
            <div class="marquee-item"><span>●</span> SCHRACK TECHNIK</div>
            <div class="marquee-item"><span>●</span> MURR ELEKTRONIK</div>
            <div class="marquee-item"><span>●</span> VARIADORES DE FRECUENCIA</div>
            <div class="marquee-item"><span>●</span> PROTECCIONES ELÉCTRICAS</div>
            <div class="marquee-item"><span>●</span> AUTOMATIZACIÓN INDUSTRIAL</div>
        </div>
    </div>

    <!-- ===== BENEFITS ===== -->
    <section class="benefits-section" id="beneficios">
        <div class="benefits-container">
            <div class="section-header reveal">
                <p class="section-tag">¿Por qué elegirnos?</p>
                <h2 class="section-title">Beneficios de <span class="highlight">ARCA ENERGIES</span></h2>
                <p class="section-desc">Soluciones industriales con tecnología europea, asesoría personalizada y soporte técnico nacional en Ecuador.</p>
            </div>
            <div class="benefits-grid">
                <div class="benefit-card reveal">
                    <div class="benefit-icon">
                        <svg class="blue" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M13 10V3L4 14h7v7l9-11h-7z"/></svg>
                    </div>
                    <h3>Control de Velocidad y Ahorro</h3>
                    <p>Reduce el consumo energético de tus motores hasta un 30% con variadores de frecuencia de última generación europea.</p>
                </div>
                <div class="benefit-card reveal">
                    <div class="benefit-icon green-bg">
                        <svg class="green" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"/></svg>
                    </div>
                    <h3>Protección Contra Sobrecargas</h3>
                    <p>Protege tus instalaciones con breakers, relés y sistemas anti-arco certificados con estándares europeos VDE y CE.</p>
                </div>
                <div class="benefit-card reveal">
                    <div class="benefit-icon">
                        <svg class="blue" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 5a1 1 0 011-1h14a1 1 0 011 1v2a1 1 0 01-1 1H5a1 1 0 01-1-1V5zM4 13a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H5a1 1 0 01-1-1v-6zM16 13a1 1 0 011-1h2a1 1 0 011 1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-6z"/></svg>
                    </div>
                    <h3>Automatización Confiable</h3>
                    <p>Sistemas de automatización industrial Murr Elektronik con tecnología IO-Link para optimizar procesos productivos.</p>
                </div>
                <div class="benefit-card reveal">
                    <div class="benefit-icon green-bg">
                        <svg class="green" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"/></svg>
                    </div>
                    <h3>Asesoría Técnica Gratuita</h3>
                    <p>Equipo técnico especializado disponible para asesorarte en la selección, instalación y mantenimiento de equipos.</p>
                </div>
                <div class="benefit-card reveal">
                    <div class="benefit-icon">
                        <svg class="blue" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"/></svg>
                    </div>
                    <h3>Calidad Europea Certificada</h3>
                    <p>Productos con certificación CE, VDE y UL que garantizan durabilidad, seguridad y rendimiento óptimo para tu industria.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== PRODUCTS ===== -->
    <section class="products-section" id="productos">
        <div class="section-header reveal">
            <p class="section-tag">Nuestros Productos</p>
            <h2 class="section-title">Soluciones <span class="highlight">Industriales Premium</span></h2>
            <p class="section-desc">Equipos de las mejores marcas europeas para automatización, control y protección eléctrica en Ecuador.</p>
        </div>

        <div class="products-tabs reveal">
            <button class="tab-btn active" onclick="showProduct('invertek')">Invertek Drives</button>
            <button class="tab-btn" onclick="showProduct('schrack')">Schrack Technik</button>
            <button class="tab-btn" onclick="showProduct('murr')">Murr Elektronik</button>
        </div>

        <!-- Invertek -->
        <div class="product-showcase active" id="product-invertek">
            <div class="product-image-container">
                <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/18a6a72e6-5c10-4465-9155-7daf2083b573.png" alt="Invertek OPTIDRIVE E3 Variador de Frecuencia">
                <div style="position:absolute;bottom:1rem;left:1rem;">
                    <span class="product-brand-badge badge-invertek">Invertek Drives</span>
                </div>
            </div>
            <div class="product-info">
                <h3>Variadores de Frecuencia <span style="color:var(--blue)">OPTIDRIVE E³</span></h3>
                <p>La serie OPTIDRIVE E3 ofrece control preciso de motores trifásicos con tecnología de punta europea. Diseñados para maximizar la eficiencia energética y prolongar la vida útil de sus equipos industriales.</p>
                <div class="product-specs">
                    <div class="spec-item">
                        <div class="spec-label">Potencia</div>
                        <div class="spec-value">0.75kW – 75kW</div>
                    </div>
                    <div class="spec-item">
                        <div class="spec-label">Fases</div>
                        <div class="spec-value">Trifásico / Monofásico</div>
                    </div>
                    <div class="spec-item">
                        <div class="spec-label">Protección</div>
                        <div class="spec-value">IP20 / IP55 / IP66</div>
                    </div>
                    <div class="spec-item">
                        <div class="spec-label">Comunicación</div>
                        <div class="spec-value">Modbus, Profibus, Ethernet</div>
                    </div>
                </div>
                <ul class="product-features-list">
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Ahorro energético hasta 30%</li>
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Arranque suave para motores</li>
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Protección IP66 para ambientes hostiles</li>
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Certificación CE y UL</li>
                </ul>
                <a href="#contacto" class="btn-primary">
                    Solicitar Cotización
                    <svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M17 8l4 4m0 0l-4 4m4-4H3"/></svg>
                </a>
            </div>
        </div>

        <!-- Schrack -->
        <div class="product-showcase" id="product-schrack">
            <div class="product-image-container">
                <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/104723d4b-7897-4241-b7cb-739babefafb3.png" alt="Schrack Technik Relés y Breakers">
                <div style="position:absolute;bottom:1rem;left:1rem;">
                    <span class="product-brand-badge badge-schrack">Schrack Technik</span>
                </div>
            </div>
            <div class="product-info">
                <h3>Breakers y Relés <span style="color:#7c3aed">Schrack Technik</span></h3>
                <p>Componentes de protección eléctrica de alta calidad para tableros industriales. Relés plug-in, breakers y protecciones contra arcos eléctricos con certificación VDE europea.</p>
                <div class="product-specs">
                    <div class="spec-item">
                        <div class="spec-label">Relés</div>
                        <div class="spec-value">8 / 14 pines plug-in</div>
                    </div>
                    <div class="spec-item">
                        <div class="spec-label">Breakers</div>
                        <div class="spec-value">Termomagnéticos</div>
                    </div>
                    <div class="spec-item">
                        <div class="spec-label">Montaje</div>
                        <div class="spec-value">Riel DIN estándar</div>
                    </div>
                    <div class="spec-item">
                        <div class="spec-label">Certificación</div>
                        <div class="spec-value">VDE / CE</div>
                    </div>
                </div>
                <ul class="product-features-list">
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Relés plug-in de alta confiabilidad</li>
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Protección contra sobrecargas</li>
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Sistemas anti-arco eléctrico</li>
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Compatible con paneles estándar</li>
                </ul>
                <a href="#contacto" class="btn-primary">
                    Solicitar Cotización
                    <svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M17 8l4 4m0 0l-4 4m4-4H3"/></svg>
                </a>
            </div>
        </div>

        <!-- Murr -->
        <div class="product-showcase" id="product-murr">
            <div class="product-image-container">
                <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/1ef232e3c-b706-4363-addc-26ae32d6cc6a.png" alt="Murr Elektronik IO-Link Module">
                <div style="position:absolute;bottom:1rem;left:1rem;">
                    <span class="product-brand-badge badge-murr">Murr Elektronik</span>
                </div>
            </div>
            <div class="product-info">
                <h3>Automatización Industrial <span style="color:var(--green)">Murr Elektronik</span></h3>
                <p>Soluciones completas de automatización distribuida para la industria moderna. Sistemas de E/S, conectores, fuentes de alimentación y tecnología IO-Link de última generación.</p>
                <div class="product-specs">
                    <div class="spec-item">
                        <div class="spec-label">Tecnología</div>
                        <div class="spec-value">IO-Link Master</div>
                    </div>
                    <div class="spec-item">
                        <div class="spec-label">Conectores</div>
                        <div class="spec-value">M8 / M12 industrial</div>
                    </div>
                    <div class="spec-item">
                        <div class="spec-label">Protocolos</div>
                        <div class="spec-value">PROFINET, EtherNet/IP</div>
                    </div>
                    <div class="spec-item">
                        <div class="spec-label">Fuentes</div>
                        <div class="spec-value">24VDC EMC filtrado</div>
                    </div>
                </div>
                <ul class="product-features-list">
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Módulos de E/S distribuidos</li>
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Cableado industrial M8/M12</li>
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Fuentes de alimentación filtradas EMC</li>
                    <li><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>Compatible con EtherCAT</li>
                </ul>
                <a href="#contacto" class="btn-primary">
                    Solicitar Cotización
                    <svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M17 8l4 4m0 0l-4 4m4-4H3"/></svg>
                </a>
            </div>
        </div>

        <!-- Product Carousel -->
        <div class="carousel-section reveal">
            <h3 style="text-align:center;font-family:'Montserrat',sans-serif;font-size:1.3rem;font-weight:700;color:var(--gray-dark);margin-bottom:2rem;">Catálogo de Productos</h3>
            <div class="carousel-wrapper">
                <div class="carousel-track" id="carouselTrack">
                    <div class="carousel-item">
                        <div class="carousel-img">
                            <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/1a22f4a33-73da-4491-8ff4-321681e6c576.png" alt="Display Variador Frecuencia">
                        </div>
                        <div class="carousel-content">
                            <h4>Display Digital VFD</h4>
                            <p>Control preciso de frecuencia y corriente</p>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <div class="carousel-img">
                            <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/104723d4b-7897-4241-b7cb-739babefafb3.png" alt="Schrack Breakers">
                        </div>
                        <div class="carousel-content">
                            <h4>Breakers Schrack</h4>
                            <p>Protección termomagnética certificada</p>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <div class="carousel-img">
                            <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/1ef232e3c-b706-4363-addc-26ae32d6cc6a.png" alt="Murr IO-Link">
                        </div>
                        <div class="carousel-content">
                            <h4>IO-Link Master</h4>
                            <p>Conectividad inteligente industrial</p>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <div class="carousel-img">
                            <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/17e6a38dc-dade-45b0-8b24-63879dbc1b12.png" alt="Fuente Murr 24VDC">
                        </div>
                        <div class="carousel-content">
                            <h4>Fuente 24VDC</h4>
                            <p>Alimentación filtrada para automatización</p>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <div class="carousel-img">
                            <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/1fa3a1b07-c171-4139-a274-f834d5d7d61e.png" alt="Panel eléctrico industrial">
                        </div>
                        <div class="carousel-content">
                            <h4>Tableros Eléctricos</h4>
                            <p>Soluciones completas de protección</p>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <div class="carousel-img">
                            <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/18a6a72e6-5c10-4465-9155-7daf2083b573.png" alt="Invertek OPTIDRIVE">
                        </div>
                        <div class="carousel-content">
                            <h4>OPTIDRIVE E³</h4>
                            <p>Variador trifásico de alto rendimiento</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="carousel-controls">
                <button class="carousel-btn" onclick="moveCarousel(-1)">
                    <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M15 19l-7-7 7-7"/></svg>
                </button>
                <button class="carousel-btn" onclick="moveCarousel(1)">
                    <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M9 5l7 7-7 7"/></svg>
                </button>
            </div>
        </div>
    </section>

    <!-- ===== STATS ===== -->
    <section class="stats-section">
        <div class="stats-container">
            <div class="stats-grid">
                <div class="stat-card reveal">
                    <div class="stat-number" data-target="30" data-suffix="%">0%</div>
                    <div class="stat-label">Ahorro Energético</div>
                </div>
                <div class="stat-card reveal">
                    <div class="stat-number" data-target="500" data-suffix="+">0+</div>
                    <div class="stat-label">Proyectos Realizados</div>
                </div>
                <div class="stat-card reveal">
                    <div class="stat-number" data-target="8" data-suffix="">0</div>
                    <div class="stat-label">Años de Experiencia</div>
                </div>
                <div class="stat-card reveal">
                    <div class="stat-number" data-target="24" data-suffix="/7">0/7</div>
                    <div class="stat-label">Soporte Técnico</div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== SERVICES ===== -->
    <section class="services-section" id="servicios">
        <div class="services-container">
            <div class="section-header reveal">
                <p class="section-tag">Nuestros Servicios</p>
                <h2 class="section-title">Soluciones <span class="highlight-green">Integrales</span></h2>
                <p class="section-desc">Ofrecemos un servicio completo desde la asesoría hasta la instalación y mantenimiento de equipos.</p>
            </div>
            <div class="services-grid">
                <div class="service-card reveal">
                    <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/14d145a18-4b06-48fd-a16a-3b9cafb69f18.png" alt="Asesoría técnica industrial" class="service-img">
                    <div class="service-content">
                        <h3>Asesoría Técnica Especializada</h3>
                        <p>Nuestro equipo de ingenieros te ayuda a seleccionar el equipo adecuado para tu aplicación, optimizando costos y rendimiento de tu inversión.</p>
                    </div>
                </div>
                <div class="service-card reveal">
                    <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/10fab250f-057c-4d08-aa53-5e7ff7f1ca24.png" alt="Instalación de tableros eléctricos" class="service-img">
                    <div class="service-content">
                        <h3>Instalación y Puesta en Marcha</h3>
                        <p>Servicio profesional de instalación, programación y puesta en marcha de variadores, protecciones y sistemas de automatización.</p>
                    </div>
                </div>
                <div class="service-card reveal">
                    <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/1fa3a1b07-c171-4139-a274-f834d5d7d61e.png" alt="Mantenimiento preventivo industrial" class="service-img">
                    <div class="service-content">
                        <h3>Mantenimiento Preventivo</h3>
                        <p>Programas de mantenimiento preventivo y correctivo para maximizar la vida útil de tus equipos y minimizar tiempos de parada.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== TESTIMONIALS ===== -->
    <section class="testimonials-section">
        <div class="testimonials-container">
            <div class="section-header reveal">
                <p class="section-tag">Testimonios</p>
                <h2 class="section-title">Lo que dicen <span class="highlight">nuestros clientes</span></h2>
                <p class="section-desc">Empresas ecuatorianas confían en ARCA ENERGIES para sus proyectos de automatización.</p>
            </div>
            <div class="testimonials-grid">
                <div class="testimonial-card reveal">
                    <span class="testimonial-quote">"</span>
                    <div class="testimonial-stars">
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                    </div>
                    <p class="testimonial-text">Redujimos nuestro consumo energético en un 28% gracias al variador Invertek instalado en nuestros sistemas de bombeo. El soporte técnico de ARCA fue excepcional.</p>
                    <div class="testimonial-author">
                        <div class="testimonial-avatar">CR</div>
                        <div>
                            <div class="testimonial-name">Carlos Ramírez</div>
                            <div class="testimonial-role">Gerente de Planta – Industrias Quito Norte</div>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card reveal">
                    <span class="testimonial-quote">"</span>
                    <div class="testimonial-stars">
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                    </div>
                    <p class="testimonial-text">La automatización de nuestra línea de producción con equipos Murr Elektronik mejoró nuestra eficiencia en un 35%. ARCA nos acompañó en todo el proceso.</p>
                    <div class="testimonial-author">
                        <div class="testimonial-avatar">ML</div>
                        <div>
                            <div class="testimonial-name">María López</div>
                            <div class="testimonial-role">Directora de Operaciones – FoodPack Ecuador</div>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card reveal">
                    <span class="testimonial-quote">"</span>
                    <div class="testimonial-stars">
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                    </div>
                    <p class="testimonial-text">Protegimos toda nuestra planta con breakers Schrack Technik. La calidad europea se nota desde el primer día. ARCA es nuestro proveedor de confianza.</p>
                    <div class="testimonial-author">
                        <div class="testimonial-avatar">JP</div>
                        <div>
                            <div class="testimonial-name">Jorge Paredes</div>
                            <div class="testimonial-role">Jefe de Mantenimiento – Textiles Guayaquil</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== ABOUT ===== -->
    <section class="about-section" id="nosotros">
        <div class="about-grid">
            <div class="about-image reveal">
                <img src="https://image.qwenlm.ai/public_source/749f9da9-f7e8-420a-9169-4fb79e1bce31/1fa3a1b07-c171-4139-a274-f834d5d7d61e.png" alt="Panel eléctrico industrial ARCA Energies">
            </div>
            <div class="about-content reveal">
                <p class="section-tag">Sobre Nosotros</p>
                <h2>Somos <span class="highlight">ARCA ENERGIES</span> <span class="highlight-green">S.A.</span></h2>
                <p>Fundada en 2018 en Quito, Ecuador, ARCA ENERGIES S.A. nació con la misión de llevar la mejor tecnología europea de automatización, control y protección eléctrica a la industria ecuatoriana.</p>
                <p>Como distribuidores autorizados exclusivos de marcas como Invertek Drives, Schrack Technik y Murr Elektronik, ofrecemos productos certificados con respaldo técnico y asesoría especializada a nivel nacional.</p>
                <p>Nuestro compromiso es brindar soluciones que generen ahorro energético real, mayor confiabilidad y productividad para nuestros clientes en todos los sectores industriales del Ecuador.</p>
                <div class="about-highlights">
                    <div class="about-highlight">
                        <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>
                        <span>Cobertura Nacional</span>
                    </div>
                    <div class="about-highlight">
                        <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>
                        <span>Equipo Calificado</span>
                    </div>
                    <div class="about-highlight">
                        <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>
                        <span>Stock Disponible</span>
                    </div>
                    <div class="about-highlight">
                        <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 13l4 4L19 7"/></svg>
                        <span>Garantía Europea</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== CTA BANNER ===== -->
    <section class="cta-banner">
        <h2>¿Listo para optimizar tu industria?</h2>
        <p>Contáctanos hoy y recibe asesoría técnica gratuita + cotización personalizada</p>
        <a href="https://wa.me/593992567537?text=Hola%20ARCA%20ENERGIES%2C%20deseo%20una%20cotización%20personalizada" target="_blank" class="btn-whatsapp">
            <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
            Escríbenos por WhatsApp Ahora
        </a>
    </section>

    <!-- ===== CONTACT ===== -->
    <section class="contact-section" id="contacto">
        <div class="contact-container">
            <div class="section-header reveal">
                <p class="section-tag">Contacto</p>
                <h2 class="section-title">Solicita tu <span class="highlight-green">Cotización</span></h2>
                <p class="section-desc">Completa el formulario y nuestro equipo técnico te contactará en menos de 24 horas.</p>
            </div>
            <div class="contact-grid">
                <form class="contact-form reveal" id="contactForm" onsubmit="handleFormSubmit(event)">
                    <div class="form-row">
                        <div class="form-group">
                            <label>Nombre Completo *</label>
                            <input type="text" name="nombre" required placeholder="Tu nombre">
                        </div>
                        <div class="form-group">
                            <label>Empresa</label>
                            <input type="text" name="empresa" placeholder="Nombre de tu empresa">
                        </div>
                    </div>
                    <div class="form-row">
                        <div class="form-group">
                            <label>Teléfono *</label>
                            <input type="tel" name="telefono" required placeholder="+593 9X XXX XXXX">
                        </div>
                        <div class="form-group">
                            <label>Email *</label>
                            <input type="email" name="email" required placeholder="tu@email.com">
                        </div>
                    </div>
                    <div class="form-group">
                        <label>Producto de Interés</label>
                        <select name="producto">
                            <option value="">Selecciona un producto</option>
                            <option value="invertek">Variadores Invertek Drives</option>
                            <option value="schrack">Protecciones Schrack Technik</option>
                            <option value="murr">Automatización Murr Elektronik</option>
                            <option value="varios">Varios Productos</option>
                            <option value="otro">Otro / Consulta General</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Mensaje</label>
                        <textarea name="mensaje" placeholder="Describe tu proyecto o necesidad..."></textarea>
                    </div>
                    <button type="submit" class="form-submit">
                        Enviar Solicitud de Cotización
                    </button>
                </form>
                <div class="contact-info reveal">
                    <div class="contact-info-card">
                        <div class="contact-icon">
                            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/></svg>
                        </div>
                        <div class="contact-detail">
                            <h4>Teléfono / WhatsApp</h4>
                            <a href="tel:+593992567537">+593 99 256 7537</a>
                        </div>
                    </div>
                    <div class="contact-info-card">
                        <div class="contact-icon green-bg">
                            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
                        </div>
                        <div class="contact-detail">
                            <h4>Email</h4>
                            <a href="mailto:info@arcaenergies.com">info@arcaenergies.com</a>
                        </div>
                    </div>
                    <div class="contact-info-card">
                        <div class="contact-icon">
                            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/><path d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/></svg>
                        </div>
                        <div class="contact-detail">
                            <h4>Ubicación</h4>
                            <p>Quito, Ecuador<br>Cobertura Nacional</p>
                        </div>
                    </div>
                    <div class="contact-info-card">
                        <div class="contact-icon green-bg">
                            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                        </div>
                        <div class="contact-detail">
                            <h4>Horario de Atención</h4>
                            <p>Lunes a Viernes: 8:00 – 18:00<br>Sábados: 9:00 – 13:00</p>
                        </div>
                    </div>
                    <div class="contact-map">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d255282.35853743783!2d-78.577842!3d-0.180653!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x91d59a4002427c9f%3A0x44b991e158ef5572!2sQuito%2C%20Ecuador!5e0!3m2!1ses!2sus!4v1700000000000!5m2!1ses!2sus" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== FOOTER ===== -->
    <footer class="footer">
        <div class="footer-container">
            <div class="footer-grid">
                <div class="footer-brand">
                    <a href="#" class="nav-logo">
                        <svg viewBox="0 0 45 45" fill="none" width="40" height="40">
                            <rect x="2" y="2" width="41" height="41" rx="10" stroke="#ffffff" stroke-width="2"/>
                            <path d="M14 28L22.5 14L31 28H14Z" fill="none" stroke="#ffffff" stroke-width="2" stroke-linejoin="round"/>
                            <line x1="22.5" y1="20" x2="22.5" y2="26" stroke="#2EB72E" stroke-width="2.5" stroke-linecap="round"/>
                        </svg>
                        <span class="nav-logo-text">ARCA <span style="color:#2EB72E">ENERGIES</span></span>
                    </a>
                    <p>Distribuidor autorizado de variadores de frecuencia, protecciones eléctricas y automatización industrial. Tecnología europea para la industria ecuatoriana desde 2018.</p>
                    <div class="footer-social">
                        <a href="https://instagram.com/arca.energies" target="_blank" class="social-link" aria-label="Instagram">
                            <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/></svg>
                        </a>
                        <a href="#" class="social-link" aria-label="LinkedIn">
                            <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
                        </a>
                        <a href="#" class="social-link" aria-label="Facebook">
                            <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/></svg>
                        </a>
                        <a href="https://wa.me/593992567537" target="_blank" class="social-link" aria-label="WhatsApp">
                            <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
                        </a>
                    </div>
                </div>
                <div class="footer-col">
                    <h4>Enlaces Rápidos</h4>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#beneficios">Beneficios</a></li>
                        <li><a href="#productos">Productos</a></li>
                        <li><a href="#servicios">Servicios</a></li>
                        <li><a href="#nosotros">Nosotros</a></li>
                        <li><a href="#contacto">Contacto</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Productos</h4>
                    <ul>
                        <li><a href="#productos">Variadores Invertek</a></li>
                        <li><a href="#productos">Protecciones Schrack</a></li>
                        <li><a href="#productos">Automatización Murr</a></li>
                        <li><a href="#productos">Fuentes 24VDC</a></li>
                        <li><a href="#productos">Conectores Industriales</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Contacto</h4>
                    <ul>
                        <li><a href="tel:+593992567537">+593 99 256 7537</a></li>
                        <li><a href="mailto:info@arcaenergies.com">info@arcaenergies.com</a></li>
                        <li><a href="#">Quito, Ecuador</a></li>
                        <li><a href="https://instagram.com/arca.energies" target="_blank">@arca.energies</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>© 2026 ARCA ENERGIES S.A. – Todos los derechos reservados.</p>
                <p>Protección europea para tu industria ecuatoriana</p>
            </div>
        </div>
    </footer>

    <!-- WhatsApp Float -->
    <a href="https://wa.me/593992567537?text=Hola%20ARCA%20ENERGIES%2C%20deseo%20información%20sobre%20sus%20productos" target="_blank" class="whatsapp-float" aria-label="WhatsApp">
        <svg width="30" height="30" fill="white" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
    </a>

    <!-- Toast -->
    <div class="toast" id="toast">
        <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
        <span>¡Mensaje enviado! Te contactaremos pronto.</span>
    </div>

    <script>
        // Hero Canvas
        const canvas = document.getElementById('heroCanvas');
        const ctx = canvas.getContext('2d');
        let geoParticles = [];

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);

        class GeoParticle {
            constructor() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.vx = (Math.random() - 0.5) * 0.4;
                this.vy = (Math.random() - 0.5) * 0.4;
                this.radius = Math.random() * 3 + 1;
                this.type = Math.random();
            }
            update() {
                this.x += this.vx;
                this.y += this.vy;
                if (this.x < 0 || this.x > canvas.width) this.vx *= -1;
                if (this.y < 0 || this.y > canvas.height) this.vy *= -1;
            }
            draw() {
                ctx.beginPath();
                if (this.type < 0.33) {
                    ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                    ctx.fillStyle = 'rgba(8,77,156,0.12)';
                } else if (this.type < 0.66) {
                    ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                    ctx.fillStyle = 'rgba(46,183,46,0.1)';
                } else {
                    ctx.rect(this.x - this.radius, this.y - this.radius, this.radius * 2, this.radius * 2);
                    ctx.fillStyle = 'rgba(101,108,112,0.08)';
                }
                ctx.fill();
            }
        }

        const count = Math.min(60, Math.floor(window.innerWidth / 25));
        for (let i = 0; i < count; i++) geoParticles.push(new GeoParticle());

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            for (let i = 0; i < geoParticles.length; i++) {
                for (let j = i + 1; j < geoParticles.length; j++) {
                    const dx = geoParticles[i].x - geoParticles[j].x;
                    const dy = geoParticles[i].y - geoParticles[j].y;
                    const dist = Math.sqrt(dx * dx + dy * dy);
                    if (dist < 180) {
                        ctx.beginPath();
                        ctx.moveTo(geoParticles[i].x, geoParticles[i].y);
                        ctx.lineTo(geoParticles[j].x, geoParticles[j].y);
                        ctx.strokeStyle = `rgba(8,77,156,${0.06 * (1 - dist / 180)})`;
                        ctx.lineWidth = 0.8;
                        ctx.stroke();
                    }
                }
            }
            geoParticles.forEach(p => { p.update(); p.draw(); });
            requestAnimationFrame(animate);
        }
        animate();

        // Navbar scroll
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            navbar.classList.toggle('scrolled', window.scrollY > 60);
        });

        // Mobile menu
        function toggleMenu() {
            document.getElementById('navLinks').classList.toggle('open');
            document.getElementById('hamburger').classList.toggle('active');
        }

        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                document.getElementById('navLinks').classList.remove('open');
                document.getElementById('hamburger').classList.remove('active');
            });
        });

        // Product tabs
        function showProduct(product) {
            document.querySelectorAll('.product-showcase').forEach(el => el.classList.remove('active'));
            document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
            document.getElementById('product-' + product).classList.add('active');
            event.target.classList.add('active');
        }

        // Carousel
        let carouselPos = 0;
        function moveCarousel(direction) {
            const track = document.getElementById('carouselTrack');
            const itemWidth = 295;
            const maxScroll = track.scrollWidth - track.parentElement.offsetWidth;
            carouselPos += direction * itemWidth;
            carouselPos = Math.max(0, Math.min(carouselPos, maxScroll));
            track.style.transform = `translateX(-${carouselPos}px)`;
        }

        // Scroll reveal
        const revealObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) entry.target.classList.add('visible');
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.reveal').forEach(el => revealObserver.observe(el));

        // Counter animation
        const counterObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const el = entry.target;
                    const target = parseInt(el.getAttribute('data-target'));
                    const suffix = el.getAttribute('data-suffix') || '';
                    let current = 0;
                    const increment = target / 50;
                    const timer = setInterval(() => {
                        current += increment;
                        if (current >= target) { current = target; clearInterval(timer); }
                        el.textContent = Math.floor(current) + suffix;
                    }, 30);
                    counterObserver.unobserve(el);
                }
            });
        }, { threshold: 0.5 });

        document.querySelectorAll('.stat-number').forEach(el => counterObserver.observe(el));

        // Form submission
        function handleFormSubmit(e) {
            e.preventDefault();
            const form = e.target;
            const fd = new FormData(form);
            const nombre = fd.get('nombre');
            const telefono = fd.get('telefono');
            const producto = fd.get('producto');
            const mensaje = fd.get('mensaje');

            let waMsg = `Hola ARCA ENERGIES, soy ${nombre}.`;
            if (producto) waMsg += ` Me interesa: ${producto}.`;
            if (mensaje) waMsg += ` ${mensaje}`;
            waMsg += ` Tel: ${telefono}`;

            document.getElementById('toast').classList.add('show');
            setTimeout(() => {
                document.getElementById('toast').classList.remove('show');
            }, 4000);

            setTimeout(() => {
                window.open(`https://wa.me/593992567537?text=${encodeURIComponent(waMsg)}`, '_blank');
            }, 1500);

            form.reset();
        }

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    const top = target.getBoundingClientRect().top + window.pageYOffset - 80;
                    window.scrollTo({ top, behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html>

