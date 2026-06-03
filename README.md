<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Siddhartha Majumder – GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0a0a0f;
    --surface: #111118;
    --card: #16161f;
    --border: rgba(255,255,255,0.07);
    --border-accent: rgba(99,102,241,0.4);
    --text: #f0f0f5;
    --muted: #8888aa;
    --accent: #6366f1;
    --accent2: #22d3ee;
    --accent3: #f59e0b;
    --accent4: #10b981;
    --red: #f43f5e;
    --mono: 'Space Mono', monospace;
    --sans: 'Syne', sans-serif;
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* HERO */
  .hero {
    position: relative;
    padding: 72px 48px 56px;
    border-bottom: 1px solid var(--border);
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -120px; left: -120px;
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(99,102,241,0.18) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero::after {
    content: '';
    position: absolute;
    bottom: -80px; right: -80px;
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(34,211,238,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: rgba(99,102,241,0.12);
    border: 1px solid rgba(99,102,241,0.3);
    color: #a5b4fc;
    font-family: var(--mono);
    font-size: 11px;
    letter-spacing: 0.08em;
    padding: 4px 12px;
    border-radius: 20px;
    margin-bottom: 20px;
  }
  .hero-badge span { width:7px; height:7px; border-radius:50%; background:#22d3ee; display:inline-block; animation: pulse 2s infinite; }
  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:.5;transform:scale(1.3)} }
  .hero h1 {
    font-size: clamp(36px, 5vw, 64px);
    font-weight: 800;
    letter-spacing: -0.02em;
    line-height: 1.05;
    margin-bottom: 16px;
  }
  .hero h1 .name-accent { color: var(--accent); }
  .hero-sub {
    font-family: var(--mono);
    font-size: 14px;
    color: var(--accent2);
    margin-bottom: 24px;
    letter-spacing: 0.05em;
  }
  .hero-desc { font-size: 16px; color: var(--muted); max-width: 560px; line-height: 1.7; margin-bottom: 32px; }
  .hero-links { display: flex; flex-wrap: wrap; gap: 12px; }
  .btn {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 10px 22px;
    border-radius: 8px;
    font-family: var(--mono);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.05em;
    text-decoration: none;
    transition: all 0.2s;
    cursor: pointer;
  }
  .btn-primary { background: var(--accent); color: #fff; border: 1px solid var(--accent); }
  .btn-primary:hover { background: #4f46e5; box-shadow: 0 0 20px rgba(99,102,241,0.4); }
  .btn-outline { background: transparent; color: var(--text); border: 1px solid var(--border-accent); }
  .btn-outline:hover { background: rgba(99,102,241,0.08); }
  .btn-cyan { background: transparent; color: var(--accent2); border: 1px solid rgba(34,211,238,0.3); }
  .btn-cyan:hover { background: rgba(34,211,238,0.08); }

  /* STAT BADGES */
  .stat-row {
    display: flex; flex-wrap: wrap; gap: 10px;
    padding: 28px 48px;
    border-bottom: 1px solid var(--border);
  }
  .stat-badge {
    display: flex; align-items: center; gap: 8px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 8px 14px;
    font-family: var(--mono);
    font-size: 12px;
    color: var(--muted);
  }
  .stat-badge img { height: 20px; }

  /* SECTION */
  .section { padding: 48px 48px 0; }
  .section-label {
    font-family: var(--mono);
    font-size: 11px;
    letter-spacing: 0.12em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 8px;
  }
  .section-title {
    font-size: 28px;
    font-weight: 800;
    letter-spacing: -0.02em;
    margin-bottom: 28px;
  }

  /* TECH STACK */
  .tech-grid {
    display: flex; flex-wrap: wrap; gap: 10px;
    margin-bottom: 48px;
  }
  .tech-chip {
    display: flex; align-items: center; gap: 8px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 8px 16px;
    font-size: 13px;
    font-weight: 600;
    transition: all 0.2s;
  }
  .tech-chip:hover { border-color: var(--border-accent); background: rgba(99,102,241,0.06); }
  .tech-chip .dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
  .dot-java { background: #f59e0b; }
  .dot-spring { background: #22c55e; }
  .dot-js { background: #facc15; }
  .dot-ts { background: #3b82f6; }
  .dot-nest { background: #e11d48; }
  .dot-react { background: #38bdf8; }
  .dot-mysql { background: #00758f; }
  .dot-git { background: #f97316; }
  .dot-post { background: #ef6c00; }
  .dot-dsa { background: #8b5cf6; }
  .dot-html { background: #f97316; }
  .dot-css { background: #2563eb; }

  /* PROJECTS */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 16px;
    margin-bottom: 48px;
  }
  .project-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 24px;
    transition: all 0.25s;
    position: relative;
    overflow: hidden;
  }
  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: var(--card-accent, var(--accent));
    opacity: 0;
    transition: opacity 0.25s;
  }
  .project-card:hover { border-color: rgba(99,102,241,0.25); transform: translateY(-2px); }
  .project-card:hover::before { opacity: 1; }
  .project-icon {
    font-size: 28px;
    margin-bottom: 14px;
    display: block;
  }
  .project-name {
    font-size: 16px;
    font-weight: 700;
    margin-bottom: 8px;
    display: flex; align-items: center; gap: 8px;
  }
  .project-type {
    font-family: var(--mono);
    font-size: 10px;
    padding: 2px 8px;
    border-radius: 4px;
    font-weight: 400;
  }
  .type-enterprise { background: rgba(99,102,241,0.15); color: #a5b4fc; }
  .type-algo { background: rgba(139,92,246,0.15); color: #c4b5fd; }
  .type-web { background: rgba(34,211,238,0.12); color: #67e8f9; }
  .type-mobile { background: rgba(16,185,129,0.15); color: #6ee7b7; }
  .project-desc { font-size: 13px; color: var(--muted); line-height: 1.6; margin-bottom: 16px; }
  .project-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 18px; }
  .tag {
    font-family: var(--mono);
    font-size: 10px;
    padding: 3px 9px;
    border-radius: 4px;
    background: rgba(255,255,255,0.05);
    color: var(--muted);
    border: 1px solid var(--border);
  }
  .project-links { display: flex; gap: 10px; }
  .project-link {
    font-family: var(--mono);
    font-size: 11px;
    padding: 6px 14px;
    border-radius: 6px;
    text-decoration: none;
    border: 1px solid var(--border);
    color: var(--text);
    transition: all 0.2s;
  }
  .project-link:hover { border-color: var(--border-accent); color: #a5b4fc; }
  .project-link.live { background: rgba(99,102,241,0.1); border-color: rgba(99,102,241,0.3); color: #a5b4fc; }

  /* STATS */
  .stats-row {
    display: flex; flex-wrap: wrap; gap: 16px;
    margin-bottom: 48px;
  }
  .stats-row img { border-radius: 8px; height: auto; }

  /* CURRENT */
  .current-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 12px;
    margin-bottom: 48px;
  }
  .current-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 18px 20px;
    display: flex; flex-direction: column; gap: 8px;
  }
  .current-card .cc-label { font-family: var(--mono); font-size: 10px; color: var(--muted); letter-spacing: 0.08em; }
  .current-card .cc-value { font-size: 15px; font-weight: 700; }
  .current-card .cc-value a { color: var(--accent2); text-decoration: none; }
  .current-card .cc-value a:hover { text-decoration: underline; }

  /* CODE BLOCK */
  .code-block {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 24px 28px;
    font-family: var(--mono);
    font-size: 13px;
    line-height: 1.8;
    margin-bottom: 48px;
    color: #c9d1d9;
    overflow-x: auto;
  }
  .code-kw { color: #ff7b72; }
  .code-fn { color: #d2a8ff; }
  .code-str { color: #a5d6ff; }
  .code-cm { color: #8b949e; }
  .code-num { color: #79c0ff; }

  /* TIMELINE */
  .timeline { display: flex; flex-direction: column; gap: 0; margin-bottom: 48px; }
  .tl-item { display: flex; gap: 20px; position: relative; }
  .tl-dot { width: 14px; height: 14px; border-radius: 50%; flex-shrink: 0; margin-top: 6px; box-shadow: 0 0 12px currentColor; }
  .tl-line {
    position: absolute;
    left: 6px; top: 22px;
    width: 2px;
    height: calc(100% + 8px);
    background: linear-gradient(to bottom, rgba(99,102,241,0.4), rgba(99,102,241,0.05));
  }
  .tl-body {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 22px 24px;
    margin-bottom: 16px;
    flex: 1;
    transition: border-color 0.2s;
  }
  .tl-body:hover { border-color: rgba(99,102,241,0.3); }
  .tl-header { display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: 8px; margin-bottom: 12px; }
  .tl-role { font-size: 16px; font-weight: 700; color: var(--text); }
  .tl-company { font-size: 14px; color: var(--muted); margin-left: 6px; }
  .tl-company a { color: var(--accent2); text-decoration: none; }
  .tl-company a:hover { text-decoration: underline; }
  .tl-period {
    font-family: var(--mono);
    font-size: 11px;
    padding: 4px 12px;
    border-radius: 20px;
    background: rgba(99,102,241,0.1);
    border: 1px solid rgba(99,102,241,0.25);
    color: #a5b4fc;
    white-space: nowrap;
  }
  .tl-desc { font-size: 13px; color: var(--muted); line-height: 1.65; margin-bottom: 14px; }
  .tl-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 16px; }
  .tl-achievements { display: flex; flex-direction: column; gap: 8px; }
  .tl-ach { display: flex; align-items: flex-start; gap: 10px; font-size: 13px; color: var(--muted); line-height: 1.5; }
  .tl-ach strong { color: var(--text); font-weight: 600; }
  .tl-ach-icon { font-size: 14px; flex-shrink: 0; margin-top: 1px; }


  .connect-grid {
    display: flex; flex-wrap: wrap; gap: 12px;
    margin-bottom: 48px;
  }
  .social-btn {
    display: inline-flex; align-items: center; gap: 10px;
    padding: 12px 20px;
    border-radius: 8px;
    background: var(--card);
    border: 1px solid var(--border);
    text-decoration: none;
    color: var(--text);
    font-size: 14px;
    font-weight: 600;
    transition: all 0.2s;
  }
  .social-btn:hover { transform: translateY(-2px); }
  .social-btn svg { width: 20px; height: 20px; flex-shrink: 0; }
  .social-btn.linkedin:hover { border-color: #0077b5; color: #0077b5; }
  .social-btn.github:hover { border-color: #6e40c9; color: #a5b4fc; }
  .social-btn.email:hover { border-color: var(--accent3); color: var(--accent3); }
  .social-btn.playstore:hover { border-color: var(--accent4); color: var(--accent4); }

  /* SPOTIFY */
  .spotify-wrap {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 20px;
    margin-bottom: 48px;
    display: inline-block;
  }
  .spotify-wrap img { border-radius: 8px; display: block; }

  /* FOOTER */
  .footer {
    padding: 32px 48px;
    border-top: 1px solid var(--border);
    display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 16px;
    margin-top: 16px;
  }
  .footer-text { font-family: var(--mono); font-size: 12px; color: var(--muted); }
  .footer-text span { color: var(--accent); }

  @media (max-width: 700px) {
    .hero, .section, .stat-row, .footer { padding-left: 24px; padding-right: 24px; }
    .hero h1 { font-size: 32px; }
    .stats-row { flex-direction: column; }
    .stats-row img { width: 100% !important; }
  }
</style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <div class="hero-badge"><span></span> 1+ YEAR EXPERIENCE · OPEN TO OPPORTUNITIES</div>
  <h1>Hi 👋 I'm<br><span class="name-accent">Siddhartha Majumder</span></h1>
  <p class="hero-sub">// SOFTWARE ENGINEER · 1+ YR · BACKEND · FULLSTACK</p>
  <p class="hero-desc">
    Software engineer with <strong style="color:var(--accent2)">1+ year of hands-on experience</strong> building enterprise-grade applications — scalable Spring Boot backends, RESTful APIs, ERP, POS, eCommerce, and EdTech platforms. Currently at <strong style="color:var(--text)">WebAppsSoft</strong>.
  </p>
  <div class="hero-links">
    <a class="btn btn-primary" href="https://docs.google.com" target="_blank">📄 Resume</a>
    <a class="btn btn-outline" href="mailto:siddhartha191122@gmail.com">✉ Email Me</a>
    <a class="btn btn-cyan" href="https://play.google.com/store/apps/details?id=com.swc_application&hl=en_IN" target="_blank">📱 SWC App</a>
  </div>
</section>

<!-- BADGES -->
<div class="stat-row">
  <div class="stat-badge">
    <img src="https://badges.pufler.dev/repos/Sid200402" alt="Repos"/>
  </div>
  <div class="stat-badge">
    <img src="https://badges.pufler.dev/commits/monthly/Sid200402" alt="Commits"/>
  </div>
  <div class="stat-badge">
    <img src="https://img.shields.io/github/followers/Sid200402?label=Followers&style=flat-square&color=6366f1&labelColor=111118&logo=github" alt="Followers"/>
  </div>
  <div class="stat-badge">
    <img src="https://img.shields.io/badge/experience-1%2B%20year-6366f1?style=flat-square&labelColor=111118" alt="Experience"/>
  </div>
  <div class="stat-badge">
    <img src="https://img.shields.io/badge/webappssoft-currently%20working-22d3ee?style=flat-square&labelColor=111118" alt="Work"/>
  </div>
</div>

<!-- WHAT I'M UP TO -->
<section class="section">
  <p class="section-label">// STATUS</p>
  <h2 class="section-title">What I'm Up To</h2>
  <div class="current-grid">
    <div class="current-card">
      <span class="cc-label">⏱ EXPERIENCE</span>
      <span class="cc-value" style="color:#f59e0b">1+ Year Professional</span>
    </div>
    <div class="current-card">
      <span class="cc-label">🏢 CURRENTLY AT</span>
      <span class="cc-value"><a href="https://webappssoft.com/" target="_blank">WebAppsSoft</a></span>
    </div>
    <div class="current-card">
      <span class="cc-label">📚 LEARNING</span>
      <span class="cc-value" style="color:#22c55e">Spring Boot · Microservices</span>
    </div>
    <div class="current-card">
      <span class="cc-label">🏗️ BUILDING</span>
      <span class="cc-value" style="color:#f59e0b">ERP · POS · EdTech · eCommerce</span>
    </div>
    <div class="current-card">
      <span class="cc-label">📫 CONTACT</span>
      <span class="cc-value"><a href="mailto:siddhartha191122@gmail.com">siddhartha191122@gmail.com</a></span>
    </div>
  </div>
</section>

<!-- EXPERIENCE TIMELINE -->
<section class="section">
  <p class="section-label">// WORK HISTORY</p>
  <h2 class="section-title">Experience</h2>
  <div class="timeline">

    <div class="tl-item">
      <div class="tl-dot" style="background:var(--accent)"></div>
      <div class="tl-line"></div>
      <div class="tl-body">
        <div class="tl-header">
          <div>
            <span class="tl-role">Software Engineer</span>
            <span class="tl-company">@ <a href="https://webappssoft.com/" target="_blank">WebAppsSoft</a></span>
          </div>
          <span class="tl-period">2023 – Present · 1+ yr</span>
        </div>
        <p class="tl-desc">Working as a full-stack software engineer building enterprise products — ERP, POS, eCommerce, and EdTech platforms. Responsible for backend API design, database modelling, and frontend integration.</p>
        <div class="tl-tags">
          <span class="tag">Spring Boot</span>
          <span class="tag">Java</span>
          <span class="tag">NestJS</span>
          <span class="tag">TypeScript</span>
          <span class="tag">MySQL</span>
          <span class="tag">REST APIs</span>
          <span class="tag">JPA / Hibernate</span>
        </div>
        <div class="tl-achievements">
          <div class="tl-ach"><span class="tl-ach-icon">🏭</span><span>Designed and developed <strong>ERP modules</strong> — HR, payroll, inventory & procurement</span></div>
          <div class="tl-ach"><span class="tl-ach-icon">🛒</span><span>Built end-to-end <strong>POS system</strong> with billing, GST, inventory & sales analytics</span></div>
          <div class="tl-ach"><span class="tl-ach-icon">🛍️</span><span>Developed <strong>eCommerce platform</strong> with cart, checkout, payments & admin dashboard</span></div>
          <div class="tl-ach"><span class="tl-ach-icon">🎓</span><span>Contributed to <strong>SWC EdTech app</strong> — 500+ downloads on Play Store</span></div>
        </div>
      </div>
    </div>

    <div class="tl-item">
      <div class="tl-dot" style="background:var(--accent2)"></div>
      <div class="tl-body">
        <div class="tl-header">
          <div>
            <span class="tl-role">Software Engineering Intern</span>
            <span class="tl-company">@ <a href="https://webappssoft.com/" target="_blank">WebAppsSoft</a></span>
          </div>
          <span class="tl-period">2023 · 6 months</span>
        </div>
        <p class="tl-desc">Started as an intern learning enterprise development practices. Worked on REST API development, database design, and frontend integration with real-world production systems.</p>
        <div class="tl-tags">
          <span class="tag">Java</span>
          <span class="tag">Spring Boot</span>
          <span class="tag">MySQL</span>
          <span class="tag">JavaScript</span>
          <span class="tag">Git</span>
        </div>
        <div class="tl-achievements">
          <div class="tl-ach"><span class="tl-ach-icon">⚡</span><span>Developed and tested <strong>CRUD REST APIs</strong> for core business modules</span></div>
          <div class="tl-ach"><span class="tl-ach-icon">🗄️</span><span>Designed relational <strong>database schemas</strong> for inventory and billing features</span></div>
          <div class="tl-ach"><span class="tl-ach-icon">🔧</span><span>Collaborated with senior devs on <strong>code reviews</strong> and agile sprints</span></div>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- TECH STACK -->
<section class="section">
  <p class="section-label">// TOOLS & LANGUAGES</p>
  <h2 class="section-title">Tech Stack</h2>
  <div class="tech-grid">
    <div class="tech-chip"><span class="dot dot-java"></span>Java</div>
    <div class="tech-chip"><span class="dot dot-spring"></span>Spring Boot</div>
    <div class="tech-chip"><span class="dot dot-spring"></span>Spring MVC</div>
    <div class="tech-chip"><span class="dot dot-spring"></span>Hibernate / JPA</div>
    <div class="tech-chip"><span class="dot dot-dsa"></span>DSA (Java)</div>
    <div class="tech-chip"><span class="dot dot-js"></span>JavaScript</div>
    <div class="tech-chip"><span class="dot dot-ts"></span>TypeScript</div>
    <div class="tech-chip"><span class="dot dot-nest"></span>NestJS</div>
    <div class="tech-chip"><span class="dot dot-react"></span>React</div>
    <div class="tech-chip"><span class="dot dot-html"></span>HTML5</div>
    <div class="tech-chip"><span class="dot dot-css"></span>CSS3</div>
    <div class="tech-chip"><span class="dot dot-mysql"></span>MySQL</div>
    <div class="tech-chip"><span class="dot dot-post"></span>Postman</div>
    <div class="tech-chip"><span class="dot dot-git"></span>Git / GitHub</div>
    <div class="tech-chip"><span class="dot dot-post"></span>TypeORM</div>
    <div class="tech-chip"><span class="dot dot-react"></span>REST APIs</div>
  </div>
</section>

<!-- PROJECTS -->
<section class="section">
  <p class="section-label">// PORTFOLIO</p>
  <h2 class="section-title">Featured Projects</h2>
  <div class="projects-grid">

    <!-- SWC Education Platform -->
    <div class="project-card" style="--card-accent: #22d3ee">
      <span class="project-icon">🎓</span>
      <div class="project-name">
        SWC Education Platform
        <span class="project-type type-mobile">EdTech · Mobile</span>
      </div>
      <p class="project-desc">All-in-one competitive exam prep app with video lectures, PDF study material, mock tests, quizzes, and real-time learning analytics. Built for SWC Learning Solutions.</p>
      <div class="project-tags">
        <span class="tag">Android</span>
        <span class="tag">Education</span>
        <span class="tag">Video Lectures</span>
        <span class="tag">PDF Books</span>
        <span class="tag">Mock Tests</span>
      </div>
      <div class="project-links">
        <a class="project-link live" href="https://play.google.com/store/apps/details?id=com.swc_application&hl=en_IN" target="_blank">▶ Play Store</a>
        <a class="project-link" href="https://swcapp.in" target="_blank">🌐 Website</a>
      </div>
    </div>

    <!-- ERP System -->
    <div class="project-card" style="--card-accent: #6366f1">
      <span class="project-icon">🏭</span>
      <div class="project-name">
        ERP System
        <span class="project-type type-enterprise">Enterprise</span>
      </div>
      <p class="project-desc">Full-featured Enterprise Resource Planning system covering HR, payroll, inventory, procurement, and reporting — built with Spring Boot backend and RESTful APIs.</p>
      <div class="project-tags">
        <span class="tag">Spring Boot</span>
        <span class="tag">Java</span>
        <span class="tag">MySQL</span>
        <span class="tag">REST API</span>
        <span class="tag">JPA</span>
      </div>
      <div class="project-links">
        <a class="project-link" href="https://webappssoft.com/" target="_blank">🏢 WebAppsSoft</a>
      </div>
    </div>

    <!-- POS System -->
    <div class="project-card" style="--card-accent: #f59e0b">
      <span class="project-icon">🛒</span>
      <div class="project-name">
        POS – Point of Sale
        <span class="project-type type-enterprise">Enterprise</span>
      </div>
      <p class="project-desc">Comprehensive Point of Sale solution with inventory management, billing, discounts, GST/tax handling, customer management, and real-time sales reports.</p>
      <div class="project-tags">
        <span class="tag">Spring Boot</span>
        <span class="tag">Java</span>
        <span class="tag">MySQL</span>
        <span class="tag">Billing</span>
        <span class="tag">Inventory</span>
      </div>
      <div class="project-links">
        <a class="project-link" href="https://webappssoft.com/" target="_blank">🏢 WebAppsSoft</a>
      </div>
    </div>

    <!-- eCommerce Platform -->
    <div class="project-card" style="--card-accent: #10b981">
      <span class="project-icon">🛍️</span>
      <div class="project-name">
        eCommerce Platform
        <span class="project-type type-web">Web App</span>
      </div>
      <p class="project-desc">Scalable eCommerce platform with product catalog, cart, checkout, order management, payment gateway integration, and admin dashboard for store management.</p>
      <div class="project-tags">
        <span class="tag">Spring Boot</span>
        <span class="tag">NestJS</span>
        <span class="tag">React</span>
        <span class="tag">MySQL</span>
        <span class="tag">REST API</span>
      </div>
      <div class="project-links">
        <a class="project-link" href="https://webappssoft.com/" target="_blank">🏢 WebAppsSoft</a>
      </div>
    </div>

    <!-- DSA in Java -->
    <div class="project-card" style="--card-accent: #8b5cf6">
      <span class="project-icon">🧮</span>
      <div class="project-name">
        DSA in Java
        <span class="project-type type-algo">Algorithms</span>
      </div>
      <p class="project-desc">Comprehensive Data Structures & Algorithms implementations in Java — arrays, linked lists, trees, graphs, sorting, searching, dynamic programming, and competitive coding problems.</p>
      <div class="project-tags">
        <span class="tag">Java</span>
        <span class="tag">DSA</span>
        <span class="tag">LeetCode</span>
        <span class="tag">OOP</span>
        <span class="tag">CP</span>
      </div>
      <div class="project-links">
        <a class="project-link" href="https://github.com/Sid200402" target="_blank">📂 GitHub</a>
      </div>
    </div>

    <!-- Spring Boot Projects -->
    <div class="project-card" style="--card-accent: #22c55e">
      <span class="project-icon">🍃</span>
      <div class="project-name">
        Spring Boot Projects
        <span class="project-type type-enterprise">Backend</span>
      </div>
      <p class="project-desc">Collection of Spring Boot microservices and REST API projects — CRUD APIs, JWT authentication, Spring Security, pagination, and database integration patterns.</p>
      <div class="project-tags">
        <span class="tag">Spring Boot</span>
        <span class="tag">Spring Security</span>
        <span class="tag">JWT</span>
        <span class="tag">Hibernate</span>
        <span class="tag">Maven</span>
      </div>
      <div class="project-links">
        <a class="project-link" href="https://github.com/Sid200402" target="_blank">📂 GitHub</a>
      </div>
    </div>

    <!-- Movie A-Z -->
    <div class="project-card" style="--card-accent: #f43f5e">
      <span class="project-icon">🎬</span>
      <div class="project-name">
        Movie A-Z
        <span class="project-type type-web">Web App</span>
      </div>
      <p class="project-desc">Browse, search, and discover movies using the TMDb API — features filtering by genre, rating, and release year with a clean responsive UI.</p>
      <div class="project-tags">
        <span class="tag">React</span>
        <span class="tag">TMDb API</span>
        <span class="tag">JavaScript</span>
        <span class="tag">CSS</span>
      </div>
      <div class="project-links">
        <a class="project-link live" href="https://movie-a-z.vercel.app/" target="_blank">🌐 Live Demo</a>
        <a class="project-link" href="https://github.com/Sid200402/movieA_Z" target="_blank">📂 Repo</a>
      </div>
    </div>

    <!-- QR Code Generator -->
    <div class="project-card" style="--card-accent: #38bdf8">
      <span class="project-icon">📱</span>
      <div class="project-name">
        QR Code Generator
        <span class="project-type type-web">Web App</span>
      </div>
      <p class="project-desc">Lightweight QR code generator that converts URLs, text, and contact info into downloadable QR codes instantly — built with vanilla JS.</p>
      <div class="project-tags">
        <span class="tag">JavaScript</span>
        <span class="tag">HTML5</span>
        <span class="tag">CSS3</span>
      </div>
      <div class="project-links">
        <a class="project-link" href="https://github.com/Sid200402/QR_code_Generator" target="_blank">📂 Repo</a>
      </div>
    </div>

  </div>
</section>

<!-- GITHUB STATS -->
<section class="section">
  <p class="section-label">// METRICS</p>
  <h2 class="section-title">GitHub Stats</h2>
  <div class="stats-row">
    <img src="https://github-readme-stats.vercel.app/api?username=Sid200402&show_icons=true&theme=midnight-purple&hide_border=true&bg_color=16161f&title_color=6366f1&icon_color=22d3ee&text_color=c9d1d9" width="48%" alt="GitHub Stats"/>
    <img src="https://github-readme-streak-stats.herokuapp.com/?user=Sid200402&theme=midnight-purple&hide_border=true&background=16161f&ring=6366f1&fire=f59e0b&currStreakLabel=22d3ee" width="48%" alt="GitHub Streak"/>
  </div>
  <div style="margin-bottom:48px">
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sid200402&layout=compact&theme=midnight-purple&hide_border=true&bg_color=16161f&title_color=6366f1&text_color=c9d1d9" width="48%" alt="Top Languages"/>
  </div>
</section>

<!-- FUN FACT / CODE BLOCK -->
<section class="section">
  <p class="section-label">// FUN FACT</p>
  <h2 class="section-title">The Developer Loop</h2>
  <div class="code-block">
<span class="code-cm">// siddhartha.java — the algorithm that runs 24/7</span>

<span class="code-kw">public class</span> <span class="code-fn">Siddhartha</span> <span class="code-kw">extends</span> <span class="code-fn">SoftwareEngineer</span> {

  <span class="code-kw">private</span> <span class="code-fn">int</span> yearsOfExperience = <span class="code-num">1</span>; <span class="code-cm">// and counting 🚀</span>
  <span class="code-kw">private</span> <span class="code-fn">String</span> currentRole = <span class="code-str">"Software Engineer @ WebAppsSoft"</span>;
  <span class="code-kw">private</span> <span class="code-fn">String</span>[] learning = { <span class="code-str">"Spring Boot"</span>, <span class="code-str">"Microservices"</span>, <span class="code-str">"DSA"</span> };
  <span class="code-kw">private</span> <span class="code-fn">boolean</span> isAlive = <span class="code-kw">true</span>;

  <span class="code-kw">public void</span> <span class="code-fn">main</span>() {
    <span class="code-kw">while</span> (isAlive) {
      <span class="code-fn">code</span>();         <span class="code-cm">// Spring Boot + Java + DSA</span>
      <span class="code-fn">buildProjects</span>(); <span class="code-cm">// ERP, POS, eComm, EdTech</span>
      <span class="code-fn">eat</span>();
      <span class="code-fn">sleep</span>(<span class="code-num">6</span>);       <span class="code-cm">// sometimes less ☕</span>
      <span class="code-fn">repeat</span>();
    }
  }
}</div>
</section>

<!-- CONNECT -->
<section class="section">
  <p class="section-label">// REACH ME</p>
  <h2 class="section-title">Connect With Me</h2>
  <div class="connect-grid">

    <a class="social-btn linkedin" href="https://linkedin.com/in/Siddhartha" target="_blank">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      LinkedIn
    </a>

    <a class="social-btn github" href="https://github.com/Sid200402" target="_blank">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
      GitHub
    </a>

    <a class="social-btn email" href="mailto:siddhartha191122@gmail.com">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
      Email
    </a>

    <a class="social-btn" href="https://stackoverflow.com/users/Siddhartha" target="_blank" style="border-color:rgba(244,130,48,0.3)">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M15.725 0l-1.72 1.277 6.39 8.588 1.716-1.277L15.725 0zm-3.94 3.418l-1.369 1.644 8.225 6.85 1.369-1.644-8.225-6.85zm-3.15 4.465l-.905 1.94 9.702 4.517.904-1.94-9.701-4.517zm-1.85 4.86l-.44 2.093 10.473 2.201.44-2.092-10.473-2.203zM1.89 15.47V24h19.19v-8.53h-2.133v6.397H4.021v-6.396H1.89zm4.265 2.133v2.13h10.66v-2.13H6.154Z"/></svg>
      Stack Overflow
    </a>

    <a class="social-btn" href="https://dev.to/Siddhartha" target="_blank" style="border-color:rgba(99,102,241,0.3)">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M7.42 10.05c-.18-.16-.46-.23-.84-.23H6l.02 2.44.04 2.45.56-.02c.41 0 .63-.07.83-.26.24-.24.26-.36.26-2.2 0-1.91-.02-1.96-.29-2.18zM0 4.94v14.12h24V4.94H0zM8.56 15.3c-.44.58-1.06.77-2.53.77H4.71V8.53h1.4c1.67 0 2.16.18 2.6.9.27.43.29.6.32 2.57.05 2.23-.02 2.73-.47 3.3zm5.09-5.47h-2.47v1.77h1.52v1.28l-.72.04-.75.03v1.77l1.22.03 1.2.04v1.28h-1.6c-1.53 0-1.6-.01-1.87-.3l-.3-.28v-3.16c0-3.02.01-3.18.25-3.48.23-.31.25-.31 1.88-.31h1.64v1.29zm4.68 5.45c-.17.43-.64.79-1 .79-.18 0-.45-.15-.67-.39-.32-.32-.45-.63-.82-2.08l-.9-3.39-.45-1.67h.76c.4 0 .75.02.75.05 0 .06 1.16 4.54 1.26 4.83.04.15.32-.7.73-2.3l.66-2.52.74-.04c.4-.02.74 0 .74.04 0 .14-1.67 6.38-1.8 6.68z"/></svg>
      Dev.to
    </a>
  </div>
</section>

<!-- SPOTIFY -->
<section class="section">
  <p class="section-label">// VIBES</p>
  <h2 class="section-title">Currently Listening To</h2>
  <div class="spotify-wrap">
    <img src="https://spotify-github-profile.vercel.app/api/view?uid=31kddq562obttiavkttuprpplbxy&cover_image=true&theme=natemoo-re&bar_color_cover=true" alt="Spotify Now Playing"/>
  </div>
</section>

<!-- FOOTER -->
<footer class="footer">
  <span class="footer-text">Built with <span>♥</span> by Siddhartha Majumder · <span>@Sid200402</span></span>
  <span class="footer-text">© 2025 · <a href="https://webappssoft.com/" target="_blank" style="color:var(--accent);text-decoration:none">sid</a></span>
</footer>

</body>
</html>
