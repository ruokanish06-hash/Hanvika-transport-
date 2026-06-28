# Hanvika-transport-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Hanvika Transport – Reliable Vehicle Transport Services</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700;900&family=Lato:wght@300;400;700&family=Oswald:wght@400;500&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --navy:   #1A2540;
    --gold:   #C8952A;
    --cream:  #F7F2EA;
    --white:  #FFFFFF;
    --steel:  #3A4A6B;
    --light:  #EAE4D8;
    --dark:   #0E1628;
    --text:   #2B2B2B;
    --muted:  #6B7280;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Lato', sans-serif;
    background: var(--cream);
    color: var(--text);
    line-height: 1.7;
  }

  /* ── TOP BAR ── */
  .topbar {
    background: var(--dark);
    color: var(--light);
    font-size: 0.8rem;
    font-family: 'Oswald', sans-serif;
    letter-spacing: 0.06em;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.45rem 2.5rem;
    gap: 1rem;
  }
  .topbar a { color: var(--gold); text-decoration: none; }
  .topbar a:hover { text-decoration: underline; }

  /* ── NAV ── */
  nav {
    background: var(--navy);
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 2.5rem;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 18px rgba(0,0,0,0.35);
  }
  .logo-wrap {
    display: flex;
    align-items: center;
    gap: 0.9rem;
    padding: 0.9rem 0;
  }
  .logo-icon {
    width: 52px; height: 52px;
    background: var(--gold);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }
  .logo-icon svg { width: 28px; height: 28px; fill: var(--navy); }
  .logo-text { line-height: 1.15; }
  .logo-text .brand { font-family: 'Playfair Display', serif; font-size: 1.35rem; color: var(--white); letter-spacing: 0.02em; }
  .logo-text .tagline { font-family: 'Oswald', sans-serif; font-size: 0.68rem; color: var(--gold); letter-spacing: 0.14em; text-transform: uppercase; }

  nav ul { list-style: none; display: flex; gap: 0.3rem; }
  nav ul li a {
    font-family: 'Oswald', sans-serif;
    font-size: 0.85rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--light);
    text-decoration: none;
    padding: 0.5rem 0.85rem;
    border-radius: 3px;
    transition: background 0.2s, color 0.2s;
  }
  nav ul li a:hover { background: var(--gold); color: var(--navy); }

  /* ── HERO ── */
  .hero {
    background: linear-gradient(135deg, var(--dark) 0%, var(--navy) 55%, var(--steel) 100%);
    position: relative;
    overflow: hidden;
    padding: 5.5rem 2.5rem 4.5rem;
    display: flex;
    align-items: center;
    min-height: 520px;
  }
  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image:
      repeating-linear-gradient(0deg, transparent, transparent 59px, rgba(200,149,42,0.07) 60px),
      repeating-linear-gradient(90deg, transparent, transparent 59px, rgba(200,149,42,0.07) 60px);
    pointer-events: none;
  }
  .hero-road {
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 6px;
    background: repeating-linear-gradient(90deg, var(--gold) 0, var(--gold) 40px, transparent 40px, transparent 80px);
    opacity: 0.35;
  }
  .hero-content { position: relative; max-width: 700px; }
  .hero-badge {
    display: inline-block;
    font-family: 'Oswald', sans-serif;
    font-size: 0.72rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    border: 1px solid var(--gold);
    padding: 0.3rem 0.9rem;
    border-radius: 2px;
    margin-bottom: 1.4rem;
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.4rem, 5vw, 3.8rem);
    font-weight: 900;
    color: var(--white);
    line-height: 1.1;
    margin-bottom: 1.1rem;
  }
  .hero h1 em { color: var(--gold); font-style: normal; }
  .hero p {
    font-size: 1.05rem;
    color: rgba(234,228,216,0.85);
    max-width: 520px;
    margin-bottom: 2rem;
    font-weight: 300;
  }
  .btn-primary {
    display: inline-block;
    background: var(--gold);
    color: var(--navy);
    font-family: 'Oswald', sans-serif;
    font-size: 0.9rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 0.8rem 2rem;
    border-radius: 3px;
    text-decoration: none;
    font-weight: 500;
    transition: background 0.2s, transform 0.15s;
    margin-right: 1rem;
  }
  .btn-primary:hover { background: #e0a930; transform: translateY(-2px); }
  .btn-ghost {
    display: inline-block;
    border: 2px solid rgba(234,228,216,0.5);
    color: var(--light);
    font-family: 'Oswald', sans-serif;
    font-size: 0.9rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 0.75rem 1.8rem;
    border-radius: 3px;
    text-decoration: none;
    transition: border-color 0.2s, color 0.2s;
  }
  .btn-ghost:hover { border-color: var(--gold); color: var(--gold); }

  .hero-truck {
    position: absolute;
    right: 3rem;
    bottom: 2.5rem;
    opacity: 0.13;
    pointer-events: none;
  }
  .hero-truck svg { width: 340px; height: auto; fill: var(--white); }

  /* ── STATS BAR ── */
  .stats-bar {
    background: var(--gold);
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 0;
  }
  .stat {
    padding: 1.2rem 2.5rem;
    text-align: center;
    border-right: 1px solid rgba(26,37,64,0.18);
    flex: 1;
    min-width: 160px;
  }
  .stat:last-child { border-right: none; }
  .stat .num {
    font-family: 'Playfair Display', serif;
    font-size: 1.9rem;
    font-weight: 900;
    color: var(--navy);
    line-height: 1;
  }
  .stat .lbl {
    font-family: 'Oswald', sans-serif;
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--dark);
    margin-top: 0.25rem;
  }

  /* ── SECTIONS ── */
  section { padding: 5rem 2.5rem; }

  .section-label {
    font-family: 'Oswald', sans-serif;
    font-size: 0.72rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 0.6rem;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3.5vw, 2.7rem);
    font-weight: 700;
    color: var(--navy);
    line-height: 1.15;
    margin-bottom: 1.2rem;
  }
  .divider {
    width: 56px; height: 3px;
    background: var(--gold);
    margin-bottom: 1.8rem;
  }
  .container { max-width: 1100px; margin: 0 auto; }

  /* ── ABOUT ── */
  #about { background: var(--white); }
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
  }
  .about-visual {
    background: var(--navy);
    border-radius: 4px;
    padding: 3rem 2rem;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .about-visual::before {
    content: '';
    position: absolute;
    top: -30px; right: -30px;
    width: 160px; height: 160px;
    border-radius: 50%;
    background: var(--gold);
    opacity: 0.1;
  }
  .about-visual svg { width: 120px; fill: var(--gold); opacity: 0.85; }
  .about-visual .owner-card {
    margin-top: 2rem;
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(200,149,42,0.3);
    border-radius: 3px;
    padding: 1.2rem;
  }
  .about-visual .owner-card p { color: var(--light); font-size: 0.9rem; line-height: 1.5; }
  .about-visual .owner-card strong { color: var(--gold); font-family: 'Playfair Display', serif; font-size: 1.05rem; display: block; margin-bottom: 0.2rem; }
  .about-text p { color: var(--muted); font-weight: 300; font-size: 1rem; margin-bottom: 1rem; }
  .checkmarks { list-style: none; margin-top: 1.5rem; display: grid; gap: 0.6rem; }
  .checkmarks li {
    display: flex; align-items: flex-start; gap: 0.7rem;
    font-size: 0.95rem;
  }
  .checkmarks li::before {
    content: '✔';
    color: var(--gold);
    font-size: 0.8rem;
    margin-top: 0.2rem;
    flex-shrink: 0;
  }

  /* ── SERVICES ── */
  #services { background: var(--cream); }
  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 1.5rem;
    margin-top: 2.5rem;
  }
  .service-card {
    background: var(--white);
    border-top: 3px solid var(--gold);
    border-radius: 3px;
    padding: 2rem 1.5rem;
    box-shadow: 0 2px 16px rgba(26,37,64,0.07);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .service-card:hover { transform: translateY(-4px); box-shadow: 0 8px 28px rgba(26,37,64,0.12); }
  .service-icon {
    width: 48px; height: 48px;
    background: var(--navy);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 1.1rem;
  }
  .service-icon svg { width: 24px; fill: var(--gold); }
  .service-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    color: var(--navy);
    margin-bottom: 0.5rem;
  }
  .service-card p { font-size: 0.88rem; color: var(--muted); line-height: 1.65; }

  /* ── WHY CHOOSE US ── */
  #why { background: var(--navy); }
  #why .section-title { color: var(--white); }
  #why .section-label { color: var(--gold); }
  .why-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2rem;
    margin-top: 3rem;
  }
  .why-card {
    text-align: center;
    padding: 1.5rem 1rem;
    border: 1px solid rgba(200,149,42,0.2);
    border-radius: 4px;
    transition: border-color 0.2s, background 0.2s;
  }
  .why-card:hover { border-color: var(--gold); background: rgba(200,149,42,0.05); }
  .why-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.8rem;
    font-weight: 900;
    color: var(--gold);
    opacity: 0.25;
    line-height: 1;
    margin-bottom: -0.5rem;
  }
  .why-card h3 { font-family: 'Playfair Display', serif; color: var(--white); font-size: 1rem; margin-bottom: 0.5rem; }
  .why-card p { font-size: 0.84rem; color: rgba(234,228,216,0.65); line-height: 1.6; }

  /* ── VEHICLES ── */
  #vehicles { background: var(--white); }
  .vehicle-feature {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3.5rem;
    align-items: center;
    margin-top: 2.5rem;
  }
  .vehicle-img {
    background: var(--cream);
    border-radius: 4px;
    border: 1px solid var(--light);
    padding: 3rem;
    display: flex; align-items: center; justify-content: center;
    position: relative;
    overflow: hidden;
  }
  .vehicle-img::after {
    content: 'BOLERO PICKUP';
    position: absolute;
    bottom: 1rem; right: 1rem;
    font-family: 'Oswald', sans-serif;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    color: var(--gold);
    border: 1px solid var(--gold);
    padding: 0.2rem 0.5rem;
    border-radius: 2px;
  }
  .vehicle-img svg { width: 220px; fill: var(--steel); }
  .vehicle-specs { list-style: none; margin-top: 1.2rem; display: grid; gap: 0.8rem; }
  .vehicle-specs li {
    display: flex;
    justify-content: space-between;
    border-bottom: 1px dashed var(--light);
    padding-bottom: 0.6rem;
    font-size: 0.9rem;
  }
  .vehicle-specs li span:first-child { color: var(--muted); }
  .vehicle-specs li span:last-child { font-weight: 700; color: var(--navy); }

  /* ── CONTACT ── */
  #contact { background: var(--dark); }
  #contact .section-title { color: var(--white); }
  #contact .section-label { color: var(--gold); }
  #contact .divider { background: var(--gold); }
  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3.5rem;
    margin-top: 2.5rem;
  }
  .contact-info { display: grid; gap: 1.5rem; }
  .cinfo {
    display: flex;
    gap: 1rem;
    align-items: flex-start;
  }
  .cinfo-icon {
    width: 42px; height: 42px; flex-shrink: 0;
    background: rgba(200,149,42,0.12);
    border: 1px solid rgba(200,149,42,0.3);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
  }
  .cinfo-icon svg { width: 18px; fill: var(--gold); }
  .cinfo-text label {
    font-family: 'Oswald', sans-serif;
    font-size: 0.68rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gold);
    display: block;
    margin-bottom: 0.2rem;
  }
  .cinfo-text p { color: var(--light); font-size: 0.95rem; line-height: 1.55; }
  .cinfo-text a { color: var(--gold); text-decoration: none; }

  .whatsapp-btn {
    display: inline-flex;
    align-items: center;
    gap: 0.6rem;
    background: #25D366;
    color: #fff;
    font-family: 'Oswald', sans-serif;
    font-size: 0.9rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 0.8rem 1.8rem;
    border-radius: 3px;
    text-decoration: none;
    margin-top: 0.5rem;
    transition: background 0.2s, transform 0.15s;
  }
  .whatsapp-btn:hover { background: #1ebe57; transform: translateY(-2px); }
  .whatsapp-btn svg { width: 20px; fill: #fff; }

  .contact-map-box {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(200,149,42,0.2);
    border-radius: 4px;
    padding: 2.5rem;
    display: flex;
    flex-direction: column;
    gap: 1.2rem;
  }
  .contact-map-box h3 { font-family: 'Playfair Display', serif; color: var(--white); font-size: 1.2rem; }
  .contact-map-box p { color: rgba(234,228,216,0.65); font-size: 0.9rem; line-height: 1.65; }
  .hours-table { width: 100%; border-collapse: collapse; margin-top: 0.5rem; }
  .hours-table td { padding: 0.5rem 0; font-size: 0.88rem; border-bottom: 1px solid rgba(255,255,255,0.06); }
  .hours-table td:first-child { color: rgba(234,228,216,0.55); }
  .hours-table td:last-child { color: var(--gold); text-align: right; font-weight: 700; }

  /* ── FOOTER ── */
  footer {
    background: var(--dark);
    border-top: 1px solid rgba(200,149,42,0.2);
    padding: 1.8rem 2.5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 1rem;
  }
  footer p { font-size: 0.8rem; color: rgba(234,228,216,0.4); }
  footer p strong { color: var(--gold); }
  .footer-links { display: flex; gap: 1.2rem; }
  .footer-links a { font-size: 0.8rem; color: rgba(234,228,216,0.4); text-decoration: none; transition: color 0.2s; }
  .footer-links a:hover { color: var(--gold); }

  /* ── MOBILE ── */
  @media (max-width: 768px) {
    .topbar { flex-direction: column; padding: 0.6rem 1rem; text-align: center; gap: 0.3rem; }
    nav { flex-direction: column; padding: 0.8rem 1rem; }
    nav ul { flex-wrap: wrap; justify-content: center; }
    .hero { padding: 3.5rem 1.2rem 3rem; min-height: auto; }
    .hero-truck { display: none; }
    .about-grid, .vehicle-feature, .contact-grid { grid-template-columns: 1fr; gap: 2rem; }
    section { padding: 3.5rem 1.2rem; }
    footer { flex-direction: column; align-items: flex-start; }
    .stats-bar { gap: 0; }
    .stat { min-width: 50%; }
  }
</style>
</head>
<body>

<!-- TOP BAR -->
<div class="topbar">
  <span>📍 Aandal Nagar Molachur Arch Opposite Sunguvarchatram</span>
  <span>📞 <a href="tel:9600648843">9600648843</a> &nbsp;|&nbsp; 🟢 24 / 7 Service Available</span>
</div>

<!-- NAV -->
<nav>
  <div class="logo-wrap">
    <div class="logo-icon">
      <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><path d="M2 20V11l4-6h14l4 6v9H2zM6 11h12l-2-3H8L6 11zM0 20h24v2H0zM26 14h4l2 4v5h-6V14zM3 22h3v2H3zM19 22h3v2h-3z"/></svg>
    </div>
    <div class="logo-text">
      <div class="brand">Hanvika Transport</div>
      <div class="tagline">Trusted · Reliable · On Time</div>
    </div>
  </div>
  <ul>
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#vehicles">Vehicles</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-content">
    <div class="hero-badge">Established · Sunguvarchatram</div>
    <h1>Transport You Can<br/><em>Always Count On</em></h1>
    <p>Hanvika Transport delivers safe, prompt, and professional vehicle transport services — day or night, every day of the year.</p>
    <a href="#contact" class="btn-primary">Book Now</a>
    <a href="tel:9600648843" class="btn-ghost">Call Us</a>
  </div>
  <div class="hero-truck">
    <svg viewBox="0 0 200 90" xmlns="http://www.w3.org/2000/svg"><rect x="10" y="30" width="110" height="45" rx="4"/><rect x="120" y="40" width="60" height="35" rx="3"/><circle cx="35" cy="78" r="10"/><circle cx="90" cy="78" r="10"/><circle cx="155" cy="78" r="10"/><rect x="120" y="50" width="55" height="18" rx="2" fill-opacity="0.3"/></svg>
  </div>
  <div class="hero-road"></div>
</section>

<!-- STATS -->
<div class="stats-bar">
  <div class="stat"><div class="num">24/7</div><div class="lbl">Service Hours</div></div>
  <div class="stat"><div class="num">100%</div><div class="lbl">On-Time Delivery</div></div>
  <div class="stat"><div class="num">Bolero</div><div class="lbl">Pickup Vehicle</div></div>
  <div class="stat"><div class="num">1 Call</div><div class="lbl">Instant Booking</div></div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="container">
    <div class="about-grid">
      <div class="about-visual">
        <svg viewBox="0 0 100 60" xmlns="http://www.w3.org/2000/svg"><rect x="5" y="15" width="60" height="30" rx="3"/><rect x="65" y="22" width="28" height="23" rx="2"/><circle cx="18" cy="47" r="7"/><circle cx="52" cy="47" r="7"/><circle cx="83" cy="47" r="7"/><rect x="65" y="28" width="26" height="12" rx="1" fill-opacity="0.4"/></svg>
        <div class="owner-card">
          <strong>Sivakumar S</strong>
          <p>Owner &amp; Founder<br/>Hanvika Transport Services</p>
        </div>
      </div>
      <div class="about-text">
        <div class="section-label">About Us</div>
        <h2 class="section-title">Your Trusted Transport Partner</h2>
        <div class="divider"></div>
        <p>Hanvika Transport is a dedicated vehicle transport service based in Sunguvarchatram, committed to delivering safe, efficient, and affordable transport solutions to individuals and businesses alike.</p>
        <p>Under the leadership of <strong>Sivakumar S</strong>, we operate with integrity, punctuality, and a customer-first mindset — ensuring every journey is handled with care.</p>
        <ul class="checkmarks">
          <li>Fully operational 24 hours a day, 7 days a week</li>
          <li>Experienced and professional drivers</li>
          <li>Bolero pickup vehicle — robust, reliable, and road-ready</li>
          <li>Direct WhatsApp booking for instant confirmation</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <div class="container">
    <div class="section-label">What We Offer</div>
    <h2 class="section-title">Our Transport Services</h2>
    <div class="divider"></div>
    <div class="services-grid">
      <div class="service-card">
        <div class="service-icon"><svg viewBox="0 0 24 24"><path d="M20 8h-3V4H3c-1.1 0-2 .9-2 2v11h2c0 1.66 1.34 3 3 3s3-1.34 3-3h6c0 1.66 1.34 3 3 3s3-1.34 3-3h2v-5l-3-4zM6 18.5c-.83 0-1.5-.67-1.5-1.5S5.17 15.5 6 15.5s1.5.67 1.5 1.5-.67 1.5-1.5 1.5zm13.5-9l1.96 2.5H17V9.5h2.5zm-1.5 9c-.83 0-1.5-.67-1.5-1.5s.67-1.5 1.5-1.5 1.5.67 1.5 1.5-.67 1.5-1.5 1.5z"/></svg></div>
        <h3>Goods Transport</h3>
        <p>Carry goods, materials, and loads safely using our Bolero Pickup — built for heavy-duty hauling.</p>
      </div>
      <div class="service-card">
        <div class="service-icon"><svg viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg></div>
        <h3>Local & Outstation</h3>
        <p>Whether it's a local run or a long outstation trip, we cover your route with the same dedication and care.</p>
      </div>
      <div class="service-card">
        <div class="service-icon"><svg vi
