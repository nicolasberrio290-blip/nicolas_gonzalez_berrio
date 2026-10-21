<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Design - UNIAJC Electiva</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.3.1/css/all.min.css">
  <link rel="stylesheet" href="css/styles.css">
</head>
<body>
  <header class="header">
    <div class="header__container">
      <a href="#" class="header__logo">
        <i class="fa-solid fa-layer-group header__logo-icon"></i>
        <span class="header__logo-text">FlexStudio</span>
      </a>
      <nav class="header__nav">
        <ul class="header__menu">
          <li class="header__menu-item"><a href="#inicio" class="header__menu-link header__menu-link--active">Inicio</a></li>
          <li class="header__menu-item"><a href="#servicios" class="header__menu-link">Servicios</a></li>
          <li class="header__menu-item"><a href="#nosotros" class="header__menu-link">Nosotros</a></li>
          <li class="header__menu-item"><a href="#contacto" class="header__menu-link">Contacto</a></li>
        </ul>
      </nav>
      <button class="header__toggle" id="menuToggle"><i class="fa-solid fa-bars"></i></button>
    </div>
  </header>

  <section class="hero" id="inicio">
    <div class="hero__content">
      <span class="hero__badge"><i class="fa-solid fa-wand-magic-sparkles"></i> Diseño Responsive</span>
      <h1 class="hero__title">Diseño que se <span class="hero__title--highlight">adapta</span> a todo</h1>
      <p class="hero__description">Metodología BEM, Media Queries, Clip-Path y FontAwesome. Ejercicio creado con apoyo de IA para entender el flujo responsive moderno.</p>
      <div class="hero__actions">
        <a href="#servicios" class="button button--primary"><i class="fa-solid fa-rocket"></i> Explorar</a>
        <a href="https://github.com/uniajc-gperezm/responsive-design-media-query" target="_blank" class="button button--secondary"><i class="fa-brands fa-github"></i> Repo Base</a>
      </div>
    </div>
    <div class="hero__visual">
      <div class="hero__shape"></div>
      <div class="hero__image">
        <i class="fa-solid fa-desktop"></i>
        <i class="fa-solid fa-tablet-screen-button"></i>
        <i class="fa-solid fa-mobile-screen-button"></i>
      </div>
    </div>
  </section>

  <section class="services" id="servicios">
    <div class="services__header">
      <h2 class="services__title">Lo que implementamos</h2>
      <p class="services__subtitle">Requisitos del ejercicio resueltos con BEM + Media Queries</p>
    </div>
    <div class="services__grid">
      <article class="card">
        <div class="card__icon card__icon--clip1"><i class="fa-solid fa-mobile-screen-button"></i></div>
        <h3 class="card__title">Media Queries</h3>
        <p class="card__text">Mobile First: 320px, 768px, 1024px. Layout se adapta con flex y grid.</p>
        <span class="card__tag"><i class="fa-solid fa-code"></i> @media</span>
      </article>
      <article class="card card--featured">
        <div class="card__icon card__icon--clip2"><i class="fa-solid fa-shapes"></i></div>
        <h3 class="card__title">Clip-Path</h3>
        <p class="card__text">Usado con clippy.f8.edu.vn para crear formas poligonales en hero, iconos y footer.</p>
        <span class="card__tag"><i class="fa-solid fa-scissors"></i> polygon()</span>
      </article>
      <article class="card">
        <div class="card__icon card__icon--clip3"><i class="fa-brands fa-font-awesome"></i></div>
        <h3 class="card__title">FontAwesome CDN</h3>
        <p class="card__text">Iconos brands, solid, whatsapp integrados desde CDN Cloudflare.</p>
        <span class="card__tag"><i class="fa-solid fa-icons"></i> CDN</span>
      </article>
    </div>
  </section>

  <section class="about" id="nosotros">
    <div class="about__container">
      <div class="about__text">
        <h2 class="about__title">Metodología BEM</h2>
        <p class="about__description">Block - Element - Modifier. Facilita mantener CSS escalable sin colisiones.</p>
        <ul class="about__list">
          <li class="about__list-item"><i class="fa-solid fa-check"></i> <strong>Block:</strong> .card, .header, .hero</li>
          <li class="about__list-item"><i class="fa-solid fa-check"></i> <strong>Element:</strong> .card__title, .header__logo</li>
          <li class="about__list-item"><i class="fa-solid fa-check"></i> <strong>Modifier:</strong> .button--primary, .card--featured</li>
        </ul>
      </div>
      <div class="about__code">
        <pre class="about__pre"><code>&lt;article class="card card--featured"&gt;
  &lt;div class="card__icon"&gt;&lt;/div&gt;
  &lt;h3 class="card__title"&gt;...&lt;/h3&gt;
&lt;/article&gt;

/* CSS con BEM */
.card { }
.card__title { }
.card--featured { }</code></pre>
      </div>
    </div>
  </section>

  <footer class="footer" id="contacto">
    <div class="footer__container">
      <div class="footer__brand">
        <h3 class="footer__title">FlexStudio</h3>
        <p class="footer__text">Ejercicio 22026-611 Electiva - Responsive Design Media Query</p>
      </div>
      <div class="footer__social">
        <a href="#" class="footer__social-link"><i class="fa-brands fa-whatsapp"></i></a>
        <a href="#" class="footer__social-link"><i class="fa-brands fa-github"></i></a>
        <a href="#" class="footer__social-link"><i class="fa-solid fa-envelope"></i></a>
        <a href="#" class="footer__social-link"><i class="fa-brands fa-linkedin"></i></a>
      </div>
    </div>
    <div class="footer__bottom">
      <p class="footer__copy">Hecho con <i class="fa-solid fa-heart"></i> + IA | GitHub Pages Ready | 2026</p>
    </div>
  </footer>

  <script>
    document.getElementById('menuToggle').addEventListener('click', () => {
      document.querySelector('.header__nav').classList.toggle('header__nav--open');
    });
  </script>
</body>
</html>