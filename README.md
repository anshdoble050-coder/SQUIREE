# SQUIREE
Author-ANSH
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SQUIREIX. — Research + Development</title>
<style>
  :root{
    --ink:#0a0f0a;
    --cream:#f2eee2;
    --gold:#f0d97a;
    --deep:#0f2a1e;
    --deep2:#1a3326;
    --olive:#3a3620;
    --muted:#a9a79c;
    --line: rgba(255,255,255,0.14);
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:
      linear-gradient(180deg, rgba(10,15,10,0.55) 0%, rgba(10,15,10,0.7) 100%),
      url('hero-bg.jpg') center 25% / cover no-repeat fixed;
    color:var(--ink);
    font-family:'Inter', 'Helvetica Neue', Arial, sans-serif;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }
  h1,h2,h3{
    font-family:'Archivo', 'Inter', sans-serif;
    font-weight:800;
    letter-spacing:-0.02em;
    line-height:0.98;
  }
  a{color:inherit; text-decoration:none;}
  img{display:block; max-width:100%;}

  /* NAV */
  header{
    position:sticky; top:0; z-index:50;
    display:flex; align-items:center; justify-content:space-between;
    padding:18px 28px;
    background:rgba(10,15,10,0.82);
    backdrop-filter:blur(6px);
    color:var(--cream);
    border-bottom:1px solid var(--line);
  }
  .brand{display:flex; align-items:center; gap:14px;}
  .mark{
    width:40px; height:40px;
    background:var(--gold);
    color:var(--ink);
    display:flex; align-items:center; justify-content:center;
    font-weight:900; font-size:18px;
    font-family:'Archivo', sans-serif;
  }
  .brand-name{font-weight:800; font-size:19px; letter-spacing:0.01em;}
  .menu-btn{
    display:flex; flex-direction:column; gap:5px; cursor:pointer;
    padding:6px;
  }
  .menu-btn span{width:24px; height:2px; background:var(--cream); display:block;}

  section{padding:88px 28px; position:relative;}
  .eyebrow{
    font-size:13px; font-weight:600; letter-spacing:0.06em;
    color:var(--gold); margin-bottom:22px;
    display:flex; align-items:center; gap:10px;
  }
  .eyebrow.dark{color:var(--deep2);}

  /* HERO */
  #hero{
    background:linear-gradient(180deg, rgba(10,15,10,0.2) 0%, rgba(10,15,10,0.55) 75%, rgba(10,15,10,0.75) 100%);
    color:var(--cream);
    min-height:92vh;
    display:flex; flex-direction:column; justify-content:center;
    padding-top:64px; padding-bottom:64px;
  }
  .hero-title{
    font-size:clamp(3rem, 13vw, 7rem);
    color:var(--cream);
  }
  .hero-title .dot{color:var(--gold);}
  .hero-sub{
    font-size:clamp(1.3rem, 3vw, 1.9rem);
    font-weight:700;
    max-width:560px;
    margin:34px 0 18px;
    color:var(--cream);
    font-family:'Archivo', sans-serif;
  }
  .hero-desc{
    font-size:1.05rem;
    color:#c7c9c0;
    max-width:520px;
    line-height:1.6;
    margin-bottom:40px;
  }
  .btn-row{display:flex; flex-wrap:wrap; gap:16px;}
  .btn{
    padding:18px 26px;
    font-size:14px; font-weight:700; letter-spacing:0.04em;
    display:inline-flex; align-items:center; gap:10px;
    cursor:pointer; border:none;
    font-family:'Inter', sans-serif;
  }
  .btn-solid{background:var(--gold); color:var(--ink);}
  .btn-outline{background:transparent; color:var(--cream); border:1px solid var(--line);}
  .btn:hover{opacity:0.88;}

  /* ABOUT */
  #about{background:rgba(10,15,10,0.82); color:var(--cream); padding-top:100px; padding-bottom:110px;}
  .about-head{font-size:clamp(2.3rem, 7vw, 4.2rem); margin-bottom:44px;}
  .about-head .accent{color:var(--gold);}
  .about-grid{display:grid; grid-template-columns: 1fr; gap:26px; max-width:780px;}
  .about-lead{font-size:1.25rem; font-weight:700; line-height:1.45; font-family:'Archivo',sans-serif;}
  .about-lead b{color:var(--cream);}
  .about-body{color:#b9bcb2; font-size:1.05rem; line-height:1.75;}
  .about-body .hl{color:var(--gold);}

  /* FIELDS */
  #fields{background:rgba(242,238,226,0.94); padding:100px 28px;}
  .fields-head{margin-bottom:56px; max-width:640px;}
  .fields-head h2{font-size:clamp(2.1rem,6vw,3.4rem); color:var(--ink);}
  .fields-head p{color:#5a584f; margin-top:16px; font-size:1.05rem;}
  .field-list{display:flex; flex-direction:column; gap:2px;}
  .field-card{
    min-height:280px;
    padding:42px 34px 34px;
    display:flex; flex-direction:column; justify-content:flex-end;
    position:relative; overflow:hidden;
    color:var(--cream);
  }
  .field-card .fnum{font-size:13px; letter-spacing:0.06em; font-weight:700; opacity:0.85; margin-bottom:12px;}
  .field-card h3{font-size:2.2rem; margin-bottom:14px;}
  .field-card p{font-size:1rem; max-width:420px; color:#dcdccf; line-height:1.5;}
  .field-card.cosmos{background:linear-gradient(160deg,#0f2a1e,#08130d);}
  .field-card.intel{background:linear-gradient(160deg,#12301f,#0a1a12); color:var(--cream);}
  .field-card.hardware{background:linear-gradient(180deg,#e7e4d8,#3a3a37); color:var(--ink);}
  .field-card.hardware h3, .field-card.hardware .fnum{color:var(--ink);}
  .field-card.hardware p{color:#3f3f3a;}
  .field-card.machines{background:linear-gradient(180deg,#c9b458,#2a2410); color:var(--cream);}
  .field-card.machines .fnum{color:var(--ink);}
  .field-card.machines h3{color:#1c1c14;}
  .field-card.machines p{color:#3a3421;}

  .glyph{position:absolute; inset:0; display:flex; align-items:center; justify-content:center; opacity:0.5; pointer-events:none;}
  .glyph svg{width:60%; max-width:340px;}

  /* GALLERY */
  #gallery{background:rgba(242,238,226,0.94); padding-top:100px; padding-bottom:20px;}
  .gallery-head{max-width:640px; margin-bottom:48px;}
  .gallery-head h2{font-size:clamp(2.1rem,6.5vw,3.6rem); color:var(--ink);}
  .gallery-head .g2{color:var(--deep);}
  .gallery-head p{color:#5a584f; margin-top:16px; font-size:1.05rem;}
  .gallery-card{
    background:linear-gradient(160deg,#153826,#0a1a11);
    padding:60px 32px; min-height:420px;
    display:flex; align-items:center; justify-content:center;
    position:relative;
  }
  .orbit-mark{
    width:150px; height:150px; border-radius:50%;
    border:1.5px solid var(--gold);
    display:flex; align-items:center; justify-content:center;
    color:var(--gold); font-size:2.6rem; font-weight:800;
    font-family:'Archivo', sans-serif;
    position:relative; z-index:2;
  }
  .orbit-ring{position:absolute; border:1px solid rgba(240,217,122,0.35); border-radius:50%;}
  .ring1{width:340px; height:220px;}
  .ring2{width:220px; height:340px;}
  .gallery-caption{
    position:absolute; left:32px; bottom:28px; color:#cfd2c6; font-size:13px; letter-spacing:0.05em; line-height:1.6;
  }

  /* CONTACT */
  #contact{background:rgba(240,217,122,0.94); padding:100px 28px 90px;}
  .contact-head h2{font-size:clamp(2.4rem,8vw,4.2rem); color:var(--ink);}
  .contact-head .green{color:var(--deep);}
  .contact-head p{max-width:520px; margin:22px 0 44px; color:#3d3a24; font-size:1.05rem; line-height:1.6;}
  form{max-width:640px; border-top:2px solid var(--ink); padding-top:36px;}
  .field{margin-bottom:30px;}
  label{display:block; font-size:12px; font-weight:700; letter-spacing:0.06em; color:#4a4728; margin-bottom:10px;}
  input, textarea{
    width:100%; background:transparent; border:none; border-bottom:1px solid rgba(10,15,10,0.35);
    padding:10px 0; font-size:1.05rem; font-family:'Inter',sans-serif; color:var(--ink);
  }
  input::placeholder, textarea::placeholder{color:#7c7a5c;}
  input:focus, textarea:focus{outline:none; border-bottom:1px solid var(--ink);}
  textarea{resize:vertical; min-height:90px;}
  .send-btn{
    margin-top:14px; background:var(--ink); color:var(--cream);
    padding:18px 32px; border:none; font-weight:700; letter-spacing:0.05em; font-size:14px; cursor:pointer;
  }
  .send-btn:hover{opacity:0.85;}

  footer{
    background:rgba(10,15,10,0.9); color:#8f9187; padding:34px 28px;
    display:flex; justify-content:space-between; flex-wrap:wrap; gap:14px;
    font-size:13px;
  }

  @media(min-width:860px){
    .about-grid{grid-template-columns: 1fr 1fr; gap:56px;}
    .field-list{display:grid; grid-template-columns:1fr 1fr; gap:2px;}
    .field-card{min-height:380px;}
  }
</style>
</head>
<body>

<header>
  <div class="brand">
    <div class="mark">S≡</div>
    <div class="brand-name">SQUIREIX.</div>
  </div>
  <div class="menu-btn" aria-label="menu"><span></span><span></span><span></span></div>
</header>

<section id="hero">
  <div class="eyebrow">RESEARCH + DEVELOPMENT / 01</div>
  <h1 class="hero-title">SQUIREIX<span class="dot">.</span></h1>
  <p class="hero-sub">Making difficult things easier to understand.</p>
  <p class="hero-desc">Exploring technology, machines, AI-ML, electronics and the universe with curiosity, experimentation and clear thinking.</p>
  <div class="btn-row">
    <button class="btn btn-solid" onclick="document.getElementById('about').scrollIntoView()">DISCOVER SQUIREIX ↘</button>
    <button class="btn btn-outline" onclick="document.getElementById('fields').scrollIntoView()">EXPLORE FIELDS ↘</button>
  </div>
</section>

<section id="about">
  <div class="eyebrow">02 / ABOUT US</div>
  <h2 class="about-head">Ideas into<br><span class="accent">understanding.</span></h2>
  <div class="about-grid">
    <p class="about-lead"><b>SQUIREIX is a Research and Development studio</b> that works on the field of improving the world by making things easy to understand and on the field of technology, machines, AI-ML, electronics and astronomical things.</p>
    <p class="about-body">We are interested in the space between <span class="hl">"How does it work?"</span> and <span class="hl">"How can we make it better?"</span> — turning curiosity into experiments, concepts and useful technology.</p>
  </div>
</section>

<section id="fields">
  <div class="fields-head">
    <h2>What we work on.</h2>
    <p>Four fields SQUIREIX keeps returning to, each feeding the others.</p>
  </div>
  <div class="field-list">
    <div class="field-card cosmos">
      <div class="glyph">
        <svg viewBox="0 0 200 200"><circle cx="100" cy="100" r="70" stroke="#f0d97a" stroke-width="1" fill="none" opacity="0.6"/><circle cx="150" cy="55" r="4" fill="#f0d97a"/><circle cx="45" cy="120" r="2.5" fill="#fff"/></svg>
      </div>
      <div class="fnum">01 — COSMOS</div>
      <h3>Astronomy</h3>
      <p>Stars, planets, galaxies, nebulae and the physics of the universe.</p>
    </div>
    <div class="field-card intel">
      <div class="glyph">
        <svg viewBox="0 0 200 200"><g stroke="#f0d97a" stroke-width="1" opacity="0.5"><line x1="40" y1="30" x2="10" y2="180"/><line x1="90" y1="30" x2="90" y2="180"/><line x1="140" y1="30" x2="170" y2="180"/><line x1="0" y1="70" x2="200" y2="70"/><line x1="0" y1="110" x2="200" y2="110"/><line x1="0" y1="150" x2="200" y2="150"/></g></svg>
      </div>
      <div class="fnum">02 — INTELLIGENCE</div>
      <h3>AI / ML</h3>
      <p>Intelligent systems, patterns, learning and useful automation.</p>
    </div>
    <div class="field-card hardware">
      <div class="glyph">
        <svg viewBox="0 0 200 200"><rect x="60" y="60" width="80" height="80" fill="none" stroke="#0a0f0a" stroke-width="3"/><rect x="72" y="72" width="56" height="56" fill="none" stroke="#f0d97a" stroke-width="10"/></svg>
      </div>
      <div class="fnum">03 — HARDWARE</div>
      <h3>Electronics</h3>
      <p>Circuits, sensors and the building blocks behind smart systems.</p>
    </div>
    <div class="field-card machines">
      <div class="glyph">
        <svg viewBox="0 0 200 200"><circle cx="100" cy="100" r="60" fill="none" stroke="#0a0f0a" stroke-width="3"/><g fill="#0f2a1e"><circle cx="100" cy="28" r="6"/><circle cx="151" cy="49" r="6"/><circle cx="172" cy="100" r="6"/><circle cx="151" cy="151" r="6"/><circle cx="100" cy="172" r="6"/><circle cx="49" cy="151" r="6"/><circle cx="28" cy="100" r="6"/><circle cx="49" cy="49" r="6"/></g></svg>
      </div>
      <div class="fnum">04 — ENGINEERING</div>
      <h3>Machines</h3>
      <p>Designing systems that turn ideas into things that work.</p>
    </div>
  </div>
</section>

<section id="gallery">
  <div class="gallery-head">
    <div class="eyebrow dark">03 / GALLERY</div>
    <h2>Curiosity has<br><span class="g2">no boundary.</span></h2>
    <p>A visual map of the worlds SQUIREIX explores — from microscopic electronics to enormous galaxies.</p>
  </div>
  <div class="gallery-card">
    <div class="orbit-ring ring1"></div>
    <div class="orbit-ring ring2"></div>
    <div class="orbit-mark">S.</div>
    <div class="gallery-caption">SQUIREIX.<br>RESEARCH &amp; DEVELOPMENT</div>
  </div>
</section>

<section id="contact">
  <div class="contact-head">
    <h2>Let's make<br><span class="green">something clear.</span></h2>
    <p>Have a question, idea, observation or suggestion? Send it to SQUIREIX.</p>
  </div>
  <form onsubmit="handleSubmit(event)">
    <div class="field">
      <label for="name">NAME</label>
      <input id="name" type="text" placeholder="Your name" required>
    </div>
    <div class="field">
      <label for="email">EMAIL ADDRESS</label>
      <input id="email" type="email" placeholder="you@example.com" required>
    </div>
    <div class="field">
      <label for="msg">MESSAGE / SUGGESTION</label>
      <textarea id="msg" placeholder="Write your message..." required></textarea>
    </div>
    <button class="send-btn" type="submit">SEND MESSAGE</button>
  </form>
</section>

<footer>
  <span>© 2026 SQUIREIX.</span>
  <span>Research + Development</span>
</footer>

<script>
function handleSubmit(e){
  e.preventDefault();
  alert("Thanks — your message has been noted. (Connect a form service to actually receive these.)");
  e.target.reset();
}
</script>

</body>
</html>