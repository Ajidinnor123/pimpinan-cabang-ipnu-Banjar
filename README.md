<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PC IPNU Kabupaten Banjar</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700;9..144,900&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#122A21;
    --forest:#0F4C3A;
    --forest-deep:#0A362A;
    --cream:#FBF6EA;
    --paper:#F3ECDA;
    --gold:#C79A2B;
    --gold-soft:#E8C874;
    --maroon:#8C3B49;
    --line: rgba(18,42,33,0.14);
    --radius: 4px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--cream);
    color:var(--ink);
    font-family:'Plus Jakarta Sans', sans-serif;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,h4{
    font-family:'Fraunces', serif;
    margin:0;
    font-weight:600;
    letter-spacing:-0.01em;
  }
  a{color:inherit; text-decoration:none;}
  .eyebrow{
    font-family:'JetBrains Mono', monospace;
    font-size:0.72rem;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:var(--gold);
    font-weight:500;
  }
  img{max-width:100%; display:block;}

  /* ---------- Facet motif (signature element) ---------- */
  .facet-divider{
    width:100%;
    height:14px;
    background:
      linear-gradient(115deg, transparent 48%, var(--gold) 48%, var(--gold) 52%, transparent 52%) 0 0/28px 28px,
      var(--forest-deep);
    opacity:0.9;
  }
  .facet-corner{
    position:absolute;
    width:120px; height:120px;
    background: conic-gradient(from 45deg,
      rgba(199,154,43,0.16) 0deg 30deg, transparent 30deg 60deg,
      rgba(199,154,43,0.16) 60deg 90deg, transparent 90deg 120deg,
      rgba(199,154,43,0.16) 120deg 150deg, transparent 150deg 180deg,
      rgba(199,154,43,0.16) 180deg 210deg, transparent 210deg 240deg,
      rgba(199,154,43,0.16) 240deg 270deg, transparent 270deg 300deg,
      rgba(199,154,43,0.16) 300deg 330deg, transparent 330deg 360deg);
    border-radius:50%;
    pointer-events:none;
  }

  /* ---------- Header ---------- */
  header{
    position:sticky; top:0; z-index:50;
    background:rgba(3, 216, 49, 0.92);
    backdrop-filter:blur(8px);
    border-bottom:1px solid var(--line);
  }
  .nav-wrap{
    max-width:1180px; margin:0 auto;
    display:flex; align-items:center; justify-content:space-between;
    padding:16px 28px;
  }
  .brand{display:flex; align-items:center; gap:12px;}
  .brand-mark{
    width:40px; height:40px;
    background:var(--forest);
    clip-path: polygon(50% 0%, 100% 38%, 82% 100%, 18% 100%, 0% 38%);
    display:flex; align-items:center; justify-content:center;
  }
  .brand-mark span{
    color:var(--gold-soft); font-family:'Fraunces',serif; font-weight:700; font-size:1rem;
  }
  .brand-mark.logo{
    clip-path:none; border-radius:9px; overflow:hidden; background:var(--forest-deep);
  }
  .brand-mark.logo img{
    width:100%; height:100%; object-fit:cover; display:block;
  }
  .brand-text{line-height:1.15;}
  .brand-text .b1{font-family:'Fraunces',serif; font-weight:700; font-size:1rem; color:var(--forest-deep);}
  .brand-text .b2{font-family:'JetBrains Mono',monospace; font-size:0.66rem; letter-spacing:0.08em; color:var(--maroon); text-transform:uppercase;}
  nav ul{
    list-style:none; display:flex; gap:30px; margin:0; padding:0;
  }
  nav a{
    font-size:0.88rem; font-weight:600; color:var(--ink);
    position:relative; padding:4px 0;
  }
  nav a::after{
    content:''; position:absolute; left:0; bottom:-2px; width:0; height:2px;
    background:var(--gold); transition:width 0.25s ease;
  }
  nav a:hover::after{width:100%;}

  /* ---------- Hero ---------- */
  .hero{
    position:relative;
    overflow:hidden;
    background:
      radial-gradient(1200px 600px at 85% -10%, rgba(7, 243, 42, 0.14), transparent 60%),
      linear-gradient(180deg, var(--cream) 0%, var(--paper) 100%);
    padding:88px 28px 70px;
  }
  .hero-inner{
    max-width:1180px; margin:0 auto;
    display:grid; grid-template-columns:1.15fr 0.85fr; gap:56px; align-items:center;
  }
  .hero h1{
    font-size:clamp(2.3rem, 4.2vw, 3.6rem);
    line-height:1.06;
    color:var(--forest-deep);
    margin:14px 0 20px;
  }
  .hero h1 em{
    font-style:normal; color:var(--maroon);
    background:linear-gradient(180deg, transparent 62%, var(--gold-soft) 62%);
  }
  .hero p{
    font-size:1.04rem; line-height:1.65; color:#3a4a42; max-width:52ch;
    margin-bottom:30px;
  }
  .cta-row{display:flex; gap:14px; flex-wrap:wrap;}
  .btn{
    display:inline-flex; align-items:center; gap:8px;
    padding:13px 24px; font-weight:700; font-size:0.92rem;
    border-radius:var(--radius); border:1.5px solid transparent; cursor:pointer;
    transition:transform 0.18s ease, box-shadow 0.18s ease;
  }
  .btn-primary{background:var(--forest); color:var(--cream);}
  .btn-primary:hover{transform:translateY(-2px); box-shadow:0 10px 22px rgba(15,76,58,0.28);}
  .btn-ghost{border-color:var(--forest-deep); color:var(--forest-deep);}
  .btn-ghost:hover{background:var(--forest-deep); color:var(--cream);}

  .hero-visual{
    position:relative;
    display:flex; flex-direction:column; align-items:center; justify-content:center;
    gap:26px; padding:20px 0;
  }
  .hero-visual .logo-emblem{
    width:100%; max-width:270px; aspect-ratio:1/1;
    border-radius:50%; overflow:hidden;
    box-shadow:0 20px 44px rgba(10,25,20,0.22);
    border:6px solid var(--cream);
    background:var(--cream);
  }
  .hero-visual .logo-emblem img{width:100%; height:100%; display:block; object-fit:cover;}
  .diamond-caption{
    position:relative; text-align:center; color:var(--forest-deep); padding:22px 30px;
    background:linear-gradient(155deg, var(--forest) 0%, var(--forest-deep) 70%);
    border-radius:18px; width:100%;
    box-shadow:0 14px 30px rgba(10,25,20,0.2);
  }
  .diamond-caption .eyebrow{color:var(--gold-soft);}
  .diamond-caption h3{color:var(--cream); font-size:1.5rem; margin-top:8px;}
  .diamond-caption p{color:rgba(251,246,234,0.75); font-size:0.85rem; margin-top:8px;}

  .hero-links{
    max-width:1180px; margin:44px auto 0; padding:0 28px;
    display:flex; gap:10px; flex-wrap:wrap;
  }
  .hero-links a{
    font-family:'JetBrains Mono', monospace; font-size:0.74rem; letter-spacing:0.05em;
    padding:9px 16px; border:1px solid var(--line); border-radius:20px;
    color:var(--forest-deep); background:rgba(255,255,255,0.5);
    transition:background 0.2s ease, border-color 0.2s ease;
  }
  .hero-links a:hover{background:var(--forest); color:var(--cream); border-color:var(--forest);}

  /* ---------- Stats ---------- */
  .stats{
    background:var(--forest-deep);
    padding:52px 28px;
    position:relative;
  }
  .stats-inner{
    max-width:1180px; margin:0 auto;
    display:grid; grid-template-columns:repeat(5,1fr); gap:0;
  }
  .stat{
    padding:0 30px; border-left:1px solid rgba(232,200,116,0.22);
    color:var(--cream);
  }
  .stat:first-child{border-left:none;}
  .stat .num{
    font-family:'Fraunces',serif; font-size:2.6rem; font-weight:700; color:var(--gold-soft);
    line-height:1;
  }
  .stat .label{margin-top:10px; font-weight:700; font-size:0.95rem;}
  .stat .sub{margin-top:4px; font-size:0.78rem; color:rgba(251,246,234,0.6); font-family:'JetBrains Mono',monospace;}

  /* ---------- Section shell ---------- */
  section.block{padding:84px 28px;}
  .block-inner{max-width:1180px; margin:0 auto;}
  .section-head{
    display:flex; justify-content:space-between; align-items:flex-end; gap:24px;
    margin-bottom:44px; flex-wrap:wrap;
    border-bottom:1px solid var(--line); padding-bottom:24px;
  }
  .section-head h2{font-size:clamp(1.7rem, 3vw, 2.3rem); color:var(--forest-deep);}
  .section-head p{color:#5b6b62; max-width:46ch; margin-top:8px; font-size:0.95rem;}

  /* ---------- Struktur ---------- */
  .tier-label{
    display:flex; align-items:center; gap:12px;
    margin:44px 0 20px;
  }
  .tier-label:first-of-type{margin-top:0;}
  .tier-label .tag{
    font-family:'JetBrains Mono',monospace; font-size:0.72rem; letter-spacing:0.1em;
    text-transform:uppercase; color:var(--cream); background:var(--maroon);
    padding:6px 12px; border-radius:20px; white-space:nowrap;
  }
  .tier-label .rule{flex:1; height:1px; background:var(--line);}

  .people-grid{
    display:grid; grid-template-columns:repeat(auto-fill, minmax(210px,1fr)); gap:16px;
  }
  .person-card{
    background:#fff; border:1px solid var(--line); padding:22px 20px;
    position:relative; overflow:hidden;
    transition:transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
  }
  .person-card::before{
    content:''; position:absolute; top:0; left:0; width:4px; height:100%;
    background:var(--gold); transform:scaleY(0); transform-origin:top;
    transition:transform 0.22s ease;
  }
  .person-card:hover{transform:translateY(-4px); box-shadow:0 14px 30px rgba(15,76,58,0.1); border-color:transparent;}
  .person-card:hover::before{transform:scaleY(1);}
  .person-card .avatar{
    width:60px; height:60px; margin-bottom:14px;
    background:var(--paper);
    background-size:cover; background-position:center;
    clip-path: polygon(50% 0%, 100% 35%, 82% 100%, 18% 100%, 0% 35%);
    display:flex; align-items:center; justify-content:center;
    font-family:'Fraunces',serif; font-weight:700; color:var(--forest); font-size:0.95rem;
    position:relative; cursor:pointer;
  }
  .person-card .avatar.has-photo{color:transparent;}
  .person-card .avatar::after{
    content:'\1F4F7'; position:absolute; inset:0;
    display:flex; align-items:center; justify-content:center;
    background:rgba(15,76,58,0.55); color:#fff; font-size:0.95rem;
    opacity:0; transition:opacity 0.2s ease; pointer-events:none;
  }
  .person-card .avatar:hover::after{opacity:1;}
  .person-card h4{font-size:1.02rem; color:var(--forest-deep);}
  .person-card h4.editable-name{
    cursor:text; outline:none; border-radius:3px;
    padding:1px 4px; margin:-1px -4px;
    transition:background 0.15s ease, box-shadow 0.15s ease;
  }
  .person-card h4.editable-name:hover{background:rgba(199,154,43,0.12);}
  .person-card h4.editable-name:focus{background:rgba(199,154,43,0.18); box-shadow:0 0 0 1px var(--gold);}
  .person-card .role{
    margin-top:5px; font-size:0.78rem; color:var(--maroon); font-weight:700;
    font-family:'JetBrains Mono',monospace; letter-spacing:0.02em;
  }
  .person-card .remove-btn{
    position:absolute; top:8px; right:8px;
    width:22px; height:22px; border-radius:50%;
    background:var(--paper); border:1px solid var(--line);
    color:var(--maroon); font-size:0.85rem; line-height:1;
    display:none; align-items:center; justify-content:center;
    cursor:pointer;
  }
  .person-card.local .remove-btn{display:flex;}
  .person-card.local, .person-card.sheet{border-color: rgba(199,154,43,0.5);}
  .person-card .local-tag{
    position:absolute; top:8px; left:8px;
    font-family:'JetBrains Mono',monospace; font-size:0.6rem; letter-spacing:0.05em;
    text-transform:uppercase; color:var(--forest); background:var(--gold-soft);
    padding:2px 7px; border-radius:20px; display:none;
  }
  .person-card.local .local-tag, .person-card.sheet .local-tag{display:inline-block;}
  .person-card.local .avatar, .person-card.sheet .avatar{margin-top:14px;}

  .add-person-card{
    background:transparent; border:1.5px dashed var(--line); padding:22px 20px;
    display:flex; flex-direction:column; align-items:center; justify-content:center;
    text-align:center; gap:8px; cursor:pointer; min-height:150px;
    transition:border-color 0.2s ease, background 0.2s ease;
    color:#5b6b62;
  }
  .add-person-card:hover{border-color:var(--gold); background:rgba(199,154,43,0.06); color:var(--forest-deep);}
  .add-person-card .plus{
    width:34px; height:34px; border-radius:50%;
    border:1.5px solid currentColor;
    display:flex; align-items:center; justify-content:center;
    font-size:1.2rem; font-weight:600;
  }
  .add-person-card span.label{font-size:0.8rem; font-weight:700;}


  /* ---------- Modal Tambah Berita ---------- */
  .btn-sm{padding:10px 18px; font-size:0.82rem;}
  .modal-overlay{
    display:none; position:fixed; inset:0; z-index:100;
    background:rgba(10,25,20,0.55);
    align-items:center; justify-content:center;
    padding:20px;
  }
  .modal-overlay.show{display:flex;}
  .modal-box{
    background:#fff; max-width:560px; width:100%;
    max-height:88vh; overflow-y:auto;
    padding:30px; border-top:4px solid var(--gold);
    box-shadow:0 30px 60px rgba(10,25,20,0.35);
  }
  .modal-head{
    display:flex; justify-content:space-between; align-items:flex-start;
    margin-bottom:6px;
  }
  .modal-head h3{font-size:1.3rem; color:var(--forest-deep); margin-top:6px;}
  .modal-close{
    background:none; border:none; font-size:1.6rem; line-height:1; cursor:pointer;
    color:var(--forest-deep); padding:4px 8px;
  }
  .modal-close:hover{color:var(--maroon);}

  .service-grid{
    display:grid; grid-template-columns:repeat(3, 1fr); gap:20px;
    margin-bottom:56px;
  }
  .service-card{
    background:#fff; border:1px solid var(--line); padding:28px 24px;
    display:flex; flex-direction:column; align-items:flex-start; gap:6px;
    position:relative; overflow:hidden;
    transition:transform 0.2s ease, box-shadow 0.2s ease;
  }
  .service-card:hover{transform:translateY(-4px); box-shadow:0 14px 30px rgba(15,76,58,0.1);}
  .service-icon{
    width:44px; height:44px; margin-bottom:10px;
    background:var(--forest);
    clip-path: polygon(50% 0%, 100% 35%, 82% 100%, 18% 100%, 0% 35%);
    position:relative;
  }
  .service-icon::after{
    content:'';
    position:absolute; inset:0;
    background:linear-gradient(115deg, transparent 45%, rgba(232,200,116,0.6) 45.8%, transparent 46.6%);
  }
  .service-card h3{font-size:1.12rem; color:var(--forest-deep);}
  .service-card p{font-size:0.87rem; color:#5b6b62; line-height:1.55; margin-bottom:14px;}
  .service-card .btn{margin-top:auto;}

  .form-grid{
    display:grid; grid-template-columns:1fr 1fr; gap:24px;
  }
  .form-card{
    background:#fff; border:1px solid var(--line); padding:32px;
    scroll-margin-top:90px;
  }
  .form-card h3{font-size:1.3rem; color:var(--forest-deep); margin:6px 0 10px;}
  .form-desc{font-size:0.86rem; color:#5b6b62; line-height:1.55; margin-bottom:22px;}
  .field{margin-bottom:16px; display:flex; flex-direction:column; gap:6px;}
  .field-row{display:grid; grid-template-columns:1fr 1fr; gap:14px;}
  label{
    font-family:'JetBrains Mono',monospace; font-size:0.7rem; letter-spacing:0.04em;
    text-transform:uppercase; color:var(--forest-deep); font-weight:500;
  }
  input, select, textarea{
    font-family:'Plus Jakarta Sans', sans-serif; font-size:0.9rem;
    padding:11px 13px; border:1px solid var(--line); border-radius:var(--radius);
    background:var(--cream); color:var(--ink); outline:none;
    transition:border-color 0.18s ease, box-shadow 0.18s ease;
  }
  input:focus, select:focus, textarea:focus{
    display:grid; grid-template-columns:repeat(auto-fit, minmax(260px,1fr)); gap:20px;
  }
  textarea{resize:vertical; font-family:'Plus Jakarta Sans', sans-serif;}
  .form-card .btn{width:100%; justify-content:center; margin-top:6px;}
  .form-note{
    margin-top:14px; font-size:0.76rem; color:#8a9690; line-height:1.5;
  }
  .form-success{
    display:none; align-items:center; gap:10px;
    background:rgba(15,76,58,0.08); border:1px solid rgba(15,76,58,0.25);
    color:var(--forest-deep); padding:12px 14px; font-size:0.85rem; font-weight:600;
    margin-top:14px;
  }
  .form-success.show{display:flex;}

  /* ---------- Berita ---------- */
  .news-grid{
    display:grid; grid-template-columns:1.3fr 1fr 1fr; gap:20px;
  }
  .news-card{
    background:#fff; border:1px solid var(--line);
    display:flex; flex-direction:column; overflow:hidden;
  }
  .news-card .thumb{
    aspect-ratio:16/10;
    background:linear-gradient(140deg, var(--forest), var(--forest-deep));
    position:relative;
  }
  .news-card.lead .thumb{aspect-ratio:16/11;}
  .news-card .thumb .facet-corner{top:0; right:0;}
  .news-card .cat{
    position:absolute; bottom:12px; left:12px;
    font-family:'JetBrains Mono',monospace; font-size:0.68rem; letter-spacing:0.08em; text-transform:uppercase;
    color:var(--forest-deep); background:var(--gold-soft); padding:5px 10px;
  }
  .news-card .body{padding:20px; flex:1; display:flex; flex-direction:column;}
  .news-card .date{font-family:'JetBrains Mono',monospace; font-size:0.72rem; color:#8a9690; margin-bottom:8px;}
  .news-card h3{font-size:1.08rem; line-height:1.3; color:var(--forest-deep);}
  .news-card.lead h3{font-size:1.4rem;}
  .news-card p{font-size:0.86rem; color:#5b6b62; margin-top:10px; line-height:1.55;}

  /* ---------- Kegiatan strip ---------- */
  .agenda{
    background:var(--paper);
  }
  .agenda-list{display:flex; flex-direction:column;}
  .agenda-item{
    display:grid; grid-template-columns:110px 1fr auto; gap:24px; align-items:center;
    padding:22px 0; border-bottom:1px solid var(--line);
  }
  .agenda-item:last-child{border-bottom:none;}
  .agenda-item .d{font-family:'Fraunces',serif; font-weight:700; color:var(--forest); font-size:1.05rem;}
  .agenda-item .d span{display:block; font-family:'JetBrains Mono',monospace; font-size:0.7rem; color:var(--maroon); font-weight:500;}
  .agenda-item h4{font-size:1.02rem; color:var(--forest-deep);}
  .agenda-item .loc{font-size:0.8rem; color:#5b6b62; margin-top:4px;}
  .agenda-item .arrow{font-size:1.3rem; color:var(--gold); transition:transform 0.2s ease;}
  .agenda-item:hover .arrow{transform:translateX(6px);}

  /* ---------- Footer ---------- */
  footer{
    background:var(--forest-deep); color:rgba(251,246,234,0.82);
    padding:64px 28px 28px;
  }
  .footer-inner{max-width:1180px; margin:0 auto;}
  .footer-grid{
    display:grid; grid-template-columns:1.4fr 1fr 1fr 1fr; gap:40px;
    padding-bottom:40px; border-bottom:1px solid rgba(232,200,116,0.18);
  }
  .footer-grid h5{
    font-family:'JetBrains Mono',monospace; font-size:0.72rem; letter-spacing:0.1em;
    text-transform:uppercase; color:var(--gold-soft); margin-bottom:16px;
  }
  .footer-grid ul{list-style:none; margin:0; padding:0;}
  .footer-grid li{margin-bottom:10px; font-size:0.88rem;}
  .footer-grid a:hover{color:var(--gold-soft);}
  .footer-brand p{font-size:0.88rem; line-height:1.6; max-width:34ch; margin-top:14px; color:rgba(251,246,234,0.65);}
  .footer-bottom{
    display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:10px;
    padding-top:24px; font-size:0.78rem; color:rgba(251,246,234,0.5);
    font-family:'JetBrains Mono',monospace;
  }

  @media (max-width:920px){
    .hero-inner{grid-template-columns:1fr;}
    .hero-visual{max-width:340px; margin:0 auto;}
    .stats-inner{grid-template-columns:1fr; gap:24px;}
    .stat{border-left:none; border-top:1px solid rgba(232,200,116,0.22); padding-top:20px;}
    .stat:first-child{border-top:none; padding-top:0;}
    .news-grid{grid-template-columns:1fr;}
    .service-grid{grid-template-columns:1fr;}
    .form-grid{grid-template-columns:1fr;}
    .field-row{grid-template-columns:1fr;}
    .footer-grid{grid-template-columns:1fr 1fr;}
    nav ul{display:none;}
    .agenda-item{grid-template-columns:1fr; text-align:left;}
  }
  @media (prefers-reduced-motion: reduce){
    *{transition:none !important;}
  }
</style>
</head>
<body>

<header>
  <div class="nav-wrap">
    <a href="#" class="brand">
      <div class="brand-mark logo"><img src="data:image/jpeg;base64,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" alt="Logo IPNU"></div>
      <div class="brand-text">
        <div class="b1">PC IPNU Banjar</div>
        <div class="b2">Kab. Banjar · Kalsel</div>
      </div>
    </a>
    <nav>
      <ul>
        <li><a href="#beranda">Beranda</a></li>
        <li><a href="#struktur">Struktur</a></li>
        <li><a href="#layanan">Layanan Kader</a></li>
        <li><a href="#berita">Berita</a></li>
        <li><a href="#agenda">Agenda</a></li>
        <li><a href="#kontak">Kontak</a></li>
      </ul>
    </nav>
  </div>
</header>

<section class="hero" id="beranda">
  <div class="hero-inner">
    <div>
      <span class="eyebrow">Selamat Datang di PC IPNU Kabupaten Banjar</span>
      <h1>Pimpinan Cabang<br><em>IPNU</em> Kabupaten Banjar</h1>
      <p>Ikatan Pelajar Nahdlatul Ulama Kabupaten Banjar — merawat tradisi keilmuan pesantren, menumbuhkan kader pelajar yang berakhlak, cerdas, dan berdaya di Bumi Serambi Mekah.</p>
      <div class="cta-row">
        <a href="#layanan" class="btn btn-primary">Layanan Kader</a>
        <a href="#form-jas" class="btn btn-ghost">Pesan Jas IPNU</a>
        <a href="#berita" id="btn-open-berita-modal-hero" class="btn btn-ghost">+ Tambah Berita</a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="logo-emblem"><img src="data:image/jpeg;base64,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" alt="Logo IPNU"></div>
      <div class="diamond-caption">
        <span class="eyebrow">Periode 2026–2028</span>
        <h3>PC IPNU<br>Kab. Banjar</h3>
        <p>Belajar, Berjuang, Bertaqwa</p>
      </div>
    </div>
  </div>
  <div class="hero-links">
    <a href="#struktur">Struktur Pimpinan</a>
    <a href="#layanan">Layanan Kader</a>
    <a href="#berita">Kabar kaderisasi</a>
    <a href="#agenda">Agenda Kegiatan</a>
  </div>
</section>

<div class="facet-divider"></div>

<section class="stats">
  <div class="stats-inner">
    <div class="stat">
      <div class="num">150+</div>
      <div class="label">Kader Ber-KTA</div>
      <div class="sub">Data sementara, tahap pemutakhiran</div>
    </div>
    <div class="stat">
      <div class="num">1000+</div>
      <div class="label">Total Kader</div>
      <div class="sub">Se-Kabupaten Banjar</div>
    </div>
    <div class="stat">
      <div class="num">10</div>
      <div class="label">Pimpinan Anak Cabang</div>
      <div class="sub">Tersebar di Kab. Banjar</div>
    </div>
    <div class="stat">
      <div class="num">2</div>
      <div class="label">Pimpinan Komisariat</div>
      <div class="sub">Se-Kabupaten Banjar</div>
    </div>
    <div class="stat">
      <div class="num">3</div>
      <div class="label">Pimpinan Ranting</div>
      <div class="sub">Se-Kabupaten Banjar</div>
    </div>
  </div>
</section>

<section class="block" id="struktur">
  <div class="block-inner">
    <div class="section-head">
      <div>
        <span class="eyebrow">Organisasi</span>
        <h2>Struktur Pimpinan Cabang</h2>
        <p>Susunan Pimpinan Cabang IPNU Kabupaten Banjar masa khidmat 2024–2026. <strong>Klik nama</strong> untuk mengedit langsung, <strong>klik foto/avatar</strong> untuk mengunggah foto pengurus. Perubahan tersimpan otomatis di perangkat ini.</p>
      </div>
    </div>

    <div class="tier-label" data-tier="Pimpinan Harian">
      <span class="tag">Pimpinan Harian</span>
      <div class="rule"></div>
    </div>
    <div class="people-grid" id="grid-pimpinan-harian" data-tier="Pimpinan Harian">
      <div class="person-card"><div class="avatar">KU</div><h4>Rahmadi</h4><div class="role">Ketua Umum</div></div>
      <div class="person-card"><div class="avatar">MA</div><h4>Maulana Al-kausar</h4><div class="role">Sekretaris</div></div>
      <div class="person-card"><div class="avatar">BU</div><h4>Nama Pengurus</h4><div class="role">Bendahara</div></div>
      <div class="person-card"><div class="avatar">W1</div><h4>Nama Pengurus</h4><div class="role">Wakil Ketua 1</div></div>
      <div class="person-card"><div class="avatar">W2</div><h4>Nama Pengurus</h4><div class="role">Wakil Ketua II</div></div>
      <div class="person-card"><div class="avatar">W3</div><h4>Nama Pengurus</h4><div class="role">Wakil Ketua III</div></div>
      <div class="person-card"><div class="avatar">W4</div><h4>Nama Pengurus</h4><div class="role">Wakil KETUA IV</div></div>
    </div>

    <div class="tier-label" data-tier="Lembaga Kaderisasi">
      <span class="tag">Lembaga Kaderisasi</span>
      <div class="rule"></div>
    </div>
    <div class="people-grid" id="grid-lembaga-kaderisasi" data-tier="Lembaga Kaderisasi">
      <div class="person-card"><div class="avatar">KB</div><h4>Nama Pengurus</h4><div class="role">Ketua Lembaga</div></div>
      <div class="person-card"><div class="avatar">SB</div><h4>Nama Pengurus</h4><div class="role">Sekretaris Lembaga</div></div>
    </div>

    <div class="tier-label" data-tier="Departemen Pendidikan &amp; Dakwah">
      <span class="tag">Departemen Pendidikan &amp; Dakwah</span>
      <div class="rule"></div>
    </div>
    <div class="people-grid" id="grid-departemen-pendidikan-dakwah" data-tier="Departemen Pendidikan &amp; Dakwah">
      <div class="person-card"><div class="avatar">KB</div><h4>Nama Pengurus</h4><div class="role">Ketua Departemen</div></div>
      <div class="person-card"><div class="avatar">SB</div><h4>Nama Pengurus</h4><div class="role">Sekretaris Departemen</div></div>
    </div>

    <div class="tier-label" data-tier="Departemen Organisasi">
      <span class="tag">Departemen Organisasi</span>
      <div class="rule"></div>
    </div>
    <div class="people-grid" id="grid-departemen-organisasi" data-tier="Departemen Organisasi">
      <div class="person-card"><div class="avatar">KB</div><h4>Nama Pengurus</h4><div class="role">Ketua Departemen</div></div>
      <div class="person-card"><div class="avatar">SB</div><h4>Nama Pengurus</h4><div class="role">Sekretaris Departemen</div></div>
    </div>

    <div class="tier-label" data-tier="Departemen Bakat Minat &amp; Olahraga">
      <span class="tag">Departemen Bakat Minat &amp; Olahraga</span>
      <div class="rule"></div>
    </div>
    <div class="people-grid" id="grid-departemen-bakat-minat-olahraga" data-tier="Departemen Bakat Minat &amp; Olahraga">
      <div class="person-card"><div class="avatar">KB</div><h4>Nama Pengurus</h4><div class="role">Ketua Departemen</div></div>
      <div class="person-card"><div class="avatar">SB</div><h4>Nama Pengurus</h4><div class="role">Sekretaris Departemen</div></div>
    </div>
  </div>
</section>

<!-- ===================== MODAL TAMBAH ANGGOTA ===================== -->
<div class="modal-overlay" id="anggota-modal-overlay">
  <div class="modal-box">
    <div class="modal-head">
      <div>
        <span class="eyebrow">Struktur Pimpinan</span>
        <h3>Tambah Anggota Baru</h3>
      </div>
      <button type="button" class="modal-close" id="btn-close-anggota-modal" aria-label="Tutup">&times;</button>
    </div>
    <p class="form-desc">Anggota baru langsung tampil di kelompok yang dipilih di perangkat ini, dan otomatis terkirim ke Google Sheet pusat (jika sudah terhubung) agar tampil untuk <strong>semua pengunjung</strong>.</p>
    <form id="form-tambah-anggota">
      <div class="field">
        <label for="na-kelompok">Kelompok / Tingkatan</label>
        <select id="na-kelompok" required>
          <option value="" disabled selected>Pilih kelompok</option>
          <option value="Pimpinan Harian">Pimpinan Harian</option>
          <option value="Lembaga Kaderisasi">Lembaga Kaderisasi</option>
          <option value="Departemen Pendidikan &amp; Dakwah">Departemen Pendidikan &amp; Dakwah</option>
          <option value="Departemen Organisasi">Departemen Organisasi</option>
          <option value="Departemen Bakat Minat &amp; Olahraga">Departemen Bakat Minat &amp; Olahraga</option>
        </select>
      </div>
      <div class="field-row">
        <div class="field">
          <label for="na-nama">Nama Lengkap</label>
          <input id="na-nama" type="text" required placeholder="Nama pengurus">
        </div>
        <div class="field">
          <label for="na-jabatan">Jabatan</label>
          <input id="na-jabatan" type="text" required placeholder="Contoh: Ketua Departemen">
        </div>
      </div>
      <div class="field-row">
        <div class="field">
          <label for="na-inisial">Inisial Avatar (2 huruf, opsional)</label>
          <input id="na-inisial" type="text" maxlength="2" placeholder="Otomatis dari nama jika kosong">
        </div>
        <div class="field">
          <label for="na-foto">Link Foto (opsional)</label>
          <input id="na-foto" type="url" placeholder="https://...">
        </div>
      </div>
      <div style="display:flex; gap:10px; flex-wrap:wrap;">
        <button type="submit" class="btn btn-primary" style="flex:1;">Tambahkan Anggota</button>
        <button type="button" class="btn btn-ghost" id="btn-copy-anggota-data">Salin Data</button>
      </div>
      <div class="form-note">Sudah ada <span id="jumlah-anggota-lokal">0</span> anggota lokal tersimpan di browser ini. <a href="#" id="btn-hapus-anggota-lokal" style="color:var(--maroon); font-weight:600;">Hapus semua anggota lokal</a></div>
      <div class="form-success" id="anggota-success">✓ Anggota berhasil ditambahkan ke struktur.</div>
    </form>
  </div>
</div>

<div class="facet-divider"></div>

<section class="block" id="layanan" style="background:var(--paper);">
  <div class="block-inner">
    <div class="section-head">
      <div>
        <span class="eyebrow">Layanan Digital</span>
        <h2>Pusat Layanan Kader</h2>
        <p>Fasilitas administratif digital untuk mempermudah pendampingan dan kebutuhan atribut kader IPNU se-Kabupaten Banjar. Semua pendaftaran/pemesanan dapat langsung diproses via WhatsApp Narahubung: <a href="https://wa.me/6283853209822" target="_blank" rel="noopener" style="color:var(--maroon); font-weight:700;">0838-5320-9822</a>.</p>
      </div>
    </div>

    <div class="service-grid">
      <div class="service-card">
        <div class="service-icon"></div>
        <h3>Konsultasi Kaderisasi</h3>
        <p>Konsultasi langsung dengan Lembaga Kaderisasi PC IPNU Banjar seputar pembinaan dan jenjang kader.</p>
        <a href="https://wa.me/6283853209822" target="_blank" rel="noopener" id="link-konsultasi-kaderisasi" class="btn btn-ghost btn-sm">Hubungi via WhatsApp</a>
      </div>
      <div class="service-card">
        <div class="service-icon"></div>
        <h3>Pemesanan Jas IPNU</h3>
        <p>Pesan Jas IPNU resmi untuk kebutuhan pribadi maupun ranting/PAC. Lengkapi formulir di samping untuk memesan.</p>
        <a href="#form-jas" class="btn btn-primary btn-sm">Isi Formulir Pemesanan</a>
      </div>
    </div>

    <div class="form-grid" style="grid-template-columns:1fr; max-width:640px; margin:0 auto;">
      <div class="form-card" id="form-jas">
        <span class="eyebrow">Formulir Pemesanan</span>
        <h3>Pemesanan Jas IPNU</h3>
        <p class="form-desc">Lengkapi data berikut, lalu klik "Kirim Pemesanan" — data akan otomatis terisi ke pesan WhatsApp ke Narahubung 0838-5320-9822 untuk diproses.</p>
        <form id="form-jas-el" data-form-name="Pemesanan Jas IPNU">
          <div class="field">
            <label for="jas-nama">Nama Lengkap</label>
            <input id="jas-nama" type="text" required placeholder="Nama pemesan">
          </div>
          <div class="field-row">
            <div class="field">
              <label for="jas-asal">Asal Pimpinan</label>
              <input id="jas-asal" type="text" required placeholder="Contoh: PR/PAC/PC IPNU ...">
            </div>
            <div class="field">
              <label for="jas-ukuran">Ukuran</label>
              <select id="jas-ukuran" required>
                <option value="" disabled selected>Pilih ukuran</option>
                <option value="S">S</option>
                <option value="M">M</option>
                <option value="L">L</option>
                <option value="XL">XL</option>
                <option value="XXL">XXL</option>
              </select>
            </div>
          </div>
          <button type="submit" class="btn btn-primary">Kirim Pemesanan via WhatsApp</button>
          <div class="form-success" id="jas-success">✓ Data tersimpan, membuka WhatsApp ke Narahubung 0838-5320-9822...</div>
          <div class="form-note">*Apabila ingin pemesanan dalam jumlah banyak, dapat langsung menghubungi 0838-5320-9822.</div>
        </form>
      </div>
    </div>
  </div>
</section>

<div class="facet-divider"></div>

<section class="block" id="berita" style="background:var(--paper);">
  <div class="block-inner">
    <div class="section-head">
      <div>
        <span class="eyebrow">Publikasi</span>
        <h2>Kabar Pimpinan Cabang Terbaru</h2>
        <p>Dinamika kegiatan dan opini kader dari ranting-ranting IPNU se-Kabupaten Banjar. Diperbarui otomatis dari Google Sheet redaksi.</p>
      </div>
      <div style="display:flex; gap:10px; flex-wrap:wrap;">
        <button type="button" class="btn btn-primary btn-sm" id="btn-open-berita-modal">+ Tambah Berita</button>
        <a href="https://instagram.com/pc.ipnukabbanjar" target="_blank" rel="noopener" class="btn btn-ghost btn-sm">Lihat Semua Berita</a>
      </div>
    </div>
    <div class="news-grid" id="news-grid">
      <div class="news-card lead">
        <div class="thumb"><div class="facet-corner"></div><span class="cat">Kegiatan</span></div>
        <div class="body">
          <span class="date">08 Jul 2026</span>
          <h3>Judul berita utama kegiatan PC IPNU Kab. Banjar</h3>
          <p>Ringkasan singkat kegiatan atau rilis pers yang menonjolkan capaian dan kontribusi kader IPNU di masyarakat...</p>
        </div>
      </div>
      <div class="news-card">
        <div class="thumb"><div class="facet-corner"></div><span class="cat">Kabar Ranting</span></div>
        <div class="body">
          <span class="date">06 Jul 2026</span>
          <h3>Judul berita dari ranting kecamatan</h3>
          <p>Cuplikan singkat isi berita ranting.</p>
        </div>
      </div>
      <div class="news-card">
        <div class="thumb"><div class="facet-corner"></div><span class="cat">Opini Kader</span></div>
        <div class="body">
          <span class="date">03 Jul 2026</span>
          <h3>Judul opini kader tentang isu pelajar</h3>
          <p>Cuplikan singkat opini kader.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===================== MODAL TAMBAH BERITA ===================== -->
<div class="modal-overlay" id="berita-modal-overlay">
  <div class="modal-box">
    <div class="modal-head">
      <div>
        <span class="eyebrow">Publikasi Cepat</span>
        <h3>Tambah Berita Baru</h3>
      </div>
      <button type="button" class="modal-close" id="btn-close-berita-modal" aria-label="Tutup">&times;</button>
    </div>
    <p class="form-desc">Berita langsung tampil di kartu berita halaman ini, dan otomatis terkirim ke Google Sheet pusat (jika sudah terhubung) agar tampil untuk semua pengunjung.</p>
    <form id="form-tambah-berita">
      <div class="field">
        <label for="nb-judul">Judul Berita</label>
        <input id="nb-judul" type="text" required placeholder="Judul berita">
      </div>
      <div class="field-row">
        <div class="field">
          <label for="nb-tanggal">Tanggal</label>
          <input id="nb-tanggal" type="text" required placeholder="Contoh: 10 Jul 2026">
        </div>
        <div class="field">
          <label for="nb-kategori">Kategori</label>
          <select id="nb-kategori" required>
            <option value="Kegiatan Cabang">Kegiatan Cabang</option>
            <option value="Kabar Penting">Kabar penting</option>
            <option value="Berita Kader">Berita Kader</option>
            <option value="Pengumuman">Pengumuman</option>
          </select>
        </div>
      </div>
      <div class="field">
        <label for="nb-ringkasan">Ringkasan (2-3 kalimat)</label>
        <textarea id="nb-ringkasan" rows="3" required placeholder="Ringkasan singkat isi berita"></textarea>
      </div>
      <div class="field-row">
        <div class="field">
          <label for="nb-foto">Link Foto (opsional)</label>
          <input id="nb-foto" type="url" placeholder="https://...">
        </div>
        <div class="field">
          <label for="nb-link">Link Berita Lengkap (opsional)</label>
          <input id="nb-link" type="url" placeholder="https://...">
        </div>
      </div>
      <div style="display:flex; gap:10px; flex-wrap:wrap;">
        <button type="submit" class="btn btn-primary" style="flex:1;">Terbitkan Berita</button>
        <button type="button" class="btn btn-ghost" id="btn-copy-berita-data">Salin Data</button>
      </div>
      <div class="form-note">Sudah ada <span id="jumlah-berita-lokal">0</span> berita lokal tersimpan di browser ini. <a href="#" id="btn-hapus-berita-lokal" style="color:var(--maroon); font-weight:600;">Hapus semua berita lokal</a></div>
      <div class="form-success" id="berita-success">✓ Berita berhasil ditambahkan dan tampil di halaman.</div>
    </form>
  </div>
</div>

<section class="block agenda" id="agenda">
  <div class="block-inner">
    <div class="section-head">
      <div>
        <span class="eyebrow">Kalender</span>
        <h2>Agenda Kegiatan</h2>
        <p>Jadwal kegiatan resmi dan program kerja Pimpinan Cabang.</p>
      </div>
    </div>
    <div class="agenda-list">
      <div class="agenda-item">
        <div class="d">14 <span>JUL 2026</span></div>
        <div><h4>Rapat Kerja Cabang</h4><div class="loc">Sekretariat PC IPNU, Martapura</div></div>
        <div class="arrow">→</div>
      </div>
      <div class="agenda-item">
        <div class="d">21 <span>JUL 2026</span></div>
        <div><h4>Pelantikan Pimpinan Ranting Baru</h4><div class="loc">Aula Kecamatan, Kab. Banjar</div></div>
        <div class="arrow">→</div>
      </div>
      <div class="agenda-item">
        <div class="d">02 <span>AGU 2026</span></div>
        <div><h4>Diklat Kepemimpinan Dasar</h4><div class="loc">Pondok Pesantren mitra</div></div>
        <div class="arrow">→</div>
      </div>
    </div>
  </div>
</section>

<footer id="kontak">
  <div class="footer-inner">
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="brand">
          <div class="brand-mark logo"><img src="data:image/jpeg;base64,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" alt="Logo IPNU"></div>
          <div class="brand-text">
            <div class="b1" style="color:var(--cream);">PC IPNU Banjar</div>
            <div class="b2">Kab. Banjar · Kalsel</div>
          </div>
        </div>
        <p>Pimpinan Cabang Ikatan Pelajar Nahdlatul Ulama Kabupaten Banjar. Wadah pergerakan pelajar Nahdliyin menuju generasi yang berilmu dan berkhidmat.</p>
      </div>
      <div>
        <h5>Organisasi</h5>
        <ul>
          <li><a href="#struktur">Struktur Pimpinan</a></li>
          <li><a href="#struktur">Lembaga &amp; Departemen</a></li>
          <li><a href="https://wa.me/6283853209822" target="_blank" rel="noopener">Dokumen Resmi</a></li>
        </ul>
      </div>
      <div>
        <h5>Publikasi</h5>
        <ul>
          <li><a href="#berita">Kabar Pimpinan Cabang</a></li>
          <li><a href="#berita">Opini Kader</a></li>
          <li><a href="#agenda">Agenda</a></li>
        </ul>
      </div>
      <div>
        <h5>Kontak</h5>
        <ul>
          <li>Sekretariat: Martapura, Kab. Banjar</li>
          <li>Email: pcipnubanjar@contoh.or.id</li>
          <li>WhatsApp Narahubung: <a href="https://wa.me/6283853209822" target="_blank" rel="noopener">0838-5320-9822</a></li>
          <li>Instagram: <a href="https://instagram.com/pc.ipnukabbanjar" target="_blank" rel="noopener">@pc.ipnukabbanjar</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 PC IPNU Kabupaten Banjar. Hak Cipta Dilindungi.</span>
      <span>Belajar · Berjuang · Bertaqwa</span>
    </div>
  </div>
</footer>
<script>
  // ================================================================
  // KONEKSI DATA PUSAT (Google Sheet + Apps Script)
  // ================================================================
  // 1. Buat 1 Google Sheet dengan 2 tab: "Anggota" dan "Berita".
  //    Tab "Anggota" kolom: PID | Tier | Nama | Jabatan | Inisial | Foto
  //    Tab "Berita"  kolom: Tanggal | Kategori | Judul | Ringkasan | LinkFoto | LinkBerita
  // 2. File > Share > Publish to web > pilih tab "Berita" > format CSV > Publish.
  //    Salin link CSV-nya ke BERITA_CSV_URL di bagian script Berita.
  //    Ulangi untuk tab "Anggota", salin ke STRUKTUR_CSV_URL di bawah ini.
  // 3. Buka Extensions > Apps Script di Sheet yang sama, tempel kode doPost()
  //    (lihat panduan yang diberikan terpisah), lalu Deploy > New deployment >
  //    Web app > Who has access: Anyone. Salin URL Web App ke APPS_SCRIPT_URL.
  // Jika APPS_SCRIPT_URL / *_CSV_URL dibiarkan placeholder, situs tetap berjalan
  // normal memakai penyimpanan lokal di browser (seperti sebelumnya).
  const APPS_SCRIPT_URL = "GANTI_DENGAN_URL_WEB_APP_APPS_SCRIPT_ANDA";
  const STRUKTUR_CSV_URL = "GANTI_DENGAN_LINK_CSV_TAB_ANGGOTA_ANDA";

  function isConfigured(url){
    return !!url && url.indexOf('GANTI_DENGAN') === -1;
  }

  // Kirim data ke Apps Script (fire-and-forget, tanpa menunggu/baca respons)
  // agar tersimpan terpusat di Google Sheet untuk semua pengunjung.
  function kirimKeSheet(sheet, data){
    if(!isConfigured(APPS_SCRIPT_URL)) return;
    try{
      fetch(APPS_SCRIPT_URL, {
        method: 'POST',
        mode: 'no-cors',
        headers: { 'Content-Type': 'text/plain;charset=utf-8' },
        body: JSON.stringify(Object.assign({ sheet: sheet }, data))
      }).catch(function(){ /* diam-diam gagal, data lokal tetap tersimpan */ });
    }catch(e){ /* browser lama tanpa fetch */ }
  }

  // Perkecil & kompres foto (dataURL) sebelum dipakai/disimpan, supaya ringan
  // dan muat sebagai satu sel di Google Sheet.
  function kompresFoto(file, callback){
    const reader = new FileReader();
    reader.onload = function(e){
      const img = new Image();
      img.onload = function(){
        const size = 220;
        const canvas = document.createElement('canvas');
        canvas.width = size; canvas.height = size;
        const ctx = canvas.getContext('2d');
        const scale = Math.max(size / img.width, size / img.height);
        const w = img.width * scale, h = img.height * scale;
        ctx.drawImage(img, (size - w) / 2, (size - h) / 2, w, h);
        callback(canvas.toDataURL('image/jpeg', 0.6));
      };
      img.src = e.target.result;
    };
    reader.readAsDataURL(file);
  }

  function parseCSVUmum(text){
    const rows = [];
    let row = [], field = '', inQuotes = false;
    for(let i = 0; i < text.length; i++){
      const c = text[i], next = text[i+1];
      if(inQuotes){
        if(c === '"' && next === '"'){ field += '"'; i++; }
        else if(c === '"'){ inQuotes = false; }
        else { field += c; }
      } else {
        if(c === '"'){ inQuotes = true; }
        else if(c === ','){ row.push(field); field = ''; }
        else if(c === '\n' || c === '\r'){
          if(field !== '' || row.length){ row.push(field); rows.push(row); }
          field = ''; row = [];
          if(c === '\r' && next === '\n') i++;
        } else { field += c; }
      }
    }
    if(field !== '' || row.length){ row.push(field); rows.push(row); }
    return rows.filter(function(r){ return r.length && r.some(function(v){ return v.trim() !== ''; }); });
  }
</script>
<script>
  // Pendaftaran/pemesanan diproses langsung via WhatsApp ke Narahubung PC IPNU Kab. Banjar.
  const NARAHUBUNG_WA = '6283853209822';

  function tanggalHariIni(){
    return new Date().toLocaleDateString('id-ID', { day:'2-digit', month:'short', year:'numeric' });
  }
  function postBeritaLayanan(item){
    if(window.ipnuTambahBerita){ window.ipnuTambahBerita(item); }
    kirimKeSheet('Berita', item);
  }

  var formJas = document.getElementById('form-jas-el');
  if(formJas){
    formJas.addEventListener('submit', function(e){
      e.preventDefault();
      var nama = document.getElementById('jas-nama').value.trim();
      var asal = document.getElementById('jas-asal').value.trim();
      var ukuran = document.getElementById('jas-ukuran').value;

      var pesan = 'Assalamu\'alaikum, saya ingin memesan Jas IPNU.%0A%0A' +
        'Nama: ' + encodeURIComponent(nama) + '%0A' +
        'Asal Pimpinan: ' + encodeURIComponent(asal) + '%0A' +
        'Ukuran: ' + encodeURIComponent(ukuran) + '%0A%0A' +
        'Mohon informasi selanjutnya. Terima kasih.';

      var successEl = document.getElementById('jas-success');
      if(successEl){ successEl.classList.add('show'); }

      var btn = formJas.querySelector('button[type="submit"]');
      if(btn){ btn.disabled = true; btn.style.opacity = '0.6'; }

      window.open('https://wa.me/' + NARAHUBUNG_WA + '?text=' + pesan, '_blank', 'noopener');

      postBeritaLayanan({
        tanggal: tanggalHariIni(),
        kategori: 'Pengumuman',
        judul: 'Pemesanan Jas IPNU — ' + nama,
        ringkasan: nama + ' dari ' + asal + ' memesan Jas IPNU ukuran ' + ukuran + '. Pesanan sedang diproses Narahubung.',
        foto: '',
        link: ''
      });

      setTimeout(function(){
        if(successEl){ successEl.classList.remove('show'); }
        if(btn){ btn.disabled = false; btn.style.opacity = '1'; }
        formJas.reset();
      }, 2500);
    });
  }

  var linkKonsultasi = document.getElementById('link-konsultasi-kaderisasi');
  if(linkKonsultasi){
    linkKonsultasi.addEventListener('click', function(){
      postBeritaLayanan({
        tanggal: tanggalHariIni(),
        kategori: 'Pengumuman',
        judul: 'Permintaan Konsultasi Kaderisasi Baru',
        ringkasan: 'Ada kader yang mengajukan konsultasi kaderisasi melalui WhatsApp Narahubung PC IPNU Kab. Banjar.',
        foto: '',
        link: ''
      });
    });
  }
</script>
<script>
  // ================================================================
  // STRUKTUR: TAMBAH ANGGOTA (lokal di browser + sinkron ke Google Sheet)
  // ================================================================
  const LOCAL_ANGGOTA_KEY = 'ipnuBanjarAnggotaLokal';

  const TIER_GRID_MAP = {
    'Pimpinan Harian': 'grid-pimpinan-harian',
    'Lembaga Kaderisasi': 'grid-lembaga-kaderisasi',
    'Departemen Pendidikan & Dakwah': 'grid-departemen-pendidikan-dakwah',
    'Departemen Organisasi': 'grid-departemen-organisasi',
    'Departemen Bakat Minat & Olahraga': 'grid-departemen-bakat-minat-olahraga'
  };

  function loadLocalAnggota(){
    try{ return JSON.parse(localStorage.getItem(LOCAL_ANGGOTA_KEY) || '[]'); }
    catch(e){ return []; }
  }
  function saveLocalAnggota(list){
    localStorage.setItem(LOCAL_ANGGOTA_KEY, JSON.stringify(list));
  }

  function escapeHTMLAnggota(str){
    const div = document.createElement('div');
    div.textContent = str || '';
    return div.innerHTML;
  }

  function initialsFromName(name){
    const parts = name.trim().split(/\s+/).filter(Boolean);
    if(!parts.length) return '??';
    if(parts.length === 1) return parts[0].slice(0,2).toUpperCase();
    return (parts[0][0] + parts[parts.length-1][0]).toUpperCase();
  }

  function buildPersonCardEl(item, source){
    const card = document.createElement('div');
    card.className = 'person-card ' + (source === 'sheet' ? 'sheet' : 'local');
    if(source === 'sheet'){ card.dataset.pid = item.id; } else { card.dataset.localId = item.id; }
    const hasFoto = !!item.foto;
    const avatarStyle = hasFoto ? ' style="background-image:url(\'' + item.foto.replace(/'/g,'') + '\')"' : '';
    const avatarClass = 'avatar' + (hasFoto ? ' has-photo' : '');
    const tagLabel = source === 'sheet' ? 'Google Sheet' : 'Baru';
    card.innerHTML =
      '<span class="local-tag">' + tagLabel + '</span>' +
      (source === 'sheet' ? '' : '<button type="button" class="remove-btn" title="Hapus anggota ini">&times;</button>') +
      '<div class="' + avatarClass + '"' + avatarStyle + '>' + (hasFoto ? '' : escapeHTMLAnggota(item.inisial)) + '</div>' +
      '<h4>' + escapeHTMLAnggota(item.nama) + '</h4>' +
      '<div class="role">' + escapeHTMLAnggota(item.jabatan) + '</div>';
    if(source !== 'sheet'){
      card.querySelector('.remove-btn').addEventListener('click', function(){
        if(confirm('Hapus anggota "' + item.nama + '" dari daftar lokal?')){
          const list = loadLocalAnggota().filter(function(a){ return a.id !== item.id; });
          saveLocalAnggota(list);
          renderLocalAnggota();
        }
      });
    }
    return card;
  }

  function clearGeneratedCards(){
    document.querySelectorAll('.person-card.local, .person-card.sheet').forEach(function(el){ el.remove(); });
  }

  function insertCardIntoGrid(card, tier){
    const gridId = TIER_GRID_MAP[tier];
    const grid = gridId ? document.getElementById(gridId) : null;
    if(!grid) return;
    const addBtn = grid.querySelector('.add-person-card');
    if(addBtn){ grid.insertBefore(card, addBtn); } else { grid.appendChild(card); }
  }

  let sheetAnggotaItems = [];

  function renderLocalAnggota(){
    clearGeneratedCards();

    // Anggota dari Google Sheet (terpusat, tampil untuk semua pengunjung)
    const localIds = loadLocalAnggota().map(function(a){ return a.id; });
    sheetAnggotaItems.forEach(function(item){
      if(localIds.indexOf(item.id) > -1) return; // hindari duplikat di perangkat yang sama
      insertCardIntoGrid(buildPersonCardEl(item, 'sheet'), item.tier);
    });

    // Anggota lokal (baru ditambahkan di perangkat ini, belum tentu tersinkron)
    const list = loadLocalAnggota();
    list.forEach(function(item){
      insertCardIntoGrid(buildPersonCardEl(item, 'local'), item.tier);
    });

    const counter = document.getElementById('jumlah-anggota-lokal');
    if(counter) counter.textContent = list.length;
  }

  function muatAnggotaDariSheet(){
    if(!isConfigured(STRUKTUR_CSV_URL)) return;
    fetch(STRUKTUR_CSV_URL)
      .then(function(res){ return res.text(); })
      .then(function(text){
        const rows = parseCSVUmum(text);
        if(rows.length < 2) return;
        const header = rows[0].map(function(h){ return h.trim().toLowerCase(); });
        const idx = {
          id: header.indexOf('pid'), tier: header.indexOf('tier'), nama: header.indexOf('nama'),
          jabatan: header.indexOf('jabatan'), inisial: header.indexOf('inisial'), foto: header.indexOf('foto')
        };
        sheetAnggotaItems = rows.slice(1).map(function(r){
          return {
            id: r[idx.id] || '', tier: r[idx.tier] || '', nama: r[idx.nama] || '',
            jabatan: r[idx.jabatan] || '', inisial: (r[idx.inisial] || '').toUpperCase().slice(0,2),
            foto: idx.foto > -1 ? (r[idx.foto] || '') : ''
          };
        }).filter(function(it){ return it.nama && TIER_GRID_MAP[it.tier]; });
        renderLocalAnggota();
      })
      .catch(function(err){ console.warn('Gagal memuat anggota dari Google Sheet:', err); });
  }

  function appendAddCardToEachGrid(){
    Object.keys(TIER_GRID_MAP).forEach(function(tier){
      const grid = document.getElementById(TIER_GRID_MAP[tier]);
      if(!grid || grid.querySelector('.add-person-card')) return;
      const addCard = document.createElement('div');
      addCard.className = 'add-person-card';
      addCard.innerHTML = '<div class="plus">+</div><span class="label">Tambah Anggota</span>';
      addCard.addEventListener('click', function(){ openAnggotaModal(tier); });
      grid.appendChild(addCard);
    });
  }

  const anggotaModalOverlay = document.getElementById('anggota-modal-overlay');
  const openAnggotaBtnHeader = null; // tombol ada di tiap kartu "+ Tambah Anggota" per grid
  const closeAnggotaModalBtn = document.getElementById('btn-close-anggota-modal');
  const formTambahAnggota = document.getElementById('form-tambah-anggota');
  const btnCopyAnggotaData = document.getElementById('btn-copy-anggota-data');
  const btnHapusAnggotaLokal = document.getElementById('btn-hapus-anggota-lokal');
  const selectKelompok = document.getElementById('na-kelompok');

  function openAnggotaModal(prefilledTier){
    if(prefilledTier && selectKelompok){ selectKelompok.value = prefilledTier; }
    anggotaModalOverlay.classList.add('show');
  }
  function closeAnggotaModal(){ anggotaModalOverlay.classList.remove('show'); }

  if(closeAnggotaModalBtn) closeAnggotaModalBtn.addEventListener('click', closeAnggotaModal);
  if(anggotaModalOverlay) anggotaModalOverlay.addEventListener('click', function(e){
    if(e.target === anggotaModalOverlay) closeAnggotaModal();
  });

  if(formTambahAnggota){
    formTambahAnggota.addEventListener('submit', function(e){
      e.preventDefault();
      const nama = document.getElementById('na-nama').value.trim();
      const jabatan = document.getElementById('na-jabatan').value.trim();
      const tier = document.getElementById('na-kelompok').value;
      const inisialInput = document.getElementById('na-inisial').value.trim();
      const fotoInput = document.getElementById('na-foto').value.trim();
      const item = {
        id: 'a' + Date.now(),
        tier: tier,
        nama: nama,
        jabatan: jabatan,
        inisial: (inisialInput || initialsFromName(nama)).toUpperCase().slice(0,2),
        foto: fotoInput
      };
      const list = loadLocalAnggota();
      list.push(item);
      saveLocalAnggota(list);
      renderLocalAnggota();
      kirimKeSheet('Anggota', { pid: item.id, tier: item.tier, nama: item.nama, jabatan: item.jabatan, inisial: item.inisial, foto: item.foto });

      const successEl = document.getElementById('anggota-success');
      if(successEl){
        successEl.classList.add('show');
        setTimeout(function(){ successEl.classList.remove('show'); closeAnggotaModal(); formTambahAnggota.reset(); }, 1400);
      }
    });
  }

  if(btnCopyAnggotaData){
    btnCopyAnggotaData.addEventListener('click', function(){
      const nama = document.getElementById('na-nama').value.trim();
      const jabatan = document.getElementById('na-jabatan').value.trim();
      const tier = document.getElementById('na-kelompok').value;
      const inisialInput = document.getElementById('na-inisial').value.trim();
      const inisial = (inisialInput || initialsFromName(nama)).toUpperCase().slice(0,2);
      const html = '<div class="person-card"><div class="avatar">' + inisial + '</div><h4>' + nama + '</h4><div class="role">' + jabatan + '</div></div>';
      navigator.clipboard.writeText(html).then(function(){
        btnCopyAnggotaData.textContent = 'Tersalin! Tempel di kode HTML';
        setTimeout(function(){ btnCopyAnggotaData.textContent = 'Salin Data'; }, 2000);
      }).catch(function(){
        alert('Gagal menyalin otomatis. Kode kartu:\n' + html);
      });
    });
  }

  if(btnHapusAnggotaLokal){
    btnHapusAnggotaLokal.addEventListener('click', function(e){
      e.preventDefault();
      if(confirm('Hapus semua anggota lokal yang tersimpan di browser ini?')){
        localStorage.removeItem(LOCAL_ANGGOTA_KEY);
        renderLocalAnggota();
      }
    });
  }

  appendAddCardToEachGrid();
  renderLocalAnggota();
  muatAnggotaDariSheet();
</script>
<script>
  // ================================================================
  // BERITA: GOOGLE SHEET (opsional) + BERITA LOKAL (fitur "+ Tambah Berita")
  // ================================================================
  // 1. Buat Google Sheet dengan kolom persis: Tanggal | Kategori | Judul | Ringkasan | LinkFoto | LinkBerita
  // 2. File -> Share -> Publish to web -> pilih sheet berita -> format CSV -> Publish
  // 3. Salin link CSV yang muncul, tempel di variabel BERITA_CSV_URL di bawah ini
  const BERITA_CSV_URL = "GANTI_DENGAN_LINK_CSV_GOOGLE_SHEET_ANDA";
  const LOCAL_BERITA_KEY = 'ipnuBanjarBeritaLokal';

  const DEFAULT_BERITA = [
    { tanggal:'08 Jul 2026', kategori:'Kegiatan', judul:'Judul berita utama kegiatan PC IPNU Kab. Banjar', ringkasan:'Ringkasan singkat kegiatan atau rilis pers yang menonjolkan capaian dan kontribusi kader IPNU di masyarakat...', foto:'', link:'' },
    { tanggal:'06 Jul 2026', kategori:'Kabar Ranting', judul:'Judul berita dari ranting kecamatan', ringkasan:'Cuplikan singkat isi berita ranting.', foto:'', link:'' },
    { tanggal:'03 Jul 2026', kategori:'Opini Kader', judul:'Judul opini kader tentang isu pelajar', ringkasan:'Cuplikan singkat opini kader.', foto:'', link:'' }
  ];

  let baseBerita = DEFAULT_BERITA; // diisi ulang kalau Google Sheet berhasil dimuat

  function loadLocalBerita(){
    try{ return JSON.parse(localStorage.getItem(LOCAL_BERITA_KEY) || '[]'); }
    catch(e){ return []; }
  }
  function saveLocalBerita(list){
    localStorage.setItem(LOCAL_BERITA_KEY, JSON.stringify(list));
  }

  // Dipanggil dari luar (mis. form Pemesanan Jas IPNU / Layanan Kader) untuk otomatis
  // menambahkan entri ke Berita ketika ada aktivitas layanan baru.
  window.ipnuTambahBerita = function(item){
    const list = loadLocalBerita();
    list.unshift(item);
    saveLocalBerita(list);
    renderAllBerita();
  };

  function escapeHTML(str){
    const div = document.createElement('div');
    div.textContent = str || '';
    return div.innerHTML;
  }

  function renderNewsGrid(items){
    const grid = document.getElementById('news-grid');
    if(!grid || !items.length) return;

    const html = items.slice(0, 6).map(function(item, i){
      const isLead = i === 0;
      const thumbStyle = item.foto
        ? 'style="background-image:url(\'' + item.foto.replace(/'/g,'') + '\');background-size:cover;background-position:center;"'
        : '';
      const cardInner =
        '<div class="thumb" ' + thumbStyle + '>' +
          (item.foto ? '' : '<div class="facet-corner"></div>') +
          '<span class="cat">' + escapeHTML(item.kategori || 'Berita') + '</span>' +
        '</div>' +
        '<div class="body">' +
          '<span class="date">' + escapeHTML(item.tanggal) + '</span>' +
          '<h3>' + escapeHTML(item.judul) + '</h3>' +
          '<p>' + escapeHTML(item.ringkasan) + '</p>' +
        '</div>';
      const cls = 'news-card' + (isLead ? ' lead' : '');
      return item.link
        ? '<a class="' + cls + '" href="' + item.link + '" target="_blank" rel="noopener" style="display:flex;flex-direction:column;">' + cardInner + '</a>'
        : '<div class="' + cls + '">' + cardInner + '</div>';
    }).join('');

    grid.innerHTML = html;
  }

  function renderAllBerita(){
    const local = loadLocalBerita();
    renderNewsGrid(local.concat(baseBerita));
    const counter = document.getElementById('jumlah-berita-lokal');
    if(counter) counter.textContent = local.length;
  }

  function parseCSV(text){
    const rows = [];
    let row = [], field = '', inQuotes = false;
    for(let i = 0; i < text.length; i++){
      const c = text[i], next = text[i+1];
      if(inQuotes){
        if(c === '"' && next === '"'){ field += '"'; i++; }
        else if(c === '"'){ inQuotes = false; }
        else { field += c; }
      } else {
        if(c === '"'){ inQuotes = true; }
        else if(c === ','){ row.push(field); field = ''; }
        else if(c === '\n' || c === '\r'){
          if(field !== '' || row.length){ row.push(field); rows.push(row); }
          field = ''; row = [];
          if(c === '\r' && next === '\n') i++;
        } else { field += c; }
      }
    }
    if(field !== '' || row.length){ row.push(field); rows.push(row); }
    return rows.filter(r => r.length && r.some(v => v.trim() !== ''));
  }

  function csvRowsToItems(rows){
    if(rows.length < 2) return [];
    const header = rows[0].map(h => h.trim().toLowerCase());
    const idx = {
      tanggal: header.indexOf('tanggal'),
      kategori: header.indexOf('kategori'),
      judul: header.indexOf('judul'),
      ringkasan: header.indexOf('ringkasan'),
      foto: header.indexOf('linkfoto'),
      link: header.indexOf('linkberita')
    };
    return rows.slice(1).reverse().map(function(r){
      return {
        tanggal: r[idx.tanggal] || '',
        kategori: r[idx.kategori] || 'Berita',
        judul: r[idx.judul] || 'Tanpa judul',
        ringkasan: r[idx.ringkasan] || '',
        foto: idx.foto > -1 ? (r[idx.foto] || '') : '',
        link: idx.link > -1 ? (r[idx.link] || '') : ''
      };
    });
  }

  // Muat data awal (lokal + default), lalu coba timpa base dengan Google Sheet kalau sudah dipasang
  renderAllBerita();
  if(BERITA_CSV_URL && BERITA_CSV_URL.indexOf('GANTI_DENGAN') === -1){
    fetch(BERITA_CSV_URL)
      .then(function(res){ return res.text(); })
      .then(function(text){
        const csvItems = csvRowsToItems(parseCSV(text));
        if(csvItems.length){ baseBerita = csvItems; renderAllBerita(); }
      })
      .catch(function(err){ console.warn('Gagal memuat berita dari Google Sheet:', err); });
  }

  // ================================================================
  // MODAL "+ TAMBAH BERITA"
  // ================================================================
  const modalOverlay = document.getElementById('berita-modal-overlay');
  const openModalBtn = document.getElementById('btn-open-berita-modal');
  const openModalBtnHero = document.getElementById('btn-open-berita-modal-hero');
  const closeModalBtn = document.getElementById('btn-close-berita-modal');
  const formTambahBerita = document.getElementById('form-tambah-berita');
  const btnCopyData = document.getElementById('btn-copy-berita-data');
  const btnHapusLokal = document.getElementById('btn-hapus-berita-lokal');

  function openBeritaModal(){ modalOverlay.classList.add('show'); }
  function closeBeritaModal(){ modalOverlay.classList.remove('show'); }

  if(openModalBtn) openModalBtn.addEventListener('click', openBeritaModal);
  if(openModalBtnHero) openModalBtnHero.addEventListener('click', function(e){
    e.preventDefault();
    openBeritaModal();
  });
  if(closeModalBtn) closeModalBtn.addEventListener('click', closeBeritaModal);
  if(modalOverlay) modalOverlay.addEventListener('click', function(e){
    if(e.target === modalOverlay) closeBeritaModal();
  });

  if(formTambahBerita){
    formTambahBerita.addEventListener('submit', function(e){
      e.preventDefault();
      const item = {
        judul: document.getElementById('nb-judul').value.trim(),
        tanggal: document.getElementById('nb-tanggal').value.trim(),
        kategori: document.getElementById('nb-kategori').value,
        ringkasan: document.getElementById('nb-ringkasan').value.trim(),
        foto: document.getElementById('nb-foto').value.trim(),
        link: document.getElementById('nb-link').value.trim()
      };
      const local = loadLocalBerita();
      local.unshift(item);
      saveLocalBerita(local);
      renderAllBerita();
      kirimKeSheet('Berita', item);

      const successEl = document.getElementById('berita-success');
      if(successEl){
        successEl.classList.add('show');
        setTimeout(function(){ successEl.classList.remove('show'); closeBeritaModal(); formTambahBerita.reset(); }, 1400);
      }
    });
  }

  if(btnCopyData){
    btnCopyData.addEventListener('click', function(){
      const row = [
        document.getElementById('nb-tanggal').value,
        document.getElementById('nb-kategori').value,
        document.getElementById('nb-judul').value,
        document.getElementById('nb-ringkasan').value,
        document.getElementById('nb-foto').value,
        document.getElementById('nb-link').value
      ].map(function(v){ return '"' + (v || '').replace(/"/g,'""') + '"'; }).join(',');
      navigator.clipboard.writeText(row).then(function(){
        btnCopyData.textContent = 'Tersalin! Tempel di Google Sheet';
        setTimeout(function(){ btnCopyData.textContent = 'Salin Data'; }, 2000);
      }).catch(function(){
        alert('Gagal menyalin otomatis. Data (format CSV):\n' + row);
      });
    });
  }

  if(btnHapusLokal){
    btnHapusLokal.addEventListener('click', function(e){
      e.preventDefault();
      if(confirm('Hapus semua berita lokal yang tersimpan di browser ini?')){
        localStorage.removeItem(LOCAL_BERITA_KEY);
        renderAllBerita();
      }
    });
  }
</script>
<script>
  // ================================================================
  // STRUKTUR: EDIT NAMA LANGSUNG + UNGGAH FOTO PENGURUS
  // Tersimpan lokal di browser untuk pratinjau instan, dan otomatis
  // dikirim ke Google Sheet pusat (jika sudah terhubung) agar berlaku
  // untuk semua pengunjung.
  // ================================================================
  const STRUKTUR_EDIT_KEY = 'ipnuBanjarStrukturEdits';

  function loadStrukturEdits(){
    try{ return JSON.parse(localStorage.getItem(STRUKTUR_EDIT_KEY) || '{}'); }
    catch(e){ return {}; }
  }
  function saveStrukturEdits(edits){
    localStorage.setItem(STRUKTUR_EDIT_KEY, JSON.stringify(edits));
  }

  let strukturEdits = loadStrukturEdits();

  function getPersonPid(card){
    if(card.dataset.pid) return card.dataset.pid; // kartu dari Google Sheet
    if(card.dataset.localId) return 'local-' + card.dataset.localId;
    const grid = card.closest('.people-grid');
    const gridId = grid ? grid.id : 'grid';
    const staticCards = grid ? Array.from(grid.querySelectorAll('.person-card:not(.local):not(.sheet)')) : [];
    const idx = staticCards.indexOf(card);
    return gridId + '-' + idx;
  }

  function applyStrukturEdit(card){
    const pid = getPersonPid(card);
    const data = strukturEdits[pid];
    if(!data) return;
    if(data.name){
      const h4 = card.querySelector('h4');
      if(h4) h4.textContent = data.name;
    }
    if(data.photo){
      const avatar = card.querySelector('.avatar');
      if(avatar){
        avatar.style.backgroundImage = 'url(' + data.photo + ')';
        avatar.classList.add('has-photo');
      }
    }
  }

  function kirimEditKeSheet(card){
    const pid = getPersonPid(card);
    const grid = card.closest('.people-grid');
    const tier = grid ? grid.dataset.tier : '';
    const h4 = card.querySelector('h4');
    const role = card.querySelector('.role');
    const avatar = card.querySelector('.avatar');
    const data = strukturEdits[pid] || {};
    kirimKeSheet('Anggota', {
      pid: pid,
      tier: tier,
      nama: (data.name || (h4 ? h4.textContent.trim() : '')),
      jabatan: role ? role.textContent.trim() : '',
      inisial: '',
      foto: data.photo || (avatar && avatar.classList.contains('has-photo') ? avatar.style.backgroundImage.slice(5, -2) : '')
    });
  }

  // Input file tersembunyi bersama, dipakai untuk semua avatar
  const strukturFileInput = document.createElement('input');
  strukturFileInput.type = 'file';
  strukturFileInput.accept = 'image/*';
  strukturFileInput.style.display = 'none';
  document.body.appendChild(strukturFileInput);
  let strukturActiveCard = null;

  strukturFileInput.addEventListener('change', function(){
    const file = strukturFileInput.files[0];
    if(!file || !strukturActiveCard) return;
    kompresFoto(file, function(dataUrl){
      const pid = getPersonPid(strukturActiveCard);
      if(!strukturEdits[pid]) strukturEdits[pid] = {};
      strukturEdits[pid].photo = dataUrl;
      saveStrukturEdits(strukturEdits);
      applyStrukturEdit(strukturActiveCard);
      kirimEditKeSheet(strukturActiveCard);
    });
    strukturFileInput.value = '';
  });

  function bindPersonCardEditing(card){
    if(card.dataset.editBound === '1') return;
    card.dataset.editBound = '1';

    const h4 = card.querySelector('h4');
    const avatar = card.querySelector('.avatar');

    if(h4){
      h4.setAttribute('contenteditable', 'true');
      h4.setAttribute('spellcheck', 'false');
      h4.classList.add('editable-name');
      h4.title = 'Klik untuk mengedit nama';
      h4.addEventListener('blur', function(){
        const pid = getPersonPid(card);
        const val = h4.textContent.trim();
        if(!strukturEdits[pid]) strukturEdits[pid] = {};
        strukturEdits[pid].name = val;
        saveStrukturEdits(strukturEdits);
        kirimEditKeSheet(card);
      });
      h4.addEventListener('keydown', function(e){
        if(e.key === 'Enter'){ e.preventDefault(); h4.blur(); }
      });
    }

    if(avatar){
      avatar.title = 'Klik untuk mengganti foto';
      avatar.addEventListener('click', function(){
        strukturActiveCard = card;
        strukturFileInput.click();
      });
    }

    applyStrukturEdit(card);
  }

  document.querySelectorAll('.person-card').forEach(bindPersonCardEditing);

  // Kartu anggota baru (dari fitur "+ Tambah Anggota" atau dari Google Sheet)
  // ditambahkan secara dinamis, jadi kita pantau perubahan pada tiap grid
  // agar kartu baru juga bisa diedit.
  document.querySelectorAll('.people-grid').forEach(function(grid){
    const observer = new MutationObserver(function(){
      grid.querySelectorAll('.person-card').forEach(bindPersonCardEditing);
    });
    observer.observe(grid, { childList: true });
  });
</script>
</body>
</html>
