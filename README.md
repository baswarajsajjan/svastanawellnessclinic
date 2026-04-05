# svastanawellnessclinic
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Svastana Wellness Clinic | Naturopathic Care by Dr. G. Monica Sravanthi</title>

  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet" />

  <style>
    *, *::before, *::after {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --sage: #2e7d4f;
      --sage-light: #e8f4ed;
      --sage-dark: #184f31;
      --teal: #1b7fa0;
      --cream: #f7f3ec;
      --warm-white: #fdfcf9;
      --charcoal: #1f2a22;
      --muted: #66756a;
      --gold: #b89b6a;
      --border: rgba(46, 125, 79, 0.14);
      --shadow-soft: 0 10px 30px rgba(23, 37, 28, 0.08);
      --shadow-card: 0 18px 50px rgba(23, 37, 28, 0.08);
      --radius-lg: 24px;
      --radius-md: 16px;
      --radius-sm: 12px;
      --font-display: 'Cormorant Garamond', Georgia, serif;
      --font-body: 'Jost', sans-serif;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: var(--font-body);
      background: var(--warm-white);
      color: var(--charcoal);
      font-weight: 300;
      line-height: 1.7;
      overflow-x: hidden;
    }

    img {
      max-width: 100%;
      display: block;
    }

    a {
      text-decoration: none;
    }

    section {
      padding: 6rem 0;
    }

    .container {
      max-width: 1180px;
      margin: 0 auto;
      padding: 0 1.5rem;
    }

    .section-tag {
      font-size: 0.72rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 0.8rem;
      display: inline-flex;
      align-items: center;
      gap: 0.7rem;
    }

    .section-tag::after {
      content: "";
      width: 36px;
      height: 1px;
      background: var(--gold);
      display: inline-block;
    }

    .section-title {
      font-family: var(--font-display);
      font-size: clamp(2.2rem, 4vw, 3.4rem);
      line-height: 1.1;
      font-weight: 500;
      margin-bottom: 1.2rem;
      color: var(--charcoal);
    }

    .section-title em {
      font-style: italic;
      color: var(--sage);
    }

    .section-copy {
      color: var(--muted);
      font-size: 0.98rem;
      line-height: 1.9;
    }

    /* NAVBAR */
    nav {
      position: fixed;
      top: 1rem;
      left: 50%;
      transform: translateX(-50%);
      width: min(1180px, calc(100% - 2rem));
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.9rem 1.2rem;
      background: rgba(253, 252, 249, 0.82);
      backdrop-filter: blur(14px);
      border: 1px solid rgba(255, 255, 255, 0.5);
      border-radius: 999px;
      box-shadow: var(--shadow-soft);
    }

    .nav-logo {
      display: flex;
      align-items: center;
      gap: 0.8rem;
    }

    .nav-logo img {
      height: 52px;
      width: auto;
      object-fit: contain;
    }

    .nav-logo-text {
      display: flex;
      flex-direction: column;
      line-height: 1.05;
    }

    .nav-logo-text span:first-child {
      font-family: var(--font-display);
      font-size: 1.25rem;
      color: var(--sage-dark);
      font-weight: 600;
    }

    .nav-logo-text span:last-child {
      font-size: 0.64rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--muted);
    }

    nav ul {
      list-style: none;
      display: flex;
      align-items: center;
      gap: 1.5rem;
    }

    nav ul a {
      font-size: 0.78rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--charcoal);
      font-weight: 500;
      transition: color 0.2s ease;
    }

    nav ul a:hover {
      color: var(--sage);
    }

    .nav-cta {
      background: linear-gradient(135deg, var(--sage-dark), var(--sage));
      color: #fff !important;
      padding: 0.8rem 1.25rem;
      border-radius: 999px;
      box-shadow: 0 10px 20px rgba(46, 125, 79, 0.22);
    }

    /* HERO */
    #hero {
      position: relative;
      min-height: 100vh;
      display: grid;
      grid-template-columns: 1.05fr 0.95fr;
      align-items: center;
      background:
        radial-gradient(circle at top right, rgba(46, 125, 79, 0.10), transparent 26%),
        linear-gradient(180deg, #fbf8f2 0%, #f7f3ec 100%);
      overflow: hidden;
      padding-top: 8rem;
    }

    #hero::before {
      content: "";
      position: absolute;
      top: -120px;
      right: -80px;
      width: 420px;
      height: 420px;
      border-radius: 50%;
      background: rgba(46, 125, 79, 0.08);
      filter: blur(8px);
    }

    .hero-text {
      padding: 3rem 2rem 3rem 5.5rem;
      position: relative;
      z-index: 2;
    }

    .hero-tag {
      display: inline-flex;
      align-items: center;
      gap: 0.7rem;
      font-size: 0.72rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 1.4rem;
    }

    .hero-tag::before {
      content: "";
      width: 32px;
      height: 1px;
      background: var(--gold);
      display: inline-block;
    }

    .hero-text h1 {
      font-family: var(--font-display);
      font-size: clamp(3rem, 5vw, 5rem);
      line-height: 1.02;
      font-weight: 500;
      margin-bottom: 1.25rem;
      color: var(--charcoal);
    }

    .hero-text h1 em {
      color: var(--sage);
      font-style: italic;
    }

    .hero-text p {
      max-width: 520px;
      font-size: 1rem;
      color: var(--muted);
      line-height: 1.95;
      margin-bottom: 2rem;
    }

    .btn-group {
      display: flex;
      align-items: center;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .btn-primary,
    .btn-outline {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 50px;
      padding: 0.9rem 1.6rem;
      font-size: 0.78rem;
      font-weight: 500;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      border-radius: 999px;
      transition: all 0.25s ease;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--sage-dark), var(--sage));
      color: #fff;
      box-shadow: 0 12px 28px rgba(46, 125, 79, 0.22);
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 16px 32px rgba(46, 125, 79, 0.28);
    }

    .btn-outline {
      border: 1px solid rgba(46, 125, 79, 0.25);
      background: rgba(255, 255, 255, 0.7);
      color: var(--sage-dark);
    }

    .btn-outline:hover {
      background: var(--sage-dark);
      color: #fff;
      border-color: var(--sage-dark);
    }

    .hero-image {
      position: relative;
      height: calc(100vh - 8rem);
      margin: 2rem 2rem 2rem 0;
      border-radius: 32px;
      overflow: hidden;
      box-shadow: var(--shadow-card);
      background: linear-gradient(160deg, #d4e8da 0%, #b8d4c2 100%);
      z-index: 2;
    }

    .hero-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center top;
    }

    .hero-badge {
      position: absolute;
      left: 1.5rem;
      bottom: 1.5rem;
      background: rgba(253, 252, 249, 0.88);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.6);
      padding: 1rem 1.2rem;
      border-radius: 18px;
      min-width: 220px;
      box-shadow: 0 12px 28px rgba(0, 0, 0, 0.08);
    }

    .hero-badge p {
      font-size: 0.72rem;
      color: var(--muted);
      letter-spacing: 0.08em;
      margin-bottom: 0.2rem;
      text-transform: uppercase;
    }

    .hero-badge strong {
      font-family: var(--font-display);
      font-size: 1.2rem;
      color: var(--charcoal);
      font-weight: 600;
    }

    /* MARQUEE */
    .marquee-wrap {
      background: var(--sage-dark);
      overflow: hidden;
      white-space: nowrap;
      padding: 0.95rem 0;
    }

    .marquee-inner {
      display: inline-block;
      min-width: 200%;
      animation: scroll-left 30s linear infinite;
    }

    .marquee-inner span {
      display: inline-block;
      font-size: 0.72rem;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      color: rgba(255, 255, 255, 0.72);
      margin: 0 2rem;
    }

    .marquee-inner span::before {
      content: "✦";
      color: var(--gold);
      margin-right: 2rem;
    }

    @keyframes scroll-left {
      from { transform: translateX(0); }
      to { transform: translateX(-50%); }
    }

    /* ABOUT */
    #about {
      background: var(--warm-white);
    }

    .about-grid {
      display: grid;
      grid-template-columns: 0.95fr 1.05fr;
      gap: 4rem;
      align-items: center;
    }

    .about-image-wrap {
      position: relative;
    }

    .about-image-box {
      aspect-ratio: 4 / 5;
      border-radius: 28px;
      overflow: hidden;
      box-shadow: var(--shadow-card);
      background: linear-gradient(160deg, #d4e8da, #b8d4c2);
    }

    .about-image-box img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center top;
    }

    .about-accent {
      position: absolute;
      width: 140px;
      height: 140px;
      right: -18px;
      bottom: -18px;
      border-radius: 28px;
      border: 1px solid rgba(46, 125, 79, 0.25);
      z-index: -1;
    }

    .about-text p {
      color: var(--muted);
      font-size: 0.98rem;
      line-height: 1.95;
      margin-bottom: 1rem;
    }

    .about-credentials {
      margin-top: 2rem;
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1rem;
    }

    .credential {
      background: linear-gradient(180deg, #ffffff 0%, #faf8f4 100%);
      border: 1px solid rgba(46, 125, 79, 0.08);
      border-radius: 20px;
      padding: 1.25rem 1rem;
      text-align: center;
      box-shadow: var(--shadow-soft);
    }

    .credential strong {
      display: block;
      font-family: var(--font-display);
      font-size: 2rem;
      color: var(--sage-dark);
      line-height: 1;
      margin-bottom: 0.35rem;
      font-weight: 600;
    }

    .credential span {
      font-size: 0.72rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--muted);
    }

    /* SERVICES */
    #services {
      background: linear-gradient(180deg, #f7f3ec 0%, #fcfaf6 100%);
    }

    .services-header {
      max-width: 700px;
      text-align: center;
      margin: 0 auto 3.5rem;
    }

    .services-header .section-tag {
      justify-content: center;
    }

    .services-header .section-tag::before {
      content: "";
      width: 36px;
      height: 1px;
      background: var(--gold);
      display: inline-block;
    }

    .two-col-services {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2rem;
    }

    .service-group {
      background: rgba(255, 255, 255, 0.7);
      backdrop-filter: blur(8px);
      border: 1px solid rgba(46, 125, 79, 0.08);
      border-radius: 28px;
      padding: 2rem;
      box-shadow: var(--shadow-soft);
    }

    .service-group h3 {
      font-family: var(--font-display);
      font-size: 1.8rem;
      font-weight: 600;
      color: var(--sage-dark);
      margin-bottom: 1.4rem;
      padding-bottom: 0.9rem;
      border-bottom: 1px solid rgba(46, 125, 79, 0.12);
    }

    .service-list {
      list-style: none;
      display: grid;
      gap: 0.75rem;
    }

    .service-list li {
      display: flex;
      align-items: center;
      gap: 0.8rem;
      padding: 0.95rem 1rem;
      border-radius: 16px;
      background: rgba(255, 255, 255, 0.7);
      transition: transform 0.2s ease, background 0.2s ease, box-shadow 0.2s ease;
    }

    .service-list li::before {
      content: "";
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--sage), var(--teal));
      flex-shrink: 0;
    }

    .service-list li:hover {
      transform: translateY(-2px);
      background: var(--sage-light);
      box-shadow: 0 10px 20px rgba(46, 125, 79, 0.08);
    }

    /* PHILOSOPHY */
    #philosophy {
      position: relative;
      overflow: hidden;
      background: linear-gradient(135deg, #163c28 0%, #1e5d3d 60%, #236b47 100%);
      color: #fff;
    }

    #philosophy::before,
    #philosophy::after {
      content: "";
      position: absolute;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.05);
      filter: blur(3px);
    }

    #philosophy::before {
      width: 360px;
      height: 360px;
      top: -100px;
      right: -80px;
    }

    #philosophy::after {
      width: 220px;
      height: 220px;
      bottom: -80px;
      left: -50px;
    }

    .philosophy-inner {
      max-width: 760px;
      margin: 0 auto;
      text-align: center;
      position: relative;
      z-index: 2;
    }

    .philosophy-inner .section-tag {
      justify-content: center;
      color: rgba(255, 255, 255, 0.65);
    }

    .philosophy-inner .section-tag::after {
      background: rgba(255, 255, 255, 0.3);
    }

    .philosophy-inner .section-title {
      color: #fff;
    }

    .philosophy-inner .section-title em {
      color: #bfe3ca;
    }

    .philosophy-inner p {
      color: rgba(255, 255, 255, 0.78);
      font-size: 1rem;
      line-height: 1.95;
      margin-bottom: 1rem;
    }

    .philosophy-inner .btn-primary {
      margin-top: 1rem;
      background: rgba(255, 255, 255, 0.12);
      border: 1px solid rgba(255, 255, 255, 0.24);
      box-shadow: none;
    }

    .philosophy-inner .btn-primary:hover {
      background: rgba(255, 255, 255, 0.2);
    }

    /* CONTACT */
    #contact {
      background: var(--warm-white);
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 0.95fr 1.05fr;
      gap: 3rem;
      align-items: start;
    }

    .contact-info p {
      color: var(--muted);
      font-size: 0.98rem;
      line-height: 1.95;
      margin-bottom: 1.4rem;
    }

    .contact-form-wrap {
      background: linear-gradient(180deg, #fff 0%, #faf8f4 100%);
      border: 1px solid rgba(46, 125, 79, 0.1);
      border-radius: 28px;
      padding: 2rem;
      box-shadow: var(--shadow-card);
    }

    .contact-form-wrap h3 {
      font-family: var(--font-display);
      font-size: 1.8rem;
      font-weight: 600;
      color: var(--charcoal);
      margin-bottom: 1.4rem;
    }

    .form-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1rem;
    }

    .form-group {
      display: flex;
      flex-direction: column;
      gap: 0.45rem;
      margin-bottom: 1rem;
    }

    .form-group label {
      font-size: 0.7rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--muted);
      font-weight: 500;
    }

    .form-group input,
    .form-group textarea {
      width: 100%;
      border: 1px solid rgba(46, 125, 79, 0.12);
      background: #fff;
      padding: 0.95rem 1rem;
      border-radius: 16px;
      font-family: var(--font-body);
      font-size: 0.95rem;
      color: var(--charcoal);
      outline: none;
      transition: border-color 0.2s ease, box-shadow 0.2s ease, transform 0.2s ease;
    }

    .form-group input:focus,
    .form-group textarea:focus {
      border-color: var(--sage);
      box-shadow: 0 0 0 4px rgba(46, 125, 79, 0.08);
      transform: translateY(-1px);
    }

    .form-group textarea {
      min-height: 120px;
      resize: vertical;
    }

    .wa-btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      min-height: 52px;
      padding: 0.95rem 1.5rem;
      border-radius: 999px;
      background: linear-gradient(135deg, #25d366, #1da851);
      color: #fff;
      font-size: 0.8rem;
      font-weight: 600;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
      box-shadow: 0 12px 24px rgba(37, 211, 102, 0.18);
      margin-top: 0.5rem;
    }

    .wa-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 16px 28px rgba(37, 211, 102, 0.22);
    }

    /* FOOTER */
    footer {
      background: #16241b;
      color: rgba(255, 255, 255, 0.68);
      padding: 4rem 0 2rem;
    }

    .footer-top {
      display: grid;
      grid-template-columns: 1.6fr 1fr 1fr;
      gap: 2rem;
      margin-bottom: 2rem;
    }

    .footer-logo-name {
      font-family: var(--font-display);
      font-size: 1.6rem;
      color: #fff;
      font-weight: 600;
      margin-bottom: 0.25rem;
    }

    .footer-logo-sub {
      font-size: 0.66rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: rgba(255, 255, 255, 0.45);
      margin-bottom: 1rem;
    }

    .footer-tagline {
      font-size: 0.92rem;
      line-height: 1.85;
      max-width: 320px;
    }

    .footer-col h4 {
      font-size: 0.68rem;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      color: rgba(255, 255, 255, 0.42);
      margin-bottom: 1rem;
    }

    .footer-col ul {
      list-style: none;
    }

    .footer-col li {
      margin-bottom: 0.65rem;
    }

    .footer-col a {
      color: rgba(255, 255, 255, 0.68);
      font-size: 0.9rem;
      transition: color 0.2s ease;
    }

    .footer-col a:hover {
      color: #fff;
    }

    .footer-bottom {
      padding-top: 1.4rem;
      border-top: 1px solid rgba(255, 255, 255, 0.08);
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
      flex-wrap: wrap;
      font-size: 0.8rem;
    }

    .social-links {
      display: flex;
      gap: 0.75rem;
    }

    .social-links a {
      width: 38px;
      height: 38px;
      border-radius: 50%;
      border: 1px solid rgba(255, 255, 255, 0.16);
      display: flex;
      align-items: center;
      justify-content: center;
      color: rgba(255, 255, 255, 0.72);
      font-size: 0.78rem;
      font-weight: 600;
      transition: all 0.2s ease;
    }

    .social-links a:hover {
      color: var(--gold);
      border-color: var(--gold);
      transform: translateY(-2px);
    }

    /* ANIMATIONS */
    .fade-up {
      opacity: 0;
      transform: translateY(24px);
      transition: opacity 0.8s ease, transform 0.8s ease;
    }

    .fade-up.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* RESPONSIVE */
    @media (max-width: 1024px) {
      nav {
        width: calc(100% - 1rem);
        top: 0.6rem;
      }

      #hero {
        grid-template-columns: 1fr;
        min-height: auto;
        padding-top: 7rem;
      }

      .hero-text {
        padding: 3rem 1.5rem 2rem;
      }

      .hero-image {
        height: 540px;
        margin: 0 1.5rem 2rem;
      }

      .about-grid,
      .contact-grid,
      .two-col-services,
      .footer-top {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 768px) {
      nav {
        border-radius: 24px;
        align-items: flex-start;
        padding: 1rem;
      }

      nav ul {
        gap: 1rem;
        flex-wrap: wrap;
        justify-content: flex-end;
      }

      .nav-logo img {
        height: 44px;
      }

      .hero-text h1 {
        font-size: clamp(2.5rem, 9vw, 4rem);
      }

      .hero-image {
        height: 420px;
      }

      .about-credentials {
        grid-template-columns: 1fr;
      }

      .form-row {
        grid-template-columns: 1fr;
      }

      .footer-bottom {
        flex-direction: column;
        align-items: flex-start;
      }
    }

    @media (max-width: 600px) {
      nav ul li:not(:last-child) {
        display: none;
      }

      section {
        padding: 4.5rem 0;
      }

      .hero-text,
      .container {
        padding-left: 1rem;
        padding-right: 1rem;
      }

      .hero-image {
        margin: 0 1rem 1.5rem;
        height: 360px;
        border-radius: 24px;
      }

      .hero-badge {
        left: 1rem;
        right: 1rem;
        bottom: 1rem;
        min-width: auto;
      }

      .service-group,
      .contact-form-wrap {
        padding: 1.4rem;
        border-radius: 22px;
      }
    }
  </style>
</head>
<body>

  <!-- NAVIGATION -->
  <nav>
    <a href="#" class="nav-logo">
      <img src="./assets/logo.png" alt="Svastana Wellness Clinic Logo" />
      <div class="nav-logo-text">
        <span>Svastana Wellness</span>
        <span>Wellness Clinic</span>
      </div>
    </a>

    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#philosophy">Philosophy</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="https://wa.me/918333888010" target="_blank" class="nav-cta">Book Now</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section id="hero">
    <div class="hero-text">
      <p class="hero-tag">Naturopathic Wellness Clinic</p>
      <h1>Healing Guided<br />by <em>Nature</em></h1>
      <p>
        Personalized naturopathic care and holistic diet planning crafted to restore your inner balance through the wisdom of natural healing.
      </p>
      <div class="btn-group">
        <a href="https://wa.me/918333888010" target="_blank" class="btn-primary">Book a Consultation</a>
        <a href="#about" class="btn-outline">Our Approach</a>
      </div>
    </div>

    <div class="hero-image">
      <img src="./assets/doctor-photo.jpeg" alt="Dr. G. Monica Sravanthi – Naturopathic Practitioner" />
      <div class="hero-badge">
        <p>Led by</p>
        <strong>Dr. G. Monica Sravanthi</strong>
      </div>
    </div>
  </section>

  <!-- MARQUEE -->
  <div class="marquee-wrap">
    <div class="marquee-inner">
      <span>Naturopathy</span>
      <span>Holistic Nutrition</span>
      <span>Acupuncture</span>
      <span>Yoga Therapy</span>
      <span>Hydrotherapy</span>
      <span>Diet Therapy</span>
      <span>Mud Therapy</span>
      <span>Physiotherapy</span>
      <span>Natural Healing</span>
      <span>Personalised Care</span>
      <span>Naturopathy</span>
      <span>Holistic Nutrition</span>
      <span>Acupuncture</span>
      <span>Yoga Therapy</span>
      <span>Hydrotherapy</span>
      <span>Diet Therapy</span>
      <span>Mud Therapy</span>
      <span>Physiotherapy</span>
      <span>Natural Healing</span>
      <span>Personalised Care</span>
    </div>
  </div>

  <!-- ABOUT -->
  <section id="about">
    <div class="container">
      <div class="about-grid">
        <div class="about-image-wrap fade-up">
          <div class="about-image-box">
            <img src="./assets/doctor-photo.jpeg" alt="Dr. G. Monica Sravanthi" />
          </div>
          <div class="about-accent"></div>
        </div>

        <div class="about-text fade-up">
          <p class="section-tag">About Dr. Monica</p>
          <h2 class="section-title">Guiding Your Journey to <em>Natural Vitality</em></h2>
          <p>
            Dr. G. Monica Sravanthi is a dedicated practitioner of naturopathy and holistic nutrition, specializing in the art of personalized diet planning. At Svastana Wellness, she serves as a compassionate guide for those seeking to harmonize their health through the wisdom of natural healing.
          </p>
          <p>
            Her expertise lies in identifying the root causes of imbalance and addressing them with artisanal care and evidence-based naturopathic protocols. With an unwavering commitment to organic minimalism in health, she believes the most profound healing occurs when the body is provided with the pure essentials of nature.
          </p>
          <p>
            Dr. Monica's approach is marked by a deep-seated passion for empowering her clients to reclaim their well-being, focusing on the transformative power of holistic nutrition as the foundation of a vibrant, balanced life.
          </p>

          <div class="about-credentials">
            <div class="credential">
              <strong>1000+</strong>
              <span>Clients Served</span>
            </div>
            <div class="credential">
              <strong>5+</strong>
              <span>Years Practice</span>
            </div>
            <div class="credential">
              <strong>BNYS</strong>
              <span>Certified</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- SERVICES -->
  <section id="services">
    <div class="container">
      <div class="services-header fade-up">
        <p class="section-tag">What We Offer</p>
        <h2 class="section-title">Therapies &amp; <em>Services</em></h2>
        <p class="section-copy">
          Each treatment is thoughtfully tailored to your unique constitution and health goals, rooted in evidence-based naturopathic protocols.
        </p>
      </div>

      <div class="two-col-services">
        <div class="service-group fade-up">
          <h3>Therapies</h3>
          <ul class="service-list">
            <li>Hydrotherapy</li>
            <li>Manipulative Therapy</li>
            <li>Acupuncture</li>
            <li>Electrotherapy</li>
            <li>Fasting Therapy</li>
            <li>Diet Therapy</li>
            <li>Yoga Therapy</li>
            <li>Physiotherapy</li>
            <li>Mud Therapy</li>
            <li>Chromo Therapy</li>
            <li>Magneto Therapy</li>
          </ul>
        </div>

        <div class="service-group fade-up">
          <h3>Services Provided</h3>
          <ul class="service-list">
            <li>Therapeutic Acupuncture</li>
            <li>Cosmetic Acupuncture</li>
            <li>Acupressure</li>
            <li>Hand and Foot Reflexology</li>
            <li>Therapeutic Yoga</li>
            <li>Hot Foot Immersion</li>
            <li>Spinal Bath</li>
            <li>Sitz Bath</li>
            <li>Douche</li>
            <li>Full Body Mud Therapy</li>
            <li>Full Body Massage</li>
            <li>Therapeutic Massage</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- PHILOSOPHY -->
  <section id="philosophy">
    <div class="container">
      <div class="philosophy-inner fade-up">
        <p class="section-tag">Our Belief</p>
        <h2 class="section-title">Nurturing Your Nature Through the<br /><em>Wisdom of Naturopathy</em></h2>
        <p>
          Unlock your body's innate healing potential with personalized guidance and science-backed naturopathic care for a more balanced life. We believe that the most profound healing occurs when the body is provided with the pure essentials of nature.
        </p>
        <p>
          Every protocol we design is rooted in the principle that true wellness comes from addressing the whole person — body, mind, and environment — not just managing individual symptoms.
        </p>
        <a href="https://wa.me/918333888010" target="_blank" class="btn-primary">Begin Your Journey</a>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="container">
      <div class="contact-grid">
        <div class="contact-info fade-up">
          <p class="section-tag">Get in Touch</p>
          <h2 class="section-title">Begin Your <em>Journey</em></h2>
          <p>
            Start a conversation today for personalized guidance on your path to natural healing and wellness. Dr. Monica is here to support you every step of the way.
          </p>
        </div>

        <div class="contact-form-wrap fade-up">
          <h3>Request a Consultation</h3>

          <div class="form-row">
            <div class="form-group">
              <label>Name</label>
              <input type="text" placeholder="Your name" />
            </div>
            <div class="form-group">
              <label>Phone</label>
              <input type="tel" placeholder="Your phone number" />
            </div>
          </div>

          <div class="form-group">
            <label>Email</label>
            <input type="email" placeholder="Your email" />
          </div>

          <div class="form-group">
            <label>Message</label>
            <textarea placeholder="Tell us how we can support your wellness journey"></textarea>
          </div>

          <a href="https://wa.me/918333888010" target="_blank" class="wa-btn">Continue on WhatsApp</a>
        </div>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <div class="container">
      <div class="footer-top">
        <div>
          <div class="footer-logo-name">Svastana Wellness</div>
          <div class="footer-logo-sub">Wellness Clinic</div>
          <p class="footer-tagline">
            Expert naturopathic care by Dr. G. Monica Sravanthi. Healing through nature, personalised for you.
          </p>
        </div>

        <div class="footer-col">
          <h4>Navigation</h4>
          <ul>
            <li><a href="#about">About Dr. Monica</a></li>
            <li><a href="#services">Therapies</a></li>
            <li><a href="#services">Services Provided</a></li>
            <li><a href="#philosophy">Our Philosophy</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </div>

        <div class="footer-col">
          <h4>Therapies</h4>
          <ul>
            <li><a href="#services">Acupuncture</a></li>
            <li><a href="#services">Hydrotherapy</a></li>
            <li><a href="#services">Yoga Therapy</a></li>
            <li><a href="#services">Mud Therapy</a></li>
            <li><a href="#services">Diet Therapy</a></li>
          </ul>
        </div>
      </div>

      <div class="footer-bottom">
        <p>© 2026 Svastana Wellness Clinic. All rights reserved. Expert Naturopathic Care by Dr. G. Monica Sravanthi.</p>

        <div class="social-links">
          <a href="https://www.instagram.com/svastana_wellness" target="_blank" title="Instagram">IG</a>
          <a href="https://wa.me/918333888010" target="_blank" title="WhatsApp">WA</a>
        </div>
      </div>
    </div>
  </footer>

  <script>
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("visible");
        }
      });
    }, { threshold: 0.12 });

    document.querySelectorAll(".fade-up").forEach((el) => observer.observe(el));
  </script>
</body>
</html>
