# vanoozzzresell-
web vanoozzzresell 
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>VanoozzzResell · Premium Digital Store</title>
  <meta name="description" content="VanoozzzResell - Jual Netflix, Capcut, Stiker, dan Bot WhatsApp dengan harga terbaik.">
  <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>👑</text></svg>">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; }
    html { scroll-behavior: smooth; }
    body {
      background: #0a0718;
      color: #f0edff;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 1.5rem 1rem;
      min-height: 100vh;
    }

    .deck {
      max-width: 1150px;
      width: 100%;
      display: flex;
      flex-direction: column;
      gap: 2.5rem;
      position: relative;
    }

    /* setiap slide */
    .slide {
      background: radial-gradient(circle at 10% 20%, #1b1435, #0e0a1f 85%);
      border-radius: 2.5rem;
      padding: 2rem 2.5rem;
      border: 1px solid rgba(180, 70, 200, 0.2);
      box-shadow: 0 20px 40px -10px #000000aa;
      backdrop-filter: blur(2px);
      transition: transform 0.3s ease, box-shadow 0.3s ease, opacity 0.4s ease;
      opacity: 1;
      transform: translateY(0);
    }
    .slide.hidden-slide {
      display: none;
    }
    .slide.fade-in {
      animation: fadeSlide 0.5s ease forwards;
    }
    @keyframes fadeSlide {
      0% { opacity: 0; transform: translateY(20px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    /* navbar */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-bottom: 1.2rem;
      border-bottom: 1px solid rgba(200, 130, 255, 0.2);
      flex-wrap: wrap;
      gap: 0.8rem 2rem;
    }
    .logo {
      font-size: 1.8rem;
      font-weight: 700;
      background: linear-gradient(135deg, #d6a2ff, #f86bb9);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      cursor: pointer;
      transition: 0.2s;
      text-decoration: none;
    }
    .logo i { color: #d68aff; font-size: 1.8rem; }
    .logo:hover { transform: scale(1.02); filter: brightness(1.1); }

    .nav-links {
      display: flex;
      gap: 1.8rem;
      font-weight: 500;
      color: #c9b8ff;
      flex-wrap: wrap;
    }
    .nav-links span {
      cursor: pointer;
      padding: 0.3rem 0.8rem;
      border-radius: 30px;
      border: 1px solid transparent;
      transition: 0.2s;
      font-size: 0.95rem;
    }
    .nav-links span:hover {
      color: #f0b6ff;
      background: rgba(200, 130, 255, 0.08);
      border-color: rgba(200, 130, 255, 0.2);
    }
    .nav-links .active {
      color: #fff;
      background: rgba(200, 100, 220, 0.15);
      border-color: #c86bff;
    }

    /* navigation dots */
    .slide-nav {
      display: flex;
      justify-content: center;
      gap: 0.8rem;
      margin-top: 0.5rem;
      flex-wrap: wrap;
    }
    .slide-nav button {
      background: rgba(200, 130, 255, 0.12);
      border: 1px solid rgba(200, 130, 255, 0.15);
      color: #c9b8ff;
      padding: 0.6rem 1.5rem;
      border-radius: 40px;
      font-weight: 500;
      cursor: pointer;
      transition: 0.25s;
      font-size: 0.9rem;
      backdrop-filter: blur(4px);
    }
    .slide-nav button:hover {
      background: rgba(200, 100, 220, 0.25);
      border-color: #b86bdf;
      color: #fff;
      transform: translateY(-2px);
      box-shadow: 0 6px 16px rgba(180, 70, 200, 0.2);
    }
    .slide-nav button.active-btn {
      background: rgba(200, 100, 220, 0.3);
      border-color: #c86bff;
      color: #fff;
      box-shadow: 0 0 20px rgba(180, 70, 200, 0.15);
    }

    /* hero */
    .hero-title {
      font-size: 3.8rem;
      font-weight: 700;
      line-height: 1.1;
      background: linear-gradient(145deg, #f2d6ff, #ff9dd6);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin: 0.8rem 0 0.5rem;
    }
    .hero-sub {
      font-size: 1.2rem;
      color: #baa9f0;
      border-left: 4px solid #c45bca;
      padding-left: 1.2rem;
      background: linear-gradient(90deg, rgba(180,80,200,0.06), transparent);
    }
    .hero-meta {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      margin-top: 1.8rem;
      padding-top: 1.2rem;
      border-top: 1px solid rgba(200,130,255,0.15);
    }
    .presented { display: flex; gap: 2rem; flex-wrap: wrap; }
    .presented-item .label { font-size: 0.7rem; text-transform: uppercase; color: #8877bb; letter-spacing: 1px; }
    .presented-item .value { font-size: 1.2rem; font-weight: 600; color: #ede0ff; }
    .status-badge {
      background: rgba(200,100,220,0.15);
      padding: 0.5rem 1.5rem;
      border-radius: 60px;
      border: 1px solid #b46bcb;
      color: #e7caff;
      font-weight: 500;
    }

    /* grid */
    .grid-3 {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 2rem;
      padding: 1.5rem 0 0.5rem;
    }
    .card {
      background: rgba(26,18,48,0.5);
      backdrop-filter: blur(2px);
      padding: 2rem 1.5rem;
      border-radius: 2rem;
      border: 1px solid rgba(200,130,255,0.12);
      transition: 0.25s;
      cursor: default;
    }
    .card:hover { border-color: #b367d6; background: rgba(40,25,70,0.5); transform: translateY(-4px); box-shadow: 0 10px 30px -10px #00000066; }
    .card i {
      font-size: 2.8rem;
      background: linear-gradient(145deg, #c77aff, #f670b6);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 0.8rem;
    }
    .card h3 { font-size: 1.8rem; font-weight: 600; color: #f0e3ff; }
    .card p { color: #b7a5e0; font-weight: 300; }

    /* about */
    .about-wrap {
      display: flex;
      flex-wrap: wrap;
      gap: 2.5rem;
      padding: 1.2rem 0;
      align-items: center;
    }
    .about-text { flex: 2 1 280px; }
    .about-text h2 {
      font-size: 2.8rem;
      background: linear-gradient(135deg, #f0d2ff, #fd9fd0);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .about-text p { color: #c9b8f0; line-height: 1.7; max-width: 550px; font-weight: 300; margin: 0.6rem 0; }
    .stats {
      display: flex;
      flex-wrap: wrap;
      gap: 2.5rem;
      background: rgba(20,12,40,0.4);
      padding: 1.2rem 2rem;
      border-radius: 40px;
      border: 1px solid rgba(180,80,200,0.12);
      margin-top: 1rem;
    }
    .stat-item .stat-number {
      font-size: 2.5rem;
      font-weight: 700;
      background: linear-gradient(145deg, #e1b6ff, #fd89c6);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      line-height: 1;
    }
    .stat-item .stat-label { font-size: 0.7rem; text-transform: uppercase; color: #927fbf; letter-spacing: 1px; }

    /* features */
    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap: 1.5rem;
      padding: 1.5rem 0 0.5rem;
    }
    .feat {
      background: rgba(18,12,38,0.5);
      backdrop-filter: blur(2px);
      border-radius: 2.5rem;
      padding: 1.5rem 1rem;
      text-align: center;
      border: 1px solid rgba(190,120,230,0.08);
      transition: 0.25s;
      cursor: default;
    }
    .feat:hover { border-color: #b668d6; background: rgba(30,18,55,0.6); transform: translateY(-4px); }
    .feat i {
      font-size: 2.8rem;
      background: linear-gradient(145deg, #d494ff, #f86bb9);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 0.3rem;
    }
    .feat h4 { font-size: 1.3rem; font-weight: 500; color: #f0e0ff; }
    .feat p { font-size: 0.85rem; color: #b09dd6; font-weight: 300; }

    /* cta */
    .cta {
      text-align: center;
      padding: 1.8rem 0 0.5rem;
    }
    .cta h2 {
      font-size: 3.6rem;
      font-weight: 700;
      background: linear-gradient(145deg, #f5deff, #ffa2d6);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      line-height: 1.2;
    }
    .contact-links {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2.5rem 4rem;
      background: rgba(16,8,36,0.5);
      padding: 1.8rem 2.5rem;
      border-radius: 80px;
      border: 1px solid rgba(200,120,240,0.12);
      backdrop-filter: blur(4px);
      margin: 1.5rem 0 0.5rem;
    }
    .contact-item { display: flex; flex-direction: column; align-items: center; gap: 0.2rem; }
    .contact-item i { font-size: 1.8rem; color: #c086e0; }
    .contact-item .label { font-size: 0.7rem; text-transform: uppercase; color: #8877b0; letter-spacing: 1px; }
    .contact-item .value { font-weight: 500; color: #ede5ff; word-break: break-word; }

    /* PRICELIST SLIDE */
    .price-slide {
      background: radial-gradient(circle at 10% 20%, #1b1435, #0e0a1f 85%);
      border-radius: 2.5rem;
      padding: 2rem 2.5rem;
      border: 1px solid rgba(180, 70, 200, 0.2);
      box-shadow: 0 20px 40px -10px #000000aa;
    }
    .price-category {
      background: rgba(22,14,44,0.5);
      backdrop-filter: blur(2px);
      border-radius: 2rem;
      padding: 1.4rem 1.8rem;
      margin-bottom: 1.8rem;
      border: 1px solid rgba(180,80,200,0.1);
      transition: 0.2s;
    }
    .price-category:hover { border-color: rgba(200,100,220,0.25); }
    .category-title {
      display: flex;
      align-items: center;
      gap: 0.8rem;
      font-size: 1.8rem;
      font-weight: 600;
      background: linear-gradient(145deg, #e8cbff, #fd8fcb);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 1rem;
    }
    .price-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0.5rem 1rem;
      border-radius: 40px;
      background: rgba(0,0,0,0.12);
      border-left: 3px solid rgba(200,100,220,0.25);
      color: #ddd0f5;
      flex-wrap: wrap;
      gap: 0.2rem 0.8rem;
      margin-bottom: 0.4rem;
      transition: 0.2s;
      cursor: pointer;
    }
    .price-row:hover {
      background: rgba(200,100,220,0.08);
      border-left-color: #c86bff;
      transform: translateX(4px);
    }
    .price-row .label { display: flex; align-items: center; gap: 0.5rem; }
    .price-row .label i { color: #b889e6; width: 1.2rem; }
    .price-row .price {
      font-weight: 600;
      background: linear-gradient(135deg, #dbb6ff, #f77ec0);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      display: flex;
      align-items: center;
      gap: 0.8rem;
      flex-wrap: wrap;
    }

    .wa-ig-strip {
      display: flex;
      flex-wrap: wrap;
      gap: 1.8rem;
      background: rgba(18,10,38,0.5);
      padding: 0.7rem 2rem;
      border-radius: 60px;
      border: 1px solid rgba(200,130,255,0.12);
      margin: 1.2rem 0 0.8rem;
      align-items: center;
    }
    .wa-ig-strip a {
      color: #f0e3ff;
      text-decoration: none;
      border-bottom: 1px dashed rgba(200,130,255,0.3);
      transition: 0.2s;
    }
    .wa-ig-strip a:hover { color: #ffb3e6; border-bottom-color: #f86bb9; }

    /* tombol wa order */
    .order-btn {
      display: inline-block;
      background: linear-gradient(135deg, #25D366, #128C7E);
      color: #fff;
      padding: 0.3rem 1rem;
      border-radius: 40px;
      font-weight: 600;
      font-size: 0.75rem;
      border: none;
      cursor: pointer;
      transition: 0.25s;
      text-decoration: none;
      white-space: nowrap;
    }
    .order-btn:hover { transform: scale(1.05); box-shadow: 0 4px 20px rgba(37,211,102,0.3); }

    /* footer */
    .footer {
      text-align: center;
      color: #4a3a66;
      font-size: 0.8rem;
      padding: 1.5rem 0 0.5rem;
      letter-spacing: 0.5px;
    }
    .footer a { color: #7a62a5; text-decoration: none; }
    .footer a:hover { color: #b889e6; }

    @media (max-width: 750px) {
      .slide, .price-slide { padding: 1.5rem; }
      .grid-3 { grid-template-columns: 1fr; }
      .hero-title { font-size: 2.8rem; }
      .contact-links { flex-direction: column; gap: 1.2rem; border-radius: 40px; }
      .stats { flex-direction: column; gap: 0.5rem; }
      .slide-nav button { padding: 0.4rem 1rem; font-size: 0.8rem; }
      .nav-links { gap: 0.8rem; }
    }
    @media (max-width: 480px) {
      .features { grid-template-columns: 1fr 1fr; }
      .price-row { flex-direction: column; align-items: flex-start; }
      .price-row .price { width: 100%; justify-content: space-between; }
    }
  </style>
</head>
<body>
<div class="deck" id="deckContainer">

  <!-- SLIDE 1 - HOME -->
  <div class="slide fade-in" data-slide="0">
    <div class="navbar">
      <a href="#" class="logo"><i class="fas fa-crown"></i> VANOZZZRESELL</a>
      <div class="nav-links">
        <span class="active" data-slide="0">HOME</span>
        <span data-slide="1">CONTENT</span>
        <span data-slide="2">ABOUT</span>
        <span data-slide="3">FEATURES</span>
        <span data-slide="4">CONTACT</span>
        <span data-slide="5">PRICELIST</span>
      </div>
    </div>
    <div class="hero-title">THE POWER OF<br>VANOZZZ</div>
    <div class="hero-sub">GROWTH FOR BUSINESSES & COMMUNITIES WORLDWIDE.<br>INNOVATIVE DIGITAL SOLUTIONS DRIVING SMARTER EXPERIENCES, STRONGER CONNECTIONS.</div>
    <div class="hero-meta">
      <div class="presented">
        <div class="presented-item"><span class="label">PRESENTED BY</span><span class="value">VANOZZZ TEAM</span></div>
        <div class="presented-item"><span class="label">UPDATED</span><span class="value">MARCH 2026</span></div>
        <div class="presented-item"><span class="label">STATUS</span><span class="value" style="font-size:0.9rem; background:rgba(180,70,200,0.2); padding:0.2rem 1rem; border-radius:30px;">FINAL DRAFT</span></div>
      </div>
      <div class="status-badge"><i class="fas fa-circle" style="font-size:0.5rem; color:#fd8cd4;"></i> LIVE · 2026</div>
    </div>
  </div>

  <!-- SLIDE 2 - CONTENT -->
  <div class="slide hidden-slide" data-slide="1">
    <div class="navbar">
      <a href="#" class="logo"><i class="fas fa-crown"></i> VANOZZZRESELL</a>
      <div class="nav-links">
        <span data-slide="0">HOME</span>
        <span class="active" data-slide="1">CONTENT</span>
        <span data-slide="2">ABOUT</span>
        <span data-slide="3">FEATURES</span>
        <span data-slide="4">CONTACT</span>
        <span data-slide="5">PRICELIST</span>
      </div>
    </div>
    <h2 style="font-size:2.2rem; background:linear-gradient(145deg,#dbb8ff,#fc8ac8); -webkit-background-clip:text; background-clip:text; color:transparent; margin:0.5rem 0;">HOW TECHNOLOGY TRANSFORMS</h2>
    <div class="grid-3">
      <div class="card"><i class="fas fa-robot"></i><h3>AUTOMATION</h3><p>Simplify repetitive daily tasks.</p></div>
      <div class="card"><i class="fas fa-graduation-cap"></i><h3>EDUCATION</h3><p>Access knowledge anytime.</p></div>
      <div class="card"><i class="fas fa-heartbeat"></i><h3>HEALTHCARE</h3><p>Support better patient care.</p></div>
    </div>
  </div>

  <!-- SLIDE 3 - ABOUT -->
  <div class="slide hidden-slide" data-slide="2">
    <div class="navbar">
      <a href="#" class="logo"><i class="fas fa-crown"></i> VANOZZZRESELL</a>
      <div class="nav-links">
        <span data-slide="0">HOME</span>
        <span data-slide="1">CONTENT</span>
        <span class="active" data-slide="2">ABOUT</span>
        <span data-slide="3">FEATURES</span>
        <span data-slide="4">CONTACT</span>
        <span data-slide="5">PRICELIST</span>
      </div>
    </div>
    <div class="about-wrap">
      <div class="about-text">
        <h2>ABOUT US</h2>
        <p>We create innovative technology solutions that help organizations improve efficiency, enhance user experiences, and embrace digital transformations with confidence.</p>
        <p style="color:#b09ad6;">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p>
        <div class="stats">
          <div class="stat-item"><span class="stat-number">95%</span><span class="stat-label">PROJECTS DELIVERED</span></div>
          <div class="stat-item"><span class="stat-number">15+</span><span class="stat-label">YEARS EXPERIENCE</span></div>
          <div class="stat-item"><span class="stat-number">250+</span><span class="stat-label">HAPPY CLIENTS</span></div>
        </div>
      </div>
      <div style="font-size:5rem; opacity:0.3; color:#9f78cf;"><i class="fas fa-rocket"></i></div>
    </div>
  </div>

  <!-- SLIDE 4 - FEATURES -->
  <div class="slide hidden-slide" data-slide="3">
    <div class="navbar">
      <a href="#" class="logo"><i class="fas fa-crown"></i> VANOZZZRESELL</a>
      <div class="nav-links">
        <span data-slide="0">HOME</span>
        <span data-slide="1">CONTENT</span>
        <span data-slide="2">ABOUT</span>
        <span class="active" data-slide="3">FEATURES</span>
        <span data-slide="4">CONTACT</span>
        <span data-slide="5">PRICELIST</span>
      </div>
    </div>
    <h2 style="font-size:2.4rem; background:linear-gradient(135deg,#dbb8ff,#fc8ac8); -webkit-background-clip:text; background-clip:text; color:transparent; margin:0.8rem 0;">WHY CHOOSE US</h2>
    <div class="features">
      <div class="feat"><i class="fas fa-lightbulb"></i><h4>INNOVATION</h4><p>Modern, digital solutions.</p></div>
      <div class="feat"><i class="fas fa-shield-alt"></i><h4>SECURITY</h4><p>Reliable protection systems.</p></div>
      <div class="feat"><i class="fas fa-tachometer-alt"></i><h4>PERFORMANCE</h4><p>Fast and efficient.</p></div>
      <div class="feat"><i class="fas fa-handshake"></i><h4>COLLABORATION</h4><p>Strong client partnerships.</p></div>
      <div class="feat"><i class="fas fa-expand-arrows-alt"></i><h4>SCALABILITY</h4><p>Ready for future growth.</p></div>
    </div>
  </div>

  <!-- SLIDE 5 - CONTACT -->
  <div class="slide hidden-slide" data-slide="4">
    <div class="navbar">
      <a href="#" class="logo"><i class="fas fa-crown"></i> VANOZZZRESELL</a>
      <div class="nav-links">
        <span data-slide="0">HOME</span>
        <span data-slide="1">CONTENT</span>
        <span data-slide="2">ABOUT</span>
        <span data-slide="3">FEATURES</span>
        <span class="active" data-slide="4">CONTACT</span>
        <span data-slide="5">PRICELIST</span>
      </div>
    </div>
    <div class="cta">
      <h2>LET'S BUILD THE<br>FUTURE TOGETHER!</h2>
      <div class="contact-links">
        <div class="contact-item"><i class="fas fa-globe"></i><span class="label">WEBSITE</span><span class="value">VANOZZZRESELL.ID</span></div>
        <div class="contact-item"><i class="fas fa-envelope"></i><span class="label">EMAIL</span><span class="value">HELLO@VANOZZZ.COM</span></div>
        <div class="contact-item"><i class="fas fa-phone-alt"></i><span class="label">PHONE</span><span class="value">+62 888-8984-256</span></div>
      </div>
    </div>
  </div>

  <!-- SLIDE 6 - PRICELIST -->
  <div class="price-slide hidden-slide" data-slide="5">
    <div class="navbar">
      <a href="#" class="logo"><i class="fas fa-crown"></i> VANOZZZRESELL</a>
      <div class="nav-links">
        <span data-slide="0">HOME</span>
        <span data-slide="1">CONTENT</span>
        <span data-slide="2">ABOUT</span>
    treatment      <span data-slide="3">FEATURES</span>
        <spa
