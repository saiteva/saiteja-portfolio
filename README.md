[saiteja_portfolio.html](https://github.com/user-attachments/files/27897373/saiteja_portfolio.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Vaddadi Sai Teja | QA Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
  :root {
    --ink: #0a0a0f; --paper: #f0f4ff; --blue: #2563eb; --blue-light: #93c5fd;
    --purple: #7c3aed; --purple-light: #ddd6fe; --green: #059669; --green-light: #d1fae5;
    --muted: #64748b; --border: rgba(10,10,15,0.1); --card: rgba(255,255,255,0.7);
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body { font-family: 'DM Sans', sans-serif; background: var(--paper); color: var(--ink); overflow-x: hidden; }

  /* NAV */
  nav { position: fixed; top: 0; left: 0; right: 0; z-index: 100; display: flex; align-items: center; justify-content: space-between; padding: 1rem 2.5rem; background: rgba(240,244,255,0.92); backdrop-filter: blur(12px); border-bottom: 1px solid var(--border); }
  .nav-logo { font-family: 'Playfair Display', serif; font-size: 1.1rem; font-weight: 700; color: var(--ink); }
  .nav-logo span { color: var(--blue); }
  .nav-links { display: flex; gap: 1.75rem; list-style: none; }
  .nav-links a { font-size: 0.78rem; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase; color: var(--muted); text-decoration: none; transition: color 0.2s; }
  .nav-links a:hover { color: var(--blue); }

  /* HERO */
  #hero { min-height: 100vh; display: grid; grid-template-columns: 1fr 1fr; align-items: center; padding: 8rem 2.5rem 4rem; position: relative; overflow: hidden; }
  .hero-bg { position: absolute; inset: 0; pointer-events: none; background: radial-gradient(ellipse 70% 80% at 85% 40%, rgba(37,99,235,0.07) 0%, rgba(124,58,237,0.05) 50%, transparent 70%); }
  .hero-dots { position: absolute; inset: 0; pointer-events: none; background-image: radial-gradient(circle, var(--border) 1px, transparent 1px); background-size: 32px 32px; opacity: 0.6; }
  .hero-left { position: relative; z-index: 2; }
  .hero-badge { display: inline-flex; align-items: center; gap: 8px; font-size: 0.72rem; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; color: var(--blue); background: rgba(37,99,235,0.08); border: 1px solid rgba(37,99,235,0.2); padding: 5px 14px; border-radius: 99px; margin-bottom: 1.5rem; animation: fadeUp 0.8s ease both; }
  .hero-name { font-family: 'Playfair Display', serif; font-size: clamp(2.4rem, 5vw, 4.2rem); font-weight: 900; line-height: 1.05; color: var(--ink); margin-bottom: 0.5rem; animation: fadeUp 0.9s 0.1s ease both; }
  .hero-name span { color: var(--blue); }
  .hero-title { font-size: 1rem; color: var(--muted); font-weight: 400; margin-bottom: 2rem; animation: fadeUp 0.9s 0.2s ease both; }
  .hero-stats { display: flex; gap: 1.75rem; margin-bottom: 2.5rem; animation: fadeUp 0.9s 0.3s ease both; flex-wrap: wrap; }
  .stat { border-left: 3px solid var(--blue); padding-left: 1rem; }
  .stat-val { font-family: 'Playfair Display', serif; font-size: 1.9rem; font-weight: 700; color: var(--ink); line-height: 1; }
  .stat-lab { font-size: 0.7rem; color: var(--muted); font-weight: 500; letter-spacing: 0.05em; text-transform: uppercase; margin-top: 2px; }
  .hero-cta { display: flex; gap: 1rem; flex-wrap: wrap; animation: fadeUp 0.9s 0.4s ease both; }
  .btn-primary { background: var(--blue); color: #fff; padding: 0.75rem 1.75rem; border-radius: 6px; font-size: 0.82rem; font-weight: 600; letter-spacing: 0.05em; text-transform: uppercase; text-decoration: none; border: none; cursor: pointer; transition: all 0.2s; display: inline-block; }
  .btn-primary:hover { background: var(--purple); transform: translateY(-2px); box-shadow: 0 8px 24px rgba(37,99,235,0.3); }
  .btn-outline { background: transparent; color: var(--ink); padding: 0.75rem 1.75rem; border-radius: 6px; font-size: 0.82rem; font-weight: 600; letter-spacing: 0.05em; text-transform: uppercase; text-decoration: none; border: 2px solid var(--border); cursor: pointer; transition: all 0.2s; display: inline-block; }
  .btn-outline:hover { background: var(--ink); color: #fff; transform: translateY(-2px); }
  .hero-right { position: relative; z-index: 2; display: flex; justify-content: center; align-items: center; animation: fadeIn 1.2s 0.3s ease both; }
  .hero-card { background: var(--ink); color: #fff; border-radius: 16px; padding: 2.25rem; width: 100%; max-width: 370px; position: relative; overflow: hidden; box-shadow: 0 24px 64px rgba(10,10,15,0.25); }
  .hero-card-glow { position: absolute; top: -80px; right: -80px; width: 220px; height: 220px; border-radius: 50%; background: rgba(37,99,235,0.2); filter: blur(40px); }
  .hero-card-glow2 { position: absolute; bottom: -60px; left: -60px; width: 180px; height: 180px; border-radius: 50%; background: rgba(124,58,237,0.15); filter: blur(40px); }
  .hero-card-title { font-family: 'Playfair Display', serif; font-size: 1.2rem; font-weight: 700; margin-bottom: 1.25rem; color: var(--blue-light); position: relative; z-index: 1; }
  .chip { display: inline-block; font-size: 0.7rem; font-weight: 600; padding: 3px 9px; border-radius: 4px; margin: 2px 2px 2px 0; position: relative; z-index: 1; }
  .chip-blue { background: rgba(37,99,235,0.2); color: var(--blue-light); border: 1px solid rgba(37,99,235,0.3); }
  .chip-purple { background: rgba(124,58,237,0.2); color: #c4b5fd; border: 1px solid rgba(124,58,237,0.3); }
  .chip-green { background: rgba(5,150,105,0.2); color: #6ee7b7; border: 1px solid rgba(5,150,105,0.3); }
  .chip-white { background: rgba(255,255,255,0.08); color: rgba(255,255,255,0.75); border: 1px solid rgba(255,255,255,0.1); }
  .hcard-contact { margin-top: 1.5rem; border-top: 1px solid rgba(255,255,255,0.1); padding-top: 1.25rem; position: relative; z-index: 1; }
  .hcard-contact p { font-size: 0.77rem; color: rgba(255,255,255,0.5); margin-bottom: 5px; }
  .hcard-contact a { color: var(--blue-light); text-decoration: none; font-weight: 500; }

  /* SECTIONS */
  section { padding: 6rem 2.5rem; }
  .section-label { font-size: 0.68rem; font-weight: 700; letter-spacing: 0.18em; text-transform: uppercase; color: var(--blue); margin-bottom: 0.5rem; display: block; }
  .section-title { font-family: 'Playfair Display', serif; font-size: clamp(1.75rem, 3vw, 2.6rem); font-weight: 900; line-height: 1.1; color: var(--ink); margin-bottom: 3rem; }
  .section-title em { font-style: italic; color: var(--purple); }

  /* ABOUT */
  #about { background: var(--ink); }
  #about .section-label { color: var(--blue-light); }
  #about .section-title { color: #fff; }
  #about .section-title em { color: var(--blue-light); }
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: start; }
  .about-text p { font-size: 0.93rem; line-height: 1.85; color: rgba(255,255,255,0.72); margin-bottom: 1rem; }
  .about-text strong { color: var(--blue-light); }
  .about-quote { border-left: 3px solid var(--blue); padding-left: 1.25rem; margin: 1.75rem 0; font-family: 'Playfair Display', serif; font-style: italic; font-size: 1.05rem; color: var(--blue-light); line-height: 1.5; }
  .awards-col { display: flex; flex-direction: column; gap: 0.85rem; }
  .award-item { background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08); border-radius: 10px; padding: 1rem 1.2rem; display: flex; align-items: flex-start; gap: 0.9rem; transition: border-color 0.2s; }
  .award-item:hover { border-color: rgba(37,99,235,0.4); }
  .award-em { font-size: 1.4rem; flex-shrink: 0; }
  .award-ttl { font-weight: 600; font-size: 0.85rem; color: var(--blue-light); margin-bottom: 2px; }
  .award-dsc { font-size: 0.76rem; color: rgba(255,255,255,0.5); line-height: 1.4; }

  /* EXPERIENCE */
  #experience { background: var(--paper); }
  .exp-wrap { max-width: 900px; margin: 0 auto; position: relative; }
  .exp-wrap::before { content: ''; position: absolute; left: 0; top: 0; bottom: 0; width: 2px; background: linear-gradient(to bottom, var(--blue), var(--purple), transparent); }
  .exp-block { padding-left: 2.5rem; padding-bottom: 3rem; position: relative; }
  .exp-dot { position: absolute; left: -8px; top: 5px; width: 18px; height: 18px; border-radius: 50%; background: var(--blue); border: 3px solid var(--paper); box-shadow: 0 0 0 3px rgba(37,99,235,0.25); }
  .exp-period { font-size: 0.7rem; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase; color: var(--blue); margin-bottom: 0.3rem; }
  .exp-role { font-family: 'Playfair Display', serif; font-size: 1.3rem; font-weight: 700; color: var(--ink); margin-bottom: 0.15rem; }
  .exp-co { font-size: 0.85rem; color: var(--purple); font-weight: 600; margin-bottom: 0.75rem; }
  .proj-cards { display: flex; flex-direction: column; gap: 0.75rem; margin-bottom: 1rem; }
  .proj-card { background: var(--card); border: 1px solid var(--border); border-radius: 8px; padding: 0.9rem 1.1rem; backdrop-filter: blur(4px); }
  .proj-name { font-size: 0.82rem; font-weight: 700; color: var(--blue); margin-bottom: 0.25rem; }
  .proj-desc { font-size: 0.78rem; color: var(--muted); line-height: 1.5; }
  .resp-list { list-style: none; display: flex; flex-direction: column; gap: 0.55rem; margin-top: 0.5rem; }
  .resp-list li { font-size: 0.85rem; color: var(--muted); line-height: 1.6; padding-left: 1.25rem; position: relative; }
  .resp-list li::before { content: '▸'; position: absolute; left: 0; color: var(--blue); font-weight: 700; }
  .resp-list li strong { color: var(--ink); }
  .tag-row { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 1rem; }
  .tag { font-size: 0.68rem; font-weight: 600; padding: 3px 9px; border-radius: 4px; background: var(--purple-light); color: var(--purple); border: 1px solid rgba(124,58,237,0.2); }

  /* SKILLS */
  #skills { background: #0f0f1a; }
  #skills .section-label { color: var(--blue-light); }
  #skills .section-title { color: #fff; }
  #skills .section-title em { color: #c4b5fd; }
  .skills-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.25rem; }
  .sg { background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.07); border-radius: 12px; padding: 1.4rem; transition: border-color 0.2s, transform 0.2s; }
  .sg:hover { border-color: rgba(37,99,235,0.35); transform: translateY(-4px); }
  .sg-title { font-size: 0.68rem; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; color: var(--blue-light); margin-bottom: 1rem; padding-bottom: 0.6rem; border-bottom: 1px solid rgba(255,255,255,0.07); }
  .sb-wrap { margin-bottom: 0.8rem; }
  .sb-top { display: flex; justify-content: space-between; margin-bottom: 4px; }
  .sb-name { font-size: 0.78rem; color: rgba(255,255,255,0.82); font-weight: 500; }
  .sb-pct { font-size: 0.7rem; color: rgba(255,255,255,0.35); }
  .sb-track { height: 4px; background: rgba(255,255,255,0.07); border-radius: 99px; overflow: hidden; }
  .sb-fill { height: 100%; border-radius: 99px; background: linear-gradient(90deg, var(--blue), var(--purple)); transform: scaleX(0); transform-origin: left; transition: transform 1.2s cubic-bezier(0.4,0,0.2,1); }
  .sb-fill.on { transform: scaleX(1); }

  /* ACHIEVEMENTS */
  #achievements { background: var(--paper); position: relative; overflow: hidden; }
  #achievements::before { content: ''; position: absolute; top: -100px; right: -100px; width: 400px; height: 400px; border-radius: 50%; background: rgba(124,58,237,0.05); pointer-events: none; }
  .ach-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.25rem; }
  .ach-card { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 1.6rem 1.4rem; position: relative; overflow: hidden; transition: all 0.2s; backdrop-filter: blur(4px); }
  .ach-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; background: linear-gradient(90deg, var(--blue), var(--purple)); }
  .ach-card:hover { transform: translateY(-4px); box-shadow: 0 16px 40px rgba(37,99,235,0.1); border-color: rgba(37,99,235,0.25); }
  .ach-ico { font-size: 2rem; margin-bottom: 0.85rem; display: block; }
  .ach-ttl { font-family: 'Playfair Display', serif; font-size: 0.95rem; font-weight: 700; color: var(--ink); margin-bottom: 0.35rem; }
  .ach-dsc { font-size: 0.78rem; color: var(--muted); line-height: 1.5; }
  .ach-yr { font-size: 0.68rem; font-weight: 700; letter-spacing: 0.1em; color: var(--blue); text-transform: uppercase; margin-top: 0.7rem; display: block; }

  /* EDUCATION */
  #education { background: var(--ink); }
  #education .section-label { color: var(--blue-light); }
  #education .section-title { color: #fff; }
  #education .section-title em { color: #c4b5fd; }
  .edu-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.25rem; }
  .edu-card { background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08); border-radius: 12px; padding: 1.5rem; transition: all 0.2s; }
  .edu-card:hover { border-color: rgba(37,99,235,0.35); transform: translateY(-4px); }
  .edu-deg { font-family: 'Playfair Display', serif; font-size: 0.95rem; font-weight: 700; color: var(--blue-light); margin-bottom: 0.3rem; }
  .edu-sch { font-size: 0.8rem; color: rgba(255,255,255,0.6); margin-bottom: 0.5rem; line-height: 1.4; }
  .edu-yr { font-size: 0.73rem; color: rgba(255,255,255,0.35); }
  .edu-score { display: inline-block; margin-top: 0.7rem; background: rgba(37,99,235,0.15); border: 1px solid rgba(37,99,235,0.25); color: var(--blue-light); font-size: 0.73rem; font-weight: 600; padding: 3px 10px; border-radius: 4px; }

  /* CONTACT */
  #contact { background: linear-gradient(135deg, #0a0a0f 0%, #1a1040 100%); text-align: center; padding: 7rem 2.5rem; }
  .contact-inner { max-width: 620px; margin: 0 auto; }
  .contact-h { font-family: 'Playfair Display', serif; font-size: clamp(1.8rem, 3.5vw, 3rem); font-weight: 900; color: #fff; margin-bottom: 1rem; line-height: 1.1; }
  .contact-h em { font-style: italic; color: var(--blue-light); }
  .contact-sub { font-size: 0.9rem; color: rgba(255,255,255,0.55); margin-bottom: 2.5rem; line-height: 1.7; }
  .contact-btns { display: flex; justify-content: center; gap: 1rem; flex-wrap: wrap; }
  .cbtn { display: inline-flex; align-items: center; gap: 8px; font-size: 0.8rem; font-weight: 600; letter-spacing: 0.06em; text-transform: uppercase; text-decoration: none; padding: 0.8rem 1.6rem; border-radius: 6px; transition: all 0.2s; }
  .cbtn-primary { background: var(--blue); color: #fff; }
  .cbtn-primary:hover { background: #1d4ed8; transform: translateY(-2px); box-shadow: 0 8px 24px rgba(37,99,235,0.4); }
  .cbtn-outline { color: rgba(255,255,255,0.8); border: 1.5px solid rgba(255,255,255,0.2); }
  .cbtn-outline:hover { background: rgba(255,255,255,0.08); transform: translateY(-2px); }

  /* FOOTER */
  footer { text-align: center; padding: 1.5rem; font-size: 0.72rem; color: var(--muted); border-top: 1px solid var(--border); background: var(--paper); letter-spacing: 0.05em; }

  /* ANIMATIONS */
  @keyframes fadeUp { from { opacity: 0; transform: translateY(22px); } to { opacity: 1; transform: translateY(0); } }
  @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
  .reveal { opacity: 0; transform: translateY(28px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  /* RESPONSIVE */
  @media (max-width: 768px) {
    #hero { grid-template-columns: 1fr; padding-top: 6rem; }
    .hero-right { display: none; }
    .about-grid, .skills-grid, .ach-grid, .edu-grid { grid-template-columns: 1fr; }
    nav { padding: 1rem 1.25rem; }
    .nav-links { gap: 0.85rem; }
    section { padding: 4rem 1.25rem; }
    #hero { padding: 6rem 1.25rem 3rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">VST <span>QA</span></div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#achievements">Awards</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg"></div>
  <div class="hero-dots"></div>
  <div class="hero-left">
    <span class="hero-badge">🧪 Open to QA opportunities · Hyderabad &amp; Bangalore</span>
    <h1 class="hero-name">Vaddadi<br><span>Sai Teja</span></h1>
    <p class="hero-title">Software Development Engineer in Test (SDET) · Verizon</p>
    <div class="hero-stats">
      <div class="stat"><div class="stat-val">3.5+</div><div class="stat-lab">Years exp.</div></div>
      <div class="stat"><div class="stat-val">5+</div><div class="stat-lab">Awards won</div></div>
      <div class="stat"><div class="stat-val">3</div><div class="stat-lab">Major migrations</div></div>
      <div class="stat"><div class="stat-val">SAFe</div><div class="stat-lab">SP5 certified</div></div>
    </div>
    <div class="hero-cta">
      <a href="#contact" class="btn-primary">Get in touch</a>
      <a href="#experience" class="btn-outline">View experience</a>
    </div>
  </div>
  <div class="hero-right">
    <div class="hero-card">
      <div class="hero-card-glow"></div>
      <div class="hero-card-glow2"></div>
      <p class="hero-card-title">Core Tech Stack</p>
      <div>
        <span class="chip chip-blue">Selenium WebDriver</span>
        <span class="chip chip-blue">Playwright</span>
        <span class="chip chip-blue">TestNG</span>
        <span class="chip chip-blue">Java</span>
        <span class="chip chip-purple">Jenkins CI/CD</span>
        <span class="chip chip-purple">Maven</span>
        <span class="chip chip-purple">JUnit</span>
        <span class="chip chip-purple">POM / BDD</span>
        <span class="chip chip-green">Postman API</span>
        <span class="chip chip-green">SQL</span>
        <span class="chip chip-green">JIRA / QTest</span>
        <span class="chip chip-white">Cucumber</span>
        <span class="chip chip-white">Git / GitHub</span>
        <span class="chip chip-white">SAFe Agile</span>
        <span class="chip chip-white">MCP Servers</span>
      </div>
      <div class="hcard-contact">
        <p>📍 Hyderabad, India</p>
        <p>📧 <a href="mailto:Saitejavaddadi3@gmail.com">Saitejavaddadi3@gmail.com</a></p>
        <p>📞 <a href="tel:+919398122881">+91-9398122881</a></p>
        <p>🔗 <a href="https://www.linkedin.com/in/sai-teja-vaddadi-623443210/" target="_blank">linkedin.com/in/sai-teja-vaddadi</a></p>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <span class="section-label">About me</span>
  <h2 class="section-title">Automating quality, <em>delivering reliability</em></h2>
  <div class="about-grid reveal">
    <div class="about-text">
      <p>I'm a <strong>Results-driven SDET</strong> with 3.5+ years at Verizon — one of the world's largest telecom companies. I design and build automation frameworks from the ground up, lead migration testing for enterprise-scale platforms, and ensure zero-defect deployments in Agile (SAFe) delivery environments.</p>
      <p>My expertise spans <strong>Selenium (Java), Playwright, API testing with Postman</strong>, and CI/CD pipeline integration with Jenkins — giving me a rare end-to-end view of the software quality lifecycle.</p>
      <blockquote class="about-quote">"Recognised for creating innovative QA tools using Playwright and MCP servers — including a Health &amp; Performance Check Tool and an Automation Defect Replication/Retest Tool."</blockquote>
      <p>I'm now seeking my next challenge as a <strong>Senior QA / SDET</strong> in Hyderabad or Bangalore where I can contribute to high-impact, quality-first engineering teams.</p>
    </div>
    <div class="awards-col">
      <div class="award-item"><span class="award-em">🌟</span><div><p class="award-ttl">Spotlight Award × 2 (2024)</p><p class="award-dsc">Recognised for accountability in CTI migration and ownership in React &amp; CXP migration initiatives.</p></div></div>
      <div class="award-item"><span class="award-em">🤝</span><div><p class="award-ttl">Cheers for Peers Award</p><p class="award-dsc">Appreciated by directors and leaders for fostering collaboration and strengthening team partnerships.</p></div></div>
      <div class="award-item"><span class="award-em">🏆</span><div><p class="award-ttl">Verizon Wall of Fame</p><p class="award-dsc">Featured for significant contributions to the Preloader migration effort at enterprise scale.</p></div></div>
      <div class="award-item"><span class="award-em">🚀</span><div><p class="award-ttl">Q3 AHM Recognition (2025)</p><p class="award-dsc">Acknowledged for driving results in the Adaptive Authentication Migration project delivery.</p></div></div>
      <div class="award-item"><span class="award-em">🛠️</span><div><p class="award-ttl">Innovation Recognition</p><p class="award-dsc">Recognised for building QA tools with Playwright &amp; MCP servers — Health Check &amp; Defect Retest tools.</p></div></div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <span class="section-label">Work experience</span>
  <h2 class="section-title">My professional <em>journey</em></h2>
  <div class="exp-wrap">
    <div class="exp-block reveal">
      <div class="exp-dot"></div>
      <p class="exp-period">Apr 2022 — Present · 3.5+ Years</p>
      <h3 class="exp-role">Software Development Engineer in Test — II</h3>
      <p class="exp-co">Verizon · Hyderabad</p>
      <div class="proj-cards">
        <div class="proj-card">
          <p class="proj-name">🔁 ACSS ESB → CXP Migration</p>
          <p class="proj-desc">Modernised the ACSS platform by transitioning backend services from legacy ESB architecture to the new Customer Experience Platform (CXP). Redesigned service interfaces, re-architected data flows, and implemented flag-based routing for phased rollout with full backward compatibility.</p>
        </div>
        <div class="proj-card">
          <p class="proj-name">📡 ACSS CTI Migration (WebSocket → SSE)</p>
          <p class="proj-desc">Migrated CTI communication from WebSockets to Server-Sent Events (SSE) — reducing bidirectional complexity, optimising server resource usage, and enabling scalable real-time event streaming for CTI interactions.</p>
        </div>
        <div class="proj-card">
          <p class="proj-name">🔐 Adaptive Authentication Migration (JS Plugins)</p>
          <p class="proj-desc">Upgraded the Adaptive Authentication module with updated JS plugins supporting modern security controls, improved risk-based evaluation, and enhanced browser compatibility.</p>
        </div>
      </div>
      <ul class="resp-list">
        <li>Analysed requirements and user stories to design <strong>effective test scenarios and test cases</strong>.</li>
        <li>Executed functional, regression, integration, system, and exploratory testing across enterprise platforms.</li>
        <li>Performed <strong>API testing with Postman</strong> and validated backend data integrity using SQL queries.</li>
        <li>Developed and maintained automation scripts using <strong>Selenium (Java), TestNG, Maven</strong>; enhanced POM, Hybrid, and Data-Driven frameworks.</li>
        <li>Automated regression suites reducing manual testing effort by 60%+; <strong>integrated with Jenkins CI/CD</strong>.</li>
        <li>Built innovative QA tools using <strong>Playwright and MCP servers</strong> — Health Check tool &amp; Defect Retest tool.</li>
        <li>Utilised <strong>Git/GitHub</strong> for version control, branching, and team collaboration across sprint cycles.</li>
        <li>Participated in <strong>SAFe Agile ceremonies</strong> (PI Planning, sprint stand-ups, QA reviews) ensuring timely delivery.</li>
        <li>Conducted root cause analysis to minimise recurring defects and maintained traceability documentation.</li>
      </ul>
      <div class="tag-row">
        <span class="tag">Selenium Java</span><span class="tag">Playwright</span><span class="tag">TestNG</span>
        <span class="tag">Jenkins</span><span class="tag">Postman</span><span class="tag">SQL</span>
        <span class="tag">JIRA</span><span class="tag">BDD / Cucumber</span><span class="tag">SAFe Agile</span>
        <span class="tag">POM</span><span class="tag">Maven</span><span class="tag">Git</span>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <span class="section-label">Technical skills</span>
  <h2 class="section-title">Tools &amp; <em>expertise</em></h2>
  <div class="skills-grid reveal">
    <div class="sg">
      <p class="sg-title">🧪 Automation</p>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">Selenium WebDriver (Java)</span><span class="sb-pct">95%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.95"></div></div></div>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">Playwright</span><span class="sb-pct">88%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.88"></div></div></div>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">TestNG / JUnit</span><span class="sb-pct">92%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.92"></div></div></div>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">Cucumber / BDD</span><span class="sb-pct">87%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.87"></div></div></div>
    </div>
    <div class="sg">
      <p class="sg-title">⚙️ CI/CD &amp; Dev Tools</p>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">Jenkins CI/CD</span><span class="sb-pct">88%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.88"></div></div></div>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">Maven</span><span class="sb-pct">90%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.90"></div></div></div>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">Git / GitHub</span><span class="sb-pct">88%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.88"></div></div></div>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">Eclipse / IntelliJ / VSCode</span><span class="sb-pct">90%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.90"></div></div></div>
    </div>
    <div class="sg">
      <p class="sg-title">🔍 Testing &amp; API</p>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">API Testing (Postman)</span><span class="sb-pct">90%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.90"></div></div></div>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">SQL / DB Testing</span><span class="sb-pct">82%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.82"></div></div></div>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">JIRA / QTest</span><span class="sb-pct">92%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.92"></div></div></div>
      <div class="sb-wrap"><div class="sb-top"><span class="sb-name">Java / Python</span><span class="sb-pct">85%</span></div><div class="sb-track"><div class="sb-fill" data-w="0.85"></div></div></div>
    </div>
  </div>
</section>

<!-- ACHIEVEMENTS -->
<section id="achievements">
  <span class="section-label">Recognition</span>
  <h2 class="section-title">Awards &amp; <em>milestones</em></h2>
  <div class="ach-grid reveal">
    <div class="ach-card"><span class="ach-ico">🌟</span><p class="ach-ttl">Spotlight Award — Accountability</p><p class="ach-dsc">Recognised for accountability and successful end-to-end execution of the CTI migration project at Verizon.</p><span class="ach-yr">2024 · Verizon</span></div>
    <div class="ach-card"><span class="ach-ico">🏅</span><p class="ach-ttl">Spotlight Award — Ownership</p><p class="ach-dsc">Honoured for ownership and measurable impact in delivering the React and CXP migration initiatives.</p><span class="ach-yr">2024 · Verizon</span></div>
    <div class="ach-card"><span class="ach-ico">🤝</span><p class="ach-ttl">Cheers for Peers Award</p><p class="ach-dsc">Appreciated by directors and leaders for fostering collaboration and strengthening cross-team partnerships.</p><span class="ach-yr">Verizon</span></div>
    <div class="ach-card"><span class="ach-ico">🏆</span><p class="ach-ttl">Verizon Wall of Fame</p><p class="ach-dsc">Featured on the Verizon Wall of Fame for significant contributions to the Preloader migration effort.</p><span class="ach-yr">Verizon</span></div>
    <div class="ach-card"><span class="ach-ico">🚀</span><p class="ach-ttl">Q3 AHM Recognition</p><p class="ach-dsc">Acknowledged for driving results and quality delivery in the Adaptive Authentication Migration project.</p><span class="ach-yr">2025 · Verizon</span></div>
    <div class="ach-card"><span class="ach-ico">🛠️</span><p class="ach-ttl">Innovation — QA Tools</p><p class="ach-dsc">Recognised for building innovative tools using Playwright &amp; MCP Servers: Health Check &amp; Defect Retest tool.</p><span class="ach-yr">Verizon</span></div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <span class="section-label">Education</span>
  <h2 class="section-title">Academic <em>background</em></h2>
  <div class="edu-grid reveal">
    <div class="edu-card"><p class="edu-deg">B.Tech — Electronics &amp; Communication</p><p class="edu-sch">Bhimavaram Institute of Engineering and Technology</p><p class="edu-yr">2017 – 2021</p><span class="edu-score">CGPA 7.17 / 10</span></div>
    <div class="edu-card"><p class="edu-deg">Intermediate — MPC</p><p class="edu-sch">Sri Chaitanya Junior College</p><p class="edu-yr">2015 – 2017</p><span class="edu-score">85%</span></div>
    <div class="edu-card"><p class="edu-deg">SSC — Secondary Education</p><p class="edu-sch">S.U.S Mpl High School</p><p class="edu-yr">2014 – 2015</p><span class="edu-score">CGPA 9.3 / 10</span></div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-inner reveal">
    <h2 class="contact-h">Let's build <em>quality</em> together</h2>
    <p class="contact-sub">I'm actively exploring Senior QA Engineer, SDET, and Test Automation Lead roles in Hyderabad and Bangalore. I respond within 24 hours — let's connect!</p>
    <div class="contact-btns">
      <a href="mailto:Saitejavaddadi3@gmail.com" class="cbtn cbtn-primary">✉ Email me</a>
      <a href="tel:+919398122881" class="cbtn cbtn-outline">📞 Call me</a>
      <a href="https://www.linkedin.com/in/sai-teja-vaddadi-623443210/" target="_blank" class="cbtn cbtn-outline">🔗 LinkedIn</a>
    </div>
  </div>
</section>

<footer>© 2026 Vaddadi Sai Teja · Hyderabad, India · QA Engineer · Verizon</footer>

<script>
const obs = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.classList.add('visible');
      e.target.querySelectorAll('.sb-fill').forEach(b => {
        b.style.transform = 'scaleX(' + b.getAttribute('data-w') + ')';
        b.classList.add('on');
      });
    }
  });
}, { threshold: 0.12 });
document.querySelectorAll('.reveal').forEach(el => obs.observe(el));
window.addEventListener('scroll', () => {
  const secs = document.querySelectorAll('section[id]');
  const links = document.querySelectorAll('.nav-links a');
  let cur = '';
  secs.forEach(s => { if (window.scrollY >= s.offsetTop - 120) cur = s.id; });
  links.forEach(a => { a.style.color = a.getAttribute('href') === '#'+cur ? 'var(--blue)' : ''; });
});
</script>
</body>
</html>
