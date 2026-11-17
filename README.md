# BlueSoul
Indumentary
<!DOCTYPE html>
<html lang="es-AR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>BlueSouls — De la pista a la calle | Catálogo Urbano</title>
  <meta name="description" content="Ropa urbana inspirada en el patinaje y el hockey sobre hielo. Diseñada para usar en la pista y en las calles de Buenos Aires." />

  <!-- Tipografías: estilo deportivo urbano + lectura limpia -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:ital,wght@0,700;0,800;1,800&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet" />

  <style>
    :root {
      --azul-profundo: #0A1F44;
      --azul-electrico: #1E5BFF;
      --negro: #0B0B0F;
      --blanco-hielo: #F5F8FF;

      --borde-suave: rgba(245, 248, 255, 0.12);
      --borde-activo: rgba(30, 91, 255, 0.7);
      --texto-secundario: rgba(245, 248, 255, 0.72);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background-color: var(--negro);
      color: var(--blanco-hielo);
      font-family: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, sans-serif;
      line-height: 1.5;
      overflow-x: hidden;
      -webkit-font-smoothing: antialiased;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      font-family: inherit;
      cursor: pointer;
      border: none;
      background: none;
      color: inherit;
    }

    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    .display-font {
      font-family: 'Barlow Condensed', sans-serif;
      text-transform: uppercase;
      letter-spacing: 0.02em;
    }

    /* ================= NAVBAR ================= */
    .navbar {
      position: sticky;
      top: 0;
      z-index: 50;
      background: rgba(11, 11, 15, 0.85);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--borde-suave);
    }

    .nav-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 72px;
      gap: 16px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .brand-name {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.65rem;
      font-weight: 800;
      letter-spacing: 0.05em;
      text-transform: uppercase;
      color: var(--blanco-hielo);
    }

    .brand-name span {
      color: var(--azul-electrico);
    }

    .nav-links {
      display: none;
      gap: 28px;
      font-size: 0.95rem;
      font-weight: 500;
      color: var(--texto-secundario);
    }

    .nav-links a:hover {
      color: var(--blanco-hielo);
    }

    .btn-primary {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      background-color: var(--azul-electrico);
      color: var(--blanco-hielo);
      font-weight: 700;
      font-size: 0.92rem;
      padding: 11px 20px;
      border-radius: 999px;
      transition: transform 0.18s ease, background-color 0.18s ease, box-shadow 0.18s ease;
    }

    .btn-primary:hover {
      background-color: #366eff;
      transform: translateY(-1px);
      box-shadow: 0 8px 24px rgba(30, 91, 255, 0.35);
    }

    .btn-outline {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      background-color: transparent;
      color: var(--blanco-hielo);
      border: 1.5px solid var(--borde-suave);
      font-weight: 600;
      font-size: 0.92rem;
      padding: 11px 22px;
      border-radius: 999px;
      transition: border-color 0.18s ease, background-color 0.18s ease;
    }

    .btn-outline:hover {
      border-color: var(--blanco-hielo);
      background-color: rgba(245, 248, 255, 0.06);
    }

    @media (min-width: 768px) {
      .nav-links {
        display: flex;
      }
    }

    /* ================= HERO ================= */
    .hero {
      position: relative;
      padding: 56px 0 64px;
      background:
        radial-gradient(circle at 80% 20%, rgba(30, 91, 255, 0.22), transparent 50%),
        radial-gradient(circle at 15% 80%, rgba(10, 31, 68, 0.7), transparent 55%),
        var(--negro);
      border-bottom: 1px solid var(--borde-suave);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 40px;
      align-items: center;
    }

    @media (min-width: 900px) {
      .hero {
        padding: 80px 0 92px;
      }
      .hero-grid {
        grid-template-columns: 1.15fr 0.85fr;
        gap: 56px;
      }
    }

    .hero-tag {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 6px 14px;
      border-radius: 999px;
      background: rgba(10, 31, 68, 0.85);
      border: 1px solid rgba(30, 91, 255, 0.45);
      font-size: 0.8rem;
      font-weight: 600;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      color: var(--blanco-hielo);
      margin-bottom: 20px;
    }

    .hero-tag-dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background-color: var(--azul-electrico);
    }

    .hero-title {
      font-size: clamp(2.9rem, 7vw, 4.8rem);
      line-height: 0.94;
      font-weight: 800;
      margin-bottom: 20px;
    }

    .hero-title .accent {
      color: var(--azul-electrico);
      font-style: italic;
    }

    .hero-desc {
      font-size: 1.06rem;
      color: var(--texto-secundario);
      max-width: 520px;
      margin-bottom: 30px;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-bottom: 34px;
    }

    .hero-meta {
      display: flex;
      flex-wrap: wrap;
      gap: 24px;
      padding-top: 22px;
      border-top: 1px solid var(--borde-suave);
      font-size: 0.88rem;
      color: var(--texto-secundario);
    }

    .hero-meta strong {
      display: block;
      color: var(--blanco-hielo);
      font-size: 1rem;
      margin-bottom: 2px;
    }

    /* Hero Feature Card */
    .hero-card {
      position: relative;
      background: linear-gradient(160deg, var(--azul-profundo) 0%, #07142c 100%);
      border: 1px solid rgba(245, 248, 255, 0.16);
      border-radius: 24px;
      padding: 28px;
      overflow: hidden;
      box-shadow: 0 24px 60px rgba(0, 0, 0, 0.55);
    }

    .hero-card-badge {
      display: inline-block;
      background: var(--blanco-hielo);
      color: var(--azul-profundo);
      font-size: 0.74rem;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 0.06em;
      padding: 5px 12px;
      border-radius: 999px;
      margin-bottom: 14px;
    }

    .hero-card-visual {
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 16px 0 20px;
    }

    .hero-card-info {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 12px;
      padding-top: 16px;
      border-top: 1px solid rgba(245, 248, 255, 0.14);
    }

    .hero-card-info h3 {
      font-size: 1.25rem;
      font-weight: 700;
    }

    .hero-card-info p {
      font-size: 0.86rem;
      color: var(--texto-secundario);
    }

    .hero-card-price {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.8rem;
      font-weight: 800;
      color: var(--blanco-hielo);
      white-space: nowrap;
    }

    /* ================= CINTA / TICKER ================= */
    .rink-strip {
      background-color: var(--azul-profundo);
      border-bottom: 3px solid var(--azul-electrico);
      padding: 13px 0;
      overflow: hidden;
    }

    .rink-strip-track {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 14px 32px;
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.05rem;
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--blanco-hielo);
    }

    .rink-strip-track span {
      display: inline-flex;
      align-items: center;
      gap: 10px;
    }

    .rink-strip-track span::before {
      content: "";
      width: 6px;
      height: 6px;
      background-color: var(--azul-electrico);
      border-radius: 50%;
    }

    /* ================= CATÁLOGO ================= */
    .section {
      padding: 72px 0;
    }

    .section-header {
      display: flex;
      flex-direction: column;
      gap: 16px;
      margin-bottom: 36px;
    }

    @media (min-width: 768px) {
      .section-header {
        flex-direction: row;
        align-items: flex-end;
        justify-content: space-between;
      }
    }

    .section-kicker {
      color: var(--azul-electrico);
      font-size: 0.85rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin-bottom: 6px;
    }

    .section-title {
      font-size: clamp(2.1rem, 4.5vw, 3.1rem);
      line-height: 1;
      font-weight: 800;
    }

    .section-subtitle {
      color: var(--texto-secundario);
      max-width: 460px;
      font-size: 0.96rem;
    }

    /* Filtros */
    .filters {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 32px;
    }

    .filter-btn {
      padding: 9px 18px;
      border-radius: 999px;
      font-size: 0.88rem;
      font-weight: 600;
      background-color: rgba(245, 248, 255, 0.05);
      color: var(--texto-secundario);
      border: 1px solid var(--borde-suave);
      transition: all 0.18s ease;
    }

    .filter-btn:hover {
      color: var(--blanco-hielo);
      border-color: rgba(245, 248, 255, 0.35);
    }

    .filter-btn.active {
      background-color: var(--azul-electrico);
      color: var(--blanco-hielo);
      border-color: var(--azul-electrico);
    }

    /* Grilla de productos */
    .catalog-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 24px;
    }

    .product-card {
      display: flex;
      flex-direction: column;
      background-color: #11131a;
      border: 1px solid var(--borde-suave);
      border-radius: 20px;
      overflow: hidden;
      transition: transform 0.2s ease, border-color 0.2s ease;
    }

    .product-card:hover {
      transform: translateY(-4px);
      border-color: var(--borde-activo);
    }

    .product-card.hidden {
      display: none;
    }

    .product-media {
      position: relative;
      height: 250px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: radial-gradient(circle at center, rgba(10, 31, 68, 0.65) 0%, #0d1018 85%);
      border-bottom: 1px solid var(--borde-suave);
      padding: 20px;
    }

    .product-badge {
      position: absolute;
      top: 14px;
      left: 14px;
      background-color: var(--azul-profundo);
      color: var(--blanco-hielo);
      border: 1px solid rgba(245, 248, 255, 0.2);
      font-size: 0.72rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.05em;
      padding: 4px 10px;
      border-radius: 999px;
    }

    .product-badge.hot {
      background-color: var(--azul-electrico);
      border-color: var(--azul-electrico);
    }

    .product-body {
      display: flex;
      flex-direction: column;
      flex: 1;
      padding: 20px;
    }

    .product-top {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 10px;
      margin-bottom: 8px;
    }

    .product-title {
      font-size: 1.12rem;
      font-weight: 700;
      line-height: 1.25;
    }

    .product-price {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.45rem;
      font-weight: 800;
      color: var(--blanco-hielo);
      white-space: nowrap;
    }

    .product-desc {
      font-size: 0.88rem;
      color: var(--texto-secundario);
      margin-bottom: 16px;
      flex: 1;
    }

    /* Selector de talles */
    .size-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 8px;
      margin-bottom: 16px;
    }

    .size-label {
      font-size: 0.78rem;
      color: var(--texto-secundario);
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.05em;
    }

    .size-pills {
      display: flex;
      gap: 6px;
    }

    .size-pill {
      min-width: 32px;
      height: 28px;
      padding: 0 8px;
      border-radius: 6px;
      font-size: 0.78rem;
      font-weight: 700;
      border: 1px solid var(--borde-suave);
      color: var(--texto-secundario);
      background-color: rgba(245, 248, 255, 0.03);
      transition: all 0.15s ease;
    }

    .size-pill:hover {
      border-color: var(--blanco-hielo);
      color: var(--blanco-hielo);
    }

    .size-pill.selected {
      background-color: var(--blanco-hielo);
      color: var(--negro);
      border-color: var(--blanco-hielo);
    }

    .btn-card-wa {
      width: 100%;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 11px 16px;
      border-radius: 12px;
      background-color: var(--azul-profundo);
      color: var(--blanco-hielo);
      border: 1px solid rgba(30, 91, 255, 0.45);
      font-size: 0.88rem;
      font-weight: 700;
      transition: background-color 0.18s ease, border-color 0.18s ease;
    }

    .btn-card-wa:hover {
      background-color: var(--azul-electrico);
      border-color: var(--azul-electrico);
    }

    /* ================= LA ONDA / PISTA & CALLE ================= */
    .vibe-section {
      background-color: var(--azul-profundo);
      border-top: 1px solid var(--borde-suave);
      border-bottom: 1px solid var(--borde-suave);
    }

    .vibe-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 20px;
    }

    @media (min-width: 768px) {
      .vibe-grid {
        grid-template-columns: repeat(3, 1fr);
      }
    }

    .vibe-card {
      background-color: rgba(11, 11, 15, 0.55);
      border: 1px solid rgba(245, 248, 255, 0.14);
      border-radius: 18px;
      padding: 26px;
    }

    .vibe-num {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 2.2rem;
      font-weight: 800;
      color: var(--azul-electrico);
      line-height: 1;
      margin-bottom: 12px;
    }

    .vibe-card h3 {
      font-size: 1.15rem;
      font-weight: 700;
      margin-bottom: 8px;
    }

    .vibe-card p {
      font-size: 0.92rem;
      color: var(--texto-secundario);
    }

    /* ================= CÓMO COMPRAR ================= */
    .steps-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 20px;
    }

    @media (min-width: 768px) {
      .steps-grid {
        grid-template-columns: repeat(3, 1fr);
      }
    }

    .step-box {
      background-color: #11131a;
      border: 1px solid var(--borde-suave);
      border-radius: 18px;
      padding: 26px;
    }

    .step-badge {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 34px;
      height: 34px;
      border-radius: 10px;
      background-color: var(--azul-electrico);
      color: var(--blanco-hielo);
      font-weight: 800;
      font-size: 0.95rem;
      margin-bottom: 14px;
    }

    .step-box h3 {
      font-size: 1.1rem;
      font-weight: 700;
      margin-bottom: 6px;
    }

    .step-box p {
      font-size: 0.9rem;
      color: var(--texto-secundario);
    }

    /* ================= CTA WHATSAPP BANNER ================= */
    .cta-banner {
      background: linear-gradient(135deg, var(--azul-profundo) 0%, #102b5c 55%, var(--azul-electrico) 140%);
      border: 1px solid rgba(245, 248, 255, 0.18);
      border-radius: 24px;
      padding: 40px 28px;
      display: flex;
      flex-direction: column;
      gap: 24px;
      align-items: flex-start;
      justify-content: space-between;
    }

    @media (min-width: 768px) {
      .cta-banner {
        flex-direction: row;
        align-items: center;
        padding: 48px 48px;
      }
    }

    .cta-banner h2 {
      font-size: clamp(2rem, 4vw, 2.8rem);
      line-height: 1;
      margin-bottom: 10px;
    }

    .cta-banner p {
      color: var(--blanco-hielo);
      opacity: 0.85;
      max-width: 520px;
      font-size: 0.98rem;
    }

    .btn-ice {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      background-color: var(--blanco-hielo);
      color: var(--azul-profundo);
      font-weight: 800;
      font-size: 0.96rem;
      padding: 14px 26px;
      border-radius: 999px;
      white-space: nowrap;
      transition: transform 0.18s ease, box-shadow 0.18s ease;
    }

    .btn-ice:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 28px rgba(11, 11, 15, 0.35);
    }

    /* ================= FOOTER ================= */
    footer {
      border-top: 1px solid var(--borde-suave);
      padding: 36px 0;
      font-size: 0.88rem;
      color: var(--texto-secundario);
    }

    .footer-inner {
      display: flex;
      flex-direction: column;
      gap: 16px;
      justify-content: space-between;
      align-items: flex-start;
    }

    @media (min-width: 768px) {
      .footer-inner {
        flex-direction: row;
        align-items: center;
      }
    }

    /* ================= BOTÓN FLOTANTE WHATSAPP ================= */
    .wa-float {
      position: fixed;
      right: 22px;
      bottom: 22px;
      z-index: 60;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background-color: var(--azul-electrico);
      color: var(--blanco-hielo);
      padding: 13px 18px;
      border-radius: 999px;
      font-weight: 700;
      font-size: 0.9rem;
      box-shadow: 0 12px 32px rgba(30, 91, 255, 0.45);
      border: 1px solid rgba(245, 248, 255, 0.25);
      transition: transform 0.2s ease, background-color 0.2s ease;
    }

    .wa-float:hover {
      transform: scale(1.04);
      background-color: #366eff;
    }

    @media (max-width: 480px) {
      .wa-float span {
        display: none;
      }
      .wa-float {
        padding: 14px;
      }
    }
  </style>
</head>
<body>

  <!-- ================= NAVBAR ================= -->
  <header class="navbar">
    <div class="container nav-inner">
      <a href="#" class="brand" aria-label="BlueSouls Inicio">
        <!-- Emblema circular BS inspirado en el jersey -->
        <svg width="40" height="40" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <circle cx="24" cy="27" r="14" fill="#0A1F44" stroke="#F5F8FF" stroke-width="2.8"/>
          <circle cx="40" cy="37" r="14" fill="#0A1F44" stroke="#F5F8FF" stroke-width="2.8"/>
          <text x="17" y="34" fill="#F5F8FF" font-family="Barlow Condensed, sans-serif" font-weight="800" font-size="20">B</text>
          <text x="34" y="44" fill="#F5F8FF" font-family="Barlow Condensed, sans-serif" font-weight="800" font-size="20">S</text>
        </svg>
        <span class="brand-name">Blue<span>Souls</span></span>
      </a>

      <nav class="nav-links" aria-label="Navegación principal">
        <a href="#catalogo">Catálogo</a>
        <a href="#la-onda">Pista &amp; Calle</a>
        <a href="#como-comprar">Cómo comprar</a>
        <a href="#contacto">Contacto</a>
      </nav>

      <a
        href="https://wa.me/5491100000000?text=Hola%20BlueSouls!%20Quiero%20consultar%20por%20el%20cat%C3%A1logo."
        target="_blank"
        rel="noopener noreferrer"
        class="btn-primary"
      >
        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
          <path d="M12.03 2C6.5 2 2 6.48 2 12c0 1.77.46 3.5 1.34 5.02L2 22l5.12-1.33A9.97 9.97 0 0 0 12.03 22C17.56 22 22 17.52 22 12S17.56 2 12.03 2zm5.8 14.23c-.24.68-1.42 1.3-1.97 1.37-.5.07-1.15.1-1.85-.12-.43-.14-.98-.32-1.69-.63-2.97-1.29-4.91-4.3-5.06-4.5-.15-.2-1.2-1.6-1.2-3.05 0-1.45.76-2.16 1.03-2.46.27-.3.59-.37.79-.37h.57c.18 0 .43-.07.67.51.24.58.83 2.02.9 2.17.07.15.12.33.02.53-.1.2-.15.32-.3.5-.15.18-.32.4-.45.54-.15.15-.31.32-.13.62.18.3.78 1.29 1.68 2.09 1.15 1.02 2.12 1.34 2.42 1.49.3.15.48.13.66-.07.18-.2.76-.88.96-1.18.2-.3.4-.25.67-.15.27.1 1.74.82 2.04.97.3.15.5.22.57.34.07.12.07.7-.17 1.38z"/>
        </svg>
        WhatsApp
      </a>
    </div>
  </header>

  <!-- ================= HERO ================= -->
  <section class="hero">
    <div class="container hero-grid">
      <div>
        <div class="hero-tag">
          <span class="hero-tag-dot"></span>
          Buenos Aires · Pista &amp; Asfalto
        </div>

        <h1 class="hero-title display-font">
          De la pista <br />
          <span class="accent">a la calle.</span>
        </h1>

        <p class="hero-desc">
          Ropa urbana cómoda y con peso, inspirada en el patinaje y el hockey sobre hielo. Pensada para tirarte encima cuando salís a patinar o para caminar por Buenos Aires con facha propia.
        </p>

        <div class="hero-actions">
          <a href="#catalogo" class="btn-primary">Ver catálogo completo</a>
          <a
            href="https://wa.me/5491100000000?text=Hola%20BlueSouls!%20Me%20gustar%C3%ADa%20consultar%20por%20talles%20y%20env%C3%ADos."
            target="_blank"
            rel="noopener noreferrer"
            class="btn-outline"
          >
            Escribinos por WhatsApp
          </a>
        </div>

        <div class="hero-meta">
          <div>
            <strong>Fit Oversize Real</strong>
            Cómodo para moverte y abrigarte
          </div>
          <div>
            <strong>Envíos en el día</strong>
            CABA, GBA y todo el país
          </div>
          <div>
            <strong>Sin vueltas</strong>
            Elegís, mandás WhatsApp y listo
          </div>
        </div>
      </div>

      <!-- Tarjeta destacada: Jersey BS -->
      <div class="hero-card">
        <span class="hero-card-badge">Pieza Central · Drop #01</span>
        <div class="hero-card-visual">
          <!-- Ilustración SVG del Jersey BS Original -->
          <svg width="260" height="230" viewBox="0 0 260 230" fill="none" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Jersey BlueSouls Azul Profundo">
            <!-- Cuerpo del jersey -->
            <path d="M72 28 L40 44 L12 118 L44 130 L62 78 L62 204 L198 204 L198 78 L216 130 L248 118 L220 44 L188 28 L158 24 C148 44 112 44 102 24 Z" fill="#0A1F44" stroke="#F5F8FF" stroke-width="2.5" stroke-linejoin="round"/>
            <!-- Cuello en V -->
            <path d="M102 24 L130 58 L158 24" fill="none" stroke="#F5F8FF" stroke-width="5" stroke-linejoin="round"/>
            <path d="M107 24 L130 50 L153 24" fill="#F5F8FF"/>
            <path d="M113 24 L130 43 L147 24" fill="#0A1F44"/>
            <!-- Franjas mangas -->
            <path d="M25 84 L55 96" stroke="#F5F8FF" stroke-width="7"/>
            <path d="M235 84 L205 96" stroke="#F5F8FF" stroke-width="7"/>
            <!-- Franjas inferiores -->
            <rect x="63" y="168" width="134" height="9" fill="#F5F8FF"/>
            <rect x="63" y="184" width="134" height="9" fill="#F5F8FF"/>
            <!-- Logo BS pecho -->
            <circle cx="119" cy="103" r="19" fill="#0A1F44" stroke="#F5F8FF" stroke-width="2.8"/>
            <circle cx="141" cy="113" r="19" fill="#0A1F44" stroke="#F5F8FF" stroke-width="2.8"/>
            <text x="110" y="112" fill="#F5F8FF" font-family="Barlow Condensed, sans-serif" font-weight="800" font-size="25">B</text>
            <text x="133" y="122" fill="#F5F8FF" font-family="Barlow Condensed, sans-serif" font-weight="800" font-size="25">S</text>
          </svg>
        </div>

        <div class="hero-card-info">
          <div>
            <h3>Jersey BS Original</h3>
            <p>Azul profundo + rayas hielo · Talles S al XL</p>
          </div>
          <div class="hero-card-price">$68.000</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ================= CINTA ESTILO PISTA ================= -->
  <div class="rink-strip">
    <div class="container rink-strip-track">
      <span>Estilo Pista &amp; Calle</span>
      <span>Oversize Cómodo</span>
      <span>Hecho para Buenos Aires</span>
      <span>Stock Limitado</span>
      <span>Atención directa por WhatsApp</span>
    </div>
  </div>

  <!-- ================= CATÁLOGO ================= -->
  <section id="catalogo" class="section">
    <div class="container">
      <div class="section-header">
        <div>
          <p class="section-kicker">Catálogo BlueSouls</p>
          <h2 class="section-title display-font">Elegí tu equipo</h2>
        </div>
        <p class="section-subtitle">
          Prendas pensadas para aguantar el frío de la pista y quedar increíbles en cualquier esquina de la ciudad. Tocá tu talle y pedí directo por WhatsApp.
        </p>
      </div>

      <!-- Filtros por categoría -->
      <div class="filters" role="tablist" aria-label="Filtrar prendas por categoría">
        <button class="filter-btn active" data-filter="all" type="button">Todo el catálogo</button>
        <button class="filter-btn" data-filter="abrigos" type="button">Jerseys &amp; Buzos</button>
        <button class="filter-btn" data-filter="pantalones" type="button">Pantalones</button>
        <button class="filter-btn" data-filter="accesorios" type="button">Accesorios</button>
      </div>

      <!-- Grilla de productos -->
      <div class="catalog-grid" id="catalogGrid">

        <!-- Producto 1: Jersey BS Original -->
        <article class="product-card" data-category="abrigos" data-name="Jersey BS Original" data-price="$68.000">
          <div class="product-media">
            <span class="product-badge hot">Más pedido</span>
            <svg width="175" height="165" viewBox="0 0 260 230" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path d="M72 28 L40 44 L12 118 L44 130 L62 78 L62 204 L198 204 L198 78 L216 130 L248 118 L220 44 L188 28 L158 24 C148 44 112 44 102 24 Z" fill="#0A1F44" stroke="#F5F8FF" stroke-width="3"/>
              <path d="M102 24 L130 56 L158 24" stroke="#F5F8FF" stroke-width="5"/>
              <path d="M25 84 L55 96" stroke="#F5F8FF" stroke-width="8"/>
              <path d="M235 84 L205 96" stroke="#F5F8FF" stroke-width="8"/>
              <rect x="63" y="168" width="134" height="9" fill="#F5F8FF"/>
              <rect x="63" y="184" width="134" height="9" fill="#F5F8FF"/>
              <circle cx="119" cy="103" r="19" fill="#0A1F44" stroke="#F5F8FF" stroke-width="3"/>
              <circle cx="141" cy="113" r="19" fill="#0A1F44" stroke="#F5F8FF" stroke-width="3"/>
              <text x="110" y="112" fill="#F5F8FF" font-family="Barlow Condensed, sans-serif" font-weight="800" font-size="24">B</text>
              <text x="133" y="122" fill="#F5F8FF" font-family="Barlow Condensed, sans-serif" font-weight="800" font-size="24">S</text>
            </svg>
          </div>
          <div class="product-body">
            <div class="product-top">
              <h3 class="product-title">Jersey BS Original</h3>
              <span class="product-price">$68.000</span>
            </div>
            <p class="product-desc">Corte amplio clásico de hockey en azul profundo. Suelto, liviano y perfecto para usar arriba de un buzo o solo.</p>
            <div class="size-row">
              <span class="size-label">Talle</span>
              <div class="size-pills">
                <button type="button" class="size-pill">S</button>
                <button type="button" class="size-pill selected">M</button>
                <button type="button" class="size-pill">L</button>
                <button type="button" class="size-pill">XL</button>
              </div>
            </div>
            <button type="button" class="btn-card-wa">Pedir por WhatsApp</button>
          </div>
        </article>

        <!-- Producto 2: Cargo Pista Negro -->
        <article class="product-card" data-category="pantalones" data-name="Cargo Pista Negro" data-price="$74.000">
          <div class="product-media">
            <span class="product-badge">Clave</span>
            <svg width="150" height="170" viewBox="0 0 180 210" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <!-- Pantalón cargo ancho -->
              <path d="M46 18 L134 18 L146 192 L106 192 L90 88 L74 192 L34 192 Z" fill="#0B0B0F" stroke="#F5F8FF" stroke-width="2.5" stroke-linejoin="round"/>
              <!-- Cintura -->
              <rect x="46" y="18" width="88" height="14" fill="#0A1F44" stroke="#F5F8FF" stroke-width="2"/>
              <!-- Bolsillos cargo -->
              <rect x="36" y="82" width="20" height="36" rx="2" fill="#151822" stroke="#F5F8FF" stroke-width="2"/>
              <rect x="124" y="82" width="20" height="36" rx="2" fill="#151822" stroke="#F5F8FF" stroke-width="2"/>
              <!-- Detalle etiqueta azul eléctrico -->
              <rect x="128" y="88" width="12" height="5" fill="#1E5BFF"/>
            </svg>
          </div>
          <div class="product-body">
            <div class="product-top">
              <h3 class="product-title">Cargo Pista Negro</h3>
              <span class="product-price">$74.000</span>
            </div>
            <p class="product-desc">Pierna ancha que cae impecable sobre zapas o patines. Tela resistente con bolsillos grandes para llevar todo encima.</p>
            <div class="size-row">
              <span class="size-label">Talle</span>
              <div class="size-pills">
                <button type="button" class="size-pill">38</button>
                <button type="button" class="size-pill selected">40</button>
                <button type="button" class="size-pill">42</button>
                <button type="button" class="size-pill">44</button>
              </div>
            </div>
            <button type="button" class="btn-card-wa">Pedir por WhatsApp</button>
          </div>
        </article>

        <!-- Producto 3: Hoodie Hielo Heavy -->
        <article class="product-card" data-category="abrigos" data-name="Hoodie Hielo Heavy" data-price="$79.000">
          <div class="product-media">
            <span class="product-badge hot">Abrigo</span>
            <svg width="165" height="165" viewBox="0 0 220 210" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <!-- Capucha -->
              <path d="M80 42 C80 18 140 18 140 42 L130 56 L90 56 Z" fill="#DDE6FF" stroke="#0A1F44" stroke-width="2.5"/>
              <!-- Cuerpo hoodie blanco hielo -->
              <path d="M74 44 L44 62 L24 134 L50 142 L64 90 L64 186 L156 186 L156 90 L170 142 L196 134 L176 62 L146 44 Z" fill="#F5F8FF" stroke="#0A1F44" stroke-width="2.5" stroke-linejoin="round"/>
              <!-- Bolsillo canguro -->
              <path d="M76 134 L144 134 L150 170 L70 170 Z" fill="#E5ECFF" stroke="#0A1F44" stroke-width="2"/>
              <!-- Estampa pecho -->
              <circle cx="102" cy="92" r="13" stroke="#1E5BFF" stroke-width="2.5"/>
              <circle cx="118" cy="100" r="13" stroke="#0A1F44" stroke-width="2.5"/>
            </svg>
          </div>
          <div class="product-body">
            <div class="product-top">
              <h3 class="product-title">Hoodie Hielo Heavy</h3>
              <span class="product-price">$79.000</span>
            </div>
            <p class="product-desc">Frisa pesada en blanco hielo bien abrigada, con capucha doble y hombros caídos. Tu aliado para las noches frías.</p>
            <div class="size-row">
              <span class="size-label">Talle</span>
              <div class="size-pills">
                <button type="button" class="size-pill">S</button>
                <button type="button" class="size-pill selected">M</button>
                <button type="button" class="size-pill">L</button>
                <button type="button" class="size-pill">XL</button>
              </div>
            </div>
            <button type="button" class="btn-card-wa">Pedir por WhatsApp</button>
          </div>
        </article>

        <!-- Producto 4: Jersey Eléctrico Rink -->
        <article class="product-card" data-category="abrigos" data-name="Jersey Eléctrico Rink" data-price="$69.500">
          <div class="product-media">
            <span class="product-badge">Nuevo</span>
            <svg width="175" height="165" viewBox="0 0 260 230" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path d="M72 28 L40 44 L12 118 L44 130 L62 78 L62 204 L198 204 L198 78 L216 130 L248 118 L220 44 L188 28 L158 24 C148 44 112 44 102 24 Z" fill="#1E5BFF" stroke="#F5F8FF" stroke-width="3"/>
              <path d="M102 24 L130 56 L158 24" stroke="#0B0B0F" stroke-width="7"/>
              <path d="M25 84 L55 96" stroke="#0B0B0F" stroke-width="9"/>
              <path d="M235 84 L205 96" stroke="#0B0B0F" stroke-width="9"/>
              <rect x="63" y="168" width="134" height="10" fill="#0B0B0F"/>
              <rect x="63" y="184" width="134" height="6" fill="#F5F8FF"/>
              <text x="130" y="128" text-anchor="middle" fill="#F5F8FF" font-family="Barlow Condensed, sans-serif" font-weight="800" font-size="48">24</text>
            </svg>
          </div>
          <div class="product-body">
            <div class="product-top">
              <h3 class="product-title">Jersey Eléctrico Rink</h3>
              <span class="product-price">$69.500</span>
            </div>
            <p class="product-desc">Azul eléctrico vibrante con vivos negros y número frontal. Para destacar apenas entrás a la pista o al subte.</p>
            <div class="size-row">
              <span class="size-label">Talle</span>
              <div class="size-pills">
                <button type="button" class="size-pill">S</button>
                <button type="button" class="size-pill">M</button>
                <button type="button" class="size-pill selected">L</button>
                <button type="button" class="size-pill">XL</button>
              </div>
            </div>
            <button type="button" class="btn-card-wa">Pedir por WhatsApp</button>
          </div>
        </article>

        <!-- Producto 5: Gorro Beanie BS -->
        <article class="product-card" data-category="accesorios" data-name="Gorro Beanie BS" data-price="$24.000">
          <div class="product-media">
            <span class="product-badge">Unisex</span>
            <svg width="145" height="145" viewBox="0 0 180 180" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path d="M40 110 C40 52 140 52 140 110 Z" fill="#0A1F44" stroke="#F5F8FF" stroke-width="2.5"/>
              <rect x="34" y="106" width="112" height="32" rx="8" fill="#0B0B0F" stroke="#F5F8FF" stroke-width="2.5"/>
              <!-- Parche BS -->
              <rect x="74" y="113" width="32" height="18" rx="4" fill="#1E5BFF"/>
              <text x="90" y="126" text-anchor="middle" fill="#F5F8FF" font-family="Barlow Condensed, sans-serif" font-weight="800" font-size="13">BS</text>
            </svg>
          </div>
          <div class="product-body">
            <div class="product-top">
              <h3 class="product-title">Gorro Beanie BS</h3>
              <span class="product-price">$24.000</span>
            </div>
            <p class="product-desc">Tejido suave que no pica, con doblez ancho y parche bordado. Abriga las orejas sin aplastar el look.</p>
            <div class="size-row">
              <span class="size-label">Talle</span>
              <div class="size-pills">
                <button type="button" class="size-pill selected">Único</button>
              </div>
            </div>
            <button type="button" class="btn-card-wa">Pedir por WhatsApp</button>
          </div>
        </article>

        <!-- Producto 6: Bolso Porta-Patines -->
        <article class="product-card" data-category="accesorios" data-name="Bolso Urbano Porta-Patines" data-price="$56.000">
          <div class="product-media">
            <span class="product-badge">Para patinar</span>
            <svg width="165" height="150" viewBox="0 0 210 180" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <!-- Correa -->
              <path d="M55 64 C55 24 155 24 155 64" stroke="#1E5BFF" stroke-width="8" stroke-linecap="round"/>
              <!-- Cuerpo bolso -->
              <rect x="32" y="64" width="146" height="84" rx="18" fill="#0B0B0F" stroke="#F5F8FF" stroke-width="2.5"/>
              <rect x="46" y="78" width="118" height="56" rx="10" fill="#0A1F44"/>
              <circle cx="96" cy="106" r="14" stroke="#F5F8FF" stroke-width="2.5"/>
              <circle cx="114" cy="112" r="14" stroke="#F5F8FF" stroke-width="2.5"/>
            </svg>
          </div>
          <div class="product-body">
            <div class="product-top">
              <h3 class="product-title">Bolso Porta-Patines</h3>
              <span class="product-price">$56.000</span>
            </div>
            <p class="product-desc">Entran tus patines, el buzo y el termo sin drama. Base reforzada impermeable y correa ancha acolchada.</p>
            <div class="size-row">
              <span class="size-label">Capacidad</span>
              <div class="size-pills">
                <button type="button" class="size-pill selected">32L</button>
              </div>
            </div>
            <button type="button" class="btn-card-wa">Pedir por WhatsApp</button>
          </div>
        </article>

      </div>
    </div>
  </section>

  <!-- ================= PISTA & CALLE (LA ONDA) ================= -->
  <section id="la-onda" class="section vibe-section">
    <div class="container">
      <div class="section-header">
        <div>
          <p class="section-kicker">Identidad BlueSouls</p>
          <h2 class="section-title display-font">No hace falta patinar para llevarla</h2>
        </div>
        <p class="section-subtitle">
          Nacimos entre las tablas de las pistas de Buenos Aires, pero diseñamos para cualquiera que busque ropa holgada, cómoda y distinta.
        </p>
      </div>

      <div class="vibe-grid">
        <div class="vibe-card">
          <div class="vibe-num">01</div>
          <h3>Espíritu de pista</h3>
          <p>Cortes anchos inspirados en los jerseys de hockey de los 90: mucha libertad de movimiento y cero rigidez cuando estás arriba del hielo.</p>
        </div>

        <div class="vibe-card">
          <div class="vibe-num">02</div>
          <h3>Calle porteña</h3>
          <p>Combiná un jersey azul profundo con un cargo negro y zapas blancas. Vas cómodo a cursar, a tomar algo o a girar por la ciudad.</p>
        </div>

        <div class="vibe-card">
          <div class="vibe-num">03</div>
          <h3>Colores que no fallan</h3>
          <p>Azul profundo, negro, blanco hielo y toques de azul eléctrico. Prendas fáciles de combinar todos los días sin pensarlo de más.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ================= CÓMO COMPRAR ================= -->
  <section id="como-comprar" class="section">
    <div class="container">
      <div class="section-header">
        <div>
          <p class="section-kicker">Sin carrito eterno</p>
          <h2 class="section-title display-font">Comprá en 3 pasos</h2>
        </div>
      </div>

      <div class="steps-grid">
        <div class="step-box">
          <div class="step-badge">1</div>
          <h3>Elegí prenda y talle</h3>
          <p>Mirá el catálogo, seleccioná tu talle en la tarjeta (o preguntanos si dudás entre dos) y tocá el botón.</p>
        </div>

        <div class="step-box">
          <div class="step-badge">2</div>
          <h3>Charlamos por WhatsApp</h3>
          <p>Se abre nuestro chat con tu pedido ya armado. Te confirmamos stock en el momento y te pasamos medidas reales.</p>
        </div>

        <div class="step-box">
          <div class="step-badge">3</div>
          <h3>Retirá o recibí en tu casa</h3>
          <p>Pagás por transferencia o efectivo y coordinamos moto en CABA/GBA, Correo Argentino o retiro en punto de entrega.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ================= BANNER CONTACTO WHATSAPP ================= -->
  <section id="contacto" class="section" style="padding-top: 0;">
    <div class="container">
      <div class="cta-banner">
        <div>
          <h2 class="display-font">¿Dudas con el talle o querés armar un combo?</h2>
          <p>Mandanos un mensaje directo. Te respondemos al toque, te pasamos las medidas exactas y coordinamos tu pedido.</p>
        </div>

        <a
          href="https://wa.me/5491100000000?text=Hola%20BlueSouls!%20Tengo%20una%20consulta%20sobre%20talles%20y%20combos."
          target="_blank"
          rel="noopener noreferrer"
          class="btn-ice"
        >
          <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
            <path d="M12.03 2C6.5 2 2 6.48 2 12c0 1.77.46 3.5 1.34 5.02L2 22l5.12-1.33A9.97 9.97 0 0 0 12.03 22C17.56 22 22 17.52 22 12S17.56 2 12.03 2zm5.8 14.23c-.24.68-1.42 1.3-1.97 1.37-.5.07-1.15.1-1.85-.12-.43-.14-.98-.32-1.69-.63-2.97-1.29-4.91-4.3-5.06-4.5-.15-.2-1.2-1.6-1.2-3.05 0-1.45.76-2.16 1.03-2.46.27-.3.59-.37.79-.37h.57c.18 0 .43-.07.67.51.24.58.83 2.02.9 2.17.07.15.12.33.02.53-.1.2-.15.32-.3.5-.15.18-.32.4-.45.54-.15.15-.31.32-.13.62.18.3.78 1.29 1.68 2.09 1.15 1.02 2.12 1.34 2.42 1.49.3.15.48.13.66-.07.18-.2.76-.88.96-1.18.2-.3.4-.25.67-.15.27.1 1.74.82 2.04.97.3.15.5.22.57.34.07.12.07.7-.17 1.38z"/>
          </svg>
          Hablar por WhatsApp
        </a>
      </div>
    </div>
  </section>

  <!-- ================= FOOTER ================= -->
  <footer>
    <div class="container footer-inner">
      <div>
        <strong style="color: var(--blanco-hielo);">BlueSouls</strong> — Ropa urbana de pista y calle. Buenos Aires, Argentina.
      </div>
      <div>
        Instagram: <a href="#" style="color: var(--blanco-hielo); text-decoration: underline;">@bluesouls.ba</a> · Atención Lun a Sáb
      </div>
    </div>
  </footer>

  <!-- ================= BOTÓN FLOTANTE WHATSAPP ================= -->
  <a
    href="https://wa.me/5491100000000?text=Hola%20BlueSouls!%20Vengo%20de%20la%20web%20y%20quiero%20hacer%20un%20pedido."
    target="_blank"
    rel="noopener noreferrer"
    class="wa-float"
    aria-label="Contactar a BlueSouls por WhatsApp"
  >
    <svg width="22" height="22" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
      <path d="M12.03 2C6.5 2 2 6.48 2 12c0 1.77.46 3.5 1.34 5.02L2 22l5.12-1.33A9.97 9.97 0 0 0 12.03 22C17.56 22 22 17.52 22 12S17.56 2 12.03 2zm5.8 14.23c-.24.68-1.42 1.3-1.97 1.37-.5.07-1.15.1-1.85-.12-.43-.14-.98-.32-1.69-.63-2.97-1.29-4.91-4.3-5.06-4.5-.15-.2-1.2-1.6-1.2-3.05 0-1.45.76-2.16 1.03-2.46.27-.3.59-.37.79-.37h.57c.18 0 .43-.07.67.51.24.58.83 2.02.9 2.17.07.15.12.33.02.53-.1.2-.15.32-.3.5-.15.18-.32.4-.45.54-.15.15-.31.32-.13.62.18.3.78 1.29 1.68 2.09 1.15 1.02 2.12 1.34 2.42 1.49.3.15.48.13.66-.07.18-.2.76-.88.96-1.18.2-.3.4-.25.67-.15.27.1 1.74.82 2.04.97.3.15.5.22.57.34.07.12.07.7-.17 1.38z"/>
    </svg>
    <span>Pedir por WhatsApp</span>
  </a>

  <!-- ================= SCRIPT ESTÁTICO (FILTROS, TALLES Y WHATSAPP) ================= -->
  <script>
    // Reemplazá este número por el WhatsApp real de BlueSouls (código país + área + número, sin + ni espacios)
    const WHATSAPP_NUMBER = "5491100000000";

    // 1. Filtro de categorías del catálogo
    const filterButtons = document.querySelectorAll(".filter-btn");
    const productCards = document.querySelectorAll(".product-card");

    filterButtons.forEach((btn) => {
      btn.addEventListener("click", () => {
        filterButtons.forEach((b) => b.classList.remove("active"));
        btn.classList.add("active");

        const category = btn.getAttribute("data-filter");
        productCards.forEach((card) => {
          const cardCat = card.getAttribute("data-category");
          if (category === "all" || cardCat === category) {
            card.classList.remove("hidden");
          } else {
            card.classList.add("hidden");
          }
        });
      });
    });

    // 2. Selección de talle y apertura directa a WhatsApp con el producto elegido
    productCards.forEach((card) => {
      const sizePills = card.querySelectorAll(".size-pill");
      const waButton = card.querySelector(".btn-card-wa");

      sizePills.forEach((pill) => {
        pill.addEventListener("click", () => {
          sizePills.forEach((p) => p.classList.remove("selected"));
          pill.classList.add("selected");
        });
      });

      waButton.addEventListener("click", () => {
        const name = card.getAttribute("data-name");
        const price = card.getAttribute("data-price");
        const selectedPill = card.querySelector(".size-pill.selected");
        const size = selectedPill ? selectedPill.textContent.trim() : "A consultar";

        const message = `Hola BlueSouls! Quiero pedir: ${name} (${price}) - Talle: ${size}. ¿Tienen stock?`;
        const url = `https://wa.me/${WHATSAPP_NUMBER}?text=${encodeURIComponent(message)}`;
        window.open(url, "_blank", "noopener,noreferrer");
      });
    });
  </script>
</body>
</html>
