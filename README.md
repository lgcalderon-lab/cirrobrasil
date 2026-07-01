[index.html](https://github.com/user-attachments/files/29564263/index.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CIRRO — Centro de Inovação em Cirurgia e Robótica</title>
<meta name="description" content="CIRRO — Precisão que forma a próxima geração de cirurgiões. Treinamento avançado em cirurgia robótica.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --petroleo: #0E3B45;
    --petroleo-profundo: #0A2C34;
    --dourado: #C6A24A;
    --dourado-claro: #D8BC72;
    --papel: #F5F2EA;
    --papel-90: #F5F2EAE6;
    --branco: #FFFFFF;
    --linha: rgba(14,59,69,0.14);
    --linha-clara: rgba(245,242,234,0.16);
    --maxw: 1180px;
  }

  *{ box-sizing:border-box; margin:0; padding:0; }
  html{ scroll-behavior:smooth; }
  body{
    background:var(--papel);
    color:var(--petroleo);
    font-family:'Space Grotesk', sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }
  h1,h2,h3,.logotype{ font-family:'Sora', sans-serif; }
  a{ color:inherit; text-decoration:none; }
  img{ max-width:100%; display:block; }
  ul{ list-style:none; }

  .wrap{ max-width:var(--maxw); margin:0 auto; padding:0 clamp(20px,5vw,48px); }

  .eyebrow{
    font-family:'Space Grotesk', sans-serif;
    font-size:0.72rem;
    letter-spacing:0.18em;
    text-transform:uppercase;
    color:var(--dourado);
    font-weight:600;
    display:flex;
    align-items:center;
    gap:12px;
  }
  .eyebrow::before{
    content:"";
    width:22px; height:1px;
    background:var(--dourado);
    display:inline-block;
  }

  /* ---------- Símbolo / Logo ---------- */
  .mark{ display:inline-flex; align-items:center; gap:12px; }
  .mark svg{ display:block; }
  .mark .logotype{
    font-weight:700;
    font-size:1.15rem;
    letter-spacing:0.05em;
    color:currentColor;
  }

  /* ---------- Header ---------- */
  header{
    position:fixed; top:0; left:0; right:0; z-index:100;
    background:var(--papel-90);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--linha);
    transition:transform .4s ease;
  }
  header .wrap{
    display:flex; align-items:center; justify-content:space-between;
    height:76px;
  }
  header .mark{ color:var(--petroleo); }
  nav.primary-nav{ display:flex; align-items:center; gap:36px; }
  nav.primary-nav a{
    font-size:0.85rem;
    letter-spacing:0.03em;
    color:var(--petroleo);
    opacity:0.72;
    transition:opacity .2s ease;
    position:relative;
  }
  nav.primary-nav a:hover{ opacity:1; }
  .btn{
    display:inline-flex; align-items:center; gap:8px;
    font-family:'Space Grotesk', sans-serif;
    font-weight:600;
    font-size:0.85rem;
    letter-spacing:0.02em;
    padding:12px 22px;
    border-radius:999px;
    border:1px solid transparent;
    cursor:pointer;
    transition:all .25s ease;
    white-space:nowrap;
  }
  .btn-primary{
    background:var(--petroleo);
    color:var(--papel);
  }
  .btn-primary:hover{ background:var(--petroleo-profundo); transform:translateY(-1px); }
  .btn-gold{
    background:var(--dourado);
    color:var(--petroleo-profundo);
  }
  .btn-gold:hover{ background:var(--dourado-claro); transform:translateY(-1px); }
  .btn-outline{
    border-color:var(--linha-clara);
    color:var(--papel);
  }
  .btn-outline:hover{ border-color:var(--dourado); color:var(--dourado); }

  .menu-toggle{ display:none; }

  /* ---------- Hero ---------- */
  .hero{
    position:relative;
    background:var(--petroleo-profundo);
    color:var(--papel);
    padding:168px 0 120px;
    overflow:hidden;
  }
  .hero::before{
    content:"";
    position:absolute; inset:0;
    background:
      radial-gradient(circle at 78% 18%, rgba(198,162,74,0.14), transparent 42%),
      radial-gradient(circle at 15% 85%, rgba(14,59,69,0.5), transparent 55%);
    pointer-events:none;
  }
  .hero .wrap{
    position:relative;
    display:grid;
    grid-template-columns:1.15fr 0.85fr;
    align-items:center;
    gap:48px;
  }
  .hero-eyebrow{
    font-size:0.72rem; letter-spacing:0.18em; text-transform:uppercase;
    color:var(--dourado-claro); font-weight:600;
    display:flex; align-items:center; gap:12px; margin-bottom:26px;
  }
  .hero-eyebrow::before{ content:""; width:22px; height:1px; background:var(--dourado); }
  .hero h1{
    font-size:clamp(2.3rem, 4.6vw, 3.7rem);
    font-weight:700;
    line-height:1.08;
    letter-spacing:-0.01em;
    max-width:14ch;
  }
  .hero p.lead{
    margin-top:26px;
    font-size:clamp(1rem, 1.3vw, 1.15rem);
    color:rgba(245,242,234,0.78);
    max-width:46ch;
  }
  .hero .cta-row{
    margin-top:40px;
    display:flex; align-items:center; gap:18px; flex-wrap:wrap;
  }
  .hero .cta-note{
    font-size:0.8rem;
    color:rgba(245,242,234,0.55);
  }

  /* orbit signature */
  .orbit-stage{
    position:relative;
    aspect-ratio:1/1;
    width:min(420px, 100%);
    justify-self:center;
  }
  .orbit-stage svg{ width:100%; height:100%; overflow:visible; }
  .orbit-dot{
    transform-origin: 200px 200px;
    animation: orbit 9s linear infinite;
  }
  @keyframes orbit{
    from{ transform:rotate(0deg); }
    to{ transform:rotate(360deg); }
  }
  .orbit-caption{
    position:absolute; bottom:-38px; left:50%; transform:translateX(-50%);
    font-size:0.72rem; letter-spacing:0.1em; text-transform:uppercase;
    color:rgba(245,242,234,0.4); white-space:nowrap;
  }

  /* ---------- Section base ---------- */
  section{ padding:104px 0; }
  section.on-petroleo{ background:var(--petroleo); color:var(--papel); }
  section.on-petroleo .eyebrow{ color:var(--dourado-claro); }
  section.on-petroleo .eyebrow::before{ background:var(--dourado-claro); }
  .section-head{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:40px;
    align-items:end;
    margin-bottom:56px;
    border-bottom:1px solid var(--linha);
    padding-bottom:32px;
  }
  section.on-petroleo .section-head{ border-color:var(--linha-clara); }
  .section-head h2{
    margin-top:18px;
    font-size:clamp(1.7rem, 2.6vw, 2.3rem);
    font-weight:700;
    line-height:1.18;
    letter-spacing:-0.01em;
  }
  .section-head .desc{
    font-size:1rem;
    color:rgba(14,59,69,0.68);
    align-self:end;
  }
  section.on-petroleo .section-head .desc{ color:rgba(245,242,234,0.72); }

  /* ---------- Conceito ---------- */
  .concept{
    display:grid;
    grid-template-columns:auto 1fr;
    gap:40px;
    align-items:center;
    background:var(--branco);
    border:1px solid var(--linha);
    border-radius:18px;
    padding:clamp(28px,4vw,48px);
  }
  .concept .mark svg{ width:88px; height:88px; }
  .concept p{ font-size:1.02rem; color:rgba(14,59,69,0.8); max-width:62ch; }
  .concept strong{ color:var(--petroleo); }
  .concept .gold-word{ color:var(--dourado); font-weight:600; }

  /* ---------- Diferenciais grid ---------- */
  .grid-diff{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:1px;
    background:var(--linha);
    border:1px solid var(--linha);
    border-radius:18px;
    overflow:hidden;
  }
  .diff-card{
    background:var(--branco);
    padding:36px 30px;
    transition:background .25s ease;
  }
  .diff-card:hover{ background:var(--papel); }
  .diff-num{
    font-family:'Sora', sans-serif;
    font-size:0.78rem;
    color:var(--dourado);
    font-weight:700;
    letter-spacing:0.05em;
  }
  .diff-card h3{
    margin-top:14px;
    font-size:1.08rem;
    font-weight:600;
    line-height:1.3;
  }
  .diff-card p{
    margin-top:10px;
    font-size:0.92rem;
    color:rgba(14,59,69,0.66);
  }

  /* ---------- Especialidades ---------- */
  .chip-field{
    display:flex; flex-wrap:wrap; gap:12px;
  }
  .chip{
    font-size:0.88rem;
    font-weight:500;
    padding:11px 20px;
    border-radius:999px;
    border:1px solid var(--linha-clara);
    color:var(--papel);
    background:rgba(245,242,234,0.04);
    transition:all .2s ease;
  }
  .chip:hover{ border-color:var(--dourado); color:var(--dourado-claro); }

  /* ---------- Valores ---------- */
  .values-grid{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:36px 40px;
  }
  .value-item{ border-top:1px solid var(--linha); padding-top:20px; }
  .value-item .dot{
    width:8px; height:8px; border-radius:50%;
    background:var(--dourado);
    display:inline-block; margin-bottom:14px;
  }
  .value-item h3{ font-size:1.02rem; font-weight:600; }
  .value-item p{ margin-top:8px; font-size:0.9rem; color:rgba(14,59,69,0.66); }

  /* ---------- Instituição / parceiros strip ---------- */
  .partners-strip{
    background:var(--branco);
    border-top:1px solid var(--linha);
    border-bottom:1px solid var(--linha);
  }
  .partners-strip .wrap{
    display:flex; align-items:center; justify-content:space-between;
    gap:24px; flex-wrap:wrap;
    padding:34px clamp(20px,5vw,48px);
  }
  .partners-strip .p-label{
    font-size:0.75rem; letter-spacing:0.12em; text-transform:uppercase;
    color:rgba(14,59,69,0.5); font-weight:600;
  }
  .partners-strip .p-names{
    display:flex; gap:32px; flex-wrap:wrap;
    font-family:'Sora', sans-serif; font-weight:600;
    font-size:1rem; color:rgba(14,59,69,0.85);
  }

  /* ---------- CTA final ---------- */
  .cta-final{
    background:var(--petroleo-profundo);
    color:var(--papel);
    position:relative;
    overflow:hidden;
    padding:120px 0;
    text-align:center;
  }
  .cta-final::before{
    content:"";
    position:absolute; inset:0;
    background:radial-gradient(circle at 50% 0%, rgba(198,162,74,0.16), transparent 55%);
  }
  .cta-final .wrap{ position:relative; }
  .cta-final .mark{ justify-content:center; margin-bottom:28px; color:var(--papel); }
  .cta-final h2{
    font-size:clamp(1.8rem, 3.4vw, 2.6rem);
    font-weight:700;
    max-width:18ch;
    margin:0 auto;
    line-height:1.16;
  }
  .cta-final p{
    margin:20px auto 0;
    max-width:48ch;
    color:rgba(245,242,234,0.72);
    font-size:1rem;
  }
  .cta-final .cta-row{
    margin-top:38px;
    display:flex; justify-content:center; gap:16px; flex-wrap:wrap;
  }

  /* ---------- Footer ---------- */
  footer{
    background:var(--petroleo-profundo);
    border-top:1px solid var(--linha-clara);
    color:rgba(245,242,234,0.55);
    padding:36px 0;
  }
  footer .wrap{
    display:flex; align-items:center; justify-content:space-between;
    flex-wrap:wrap; gap:16px;
  }
  footer .mark{ color:rgba(245,242,234,0.85); }
  footer .f-note{ font-size:0.82rem; }
  footer .f-links{ display:flex; gap:22px; }
  footer .f-links a{ font-size:0.82rem; opacity:0.8; }
  footer .f-links a:hover{ opacity:1; color:var(--dourado-claro); }

  /* ---------- reveal on scroll ---------- */
  .reveal{ opacity:0; transform:translateY(18px); transition:opacity .7s ease, transform .7s ease; }
  .reveal.in{ opacity:1; transform:translateY(0); }

  /* ---------- responsive ---------- */
  @media (max-width:880px){
    nav.primary-nav{ display:none; }
    .menu-toggle{
      display:inline-flex; align-items:center; justify-content:center;
      width:40px; height:40px; border-radius:10px; border:1px solid var(--linha);
      background:transparent; cursor:pointer;
    }
    .hero .wrap{ grid-template-columns:1fr; text-align:left; }
    .hero h1{ max-width:100%; }
    .orbit-stage{ margin-top:20px; width:min(280px,80vw); }
    .section-head{ grid-template-columns:1fr; }
    .concept{ grid-template-columns:1fr; text-align:left; }
    .concept .mark{ justify-content:flex-start; }
    .grid-diff{ grid-template-columns:1fr; }
    .values-grid{ grid-template-columns:1fr 1fr; }
    .partners-strip .wrap{ flex-direction:column; align-items:flex-start; }
  }
  @media (max-width:520px){
    .values-grid{ grid-template-columns:1fr; }
    footer .wrap{ flex-direction:column; align-items:flex-start; }
  }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    .orbit-dot{ animation:none; }
    .reveal{ transition:none; opacity:1; transform:none; }
  }

  :focus-visible{
    outline:2px solid var(--dourado);
    outline-offset:3px;
  }
</style>
</head>
<body>

<!-- ============ HEADER ============ -->
<header>
  <div class="wrap">
    <a href="#topo" class="mark" aria-label="CIRRO — início">
      <svg width="34" height="34" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M29.04 7.28A15.6 15.6 0 1 0 34.2 26.47"
          stroke="currentColor" stroke-width="3.1" stroke-linecap="round"/>
        <circle cx="20.89" cy="19.92" r="3.86" fill="var(--dourado)"/>
      </svg>
      <span class="logotype">CIRRO</span>
    </a>
    <nav class="primary-nav">
      <a href="#conceito">Conceito</a>
      <a href="#diferenciais">Diferenciais</a>
      <a href="#especialidades">Especialidades</a>
      <a href="#valores">Valores</a>
      <a href="https://www.instagram.com/cirrobrasil" target="_blank" rel="noopener" class="btn btn-primary">
        <svg width="15" height="15" viewBox="0 0 24 24" fill="none"><path d="M12 2c2.7 0 3.06.01 4.12.06 1.06.05 1.79.22 2.43.47a4.9 4.9 0 0 1 1.77 1.15 4.9 4.9 0 0 1 1.15 1.77c.25.64.42 1.37.47 2.43C21.99 8.94 22 9.3 22 12s-.01 3.06-.06 4.12c-.05 1.06-.22 1.79-.47 2.43a4.9 4.9 0 0 1-1.15 1.77 4.9 4.9 0 0 1-1.77 1.15c-.64.25-1.37.42-2.43.47C15.06 21.99 14.7 22 12 22s-3.06-.01-4.12-.06c-1.06-.05-1.79-.22-2.43-.47a4.9 4.9 0 0 1-1.77-1.15 4.9 4.9 0 0 1-1.15-1.77c-.25-.64-.42-1.37-.47-2.43C2.01 15.06 2 14.7 2 12s.01-3.06.06-4.12c.05-1.06.22-1.79.47-2.43a4.9 4.9 0 0 1 1.15-1.77A4.9 4.9 0 0 1 5.45 2.53c.64-.25 1.37-.42 2.43-.47C8.94 2.01 9.3 2 12 2Zm0 5a5 5 0 1 1 0 10 5 5 0 0 1 0-10Zm0 1.8a3.2 3.2 0 1 0 0 6.4 3.2 3.2 0 0 0 0-6.4Zm5.2-2.9a1.17 1.17 0 1 1 0 2.34 1.17 1.17 0 0 1 0-2.34Z" fill="#F5F2EA"/></svg>
        Instagram
      </a>
    </nav>
    <button class="menu-toggle" id="menuToggle" aria-label="Abrir menu" aria-expanded="false">
      <svg width="18" height="14" viewBox="0 0 18 14" fill="none"><path d="M0 1H18M0 7H18M0 13H18" stroke="#0E3B45" stroke-width="1.6"/></svg>
    </button>
  </div>
  <div id="mobileMenu" style="display:none; border-top:1px solid var(--linha); background:var(--papel);">
    <div class="wrap" style="display:flex; flex-direction:column; gap:4px; padding:18px clamp(20px,5vw,48px) 24px;">
      <a href="#conceito" style="padding:10px 0;">Conceito</a>
      <a href="#diferenciais" style="padding:10px 0;">Diferenciais</a>
      <a href="#especialidades" style="padding:10px 0;">Especialidades</a>
      <a href="#valores" style="padding:10px 0;">Valores</a>
      <a href="https://www.instagram.com/cirrobrasil" target="_blank" rel="noopener" class="btn btn-primary" style="margin-top:10px; justify-content:center;">
        <svg width="15" height="15" viewBox="0 0 24 24" fill="none"><path d="M12 2c2.7 0 3.06.01 4.12.06 1.06.05 1.79.22 2.43.47a4.9 4.9 0 0 1 1.77 1.15 4.9 4.9 0 0 1 1.15 1.77c.25.64.42 1.37.47 2.43C21.99 8.94 22 9.3 22 12s-.01 3.06-.06 4.12c-.05 1.06-.22 1.79-.47 2.43a4.9 4.9 0 0 1-1.15 1.77 4.9 4.9 0 0 1-1.77 1.15c-.64.25-1.37.42-2.43.47C15.06 21.99 14.7 22 12 22s-3.06-.01-4.12-.06c-1.06-.05-1.79-.22-2.43-.47a4.9 4.9 0 0 1-1.77-1.15 4.9 4.9 0 0 1-1.15-1.77c-.25-.64-.42-1.37-.47-2.43C2.01 15.06 2 14.7 2 12s.01-3.06.06-4.12c.05-1.06.22-1.79.47-2.43a4.9 4.9 0 0 1 1.15-1.77A4.9 4.9 0 0 1 5.45 2.53c.64-.25 1.37-.42 2.43-.47C8.94 2.01 9.3 2 12 2Zm0 5a5 5 0 1 1 0 10 5 5 0 0 1 0-10Zm0 1.8a3.2 3.2 0 1 0 0 6.4 3.2 3.2 0 0 0 0-6.4Zm5.2-2.9a1.17 1.17 0 1 1 0 2.34 1.17 1.17 0 0 1 0-2.34Z" fill="#F5F2EA"/></svg>
        Seguir no Instagram
      </a>
    </div>
  </div>
</header>

<!-- ============ HERO ============ -->
<section class="hero" id="topo">
  <div class="wrap">
    <div>
      <div class="hero-eyebrow">Centro de Inovação em Cirurgia e Robótica</div>
      <h1>Precisão que forma a próxima geração de cirurgiões.</h1>
      <p class="lead">O CIRRO capacita médicos a dominar a cirurgia robótica, unindo simulação de alta fidelidade, prática em cadáver e parcerias com instituições de referência.</p>
      <div class="cta-row">
        <a href="https://www.instagram.com/cirrobrasil" target="_blank" rel="noopener" class="btn btn-gold">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M12 2c2.7 0 3.06.01 4.12.06 1.06.05 1.79.22 2.43.47a4.9 4.9 0 0 1 1.77 1.15 4.9 4.9 0 0 1 1.15 1.77c.25.64.42 1.37.47 2.43C21.99 8.94 22 9.3 22 12s-.01 3.06-.06 4.12c-.05 1.06-.22 1.79-.47 2.43a4.9 4.9 0 0 1-1.15 1.77 4.9 4.9 0 0 1-1.77 1.15c-.64.25-1.37.42-2.43.47C15.06 21.99 14.7 22 12 22s-3.06-.01-4.12-.06c-1.06-.05-1.79-.22-2.43-.47a4.9 4.9 0 0 1-1.77-1.15 4.9 4.9 0 0 1-1.15-1.77c-.25-.64-.42-1.37-.47-2.43C2.01 15.06 2 14.7 2 12s.01-3.06.06-4.12c.05-1.06.22-1.79.47-2.43a4.9 4.9 0 0 1 1.15-1.77A4.9 4.9 0 0 1 5.45 2.53c.64-.25 1.37-.42 2.43-.47C8.94 2.01 9.3 2 12 2Zm0 5a5 5 0 1 1 0 10 5 5 0 0 1 0-10Zm0 1.8a3.2 3.2 0 1 0 0 6.4 3.2 3.2 0 0 0 0-6.4Zm5.2-2.9a1.17 1.17 0 1 1 0 2.34 1.17 1.17 0 0 1 0-2.34Z" fill="currentColor"/></svg>
          Siga no Instagram
        </a>
        <a href="#conceito" class="btn btn-outline">Conhecer o CIRRO</a>
      </div>
      <p class="cta-note">@cirrobrasil — em breve, mais canais de contato.</p>
    </div>

    <div class="orbit-stage" aria-hidden="true">
      <svg viewBox="0 0 400 400">
        <circle cx="200" cy="200" r="150" fill="none" stroke="rgba(245,242,234,0.08)" stroke-width="1"/>
        <path d="M278.2 90.0A135 135 0 1 0 322.8 256.0"
          stroke="var(--papel)" stroke-width="9" stroke-linecap="round" fill="none" opacity="0.92"/>
        <g class="orbit-dot">
          <circle cx="120" cy="200" r="9" fill="var(--dourado)"/>
        </g>
      </svg>
      <div class="orbit-caption">O pivô dourado — ponto de precisão</div>
    </div>
  </div>
</section>

<!-- ============ CONCEITO ============ -->
<section id="conceito">
  <div class="wrap">
    <div class="section-head reveal">
      <div>
        <div class="eyebrow">01 · Conceito</div>
        <h2>Um símbolo, uma missão.</h2>
      </div>
      <p class="desc">O CIRRO existe para formar cirurgiões com domínio real da técnica robótica — não apenas exposição a ela.</p>
    </div>

    <div class="concept reveal">
      <div class="mark">
        <svg width="88" height="88" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M29.04 7.28A15.6 15.6 0 1 0 34.2 26.47"
            stroke="var(--petroleo)" stroke-width="3.1" stroke-linecap="round"/>
          <circle cx="20.89" cy="19.92" r="3.86" fill="var(--dourado)"/>
        </svg>
      </div>
      <p>
        O símbolo do CIRRO é um anel aberto que forma a inicial <strong>“C”</strong> — a órbita de um braço robótico em torno de um ponto de foco.
        O <span class="gold-word">pivô dourado</span> marca o ponto de precisão: o gesto exato, o centro do movimento cirúrgico.
        A mesma lógica orienta o centro — <strong>precisão</strong>, <strong>solidez</strong> e <strong>confiança</strong> aplicadas à formação de cirurgiões em robótica.
      </p>
    </div>
  </div>
</section>

<!-- ============ DIFERENCIAIS ============ -->
<section id="diferenciais">
  <div class="wrap">
    <div class="section-head reveal">
      <div>
        <div class="eyebrow">02 · Diferenciais</div>
        <h2>Formação construída para gerar competência real.</h2>
      </div>
      <p class="desc">Cada diferencial do CIRRO responde a uma lacuna concreta na formação em cirurgia robótica no Brasil.</p>
    </div>

    <div class="grid-diff reveal">
      <div class="diff-card">
        <div class="diff-num">01</div>
        <h3>Robótica &amp; inovação tecnológica</h3>
        <p>Programas construídos em torno dos sistemas cirúrgicos robóticos mais recentes, com foco exclusivo em técnica minimamente invasiva.</p>
      </div>
      <div class="diff-card">
        <div class="diff-num">02</div>
        <h3>Cadáver + simulação de alta fidelidade</h3>
        <p>Prática em cadáver combinada a simuladores com realidade virtual — condições muito próximas das reais antes do paciente.</p>
      </div>
      <div class="diff-card">
        <div class="diff-num">03</div>
        <h3>Parcerias com hospitais de referência</h3>
        <p>Colaborações estratégicas com fabricantes de equipamentos e instituições de saúde de ponta para acesso a tecnologia atual.</p>
      </div>
      <div class="diff-card">
        <div class="diff-num">04</div>
        <h3>Certificação reconhecida</h3>
        <p>Programas de certificação alinhados a padrões aceitos por associações médicas, com valor de validação de competência.</p>
      </div>
      <div class="diff-card">
        <div class="diff-num">05</div>
        <h3>Pesquisa &amp; desenvolvimento</h3>
        <p>Departamento dedicado a inovação cirúrgica, com projetos colaborativos junto a universidades e centros de pesquisa.</p>
      </div>
      <div class="diff-card">
        <div class="diff-num">06</div>
        <h3>Turmas reduzidas, mentoria real</h3>
        <p>Ambiente de aprendizado personalizado, com atenção individualizada e planos adaptados a cada cirurgião.</p>
      </div>
    </div>
  </div>
</section>

<!-- ============ ESPECIALIDADES ============ -->
<section id="especialidades" class="on-petroleo">
  <div class="wrap">
    <div class="section-head reveal">
      <div>
        <div class="eyebrow">03 · Especialidades</div>
        <h2>Áreas cirúrgicas atendidas</h2>
      </div>
      <p class="desc">O treinamento do CIRRO cobre as principais especialidades com aplicação em cirurgia robótica.</p>
    </div>

    <div class="chip-field reveal">
      <span class="chip">Cirurgia Geral</span>
      <span class="chip">Cirurgia Oncológica</span>
      <span class="chip">Cirurgia Cardiotorácica</span>
      <span class="chip">Cirurgia Urológica</span>
      <span class="chip">Cirurgia Ginecológica</span>
      <span class="chip">Cirurgia Coloproctológica</span>
      <span class="chip">Cirurgia de Cabeça e Pescoço</span>
      <span class="chip">Cirurgia Hepatobiliar e Pancreática</span>
      <span class="chip">Cirurgia Pediátrica</span>
    </div>
  </div>
</section>

<!-- ============ VALORES ============ -->
<section id="valores">
  <div class="wrap">
    <div class="section-head reveal">
      <div>
        <div class="eyebrow">04 · Valores</div>
        <h2>O que orienta cada decisão no CIRRO</h2>
      </div>
      <p class="desc">Princípios aplicados desde o desenho dos programas até a relação com cada paciente atendido.</p>
    </div>

    <div class="values-grid reveal">
      <div class="value-item">
        <span class="dot"></span>
        <h3>Excelência</h3>
        <p>Compromisso com a mais alta qualidade em todos os aspectos do treinamento.</p>
      </div>
      <div class="value-item">
        <span class="dot"></span>
        <h3>Inovação</h3>
        <p>Uso de tecnologia de ponta para revolucionar a prática cirúrgica e o ensino.</p>
      </div>
      <div class="value-item">
        <span class="dot"></span>
        <h3>Ética</h3>
        <p>Integridade e transparência como base da atuação médica e educacional.</p>
      </div>
      <div class="value-item">
        <span class="dot"></span>
        <h3>Colaboração</h3>
        <p>Trabalho em equipe entre profissionais, instituições e indústria.</p>
      </div>
      <div class="value-item">
        <span class="dot"></span>
        <h3>Segurança</h3>
        <p>Prioridade à segurança de pacientes e profissionais em todo o processo.</p>
      </div>
      <div class="value-item">
        <span class="dot"></span>
        <h3>Compromisso social</h3>
        <p>Formação de cirurgiões que ampliam o acesso à cirurgia robótica no SUS.</p>
      </div>
    </div>
  </div>
</section>

<!-- ============ CTA FINAL ============ -->
<section class="cta-final">
  <div class="wrap">
    <div class="mark">
      <svg width="30" height="30" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M29.04 7.28A15.6 15.6 0 1 0 34.2 26.47"
          stroke="currentColor" stroke-width="3.1" stroke-linecap="round"/>
        <circle cx="20.89" cy="19.92" r="3.86" fill="var(--dourado)"/>
      </svg>
      <span class="logotype">CIRRO</span>
    </div>
    <h2>Acompanhe o próximo capítulo da cirurgia robótica no Brasil.</h2>
    <p>O site institucional completo, com programas, calendário e formas de contato, está em construção. Por enquanto, o Instagram é o canal oficial.</p>
    <div class="cta-row">
      <a href="https://www.instagram.com/cirrobrasil" target="_blank" rel="noopener" class="btn btn-gold">Seguir @cirrobrasil</a>
    </div>
  </div>
</section>

<!-- ============ FOOTER ============ -->
<footer>
  <div class="wrap">
    <div class="mark">
      <svg width="22" height="22" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M29.04 7.28A15.6 15.6 0 1 0 34.2 26.47"
          stroke="currentColor" stroke-width="3.1" stroke-linecap="round"/>
        <circle cx="20.89" cy="19.92" r="3.86" fill="var(--dourado)"/>
      </svg>
      <span class="logotype" style="font-size:0.95rem;">CIRRO</span>
    </div>
    <p class="f-note">© 2026 CIRRO — Centro de Inovação em Cirurgia e Robótica. Todos os direitos reservados.</p>
    <div class="f-links">
      <a href="https://www.instagram.com/cirrobrasil" target="_blank" rel="noopener">Instagram</a>
    </div>
  </div>
</footer>

<script>
  // menu mobile
  const toggle = document.getElementById('menuToggle');
  const mobileMenu = document.getElementById('mobileMenu');
  toggle.addEventListener('click', () => {
    const open = mobileMenu.style.display === 'block';
    mobileMenu.style.display = open ? 'none' : 'block';
    toggle.setAttribute('aria-expanded', String(!open));
  });
  document.querySelectorAll('#mobileMenu a').forEach(a=>{
    a.addEventListener('click', ()=>{ mobileMenu.style.display='none'; });
  });

  // reveal on scroll
  const revealEls = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(entry=>{
      if(entry.isIntersecting){
        entry.target.classList.add('in');
        io.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12 });
  revealEls.forEach(el => io.observe(el));
</script>

</body>
</html>
