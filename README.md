<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0">
    <title>ARCA ENERGIES S.A. | Distribuidor Autorizado</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --gris: #656C70;
            --gris-claro: #F4F6F8;
            --amarillo: #f8be10;
            --blanco: #FFFFFF;
            --lila: #535486; 
            --verde: #2EB72E;
            --verde-oscuro: #249A24;
            --azul: #084D9C;
            --azul-oscuro: #063B7A;
            --sombra: 0 8px 32px rgba(8,77,156,0.12);
            --sombra-fuerte: 0 20px 50px rgba(8,77,156,0.18);
            --sombra-sm: 0 4px 12px rgba(8,77,156,0.15);
            --sombra-md: 0 8px 24px rgba(8,77,156,0.25);
        }
        * { margin:0; padding:0; box-sizing:border-box; }
        html { scroll-behavior: smooth; }
        body { font-family: 'Inter', system-ui, sans-serif; color: #333; overflow-x: hidden; }
        /* ===== NAVIGATION - OCULTA POR DEFECTO ===== */
        .navbar {
            position: fixed;
            top: 0; left: 0; right: 0;
            z-index: 1000;
            padding: 0;
            background: rgba(223,232,239,0.97);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(8,77,156,0.1);
            box-shadow: 0 2px 12px rgba(0,0,0,0.08);
            transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            transform: translateY(-100%);
        }
        .navbar.visible {
            transform: translateY(0);
        }
        .nav-container {
            max-width: 1300px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.45rem 2rem;
            height: 68px;
        }
        .nav-logo {
            display: flex;
            align-items: center;
            gap: 0.6rem;
            text-decoration: none;
            flex-shrink: 0;
        }
        .nav-logo img {
            height: 50px;
            width: auto;
            object-fit: contain;
        }
        .nav-slogan {
            font-size: 0.65rem;
            color: var(--azul-oscuro);
            font-style: italic;
            display: block;
            line-height: 1.2;
        }
        .nav-links {
            display: flex;
            list-style: none;
            gap: 1.5rem;
            align-items: center;
        }
        .nav-links a {
            color: var(--gris);
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 600;
            transition: color 0.3s;
            position: relative;
            white-space: nowrap;
        }
        .nav-links a:hover { color: var(--azul); }
        .nav-cta {
            background: var(--azul-oscuro) !important;
            color: var(--blanco) !important;
            padding: 0.55rem 1.4rem;
            border-radius: 50px;
            font-weight: 600 !important;
            border: none;
            cursor: pointer;
            transition: all 0.3s !important;
        }
        .nav-cta:hover {
            background: var(--azul) !important;
            transform: translateY(-2px);
            box-shadow: var(--sombra-md);
        }
        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 5px;
        }
        .hamburger span {
            width: 26px; height: 2.5px;
            background: var(--azul-oscuro);
            transition: all 0.3s;
            border-radius: 2px;
        }
        .hamburger.active span:nth-child(1) { transform: rotate(45deg) translate(5px, 5px); }
        .hamburger.active span:nth-child(2) { opacity: 0; }
        .hamburger.active span:nth-child(3) { transform: rotate(-45deg) translate(5px, -5px);}
        /* TOP BANNER */
        .top-banner {
            background: var(--verde-oscuro);
            color: var(--blanco);
            text-align: center;
            padding: 8px 16px;
            font-size: 0.9rem;
            font-weight: 600;
            letter-spacing: 0.3px;
            position: relative;
            line-height: 1.4;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            gap: 8px;
        }
        .top-banner .badge {
            display: inline-block;
            background: var(--amarillo);
            color: #1a1a2e;
            padding: 3px 14px;
            border-radius: 50px;
            font-size: 0.72rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        /* ===== HERO FULL SCREEN ===== */
        .hero {
            height: 100vh;
            min-height: 100vh;
            width: 100%;
            background: url("https://arcaenergies.com/wp-content/uploads/2026/Bases/Fondo_03.jpg") center/cover no-repeat;
            position: relative;
            display: flex;
            align-items: center;
        }
        .hero::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background: rgba(0,0,0,0.2);
            z-index: 1;
        }
        .hero-content {
            max-width: 1300px;
            width: 100%;
            margin: 0 auto;
            padding: 0 40px;
            display: grid;
            grid-template-columns: 1.1fr 0.9fr;
            gap: 30px;
            align-items: center;
            z-index: 2;
            position: relative;
            height: 100%;
        }
        .hero-text {
            width: 100%;
            color: var(--blanco);
        }
        .hero-text h1 {
            font-size: 3.6rem;
            line-height: 1.05;
            color: var(--blanco);
            font-weight: 900;
            margin-bottom: 14px;
            letter-spacing: -1.5px;
        }
        .hero-text h1 .accent {
            color: var(--verde);
        }
        .tagline {
            font-size: 1.5rem;
            color: var(--blanco);
            font-weight: 700;
            margin-bottom: 18px;
        }
        .hero-text .subtitle {
            font-size: 1.05rem;
            color: rgba(255,255,255,0.92);
            line-height: 1.65;
            max-width: 520px;
            margin-bottom: 30px;
        }
        .hero-text .subtitle strong {
            color: var(--blanco);
        }
        .hero-buttons {
            display: flex;
            gap: 14px;
            flex-wrap: wrap;
            margin-bottom: 20px;
        }
        .btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 15px 32px;
            font-size: 1rem;
            font-weight: 700;
            border-radius: 50px;
            text-decoration: none;
            transition: all 0.35s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            cursor: pointer;
            border: none;
            font-family: inherit;
        }
        .btn-azul {
            background: var(--azul);
            color: var(--blanco);
            box-shadow: 0 8px 24px rgba(8,77,156,0.35);
        }
        .btn-azul:hover {
            background: var(--azul-oscuro);
            transform: translateY(-3px);
            box-shadow: 0 12px 30px rgba(8,77,156,0.45);
        }
        .btn-verde {
            background: var(--verde);
            color: var(--blanco);
            box-shadow: 0 8px 24px rgba(46,183,46,0.35);
        }
        .btn-verde:hover {
            background: var(--verde-oscuro);
            transform: translateY(-3px);
            box-shadow: 0 12px 30px rgba(46,183,46,0.45);
        }
        .contact-info {
            font-size: 0.82rem;
            color: rgba(255,255,255,0.85);
            line-height: 1.6;
        }
        .contact-info strong {
            color: var(--blanco);
        }
        /* Hero Visual / Product Image */
        .hero-visual {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
        }
        .hero-card {
            width: 100%;
            max-width: 460px;
        }
        .hero-card-inner {
            position: relative;
            width: 100%;
            background: linear-gradient(135deg, rgba(83,84,134,0.6) 0%, rgba(200,210,220,0.5) 100%);
            border-radius: 24px;
            overflow: visible;
            padding: 10px 16px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.2);
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
        }
        .hero-card-inner .hero-image {
            width: 100%;
            height: auto;
            display: block;
            border-radius: 14px;
            object-fit: contain;
        }
        /* Floating Badge */
        .floating-badge {
            position: absolute;
            z-index: 20;
            padding: 12px 20px;
            border-radius: 14px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 700;
            white-space: nowrap;
            border: 1px solid rgba(255,255,255,0.6);
            backdrop-filter: blur(10px);
            background: rgba(255,255,255,0.95);
            color: #1f2937;
        }
        .floating-badge.energy {
            top: 16px;
            left: -12px;
        }
        .floating-badge .icon {
            width: 32px;
            height: 32px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            font-size: 16px;
            flex-shrink: 0;
            background: #ffd43b;
        }
        .floating-badge .label {
            font-size: 0.9rem;
            font-weight: 700;
            line-height: 1.2;
            color: #1f2937;
        }
        .floating-badge .sublabel {
            font-size: 0.72rem;
            color: var(--gris);
            margin-top: 1px;
        }
        /* STATS BAR */
        .stats-bar {
            background: var(--azul-oscuro);
            padding: 40px 40px;
        }
        .stats-inner {
            max-width: 1280px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
        }
        .stat-item { text-align: center; color: var(--blanco); }
        .stat-number {
            font-size: 2.4rem;
            font-weight: 900;
            letter-spacing: -1px;
            margin-bottom: 4px;
        }
        .stat-number .verde { color: var(--verde); }
        .stat-label { font-size: 0.88rem; opacity: 0.8; font-weight: 500; }
        /* BRANDS SECTION */
        .brands-section {
            padding: 80px 40px;
            background: var(--blanco);
        }
        .section-header {
            text-align: center;
            margin-bottom: 48px;
        }
        .section-label {
            display: inline-block;
            background: rgba(46,183,46,0.1);
            color: var(--verde);
            padding: 6px 18px;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 14px;
        }
        .section-title {
            font-size: 2.4rem;
            color: var(--azul);
            font-weight: 800;
            letter-spacing: -0.8px;
            margin-bottom: 14px;
        }
        .section-subtitle {
            font-size: 1.05rem;
            color: var(--gris);
            max-width: 580px;
            margin: 0 auto;
            line-height: 1.65;
        }
        .brands-grid {
            max-width: 1280px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 28px;
        }
        .brand-card {
            background: var(--gris-claro);
            border-radius: 18px;
            padding: 40px 28px;
            text-align: center;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            border: 2px solid transparent;
            position: relative;
            overflow: hidden;
        }
        .brand-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--azul), var(--verde));
            transform: scaleX(0);
            transition: transform 0.4s;
        }
        .brand-card:hover {
            transform: translateY(-6px);
            box-shadow: var(--sombra-fuerte);
            border-color: rgba(8,77,156,0.1);
            background: var(--blanco);
        }
        .brand-card:hover::before { transform: scaleX(1); }
        .brand-icon {
            width: 70px; height: 70px;
            border-radius: 18px;
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
        }
        .brand-icon.invertek { background: linear-gradient(135deg, #084D9C, #0A6BC2); color: white; }
        .brand-icon.schrack { background: linear-gradient(135deg, #D4380D, #FF6B3D); color: white; }
        .brand-icon.murr { background: linear-gradient(135deg, #1A1A2E, #16213E); color: #E94560; }
        .brand-card h3 {
            font-size: 1.25rem;
            color: var(--azul);
            font-weight: 800;
            margin-bottom: 6px;
        }
        .brand-card .origin {
            font-size: 0.8rem;
            color: var(--verde);
            font-weight: 600;
            margin-bottom: 12px;
        }
        .brand-card p {
            font-size: 0.88rem;
            color: var(--gris);
            line-height: 1.55;
        }
        /* PRODUCTS SECTION */
        .products-section {
            padding: 80px 40px;
            background: linear-gradient(180deg, var(--gris-claro) 0%, var(--blanco) 100%);
        }
        .products-grid {
            max-width: 1280px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 24px;
        }
        .product-card {
            background: var(--blanco);
            border-radius: 18px;
            overflow: hidden;
            box-shadow: 0 4px 16px rgba(0,0,0,0.06);
            transition: all 0.4s;
            border: 1px solid rgba(0,0,0,0.04);
        }
        .product-card:hover {
            transform: translateY(-6px);
            box-shadow: var(--sombra-fuerte);
        }
        .product-image {
            height: 180px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }
        .product-image svg {
            width: 100px;
            height: 100px;
            transition: transform 0.4s;
        }
        .product-card:hover .product-image svg { transform: scale(1.08); }
        .product-image.bg-azul { background: linear-gradient(135deg, #EDF4FB, #D4E8F7); }
        .product-image.bg-orange { background: linear-gradient(135deg, #FFF0E8, #FFD4B8); }
        .product-image.bg-dark { background: linear-gradient(135deg, #E8E8F0, #D0D0E0); }
        .product-image.bg-verde { background: linear-gradient(135deg, #E8F5E8, #C8E6C9); }
        .product-image.bg-purple { background: linear-gradient(135deg, #F0E8F8, #E0D0F0); }
        .product-image.bg-teal { background: linear-gradient(135deg, #E0F4F0, #C0E8E0); }
        .product-body { padding: 22px; }
        .product-tag {
            display: inline-block;
            background: rgba(8,77,156,0.08);
            color: var(--azul);
            padding: 3px 12px;
            border-radius: 50px;
            font-size: 0.7rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 10px;
        }
        .product-tag.verde { background: rgba(46,183,46,0.1); color: var(--verde); }
        .product-body h3 {
            font-size: 1.05rem;
            color: var(--azul);
            font-weight: 800;
            margin-bottom: 8px;
            line-height: 1.3;
        }
        .product-body p {
            font-size: 0.85rem;
            color: var(--gris);
            line-height: 1.55;
            margin-bottom: 14px;
        }
        .product-link {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            color: var(--azul);
            font-weight: 700;
            font-size: 0.85rem;
            text-decoration: none;
            transition: gap 0.3s;
        }
        .product-link:hover { gap: 12px; }
        /* MARQUEE */
        .brands-marquee {
            background: var(--gris-claro);
            padding: 1.2rem 0;
            overflow: hidden;
            border-top: 1px solid #E5E9ED;
            border-bottom: 1px solid #E5E9ED;
        }
        .marquee-track {
            display: flex;
            gap: 3rem;
            animation: marquee 25s linear infinite;
            width: max-content;
        }
        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }
        .marquee-item {
            font-family: 'Inter', sans-serif;
            font-size: 1rem;
            font-weight: 700;
            color: var(--gris);
            opacity: 0.4;
            white-space: nowrap;
            display: flex;
            align-items: center;
            gap: 0.6rem;
        }
        .marquee-item span {
            color: var(--azul);
            opacity: 0.6;
        }
        /* WHY US */
        .why-section {
            padding: 80px 40px;
            background: var(--blanco);
        }
        .why-grid {
            max-width: 1280px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 24px;
        }
        .why-card {
            text-align: center;
            padding: 30px 20px;
            border-radius: 18px;
            transition: all 0.3s;
        }
        .why-card:hover { background: var(--gris-claro); }
        .why-icon {
            width: 58px; height: 58px;
            border-radius: 14px;
            background: rgba(8,77,156,0.08);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 16px;
            font-size: 1.5rem;
        }
        .why-card h4 {
            font-size: 1rem;
            color: var(--azul);
            font-weight: 800;
            margin-bottom: 8px;
        }
        .why-card p {
            font-size: 0.85rem;
            color: var(--gris);
            line-height: 1.55;
        }
        /* CTA */
        .cta-section {
            padding: 80px 40px;
            background: linear-gradient(135deg, var(--azul) 0%, var(--azul-oscuro) 100%);
            position: relative;
            overflow: hidden;
        }
        .cta-section::before {
            content: '';
            position: absolute;
            top: -100px; right: -100px;
            width: 400px; height: 400px;
            background: radial-gradient(circle, rgba(46,183,46,0.15) 0%, transparent 70%);
            border-radius: 50%;
        }
        .cta-inner {
            max-width: 700px;
            margin: 0 auto;
            text-align: center;
            position: relative;
            z-index: 2;
        }
        .cta-inner h2 {
            font-size: 2.4rem;
            color: var(--blanco);
            font-weight: 900;
            margin-bottom: 16px;
        }
        .cta-inner h2 .verde { color: var(--verde); }
        .cta-inner p {
            font-size: 1.05rem;
            color: rgba(255,255,255,0.8);
            margin-bottom: 32px;
            line-height: 1.65;
        }
        .cta-buttons { display: flex; gap: 14px; justify-content: center; flex-wrap: wrap; }
        .btn-white {
            background: var(--blanco);
            color: var(--azul);
            box-shadow: 0 8px 24px rgba(0,0,0,0.15);
        }
        .btn-white:hover {
            background: var(--gris-claro);
            transform: translateY(-3px);
        }
        .btn-outline-white {
            background: transparent;
            color: var(--blanco);
            border: 2px solid rgba(255,255,255,0.4);
        }
        .btn-outline-white:hover {
            background: rgba(255,255,255,0.1);
            border-color: var(--blanco);
            transform: translateY(-3px);
        }
        /* CONTACT */
        .contact-section {
            padding: 80px 40px;
            background: var(--gris-claro);
        }
        .contact-grid {
            max-width: 1280px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 48px;
            align-items: start;
        }
        .contact-info-card {
            background: var(--blanco);
            border-radius: 22px;
            padding: 40px;
            box-shadow: var(--sombra);
        }
        .contact-info-card h3 {
            font-size: 1.6rem;
            color: var(--azul);
            font-weight: 800;
            margin-bottom: 20px;
        }
        .contact-detail {
            display: flex;
            gap: 14px;
            margin-bottom: 20px;
            align-items: flex-start;
        }
        .contact-detail .icon-box {
            width: 44px; height: 44px;
            border-radius: 12px;
            background: rgba(8,77,156,0.08);
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            font-size: 1.1rem;
        }
        .contact-detail .text strong {
            display: block;
            color: var(--azul);
            font-size: 0.88rem;
            margin-bottom: 3px;
        }
        .contact-detail .text a {
            color: var(--gris);
            font-size: 0.85rem;
            text-decoration: none;
            line-height: 1.5;
        }
        .contact-detail .text a:hover { color: var(--verde); }
        .contact-form-card {
            background: var(--blanco);
            border-radius: 22px;
            padding: 40px;
            box-shadow: var(--sombra);
        }
        .contact-form-card h3 {
            font-size: 1.35rem;
            color: var(--azul);
            font-weight: 800;
            margin-bottom: 24px;
        }
        .form-group { margin-bottom: 16px; }
        .form-group label {
            display: block;
            font-size: 0.82rem;
            font-weight: 600;
            color: var(--azul);
            margin-bottom: 6px;
        }
        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 12px 16px;
            border: 2px solid #E8ECF0;
            border-radius: 10px;
            font-family: inherit;
            font-size: 0.9rem;
            color: #333;
            transition: border-color 0.3s;
            outline: none;
            background: var(--gris-claro);
        }
        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            border-color: var(--azul);
            background: var(--blanco);
        }
        .form-group textarea { resize: vertical; min-height: 90px; }
        .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
        .form-submit {
            width: 100%;
            padding: 14px;
            background: var(--azul);
            color: var(--blanco);
            border: none;
            border-radius: 10px;
            font-family: inherit;
            font-size: 1rem;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
        }
        .form-submit:hover {
            background: var(--azul-oscuro);
            transform: translateY(-2px);
            box-shadow: var(--sombra);
        }
        /* FOOTER */
        .footer {
            background: #0A1628;
            color: rgba(255,255,255,0.7);
            padding: 50px 40px 28px;
        }
        .footer-inner {
            max-width: 1280px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1.5fr 1fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }
        .footer-brand h3 {
            font-size: 1.4rem;
            color: var(--blanco);
            font-weight: 900;
            margin-bottom: 10px;
        }
        .footer-brand h3 span { color: var(--verde); }
        .footer-brand p { font-size: 0.85rem; line-height: 1.6; margin-bottom: 16px; }
        .footer-col h4 {
            color: var(--blanco);
            font-size: 0.88rem;
            font-weight: 700;
            margin-bottom: 16px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        .footer-col a {
            display: block;
            color: rgba(255,255,255,0.6);
            text-decoration: none;
            font-size: 0.85rem;
            margin-bottom: 10px;
            transition: color 0.3s;
        }
        .footer-col a:hover { color: var(--verde); }
        .footer-bottom {
            max-width: 1280px;
            margin: 0 auto;
            padding-top: 24px;
            border-top: 1px solid rgba(255,255,255,0.08);
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.8rem;
        }
        /* WHATSAPP FLOAT */
        .whatsapp-float {
            position: fixed;
            bottom: 18px;
            right: 18px;
            width: 56px;
            height: 56px;
            background: #25D366;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 6px 20px rgba(37,211,102,0.4);
            z-index: 999;
            transition: all 0.3s;
            text-decoration: none;
            animation: pulse-wa 2s infinite;
        }
        .whatsapp-float:hover { transform: scale(1.1); }
        .whatsapp-float svg { width: 30px; height: 30px; fill: white; }
        @keyframes pulse-wa {
            0% { box-shadow: 0 6px 20px rgba(37,211,102,0.4); }
            50% { box-shadow: 0 6px 20px rgba(37,211,102,0.4), 0 0 0 10px rgba(37,211,102,0.12); }
            100% { box-shadow: 0 6px 20px rgba(37,211,102,0.4); }
        }
        /* SCROLL ANIMATIONS */
        .fade-up {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        .fade-up.visible { opacity: 1; transform: translateY(0); }
        /* ============================================
           RESPONSIVE - TABLET 1024px
           ============================================ */
        @media (max-width: 1024px) {
            .nav-container { padding: 0.4rem 1.2rem; height: 60px; }
            .nav-logo img { height: 42px; }
            .hero-content { grid-template-columns: 1fr; gap: 24px; text-align: center; padding: 0 24px; }
            .hero-text h1 { font-size: 2.8rem; }
            .tagline { font-size: 1.2rem; }
            .hero-text .subtitle { margin: 0 auto 24px; }
            .hero-buttons { justify-content: center; }
            .hero-visual { max-width: 380px; margin: 0 auto; }
            .hero-card-inner { max-width: 380px; }
            .brands-grid { grid-template-columns: repeat(2, 1fr); }
            .products-grid { grid-template-columns: repeat(2, 1fr); }
            .why-grid { grid-template-columns: repeat(2, 1fr); }
            .stats-inner { grid-template-columns: repeat(4, 1fr); gap: 20px; }
            .stat-number { font-size: 2rem; }
            .contact-grid { grid-template-columns: 1fr; gap: 32px; }
            .footer-inner { grid-template-columns: repeat(2, 1fr); gap: 28px; }
            .brands-section, .products-section, .why-section, .cta-section, .contact-section { padding: 64px 24px; }
        }
        /* ============================================
           RESPONSIVE - TABLET PORTRAIT 768px
           ============================================ */
        @media (max-width: 768px) {
            .nav-container { padding: 0.35rem 1rem; height: 56px; }
            .nav-logo img { height: 38px !important; }
            .nav-slogan { display: none; }
            .hero {
                height: 100vh;
                min-height: 100vh;
            }
            .hero-content {
                grid-template-columns: 1fr;
                gap: 20px;
                padding: 0 18px;
                align-items: center;
                justify-items: center;
            }
            .hero-text { text-align: center; }
            .hero-text h1 { font-size: 2.2rem; }
            .tagline { font-size: 1.05rem; }
            .hero-text .subtitle { font-size: 0.9rem; margin: 0 auto 20px; }
            .hero-buttons { gap: 10px; justify-content: center; }
            .btn { padding: 12px 24px; font-size: 0.9rem; }
            .contact-info { font-size: 0.75rem; text-align: center; }
            .hero-card { max-width: 340px; }
            .hero-card-inner { max-width: 340px; padding: 8px 12px; }
            .hero-card-inner .hero-image { border-radius: 10px; }
            .floating-badge { display: none; }
            .section-title { font-size: 1.8rem; }
            .cta-inner h2 { font-size: 1.7rem; }
            .brands-grid { grid-template-columns: 1fr; max-width: 420px; margin: 0 auto; }
            .products-grid { grid-template-columns: repeat(2, 1fr); gap: 14px; }
            .why-grid { grid-template-columns: repeat(2, 1fr); gap: 14px; }
            .stats-inner { grid-template-columns: repeat(2, 1fr); gap: 14px; padding: 30px 18px; }
            .stat-number { font-size: 1.6rem; }
            .stat-label { font-size: 0.78rem; }
            .brands-section, .products-section, .why-section, .cta-section, .contact-section { padding: 50px 18px; }
            .brand-card { padding: 28px 18px; }
            .product-image { height: 140px; }
            .product-body { padding: 14px; }
            .product-body h3 { font-size: 0.92rem; }
            .contact-info-card, .contact-form-card { padding: 24px; }
            .contact-info-card h3 { font-size: 1.3rem; }
            .contact-form-card h3 { font-size: 1.15rem; }
            .footer { padding: 40px 18px 20px; }
            .footer-inner { grid-template-columns: 1fr 1fr; gap: 24px; }
            .footer-bottom { flex-direction: column; gap: 8px; text-align: center; }
            .whatsapp-float { width: 48px; height: 48px; bottom: 14px; right: 14px; }
            .whatsapp-float svg { width: 24px; height: 24px; }
            /* Hamburger */
            .nav-links { display: none; }
            .hamburger { display: flex; }
            .nav-links.open {
                display: flex;
                flex-direction: column;
                position: fixed;
                top: 0; left: 0; right: 0; bottom: 0;
                background: rgba(255,255,255,0.98);
                backdrop-filter: blur(10px);
                padding: 65px 20px 24px;
                gap: 12px;
                z-index: 999;
                overflow-y: auto;
                align-items: flex-start;
            }
            .nav-links.open a {
                font-size: 1rem;
                color: var(--azul);
                padding: 8px 0;
                border-bottom: 1px solid rgba(0,0,0,0.05);
                width: 100%;
            }
            .nav-links.open .nav-cta {
                margin-top: 8px;
                text-align: center;
                width: 100%;
                color: var(--blanco) !important;
            }
        }
        /* ============================================
           RESPONSIVE - ANDROID PHONES 480px
           ============================================ */
        @media (max-width: 480px) {
            .nav-container { padding: 0.3rem 0.7rem; height: 50px; }
            .nav-logo img { height: 34px !important; }
            .top-banner { font-size: 0.68rem; padding: 6px 10px; }
            .top-banner .badge { font-size: 0.58rem; padding: 2px 8px; }

            .hero {
                height: 100vh;
                min-height: 100vh;
            }
            .hero-content {
                grid-template-columns: 1fr;
                gap: 16px;
                padding: 0 14px;
            }
            .hero-text { text-align: center; }
            .hero-text h1 { font-size: 1.8rem; letter-spacing: -0.3px; }
            .tagline { font-size: 0.92rem; margin-bottom: 12px; }
            .hero-text .subtitle { font-size: 0.8rem; line-height: 1.5; margin: 0 auto 16px; }
            .hero-buttons { flex-direction: column; gap: 8px; margin-bottom: 12px; align-items: center; }
            .btn { padding: 12px 20px; font-size: 0.85rem; width: 100%; max-width: 280px; justify-content: center; }
            .contact-info { font-size: 0.72rem; line-height: 1.5; text-align: center; }
            .hero-card { max-width: 100%; }
            .hero-card-inner { max-width: 100%; padding: 6px 10px; border-radius: 16px; }
            .floating-badge { display: none; }
            .section-title { font-size: 1.5rem; }
            .section-subtitle { font-size: 0.85rem; }
            .section-label { font-size: 0.68rem; }
            .brands-section, .products-section, .why-section, .cta-section, .contact-section { padding: 40px 14px; }
            .section-header { margin-bottom: 28px; }
            .brands-grid { gap: 14px; }
            .brand-card { padding: 22px 14px; }
            .brand-icon { width: 50px; height: 50px; font-size: 1.3rem; margin-bottom: 12px; }
            .brand-card h3 { font-size: 0.98rem; }
            .brand-card p { font-size: 0.8rem; }
            .products-grid { grid-template-columns: 1fr; gap: 12px; }
            .product-card { border-radius: 12px; }
            .product-image { height: 130px; }
            .product-image svg { width: 70px; height: 70px; }
            .product-body { padding: 14px; }
            .product-body h3 { font-size: 0.9rem; }
            .product-body p { font-size: 0.8rem; }
            .product-tag { font-size: 0.65rem; }
            .why-grid { grid-template-columns: 1fr; gap: 10px; }
            .why-card { padding: 18px 12px; }
            .why-icon { width: 44px; height: 44px; font-size: 1.1rem; }
            .why-card h4 { font-size: 0.92rem; }
            .why-card p { font-size: 0.8rem; }
            .stats-bar { padding: 24px 14px; }
            .stats-inner { gap: 10px; }
            .stat-number { font-size: 1.35rem; }
            .stat-label { font-size: 0.68rem; }
            .cta-section { padding: 40px 14px; }
            .cta-inner h2 { font-size: 1.35rem; }
            .cta-inner p { font-size: 0.85rem; margin-bottom: 20px; }
            .cta-buttons { flex-direction: column; align-items: center; }
            .cta-buttons .btn { width: 100%; max-width: 280px; }
            .contact-grid { gap: 16px; }
            .contact-info-card, .contact-form-card { padding: 18px; border-radius: 14px; }
            .contact-info-card h3 { font-size: 1.1rem; margin-bottom: 14px; }
            .contact-form-card h3 { font-size: 1.05rem; margin-bottom: 14px; }
            .contact-detail { gap: 10px; margin-bottom: 12px; }
            .contact-detail .icon-box { width: 36px; height: 36px; font-size: 0.9rem; }
            .contact-detail .text strong { font-size: 0.78rem; }
            .contact-detail .text a { font-size: 0.75rem; }
            .form-row { grid-template-columns: 1fr; gap: 0; }
            .form-group input, .form-group select, .form-group textarea { padding: 10px 12px; font-size: 0.82rem; }
            .form-group label { font-size: 0.75rem; }
            .form-submit { padding: 12px; font-size: 0.88rem; }
            .footer { padding: 28px 14px 16px; }
            .footer-inner { grid-template-columns: 1fr; gap: 20px; }
            .footer-brand h3 { font-size: 1.1rem; }
            .footer-brand p { font-size: 0.75rem; }
            .footer-col h4 { font-size: 0.78rem; margin-bottom: 10px; }
            .footer-col a { font-size: 0.75rem; margin-bottom: 5px; }
            .footer-bottom { font-size: 0.68rem; padding-top: 14px; }

            .whatsapp-float { width: 44px; height: 44px; bottom: 12px; right: 12px; }
            .whatsapp-float svg { width: 20px; height: 20px; }
            .marquee-item { font-size: 0.85rem; }
        }
        /* ============================================
           RESPONSIVE - SMALL PHONES 360px
           ============================================ */
        @media (max-width: 360px) {
            .nav-container { padding: 0.25rem 0.5rem; height: 46px; }
            .nav-logo img { height: 30px !important; }
            .hero-content { padding: 0 12px; gap: 12px; }
            .hero-text h1 { font-size: 1.55rem; }
            .tagline { font-size: 0.82rem; }
            .hero-text .subtitle { font-size: 0.74rem; }
            .btn { padding: 10px 16px; font-size: 0.78rem; }
            .hero-card-inner { padding: 4px 8px; border-radius: 12px; }
            .section-title { font-size: 1.3rem; }
            .brands-section, .products-section, .why-section, .cta-section, .contact-section { padding: 32px 12px; }
            .brand-card { padding: 18px 12px; }
            .product-image { height: 110px; }
            .stat-number { font-size: 1.2rem; }
            .cta-inner h2 { font-size: 1.2rem; }
            .cta-inner p { font-size: 0.78rem; }
            .contact-info-card, .contact-form-card { padding: 14px; }
            .footer { padding: 22px 12px 12px; }
        }
        @media (max-width: 520px) {
            .hamburger { gap: 4px; }
            .hamburger span { width: 22px; height: 2.5px; background: var(--azul-oscuro); }
        }
    </style>
</head>
<body>
 <!-- ===== NAVIGATION - OCULTA POR DEFECTO ===== -->
    <nav class="navbar" id="navbar">
        <div class="nav-container">
            <a href="#" class="nav-logo">
                <img src="https://arcaenergies.com/wp-content/uploads/2026/Bases/LogoFD.png" 
                     alt="ARCA ENERGIES Logo">
                <span class="nav-slogan">Navegamos hacia la innovación</span>
            </a>
            <ul class="nav-links" id="navLinks">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#marcas">Nuestras Marcas</a></li>
                <li><a href="#productos">Productos</a></li>
                <li><a href="#nosotros">Nosotros</a></li>
                <li><a href="#contacto">Contacto</a></li>
                <li><a href="#contacto" class="nav-cta">Cotizar Ahora</a></li>
            </ul>
            <div class="hamburger" id="hamburger">
                <span></span><span></span><span></span>
            </div>
        </div>
    </nav>
    <!-- TOP BANNER -->
    <div class="top-banner">
        <span class="badge">DISTRIBUIDOR AUTORIZADO</span>
        Invertek • Schrack Technik • Murr Elektronik en Ecuador 🇪
    </div>
    <!-- ===== HERO FULL SCREEN ===== -->
    <header class="hero" id="inicio">
        <div class="hero-content">
            <div class="hero-text">
                <h1>ARCA <span class="accent">ENERGIES</span> S.A.</h1>
                <p class="tagline">Tecnología europea para tu industria</p>
                <p class="subtitle">
                    Variadores de frecuencia <strong>Invertek</strong> • Protecciones <strong>Schrack Technik</strong> • 
                    Automatización <strong>Murr Elektronik</strong><br>
                    <strong>Control • Ahorro energético • Protección total</strong>
                </p>
                <div class="hero-buttons">
                    <a href="#cotiza" class="btn btn-azul">
                        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>
                        COTIZA TU SOLUCIÓN
                    </a>
                    <a href="https://wa.me/593992567537?text=Hola%20ARCA%20Energies%2C%20quiero%20una%20cotizaci%C3%B3n" target="_blank" class="btn btn-verde">
                        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.127.555 4.122 1.523 5.857L.06 23.573a.75.75 0 0 0 .914.914l5.716-1.463A11.94 11.94 0 0 0 12 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 22c-1.94 0-3.765-.54-5.33-1.48l-.372-.222-3.894.997 1.039-3.798-.244-.388A9.96 9.96 0 0 1 2 12C2 6.486 6.486 2 12 2s10 4.486 10 10-4.486 10-10 10z"/></svg>
                        WhatsApp
                    </a>
                </div>
                <div class="contact-info">
                    <strong>ventas1@arcaenergies.com</strong> • ventas3@arcaenergies.com<br>
                    +593 99 256 7537 • Quito • Cobertura Nacional
                </div>
            </div>
            <div class="hero-visual">
                <div class="hero-card">
                    <div class="hero-card-inner">
                        <img 
                            src="https://arcaenergies.com/wp-content/uploads/2026/Bases/VFportada.png" 
                            alt="Variador de Frecuencia Invertek" 
                            class="hero-image">
                        <div class="floating-badge energy">
                            <div class="icon">⚡</div>
                            <div>
                                <div class="label">Ahorro Energético</div>
                                <div class="sublabel">Hasta 60% de eficiencia</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
    <!-- STATS -->
    <section class="stats-bar">
        <div class="stats-inner">
            <div class="stat-item fade-up">
                <div class="stat-number">8<span class="verde">+</span></div>
                <div class="stat-label">Años de experiencia</div>
            </div>
            <div class="stat-item fade-up">
                <div class="stat-number">500<span class="verde">+</span></div>
                <div class="stat-label">Proyectos realizados</div>
            </div>
            <div class="stat-item fade-up">
                <div class="stat-number">3</div>
                <div class="stat-label">Marcas europeas líderes</div>
            </div>
            <div class="stat-item fade-up">
                <div class="stat-number">24<span class="verde">/7</span></div>
                <div class="stat-label">Soporte técnico</div>
            </div>
        </div>
    </section>
    <!-- MARQUEE -->
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
    <!-- BRANDS -->
    <section class="brands-section" id="marcas">
        <div class="section-header fade-up">
            <div class="section-label">Nuestras Marcas</div>
            <h2 class="section-title">Distribuidor Autorizado en Ecuador</h2>
            <p class="section-subtitle">Representamos las marcas europeas más confiables en automatización, control de motores y protección eléctrica industrial.</p>
        </div>
        <div class="brands-grid">
            <div class="brand-card fade-up">
                <div class="brand-icon invertek">
                    <svg width="36" height="36" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>
                </div>
                <h3>Invertek Drives</h3>
                <div class="origin">🇬 Reino Unido</div>
                <p>Variadores de frecuencia Optidrive de alta eficiencia. Control preciso de motores AC para aplicaciones industriales de todo tipo.</p>
            </div>
            <div class="brand-card fade-up">
                <div class="brand-icon schrack">
                    <svg width="36" height="36" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
                </div>
                <h3>Schrack Technik</h3>
                <div class="origin">🇦 Austria</div>
                <p>Protecciones eléctricas, relés, contactores y soluciones de seguridad para tableros industriales y sistemas de distribución.</p>
            </div>
            <div class="brand-card fade-up">
                <div class="brand-icon murr">
                    <svg width="36" height="36" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="3"/><path d="M12 1v6m0 6v6m-6.36-12.36l4.24 4.24m4.24 4.24l4.24 4.24M1 12h6m6 0h6M3.64 3.64l4.24 4.24m8.48 8.48l4.24 4.24"/></svg>
                </div>
                <h3>Murr Elektronik</h3>
                <div class="origin">🇩 Alemania</div>
                <p>Conectividad, fuentes de poder, módulos I/O y soluciones de automatización para Industry 4.0 con tecnología alemana de precisión.</p>
            </div>
        </div>
    </section>
    <!-- PRODUCTS -->
    <section class="products-section" id="productos">
        <div class="section-header fade-up">
            <div class="section-label">Catálogo</div>
            <h2 class="section-title">Soluciones Industriales</h2>
            <p class="section-subtitle">Equipos de alta calidad para control de motores, protección eléctrica y automatización de procesos.</p>
        </div>
        <div class="products-grid">
            <div class="product-card fade-up">
                <div class="product-image bg-azul">
                    <svg viewBox="0 0 120 120" fill="none">
                        <rect x="20" y="30" width="80" height="60" rx="6" fill="#084D9C" opacity="0.15" stroke="#084D9C" stroke-width="2"/>
                        <rect x="30" y="40" width="60" height="30" rx="3" fill="#084D9C" opacity="0.1"/>
                        <circle cx="45" cy="80" r="4" fill="#2EB72E"/>
                        <circle cx="60" cy="80" r="4" fill="#084D9C"/>
                        <circle cx="75" cy="80" r="4" fill="#2EB72E" opacity="0.5"/>
                        <text x="60" y="58" text-anchor="middle" font-size="8" fill="#084D9C" font-weight="700" font-family="Inter">OPTIDRIVE</text>
                    </svg>
                </div>
                <div class="product-body">
                    <span class="product-tag">Invertek</span>
                    <h3>Variadores Optidrive E3 / PNP</h3>
                    <p>Control de velocidad para motores trifásicos. Desde 0.4kW hasta 250kW. Ideal para bombas, ventiladores y transportadores.</p>
                    <a href="#contacto" class="product-link">Solicitar cotización →</a>
                </div>
            </div>
            <div class="product-card fade-up">
                <div class="product-image bg-orange">
                    <svg viewBox="0 0 120 120" fill="none">
                        <rect x="25" y="20" width="70" height="80" rx="4" fill="#D4380D" opacity="0.12" stroke="#D4380D" stroke-width="2"/>
                        <line x1="40" y1="40" x2="80" y2="40" stroke="#D4380D" stroke-width="2" opacity="0.4"/>
                        <line x1="40" y1="55" x2="80" y2="55" stroke="#D4380D" stroke-width="2" opacity="0.4"/>
                        <line x1="40" y1="70" x2="80" y2="70" stroke="#D4380D" stroke-width="2" opacity="0.4"/>
                        <circle cx="60" cy="85" r="5" fill="#D4380D" opacity="0.3"/>
                        <path d="M50 35 L60 28 L70 35" stroke="#D4380D" stroke-width="2" fill="none"/>
                    </svg>
                </div>
                <div class="product-body">
                    <span class="product-tag verde">Schrack</span>
                    <h3>Relés de Protección y Contactores</h3>
                    <p>Protección de sobrecarga, cortocircuito y fallas a tierra. Relés industriales y contactores para tableros eléctricos.</p>
                    <a href="#contacto" class="product-link">Solicitar cotización →</a>
                </div>
            </div>
            <div class="product-card fade-up">
                <div class="product-image bg-dark">
                    <svg viewBox="0 0 120 120" fill="none">
                        <rect x="20" y="25" width="80" height="70" rx="6" fill="#1A1A2E" opacity="0.12" stroke="#1A1A2E" stroke-width="2"/>
                        <rect x="30" y="35" width="25" height="15" rx="3" fill="#1A1A2E" opacity="0.15"/>
                        <rect x="65" y="35" width="25" height="15" rx="3" fill="#1A1A2E" opacity="0.15"/>
                        <rect x="30" y="58" width="60" height="8" rx="2" fill="#1A1A2E" opacity="0.1"/>
                        <circle cx="45" cy="80" r="3" fill="#2EB72E"/>
                        <circle cx="60" cy="80" r="3" fill="#2EB72E"/>
                        <circle cx="75" cy="80" r="3" fill="#2EB72E"/>
                    </svg>
                </div>
                <div class="product-body">
                    <span class="product-tag">Murr</span>
                    <h3>Módulos I/O y Conectividad</h3>
                    <p>Sistemas de E/S distribuidos, conectores M8/M12 y cables preensamblados. Soluciones plug & play para automatización.</p>
                    <a href="#contacto" class="product-link">Solicitar cotización →</a>
                </div>
            </div>
            <div class="product-card fade-up">
                <div class="product-image bg-verde">
                    <svg viewBox="0 0 120 120" fill="none">
                        <circle cx="60" cy="60" r="35" fill="#2EB72E" opacity="0.1" stroke="#2EB72E" stroke-width="2"/>
                        <path d="M45 60 L55 70 L75 50" stroke="#2EB72E" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
                        <circle cx="60" cy="60" r="45" fill="none" stroke="#2EB72E" stroke-width="1" opacity="0.2" stroke-dasharray="4 4"/>
                    </svg>
                </div>
                <div class="product-body">
                    <span class="product-tag verde">Schrack</span>
                    <h3>Interruptores Automáticos</h3>
                    <p>Interruptores termomagnéticos y diferenciales para protección de circuitos industriales y residenciales. Certificados IEC.</p>
                    <a href="#contacto" class="product-link">Solicitar cotización →</a>
                </div>
            </div>
            <div class="product-card fade-up">
                <div class="product-image bg-purple">
                    <svg viewBox="0 0 120 120" fill="none">
                        <rect x="30" y="30" width="60" height="60" rx="4" fill="#6B21A8" opacity="0.1" stroke="#6B21A8" stroke-width="2"/>
                        <rect x="38" y="38" width="18" height="12" rx="2" fill="#6B21A8" opacity="0.15"/>
                        <rect x="64" y="38" width="18" height="12" rx="2" fill="#6B21A8" opacity="0.15"/>
                        <rect x="38" y="56" width="44" height="6" rx="2" fill="#6B21A8" opacity="0.1"/>
                        <line x1="30" y1="80" x2="90" y2="80" stroke="#6B21A8" stroke-width="1" opacity="0.2"/>
                        <line x1="38" y1="85" x2="50" y2="85" stroke="#6B21A8" stroke-width="2" opacity="0.3"/>
                        <line x1="56" y1="85" x2="68" y2="85" stroke="#6B21A8" stroke-width="2" opacity="0.3"/>
                        <line x1="74" y1="85" x2="86" y2="85" stroke="#6B21A8" stroke-width="2" opacity="0.3"/>
                    </svg>
                </div>
                <div class="product-body">
                    <span class="product-tag">Murr</span>
                    <h3>Fuentes de Poder y Transformadores</h3>
                    <p>Fuentes conmutadas industriales 24VDC, transformadores de aislamiento y filtros EMC para máxima estabilidad eléctrica.</p>
                    <a href="#contacto" class="product-link">Solicitar cotización →</a>
                </div>
            </div>
            <div class="product-card fade-up">
                <div class="product-image bg-teal">
                    <svg viewBox="0 0 120 120" fill="none">
                        <path d="M60 25 L95 45 L95 85 L60 105 L25 85 L25 45 Z" fill="#0D9488" opacity="0.08" stroke="#0D9488" stroke-width="2"/>
                        <path d="M60 35 L85 50 L85 80 L60 95 L35 80 L35 50 Z" fill="#0D9488" opacity="0.06"/>
                        <circle cx="60" cy="65" r="12" fill="#0D9488" opacity="0.15"/>
                        <text x="60" y="69" text-anchor="middle" font-size="10" fill="#0D9488" font-weight="700" font-family="Inter">IO</text>
                    </svg>
                </div>
                <div class="product-body">
                    <span class="product-tag verde">Invertek</span>
                    <h3>Soft Starters y Accesorios</h3>
                    <p>Arrancadores suaves, filtros EMC, tarjetas de comunicación y kits de frenado. Complementos completos para su variador.</p>
                    <a href="#contacto" class="product-link">Solicitar cotización →</a>
                </div>
            </div>
        </div>
    </section>
    <!-- WHY US -->
    <section class="why-section" id="nosotros">
        <div class="section-header fade-up">
            <div class="section-label">¿Por qué elegirnos?</div>
            <h2 class="section-title">Su socio tecnológico en Ecuador</h2>
            <p class="section-subtitle">Más de 15 años brindando soluciones industriales con respaldo técnico directo de fábrica.</p>
        </div>
        <div class="why-grid">
            <div class="why-card fade-up">
                <div class="why-icon">🏆</div>
                <h4>Distribuidor Autorizado</h4>
                <p>Representación oficial con garantía directa de fábrica y acceso a soporte técnico de nivel 1 y 2.</p>
            </div>
            <div class="why-card fade-up">
                <div class="why-icon">⚙️</div>
                <h4>Soporte Especializado</h4>
                <p>Ingenieros capacitados para programación, puesta en marcha y mantenimiento de equipos.</p>
            </div>
            <div class="why-card fade-up">
                <div class="why-icon">📦</div>
                <h4>Stock en Ecuador</h4>
                <p>Inventario local para entregas rápidas. No espere semanas por equipos importados.</p>
            </div>
            <div class="why-card fade-up">
                <div class="why-icon">🌐</div>
                <h4>Cobertura Nacional</h4>
                <p>Entregas en Quito, Guayaquil, Cuenca y todas las ciudades del Ecuador con logística optimizada.</p>
            </div>
        </div>
    </section>
    <!-- CTA -->
    <section class="cta-section" id="cotiza">
        <div class="cta-inner fade-up">
            <h2>¿Necesitas una <span class="verde">solución industrial</span>?</h2>
            <p>Nuestro equipo de ingenieros te asesora en la selección del equipo correcto para tu aplicación. Cotización sin compromiso con respuesta en menos de 24 horas.</p>
            <div class="cta-buttons">
                <a href="https://wa.me/593992567537?text=Hola%20ARCA%20Energies%2C%20necesito%20una%20cotización%20para%20mi%20proyecto" target="_blank" class="btn btn-white">
                    <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.127.555 4.122 1.523 5.857L.06 23.573a.75.75 0 0 0 .914.914l5.716-1.463A11.94 11.94 0 0 0 12 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 22c-1.94 0-3.765-.54-5.33-1.48l-.372-.222-3.894.997 1.039-3.798-.244-.388A9.96 9.96 0 0 1 2 12C2 6.486 6.486 2 12 2s10 4.486 10 10-4.486 10-10 10z"/></svg>
                    Escribir por WhatsApp
                </a>
                <a href="#contacto" class="btn btn-outline-white">Enviar formulario →</a>
            </div>
        </div>
    </section>
    <!-- CONTACT -->
    <section class="contact-section" id="contacto">
        <div class="section-header fade-up">
            <div class="section-label">Contacto</div>
            <h2 class="section-title">Hablemos de tu proyecto</h2>
            <p class="section-subtitle">Completa el formulario o contáctanos directamente. Respondemos en menos de 24 horas.</p>
        </div>
        <div class="contact-grid">
            <div class="contact-info-card fade-up">
                <h3>Información de contacto</h3>
                <div class="contact-detail">
                    <div class="icon-box">📧</div>
                    <div class="text">
                        <strong>Correo electrónico</strong>
                        <a href="mailto:ventas1@arcaenergies.com">ventas1@arcaenergies.com</a><br>
                        <a href="mailto:ventas3@arcaenergies.com">ventas3@arcaenergies.com</a>
                    </div>
                </div>
                <div class="contact-detail">
                    <div class="icon-box">📱</div>
                    <div class="text">
                        <strong>Teléfono / WhatsApp</strong>
                        <a href="tel:+593992567537">+593 99 256 7537</a>
                    </div>
                </div>
                <div class="contact-detail">
                    <div class="icon-box">📍</div>
                    <div class="text">
                        <strong>Ubicación</strong>
                        Quito, Ecuador<br>Cobertura nacional
                    </div>
                </div>
                <div class="contact-detail">
                    <div class="icon-box">🕐</div>
                    <div class="text">
                        <strong>Horario de atención</strong>
                        Lunes a Viernes: 8:00 - 17:00<br>Sábados: 9:00 - 13:00
                    </div>
                </div>
                <div style="margin-top: 20px; padding: 18px; background: rgba(46,183,46,0.08); border-radius: 12px; border-left: 4px solid var(--verde);">
                    <strong style="color: var(--verde); font-size: 0.88rem;">⚡ Respuesta garantizada en 24h</strong>
                    <p style="color: var(--gris); font-size: 0.8rem; margin-top: 5px; line-height: 1.5;">Nuestro equipo técnico revisa cada solicitud para ofrecerte la solución más adecuada.</p>
                </div>
            </div>
            <div class="contact-form-card fade-up">
                <h3>Solicitar cotización</h3>
                <form id="contactForm">
                    <div class="form-row">
                        <div class="form-group">
                            <label>Nombre completo</label>
                            <input type="text" placeholder="Ej: Juan Pérez" required>
                        </div>
                        <div class="form-group">
                            <label>Empresa</label>
                            <input type="text" placeholder="Nombre de su empresa">
                        </div>
                    </div>
                    <div class="form-row">
                        <div class="form-group">
                            <label>Email</label>
                            <input type="email" placeholder="correo@empresa.com" required>
                        </div>
                        <div class="form-group">
                            <label>Teléfono</label>
                            <input type="tel" placeholder="+593 99 000 0000">
                        </div>
                    </div>
                    <div class="form-group">
                        <label>Marca de interés</label>
                        <select>
                            <option value="">Seleccionar marca...</option>
                            <option>Invertek Drives</option>
                            <option>Schrack Technik</option>
                            <option>Murr Elektronik</option>
                            <option>Varias marcas / No estoy seguro</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Descripción del proyecto</label>
                        <textarea placeholder="Cuéntenos sobre su aplicación, equipos necesarios, cantidades estimadas..."></textarea>
                    </div>
                    <button type="submit" class="form-submit">Enviar solicitud de cotización</button>
                </form>
            </div>
        </div>
    </section>
    <!-- FOOTER -->
    <footer class="footer">
        <div class="footer-inner">
            <div class="footer-brand">
                <h3>ARCA<span>ENERGIES</span> S.A.</h3>
                <p>Distribuidor autorizado de marcas europeas líderes en automatización industrial, control de motores y protección eléctrica en Ecuador.</p>
            </div>
            <div class="footer-col">
                <h4>Marcas</h4>
                <a href="#marcas">Invertek Drives</a>
                <a href="#marcas">Schrack Technik</a>
                <a href="#marcas">Murr Elektronik</a>
            </div>
            <div class="footer-col">
                <h4>Productos</h4>
                <a href="#productos">Variadores de frecuencia</a>
                <a href="#productos">Protecciones eléctricas</a>
                <a href="#productos">Conectividad industrial</a>
                <a href="#productos">Fuentes de poder</a>
            </div>
            <div class="footer-col">
                <h4>Contacto</h4>
                <a href="mailto:ventas1@arcaenergies.com">ventas1@arcaenergies.com</a>
                <a href="tel:+593992567537">+593 99 256 7537</a>
                <a href="#contacto">Solicitar cotización</a>
                <a href="https://wa.me/593992567537" target="_blank">WhatsApp directo</a>
            </div>
        </div>
        <div class="footer-bottom">
            <span>© 2026 ARCA ENERGIES S.A. Todos los derechos reservados.</span>
            <span>Quito, Ecuador 🇪🇨</span>
        </div>
    </footer>
    <!-- WHATSAPP FLOAT -->
    <a href="https://wa.me/593992567537?text=Hola%20ARCA%20Energies%2C%20quiero%20información" target="_blank" class="whatsapp-float" aria-label="WhatsApp">
        <svg viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.981.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
    </a>
    <script>
        // Navbar: oculta en inicio, aparece al hacer scroll, se oculta al volver arriba
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            const scrollY = window.pageYOffset;
             if (scrollY > 150) {
                navbar.classList.add('visible');
            } else {
                navbar.classList.remove('visible');
            }
        });
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.getElementById('navLinks');
        hamburger.addEventListener('click', () => {
            hamburger.classList.toggle('active');
            navLinks.classList.toggle('open');
        });
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('open');
                hamburger.classList.remove('active');
            });
        });
        const fadeElements = document.querySelectorAll('.fade-up');
        const observerOptions = {
            threshold: 0.12,
            rootMargin: '0px 0px -30px 0px'
        };
        const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);
        fadeElements.forEach(el => observer.observe(el));
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const btn = this.querySelector('.form-submit');
            const originalText = btn.textContent;
            btn.textContent = '✓ ¡Solicitud enviada con éxito!';
            btn.style.background = '#2EB72E';
            setTimeout(() => {
                btn.textContent = originalText;
                btn.style.background = '';
                this.reset();
            }, 3000);
        });
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    e.preventDefault();
                    const offset = 70;
                    const position = target.getBoundingClientRect().top + window.pageYOffset - offset;
                    window.scrollTo({ top: position, behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html>
