<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Descubre el Corazón de Franuí — Experiencia Exclusiva</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@400;500;600;700&family=Nunito:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  :root{
    --vino:#6E1A23;
    --vino-medio:#8E2230;
    --vino-claro:#A93544;
    --rosa:#EFBFCC;
    --rosa-suave:#F8E0E6;
    --rosa-fuerte:#E89AAC;
    --crema:#F1E8D6;
    --crema-claro:#F8F2E6;
    --crema-textura:#EDE3CF;
    --choco:#3A2017;
    --choco-leche:#7A4A33;
    --choco-medio:#5C3422;
    --texto:#4A2A2A;
    --texto-suave:#7A5A56;
    --sombra:0 30px 70px -32px rgba(110,26,35,.4);
    --radio:30px;
  }
  *{margin:0;padding:0;box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{
    font-family:'Nunito',sans-serif;color:var(--texto);line-height:1.7;
    background:var(--crema);overflow-x:hidden;-webkit-font-smoothing:antialiased;position:relative;
  }
  /* canvas/linen texture overlay */
  body::before{
    content:'';position:fixed;inset:0;pointer-events:none;z-index:1;opacity:.5;mix-blend-mode:multiply;
    background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='140' height='140'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.09'/%3E%3C/svg%3E");
  }
  h1,h2,h3,h4{font-family:'Fredoka',sans-serif;font-weight:600;line-height:1.12;letter-spacing:-.01em}
  a{text-decoration:none;color:inherit}
  img{max-width:100%;display:block}
  .wrap{max-width:1180px;margin:0 auto;padding:0 28px;position:relative;z-index:2}
  .eyebrow{
    font-family:'Nunito',sans-serif;font-weight:800;font-size:.74rem;
    letter-spacing:.32em;text-transform:uppercase;color:var(--vino-claro);
    display:inline-block;margin-bottom:20px;
  }

  /* ---------- NAV ---------- */
  nav{position:fixed;top:0;left:0;width:100%;z-index:100;padding:20px 0;transition:all .45s ease}
  nav.scrolled{background:rgba(248,242,230,.88);backdrop-filter:blur(16px);padding:12px 0;box-shadow:0 10px 36px -26px rgba(110,26,35,.5)}
  .nav-inner{display:flex;align-items:center;justify-content:space-between}
  .logo{font-family:'Fredoka',sans-serif;font-size:2rem;font-weight:700;color:var(--vino);letter-spacing:-.02em;line-height:1;display:flex;align-items:flex-start}
  .logo .dot{width:8px;height:11px;background:var(--vino);border-radius:50% 50% 50% 50%/60% 60% 40% 40%;display:inline-block;margin:2px 0 0 1px;transform:rotate(8deg)}
  .nav-links{display:flex;gap:36px;align-items:center}
  .nav-links a{font-size:.9rem;font-weight:700;color:var(--vino);transition:color .3s;position:relative}
  .nav-links a::after{content:'';position:absolute;left:0;bottom:-6px;width:0;height:2px;background:var(--vino-claro);border-radius:2px;transition:width .35s}
  .nav-links a:not(.btn):hover{color:var(--vino-claro)}
  .nav-links a:not(.btn):hover::after{width:100%}
  .btn{
    display:inline-flex;align-items:center;gap:10px;font-family:'Fredoka',sans-serif;font-weight:600;
    font-size:.95rem;letter-spacing:.01em;padding:14px 30px;border-radius:100px;border:none;cursor:pointer;
    background:var(--vino);color:var(--crema-claro);transition:all .4s cubic-bezier(.2,.8,.2,1);
  }
  .btn:hover{background:var(--vino-claro);transform:translateY(-2px);box-shadow:0 16px 30px -12px rgba(110,26,35,.55)}
  .btn-ghost{background:transparent;color:var(--vino);border:2px solid rgba(110,26,35,.25)}
  .btn-ghost:hover{background:var(--vino);color:var(--crema-claro);border-color:var(--vino)}
  .nav-toggle{display:none;background:none;border:none;cursor:pointer;flex-direction:column;gap:5px}
  .nav-toggle span{width:26px;height:2.5px;background:var(--vino);border-radius:2px;transition:.3s}

  /* ---------- HERO ---------- */
  .hero{position:relative;min-height:auto;display:flex;align-items:center;padding:104px 0 56px;overflow:hidden}
  .hero-grid{display:grid;grid-template-columns:1.08fr .92fr;gap:24px;align-items:center;width:100%}
  .hero h1{font-size:clamp(2.9rem,6.2vw,5.2rem);color:var(--vino);margin-bottom:24px;font-weight:700}
  .hero h1 em{font-style:normal;color:var(--vino-claro)}
  .hero .sub{font-size:1.16rem;font-weight:500;max-width:460px;color:var(--texto-suave);margin-bottom:30px}
  .hero-cta{display:flex;gap:14px;align-items:center;flex-wrap:wrap}
  .hero-note{display:flex;align-items:center;gap:10px;font-size:.84rem;font-weight:700;color:var(--vino);margin-top:24px}
  .pulse{width:9px;height:9px;border-radius:50%;background:var(--vino-claro);box-shadow:0 0 0 0 rgba(169,53,68,.5);animation:pulse 2.2s infinite}
  @keyframes pulse{0%{box-shadow:0 0 0 0 rgba(169,53,68,.5)}70%{box-shadow:0 0 0 14px rgba(169,53,68,0)}100%{box-shadow:0 0 0 0 rgba(169,53,68,0)}}

  /* Franui hero art — pink circle + bonbones */
  .hero-art{position:relative;display:flex;justify-content:center;align-items:center}
  .franui-stage{position:relative;width:min(520px,100%);aspect-ratio:1;animation:float 7s ease-in-out infinite}
  @keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-18px)}}
  .franui-stage svg{position:relative;z-index:2}
  .splash{position:absolute;z-index:1;opacity:.9}
  .floating-bonbon{position:absolute;z-index:3;width:56px;filter:drop-shadow(0 12px 16px rgba(58,32,23,.35))}
  .fb1{top:4%;left:0%;animation:bob 5s ease-in-out infinite}
  .fb2{bottom:6%;right:0%;width:44px;animation:bob 6.4s ease-in-out infinite reverse}
  .fb3{bottom:26%;left:-5%;width:38px;animation:bob 5.6s ease-in-out infinite .6s}
  @keyframes bob{0%,100%{transform:translateY(0) rotate(-5deg)}50%{transform:translateY(-14px) rotate(6deg)}}

  .scroll-cue{position:absolute;bottom:18px;left:50%;transform:translateX(-50%);display:flex;flex-direction:column;
    align-items:center;gap:6px;font-size:.66rem;letter-spacing:.3em;text-transform:uppercase;color:var(--vino);font-weight:800;opacity:.7;z-index:2}
  .scroll-cue .line{width:2px;height:30px;background:linear-gradient(var(--vino),transparent);border-radius:2px;animation:drop 2s infinite}
  @keyframes drop{0%{transform:scaleY(.2);transform-origin:top}50%{transform:scaleY(1);transform-origin:top}50.1%{transform-origin:bottom}100%{transform:scaleY(.2);transform-origin:bottom}}

  /* ---------- SECTION BASE ---------- */
  .section-pad{padding:120px 0}
  .center{text-align:center}
  .section-title{font-size:clamp(2.1rem,4.4vw,3.4rem);color:var(--vino);margin-bottom:20px;font-weight:700}
  .section-title em{font-style:normal;color:var(--vino-claro)}
  .lead{font-size:1.12rem;color:var(--texto-suave);max-width:640px;margin:0 auto;font-weight:500}
  .reveal{opacity:0;transform:translateY(34px);transition:opacity .9s cubic-bezier(.2,.7,.2,1),transform .9s cubic-bezier(.2,.7,.2,1)}
  .reveal.in{opacity:1;transform:none}
  .d1{transition-delay:.1s}.d2{transition-delay:.2s}.d3{transition-delay:.3s}.d4{transition-delay:.4s}.d5{transition-delay:.5s}

  /* ---------- QUÉ ES (sección 2) ---------- */
  .quees{background:var(--crema-claro)}
  .quees-grid{display:grid;grid-template-columns:1fr 1fr;gap:70px;align-items:center}
  .quees-text p{font-size:1.08rem;color:var(--texto-suave);margin-bottom:20px;font-weight:500}
  .feature-row{display:flex;flex-direction:column;gap:24px;margin-top:36px}
  .feature{display:flex;gap:18px;align-items:flex-start}
  .feature .ic{flex-shrink:0;width:54px;height:54px;border-radius:18px;display:flex;align-items:center;justify-content:center;background:var(--rosa-suave);color:var(--vino)}
  .feature h4{font-size:1.2rem;color:var(--vino);margin-bottom:4px;font-weight:600}
  .feature p{font-size:.96rem;color:var(--texto-suave);margin:0;font-weight:500}
  .quees-art{position:relative;aspect-ratio:4/5;display:flex;align-items:center;justify-content:center}
  .quees-art .circle{position:absolute;width:90%;aspect-ratio:1;border-radius:50%;background:radial-gradient(circle at 38% 32%,var(--rosa) 0%,var(--rosa-fuerte) 100%);box-shadow:var(--sombra)}
  .quees-art svg{position:relative;z-index:2;width:74%;filter:drop-shadow(0 26px 34px rgba(58,32,23,.4))}

  /* ---------- QUÉ INCLUYE (sección 3) ---------- */
  .incluye{background:var(--crema)}
  .cards{display:grid;grid-template-columns:repeat(3,1fr);gap:26px;margin-top:62px}
  .card{background:var(--crema-claro);border-radius:var(--radio);padding:40px 34px;border:1.5px solid rgba(110,26,35,.08);
    box-shadow:0 20px 50px -38px rgba(110,26,35,.45);transition:transform .5s cubic-bezier(.2,.8,.2,1),box-shadow .5s;position:relative;overflow:hidden}
  .card::before{content:'';position:absolute;top:0;left:0;width:100%;height:5px;background:linear-gradient(90deg,var(--rosa-fuerte),var(--vino));transform:scaleX(0);transform-origin:left;transition:transform .5s}
  .card:hover{transform:translateY(-10px);box-shadow:0 40px 70px -42px rgba(110,26,35,.5)}
  .card:hover::before{transform:scaleX(1)}
  .card .ic{width:66px;height:66px;border-radius:20px;display:flex;align-items:center;justify-content:center;background:var(--rosa-suave);color:var(--vino);margin-bottom:24px}
  .card h3{font-size:1.4rem;color:var(--vino);margin-bottom:10px;font-weight:600}
  .card p{font-size:.97rem;color:var(--texto-suave);font-weight:500}
  .card .num{position:absolute;top:26px;right:30px;font-family:'Fredoka',sans-serif;font-size:1.15rem;color:var(--rosa-fuerte);font-weight:600}

  /* ---------- DETALLES (sección 4) ---------- */
  .detalles{background:var(--vino);color:var(--crema-claro);overflow:hidden;position:relative}
  .detalles::after{content:'';position:absolute;top:-25%;right:-8%;width:520px;height:520px;border-radius:50%;background:radial-gradient(circle,rgba(239,191,204,.2),transparent 65%)}
  .detalles .eyebrow{color:var(--rosa)}
  .detalles .section-title{color:var(--crema-claro)}
  .detalles .section-title em{color:var(--rosa)}
  .ticket{margin:58px auto 0;max-width:880px;background:rgba(255,255,255,.05);border:1.5px solid rgba(239,191,204,.25);
    border-radius:34px;overflow:hidden;display:grid;grid-template-columns:1.4fr 1fr;backdrop-filter:blur(6px);position:relative;z-index:2}
  .ticket-main{padding:52px 50px;border-right:2px dashed rgba(239,191,204,.3)}
  .ticket-main h3{font-size:2rem;color:var(--crema-claro);margin-bottom:32px;font-weight:600}
  .detail-grid{display:grid;grid-template-columns:1fr 1fr;gap:30px 24px}
  .detail-item .dlabel{font-size:.7rem;letter-spacing:.28em;text-transform:uppercase;color:var(--rosa);margin-bottom:8px;font-weight:800}
  .detail-item .dval{font-family:'Fredoka',sans-serif;font-size:1.35rem;color:var(--crema-claro);font-weight:500}
  .detail-item .dsub{font-size:.85rem;color:rgba(248,242,230,.6);font-weight:500}
  .ticket-side{padding:52px 40px;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;background:linear-gradient(160deg,rgba(232,154,172,.28),rgba(239,191,204,.1))}
  .ticket-side .cap{font-family:'Fredoka',sans-serif;font-size:1.5rem;color:var(--crema-claro);margin-bottom:14px;font-weight:600}
  .ticket-side p{font-size:.92rem;color:rgba(248,242,230,.8);margin-bottom:24px;font-weight:500}
  .seats{font-size:.74rem;letter-spacing:.16em;text-transform:uppercase;color:var(--rosa);margin-top:18px;font-weight:800}

  /* ---------- GALERÍA (sección 5) ---------- */
  .galeria{background:var(--crema-claro)}
  .gallery-grid{display:grid;grid-template-columns:repeat(4,1fr);grid-auto-rows:200px;gap:18px;margin-top:58px}
  .gtile{border-radius:24px;overflow:hidden;position:relative;cursor:pointer}
  .gtile .art{position:absolute;inset:0;transition:transform .9s cubic-bezier(.2,.8,.2,1)}
  .gtile:hover .art{transform:scale(1.09)}
  .gtile .cap{position:absolute;left:0;bottom:0;width:100%;padding:30px 22px 18px;z-index:3;color:#fff;font-family:'Fredoka',sans-serif;
    font-size:1.08rem;font-weight:500;background:linear-gradient(transparent,rgba(58,32,23,.72));opacity:0;transform:translateY(10px);transition:.5s}
  .gtile:hover .cap{opacity:1;transform:none}
  .g-tall{grid-row:span 2}
  .g-wide{grid-column:span 2}
  .art-svg{width:100%;height:100%;display:block}

  /* ---------- REGISTRO (sección 6) ---------- */
  .registro{background:linear-gradient(165deg,var(--rosa-suave) 0%,var(--crema) 72%);position:relative;overflow:hidden}
  .registro::before{content:'';position:absolute;bottom:-15%;left:-8%;width:420px;height:420px;border-radius:50%;background:radial-gradient(circle,rgba(239,191,204,.55),transparent 65%)}
  .form-wrap{max-width:640px;margin:54px auto 0;background:var(--crema-claro);border-radius:var(--radio);padding:56px 54px;box-shadow:var(--sombra);position:relative;z-index:2;border:1.5px solid rgba(255,255,255,.7)}
  .field{margin-bottom:22px}
  .field label{display:block;font-size:.74rem;letter-spacing:.16em;text-transform:uppercase;color:var(--vino);font-weight:800;margin-bottom:10px}
  .field input{width:100%;padding:16px 20px;border-radius:16px;border:2px solid rgba(110,26,35,.12);background:var(--crema);font-family:'Nunito',sans-serif;font-size:1rem;font-weight:500;color:var(--texto);transition:.3s}
  .field input:focus{outline:none;border-color:var(--vino-claro);background:#fff;box-shadow:0 0 0 4px rgba(169,53,68,.12)}
  .field input.err{border-color:var(--vino-claro);background:#fbeef0}
  .checkbox{display:flex;gap:14px;align-items:flex-start;margin:6px 0 28px;cursor:pointer}
  .checkbox input{width:22px;height:22px;flex-shrink:0;accent-color:var(--vino);margin-top:2px;cursor:pointer}
  .checkbox span{font-size:.93rem;color:var(--texto-suave);font-weight:500}
  .form-wrap .btn{width:100%;justify-content:center;padding:18px;font-size:1.02rem}
  .form-success{text-align:center;padding:24px 0}
  .form-success .check{width:72px;height:72px;margin:0 auto 22px;border-radius:50%;background:var(--rosa-suave);display:flex;align-items:center;justify-content:center;color:var(--vino);animation:pop .5s cubic-bezier(.2,1.4,.4,1)}
  @keyframes pop{0%{transform:scale(0)}100%{transform:scale(1)}}
  .form-success h3{font-size:1.7rem;color:var(--vino);margin-bottom:10px;font-weight:600}
  .form-success p{color:var(--texto-suave);font-weight:500}

  /* ---------- FOOTER ---------- */
  footer{background:var(--vino);color:var(--crema-claro);padding:90px 0 40px;text-align:center;position:relative}
  footer .quote{font-family:'Fredoka',sans-serif;font-size:clamp(1.6rem,3.6vw,2.6rem);max-width:760px;margin:0 auto 48px;line-height:1.28;color:var(--crema-claro);font-weight:500}
  footer .quote span{color:var(--rosa)}
  .foot-logo{font-family:'Fredoka',sans-serif;font-size:2.4rem;font-weight:700;margin-bottom:24px;color:var(--crema-claro);display:inline-flex;align-items:flex-start}
  .foot-logo .dot{width:9px;height:13px;background:var(--rosa);border-radius:50% 50% 50% 50%/60% 60% 40% 40%;display:inline-block;margin:3px 0 0 1px;transform:rotate(8deg)}
  .socials{display:flex;justify-content:center;gap:18px;margin-bottom:40px}
  .socials a{width:46px;height:46px;border-radius:50%;border:1.5px solid rgba(239,191,204,.35);display:flex;align-items:center;justify-content:center;color:var(--rosa);transition:.4s}
  .socials a:hover{background:var(--rosa-fuerte);border-color:var(--rosa-fuerte);color:var(--vino);transform:translateY(-3px)}
  .foot-bottom{font-size:.82rem;color:rgba(248,242,230,.5);font-weight:500;border-top:1.5px solid rgba(239,191,204,.18);padding-top:30px}

  /* ---------- RESPONSIVE ---------- */
  @media(max-width:920px){
    .nav-links{position:fixed;top:0;right:0;height:100vh;width:75%;max-width:320px;background:var(--crema-claro);flex-direction:column;justify-content:center;gap:30px;transform:translateX(100%);transition:.5s;box-shadow:var(--sombra)}
    .nav-links.open{transform:none}
    .nav-toggle{display:flex;z-index:101}
    .hero-grid,.quees-grid{grid-template-columns:1fr;gap:50px}
    .hero-art{order:-1}
    .franui-stage{width:min(340px,72%)}
    .cards{grid-template-columns:1fr 1fr}
    .ticket{grid-template-columns:1fr}
    .ticket-main{border-right:none;border-bottom:2px dashed rgba(239,191,204,.3)}
    .gallery-grid{grid-template-columns:repeat(2,1fr)}
  }
  @media(max-width:560px){
    .wrap{padding:0 20px}
    .section-pad{padding:80px 0}
    .cards{grid-template-columns:1fr}
    .detail-grid{grid-template-columns:1fr}
    .ticket-main,.ticket-side{padding:38px 30px}
    .form-wrap{padding:40px 26px}
    .gallery-grid{grid-template-columns:1fr;grid-auto-rows:180px}
    .g-wide{grid-column:span 1}
    .hero-cta{flex-direction:column;align-items:stretch}
    .hero-cta .btn{justify-content:center}
  }
</style>
</head>
<body>

<!-- ============ NAV ============ -->
<nav id="nav">
  <div class="wrap nav-inner">
    <div class="logo">franuí<span class="dot"></span></div>
    <div class="nav-links" id="navLinks">
      <a href="#experiencia">La experiencia</a>
      <a href="#incluye">Qué incluye</a>
      <a href="#evento">El evento</a>
      <a href="#galeria">Galería</a>
      <a href="#registro" class="btn">Reservar mi cupo</a>
    </div>
    <button class="nav-toggle" id="navToggle" aria-label="Menú"><span></span><span></span><span></span></button>
  </div>
</nav>

<!-- ============ HERO ============ -->
<header class="hero">
  <div class="wrap hero-grid">
    <div class="hero-copy">
      <span class="eyebrow reveal">Experiencia exclusiva · Solo por invitación</span>
      <h1 class="reveal d1">Descubre el <em>Corazón</em> de Franuí</h1>
      <p class="sub reveal d2">Una experiencia única donde la fruta real y el chocolate se encuentran para sorprender tus sentidos.</p>
      <div class="hero-cta reveal d3">
        <a href="#registro" class="btn">Reservar mi cupo
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M5 12h14M13 6l6 6-6 6" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </a>
        <a href="#experiencia" class="btn btn-ghost">Conocer más</a>
      </div>
      <div class="hero-note reveal d4"><span class="pulse"></span> Llegaste aquí desde tu caja Franuí · Cupos limitados</div>
    </div>

    <div class="hero-art reveal d2">
      <div class="franui-stage">
        <!-- chocolate + cream splash behind -->
        <svg class="splash" viewBox="0 0 460 460" width="100%" height="100%" style="top:0;left:0">
          <path d="M70 150 q-40 -20 -10 -55 q40 -10 55 25 q30 -50 70 -20 q10 40 -25 55 q40 30 5 65 q-45 5 -55 -30 q-30 35 -60 10 q-15 -35 20 -50z" fill="#F4E9D2" opacity=".0"/>
          <g fill="#4A2A18" opacity=".85">
            <path d="M360 90 q35 -25 55 5 q15 35 -20 50 q40 15 25 55 q-35 25 -60 -5 q-10 35 -45 25 q-20 -30 10 -50 q-35 -15 -15 -50 q35 -20 55 5 q-15 -25 -10 -35z"/>
          </g>
          <g fill="#F4E7CD" opacity=".9">
            <path d="M95 95 q-30 -20 -5 -45 q35 -10 45 20 q25 -40 55 -15 q10 30 -20 45 q35 20 5 50 q-40 5 -45 -25 q-25 30 -50 8 q-12 -30 15 -45z"/>
          </g>
        </svg>
        <!-- pink circle + cup of bonbones (signature franui frame) -->
        <svg viewBox="40 40 380 380" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <radialGradient id="pink" cx="38%" cy="32%" r="72%"><stop offset="0%" stop-color="#F6D2DB"/><stop offset="100%" stop-color="#E89AAC"/></radialGradient>
            <radialGradient id="choc" cx="36%" cy="30%" r="72%"><stop offset="0%" stop-color="#8A5638"/><stop offset="55%" stop-color="#5C3422"/><stop offset="100%" stop-color="#3A2017"/></radialGradient>
            <radialGradient id="rasp" cx="40%" cy="36%" r="72%"><stop offset="0%" stop-color="#D45B72"/><stop offset="100%" stop-color="#8E2230"/></radialGradient>
          </defs>
          <circle cx="230" cy="230" r="175" fill="url(#pink)"/>
          <!-- the cup -->
          <g transform="translate(150 150)">
            <path d="M10 30 L150 30 L138 175 Q138 188 124 188 L36 188 Q22 188 22 175 Z" fill="#F8F2E6"/>
            <ellipse cx="80" cy="30" rx="70" ry="16" fill="#FBF7EE"/>
            <rect x="22" y="56" width="116" height="58" rx="4" fill="#EFBFCC"/>
            <text x="80" y="92" font-family="Fredoka,sans-serif" font-size="26" font-weight="700" fill="#6E1A23" text-anchor="middle">franuí</text>
            <!-- bonbones piled -->
            <g fill="url(#choc)" stroke="#2E1810" stroke-width="1">
              <ellipse cx="55" cy="22" rx="17" ry="15"/><ellipse cx="88" cy="16" rx="17" ry="15"/><ellipse cx="118" cy="24" rx="16" ry="14"/>
              <ellipse cx="40" cy="6" rx="15" ry="13"/><ellipse cx="72" cy="2" rx="16" ry="14"/><ellipse cx="104" cy="5" rx="15" ry="13"/>
              <ellipse cx="60" cy="-12" rx="14" ry="12"/><ellipse cx="92" cy="-16" rx="15" ry="13"/>
            </g>
            <g fill="#A9694A" opacity=".5"><ellipse cx="50" cy="16" rx="5" ry="4"/><ellipse cx="84" cy="10" rx="5" ry="4"/><ellipse cx="67" cy="-6" rx="4" ry="3"/></g>
          </g>
          <!-- spilled bonbones + cross section showing raspberry -->
          <g stroke="#2E1810" stroke-width="1">
            <ellipse cx="120" cy="330" rx="20" ry="17" fill="url(#choc)"/>
            <ellipse cx="165" cy="350" rx="18" ry="15" fill="url(#choc)"/>
            <ellipse cx="300" cy="345" rx="19" ry="16" fill="url(#choc)"/>
          </g>
          <!-- cut bonbon: raspberry heart inside -->
          <g transform="translate(335 300)">
            <circle r="30" fill="url(#choc)" stroke="#2E1810" stroke-width="1"/>
            <circle r="19" fill="#F3E6D0"/>
            <circle r="11" fill="url(#rasp)"/>
            <g fill="#C75570"><circle cx="-4" cy="-3" r="3.4"/><circle cx="4" cy="-3" r="3.4"/><circle cx="0" cy="4" r="3.4"/></g>
          </g>
        </svg>
      </div>
      <svg class="floating-bonbon fb1" viewBox="0 0 60 60"><ellipse cx="30" cy="32" rx="24" ry="20" fill="#5C3422"/><ellipse cx="22" cy="24" rx="6" ry="4" fill="#A9694A" opacity=".5"/></svg>
      <svg class="floating-bonbon fb2" viewBox="0 0 60 60"><circle cx="30" cy="30" r="24" fill="#5C3422"/><circle cx="30" cy="30" r="13" fill="#8E2230"/><circle cx="30" cy="30" r="5" fill="#C75570"/></svg>
      <svg class="floating-bonbon fb3" viewBox="0 0 60 60"><ellipse cx="30" cy="32" rx="22" ry="19" fill="#3A2017"/><ellipse cx="23" cy="25" rx="5" ry="4" fill="#7A4A33" opacity=".6"/></svg>
    </div>
  </div>
  <div class="scroll-cue"><span>Desliza</span><span class="line"></span></div>
</header>

<!-- ============ SECCIÓN 2: QUÉ ES ============ -->
<section class="quees section-pad" id="experiencia">
  <div class="wrap quees-grid">
    <div class="quees-text">
      <span class="eyebrow reveal">La experiencia</span>
      <h2 class="section-title reveal d1">Un ritual para los <em>pequeños placeres</em></h2>
      <p class="reveal d2">La Experiencia Franuí es un evento exclusivo diseñado para los amantes de los pequeños placeres.</p>
      <p class="reveal d2">Durante una tarde especial podrás descubrir la historia detrás de Franuí, degustar diferentes variedades del producto y vivir una experiencia sensorial que combina sabor, textura y emoción.</p>
      <div class="feature-row">
        <div class="feature reveal d3">
          <div class="ic"><svg width="24" height="24" viewBox="0 0 24 24" fill="none"><path d="M12 21s-7-4.5-7-10a4 4 0 017-2.65A4 4 0 0119 11c0 5.5-7 10-7 10z" stroke="currentColor" stroke-width="1.9" stroke-linejoin="round"/></svg></div>
          <div><h4>Sabor auténtico</h4><p>Frambuesa real envuelta en capas de chocolate con leche y negro.</p></div>
        </div>
        <div class="feature reveal d4">
          <div class="ic"><svg width="24" height="24" viewBox="0 0 24 24" fill="none"><circle cx="12" cy="12" r="9" stroke="currentColor" stroke-width="1.9"/><path d="M12 7v5l3 2" stroke="currentColor" stroke-width="1.9" stroke-linecap="round"/></svg></div>
          <div><h4>Una tarde única</h4><p>Un encuentro pensado al detalle para activar todos tus sentidos.</p></div>
        </div>
        <div class="feature reveal d5">
          <div class="ic"><svg width="24" height="24" viewBox="0 0 24 24" fill="none"><path d="M12 3l2.4 5 5.6.6-4.2 3.8 1.2 5.6L12 15.8 7 18l1.2-5.6L4 8.6 9.6 8z" stroke="currentColor" stroke-width="1.7" stroke-linejoin="round"/></svg></div>
          <div><h4>Detalles de lujo</h4><p>Cada momento curado para que te lleves algo más que un sabor.</p></div>
        </div>
      </div>
    </div>
    <div class="quees-art reveal d2">
      <div class="circle"></div>
      <svg viewBox="0 0 240 240"><defs><radialGradient id="c2" cx="36%" cy="30%" r="72%"><stop offset="0%" stop-color="#8A5638"/><stop offset="100%" stop-color="#3A2017"/></radialGradient></defs>
        <g fill="url(#c2)" stroke="#2E1810" stroke-width="1.5"><ellipse cx="120" cy="96" rx="30" ry="26"/><ellipse cx="86" cy="116" rx="30" ry="26"/><ellipse cx="154" cy="116" rx="30" ry="26"/><ellipse cx="104" cy="146" rx="30" ry="26"/><ellipse cx="140" cy="146" rx="30" ry="26"/></g>
        <g fill="#A9694A" opacity=".5"><ellipse cx="112" cy="88" rx="8" ry="6"/><ellipse cx="78" cy="108" rx="8" ry="6"/><ellipse cx="146" cy="108" rx="8" ry="6"/></g>
      </svg>
    </div>
  </div>
</section>

<!-- ============ SECCIÓN 3: QUÉ INCLUYE ============ -->
<section class="incluye section-pad" id="incluye">
  <div class="wrap center">
    <span class="eyebrow reveal">Todo lo que vivirás</span>
    <h2 class="section-title reveal d1">¿Qué incluye tu <em>experiencia</em>?</h2>
    <p class="lead reveal d2">Cada elemento ha sido elegido para que la tarde se convierta en un recuerdo inolvidable.</p>
    <div class="cards">
      <div class="card reveal d1"><span class="num">01</span>
        <div class="ic"><svg width="30" height="30" viewBox="0 0 24 24" fill="none"><path d="M6 3v7a4 4 0 008 0V3M10 3v18M6 3h8" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <h3>Degustación guiada</h3><p>Un recorrido sensorial por las variedades de Franuí, narrado paso a paso.</p>
      </div>
      <div class="card reveal d2"><span class="num">02</span>
        <div class="ic"><svg width="30" height="30" viewBox="0 0 24 24" fill="none"><path d="M8 22h8M12 15v7M5 3h14l-1 7a6 6 0 01-12 0L5 3z" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <h3>Maridaje selecto</h3><p>Bebidas cuidadosamente seleccionadas para realzar cada nota de sabor.</p>
      </div>
      <div class="card reveal d3"><span class="num">03</span>
        <div class="ic"><svg width="30" height="30" viewBox="0 0 24 24" fill="none"><rect x="3" y="6" width="18" height="14" rx="3" stroke="currentColor" stroke-width="1.8"/><circle cx="12" cy="13" r="4" stroke="currentColor" stroke-width="1.8"/><path d="M8 6l1.5-3h5L16 6" stroke="currentColor" stroke-width="1.8" stroke-linejoin="round"/></svg></div>
        <h3>Photobooth</h3><p>Un set diseñado para capturar el momento con una estética digna de Franuí.</p>
      </div>
      <div class="card reveal d1"><span class="num">04</span>
        <div class="ic"><svg width="30" height="30" viewBox="0 0 24 24" fill="none"><path d="M20 12v9H4v-9M2 7h20v5H2zM12 7V4a2.5 2.5 0 10-5 0c0 2 2.5 3 5 3zM12 7V4a2.5 2.5 0 115 0c0 2-2.5 3-5 3zM12 7v14" stroke="currentColor" stroke-width="1.7" stroke-linejoin="round"/></svg></div>
        <h3>Regalos exclusivos</h3><p>Un obsequio especial pensado solo para los asistentes de la experiencia.</p>
      </div>
      <div class="card reveal d2"><span class="num">05</span>
        <div class="ic"><svg width="30" height="30" viewBox="0 0 24 24" fill="none"><path d="M12 3l2.4 5 5.6.6-4.2 3.8 1.2 5.6L12 15.8 7 18l1.2-5.6L4 8.6 9.6 8z" stroke="currentColor" stroke-width="1.7" stroke-linejoin="round"/></svg></div>
        <h3>Sorteos & sorpresas</h3><p>Experiencias inesperadas que solo se viven dentro del corazón de Franuí.</p>
      </div>
      <div class="card reveal d3"><span class="num">06</span>
        <div class="ic"><svg width="30" height="30" viewBox="0 0 24 24" fill="none"><circle cx="12" cy="8" r="4" stroke="currentColor" stroke-width="1.8"/><path d="M5 21a7 7 0 0114 0" stroke="currentColor" stroke-width="1.8" stroke-linecap="round"/></svg></div>
        <h3>Anfitriones expertos</h3><p>Un equipo apasionado te acompaña en cada instante de la velada.</p>
      </div>
    </div>
  </div>
</section>

<!-- ============ SECCIÓN 4: DETALLES ============ -->
<section class="detalles section-pad" id="evento">
  <div class="wrap center">
    <span class="eyebrow reveal">Reserva tu lugar</span>
    <h2 class="section-title reveal d1">Los detalles de la <em>velada</em></h2>
    <div class="ticket reveal d2">
      <div class="ticket-main">
        <h3>Descubre el Corazón de Franuí</h3>
        <div class="detail-grid">
          <div class="detail-item"><div class="dlabel">Fecha</div><div class="dval">15 de diciembre</div><div class="dsub">2026</div></div>
          <div class="detail-item"><div class="dlabel">Hora</div><div class="dval">6:00 PM</div><div class="dsub">Apertura de puertas 5:30 PM</div></div>
          <div class="detail-item"><div class="dlabel">Lugar</div><div class="dval">Espacio Gourmet Franuí</div><div class="dsub">Te enviaremos la ubicación exacta</div></div>
          <div class="detail-item"><div class="dlabel">Dress code</div><div class="dval">Elegante</div><div class="dsub">Ven listo para las fotos</div></div>
        </div>
      </div>
      <div class="ticket-side">
        <div class="cap">Capacidad limitada</div>
        <p>“Cupos limitados. Reserva tu experiencia antes de que se agoten.”</p>
        <a href="#registro" class="btn">Reservar mi cupo</a>
        <div class="seats">● Quedan pocos lugares</div>
      </div>
    </div>
  </div>
</section>

<!-- ============ SECCIÓN 5: GALERÍA ============ -->
<section class="galeria section-pad" id="galeria">
  <div class="wrap center">
    <span class="eyebrow reveal">Un anticipo</span>
    <h2 class="section-title reveal d1">Momentos que te <em>esperan</em></h2>
    <p class="lead reveal d2">Texturas, color y emoción. Una pequeña muestra de lo que vivirás.</p>
    <div class="gallery-grid">
      <div class="gtile g-tall reveal d1">
        <div class="art"><svg class="art-svg" viewBox="0 0 200 400" preserveAspectRatio="xMidYMid slice"><rect width="200" height="400" fill="#E89AAC"/><g fill="#5C3422" stroke="#2E1810" stroke-width="2"><ellipse cx="70" cy="120" rx="42" ry="36"/><ellipse cx="130" cy="170" rx="42" ry="36"/><ellipse cx="60" cy="220" rx="42" ry="36"/><ellipse cx="135" cy="270" rx="42" ry="36"/><ellipse cx="80" cy="320" rx="42" ry="36"/></g><g fill="#A9694A" opacity=".5"><ellipse cx="58" cy="108" rx="11" ry="8"/><ellipse cx="118" cy="158" rx="11" ry="8"/></g></svg></div>
        <div class="cap">Bombones Franuí</div>
      </div>
      <div class="gtile g-wide reveal d2">
        <div class="art"><svg class="art-svg" viewBox="0 0 400 200" preserveAspectRatio="xMidYMid slice"><rect width="400" height="200" fill="#3A2017"/><g fill="#5C3422"><circle cx="100" cy="100" r="70"/><circle cx="240" cy="80" r="60"/><circle cx="340" cy="140" r="60"/></g><ellipse cx="120" cy="60" rx="50" ry="20" fill="#F4E7CD" opacity=".18"/></svg></div>
        <div class="cap">Chocolate fundido</div>
      </div>
      <div class="gtile reveal d3">
        <div class="art"><svg class="art-svg" viewBox="0 0 200 200" preserveAspectRatio="xMidYMid slice"><rect width="200" height="200" fill="#EFBFCC"/><circle cx="100" cy="100" r="62" fill="#3A2017"/><circle cx="100" cy="100" r="36" fill="#8E2230"/><g fill="#C75570"><circle cx="90" cy="92" r="9"/><circle cx="110" cy="92" r="9"/><circle cx="100" cy="110" r="9"/></g></svg></div>
        <div class="cap">El corazón Franuí</div>
      </div>
      <div class="gtile reveal d1">
        <div class="art"><svg class="art-svg" viewBox="0 0 200 200" preserveAspectRatio="xMidYMid slice"><rect width="200" height="200" fill="#F8F2E6"/><g fill="#5C3422" stroke="#2E1810" stroke-width="2"><ellipse cx="80" cy="80" rx="28" ry="24"/><ellipse cx="120" cy="92" rx="28" ry="24"/><ellipse cx="98" cy="118" rx="28" ry="24"/></g><rect x="40" y="152" width="120" height="11" rx="5" fill="#E89AAC"/></svg></div>
        <div class="cap">Mesa de degustación</div>
      </div>
      <div class="gtile g-wide reveal d2">
        <div class="art"><svg class="art-svg" viewBox="0 0 400 200" preserveAspectRatio="xMidYMid slice"><rect width="400" height="200" fill="#EFBFCC"/><g fill="#F8E0E6"><circle cx="60" cy="60" r="34"/><circle cx="160" cy="120" r="40"/><circle cx="280" cy="60" r="34"/><circle cx="360" cy="140" r="40"/></g><g fill="#6E1A23" opacity=".25"><circle cx="160" cy="108" r="10"/><circle cx="280" cy="50" r="9"/></g></svg></div>
        <div class="cap">Brindis & maridaje</div>
      </div>
      <div class="gtile reveal d3">
        <div class="art"><svg class="art-svg" viewBox="0 0 200 200" preserveAspectRatio="xMidYMid slice"><rect width="200" height="200" fill="#6E1A23"/><circle cx="100" cy="88" r="46" fill="#8E2230"/><path d="M100 134v42M68 176h64" stroke="#EFBFCC" stroke-width="9" stroke-linecap="round"/></svg></div>
        <div class="cap">Ambiente íntimo</div>
      </div>
    </div>
  </div>
</section>

<!-- ============ SECCIÓN 6: REGISTRO ============ -->
<section class="registro section-pad" id="registro">
  <div class="wrap center">
    <span class="eyebrow reveal">Tu cupo te espera</span>
    <h2 class="section-title reveal d1">Reserva tu <em>cupo</em></h2>
    <p class="lead reveal d2">Completa tus datos y asegura tu cupo en una de las experiencias más exclusivas de Franuí.</p>
    <div class="form-wrap reveal d2">
      <form id="reserva" novalidate>
        <div class="field"><label for="nombre">Nombre completo</label><input type="text" id="nombre" placeholder="Tu nombre" autocomplete="name"></div>
        <div class="field"><label for="correo">Correo electrónico</label><input type="email" id="correo" placeholder="tucorreo@ejemplo.com" autocomplete="email"></div>
        <div class="field"><label for="telefono">Teléfono</label><input type="tel" id="telefono" placeholder="+57 300 000 0000" autocomplete="tel"></div>
        <label class="checkbox"><input type="checkbox" id="novedades"><span>Deseo recibir novedades y experiencias exclusivas de Franuí.</span></label>
        <button type="submit" class="btn">Reservar mi cupo
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M5 12h14M13 6l6 6-6 6" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </button>
      </form>
      <div class="form-success" id="success" style="display:none">
        <div class="check"><svg width="34" height="34" viewBox="0 0 24 24" fill="none"><path d="M5 13l4 4L19 7" stroke="currentColor" stroke-width="2.6" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <h3>¡Tu cupo está reservado!</h3>
        <p>Pronto recibirás un correo con todos los detalles de tu experiencia Franuí.</p>
      </div>
    </div>
  </div>
</section>

<!-- ============ FOOTER ============ -->
<footer>
  <div class="wrap">
    <p class="quote">“Porque algunas experiencias no se explican. <span>Se prueban.</span>”</p>
    <div class="foot-logo">franuí<span class="dot"></span></div>
    <div class="socials">
      <a href="#" aria-label="Instagram"><svg width="20" height="20" viewBox="0 0 24 24" fill="none"><rect x="3" y="3" width="18" height="18" rx="5" stroke="currentColor" stroke-width="1.8"/><circle cx="12" cy="12" r="4" stroke="currentColor" stroke-width="1.8"/><circle cx="17.5" cy="6.5" r="1.3" fill="currentColor"/></svg></a>
      <a href="#" aria-label="Facebook"><svg width="20" height="20" viewBox="0 0 24 24" fill="none"><path d="M14 8h2V5h-2a3 3 0 00-3 3v2H9v3h2v6h3v-6h2.2l.8-3H14V8.5a.5.5 0 01.5-.5z" stroke="currentColor" stroke-width="1.6" stroke-linejoin="round"/></svg></a>
      <a href="#" aria-label="TikTok"><svg width="20" height="20" viewBox="0 0 24 24" fill="none"><path d="M14 4v9.5a3.5 3.5 0 11-3.5-3.5M14 4c0 2.5 2 4.5 4.5 4.5" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></a>
      <a href="#" aria-label="YouTube"><svg width="20" height="20" viewBox="0 0 24 24" fill="none"><rect x="3" y="6" width="18" height="12" rx="4" stroke="currentColor" stroke-width="1.8"/><path d="M11 9.5l4 2.5-4 2.5z" fill="currentColor"/></svg></a>
    </div>
    <div class="foot-bottom">© 2026 Franuí · Experiencia exclusiva. Diseñado para los amantes de los pequeños placeres.</div>
  </div>
</footer>

<script>
  const nav=document.getElementById('nav');
  window.addEventListener('scroll',()=>nav.classList.toggle('scrolled',window.scrollY>40));
  const toggle=document.getElementById('navToggle'),links=document.getElementById('navLinks');
  toggle.addEventListener('click',()=>links.classList.toggle('open'));
  links.querySelectorAll('a').forEach(a=>a.addEventListener('click',()=>links.classList.remove('open')));
  const io=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting){e.target.classList.add('in');io.unobserve(e.target);}}),{threshold:.14});
  document.querySelectorAll('.reveal').forEach(el=>io.observe(el));
  const form=document.getElementById('reserva'),success=document.getElementById('success');
  form.addEventListener('submit',ev=>{
    ev.preventDefault();
    const n=document.getElementById('nombre'),c=document.getElementById('correo'),t=document.getElementById('telefono');
    let ok=true;[n,c,t].forEach(f=>f.classList.remove('err'));
    if(!n.value.trim()){n.classList.add('err');ok=false;}
    if(!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(c.value)){c.classList.add('err');ok=false;}
    if(t.value.replace(/\D/g,'').length<7){t.classList.add('err');ok=false;}
    if(!ok)return;
    form.style.display='none';success.style.display='block';
    success.scrollIntoView({behavior:'smooth',block:'center'});
  });
</script>
</body>
</html>
