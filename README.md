<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Md. Sadman Sakib — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #060b14;
    --surface: #0d1825;
    --card: #101e2e;
    --border: #1a3050;
    --accent: #00d4ff;
    --accent2: #ff6b35;
    --accent3: #7fff7f;
    --text: #c8dff0;
    --muted: #4a6a8a;
    --glow: rgba(0, 212, 255, 0.15);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Animated grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 50px 50px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 60px 24px;
    position: relative;
    z-index: 1;
  }

  /* ---- HERO ---- */
  .hero {
    text-align: center;
    margin-bottom: 64px;
    position: relative;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -40px; left: 50%;
    transform: translateX(-50%);
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(0,212,255,0.07) 0%, transparent 70%);
    pointer-events: none;
  }

  .badge {
    display: inline-block;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--accent);
    border: 1px solid var(--border);
    padding: 6px 16px;
    border-radius: 2px;
    margin-bottom: 24px;
    animation: fadeDown 0.6s ease both;
  }
  .badge::before { content: '> '; opacity: 0.5; }

  .hero h1 {
    font-size: clamp(2.2rem, 6vw, 3.8rem);
    font-weight: 800;
    line-height: 1.1;
    letter-spacing: -1px;
    animation: fadeDown 0.6s 0.1s ease both;
    margin-bottom: 8px;
  }

  .hero h1 .highlight {
    color: var(--accent);
    position: relative;
  }
  .hero h1 .highlight::after {
    content: '';
    position: absolute;
    bottom: -2px; left: 0; right: 0;
    height: 2px;
    background: var(--accent);
    box-shadow: 0 0 12px var(--accent);
  }

  .hero .role {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    color: var(--muted);
    letter-spacing: 2px;
    margin-top: 16px;
    animation: fadeDown 0.6s 0.2s ease both;
  }
  .hero .role span {
    color: var(--accent2);
    font-weight: 700;
  }

  .hero .views-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    border: 1px solid var(--border);
    padding: 5px 12px;
    border-radius: 2px;
    margin-top: 20px;
    animation: fadeDown 0.6s 0.3s ease both;
  }
  .views-badge .dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--accent3);
    box-shadow: 0 0 8px var(--accent3);
    animation: pulse 2s infinite;
  }

  /* ---- TERMINAL CARD ---- */
  .terminal {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    margin-bottom: 32px;
    overflow: hidden;
    animation: fadeUp 0.6s 0.3s ease both;
  }
  .terminal-bar {
    background: var(--surface);
    padding: 10px 16px;
    display: flex;
    align-items: center;
    gap: 8px;
    border-bottom: 1px solid var(--border);
  }
  .terminal-bar .dot { width: 10px; height: 10px; border-radius: 50%; }
  .terminal-bar .dot:nth-child(1) { background: #ff5f57; }
  .terminal-bar .dot:nth-child(2) { background: #febc2e; }
  .terminal-bar .dot:nth-child(3) { background: #28c840; }
  .terminal-bar .title {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    margin-left: 8px;
    letter-spacing: 1px;
  }
  .terminal-body {
    padding: 24px;
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    line-height: 2;
  }
  .terminal-body .line { display: flex; gap: 12px; flex-wrap: wrap; }
  .terminal-body .prompt { color: var(--accent); }
  .terminal-body .cmd { color: var(--accent3); }
  .terminal-body .val { color: var(--text); }
  .terminal-body .link { color: var(--accent2); text-decoration: none; border-bottom: 1px solid transparent; transition: border-color 0.2s; }
  .terminal-body .link:hover { border-color: var(--accent2); }
  .terminal-body .comment { color: var(--muted); }

  /* ---- SECTION HEADER ---- */
  .section-header {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 24px;
    margin-top: 48px;
  }
  .section-header h2 {
    font-size: 11px;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
  }
  .section-header::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }
  .section-header .num {
    color: var(--accent);
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    margin-right: -8px;
  }

  /* ---- SKILL GRID ---- */
  .skill-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(64px, 1fr));
    gap: 12px;
    animation: fadeUp 0.6s 0.4s ease both;
  }

  .skill-item {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 14px 8px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    transition: all 0.25s ease;
    cursor: default;
  }
  .skill-item:hover {
    border-color: var(--accent);
    background: rgba(0, 212, 255, 0.05);
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(0,212,255,0.1);
  }
  .skill-item img { width: 32px; height: 32px; object-fit: contain; filter: brightness(0.9); transition: filter 0.2s; }
  .skill-item:hover img { filter: brightness(1.2); }
  .skill-item span {
    font-family: 'Space Mono', monospace;
    font-size: 9px;
    color: var(--muted);
    text-align: center;
    letter-spacing: 0.5px;
  }

  /* ---- STATS ---- */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    animation: fadeUp 0.6s 0.5s ease both;
  }
  @media (max-width: 600px) { .stats-grid { grid-template-columns: 1fr; } }

  .stats-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    overflow: hidden;
    transition: border-color 0.2s;
  }
  .stats-card:hover { border-color: var(--accent); }
  .stats-card img {
    width: 100%;
    display: block;
    border-radius: 0;
    filter: hue-rotate(0deg);
  }
  .stats-card.full { grid-column: 1 / -1; }

  /* ---- CONNECT ---- */
  .connect-row {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
    animation: fadeUp 0.6s 0.5s ease both;
  }
  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 12px 20px;
    text-decoration: none;
    color: var(--text);
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    transition: all 0.25s ease;
    letter-spacing: 1px;
  }
  .connect-btn:hover {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(0, 212, 255, 0.05);
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(0,212,255,0.1);
  }
  .connect-btn svg { width: 18px; height: 18px; fill: currentColor; }
  .connect-btn.fb:hover { border-color: #4267B2; color: #4267B2; background: rgba(66,103,178,0.05); box-shadow: 0 6px 20px rgba(66,103,178,0.1); }

  /* ---- STATUS CHIPS ---- */
  .status-row {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    margin-bottom: 48px;
    animation: fadeUp 0.6s 0.35s ease both;
  }
  .chip {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    border: 1px solid var(--border);
    padding: 7px 14px;
    border-radius: 2px;
  }
  .chip .icon { font-size: 14px; }
  .chip a { color: var(--accent2); text-decoration: none; }
  .chip a:hover { text-decoration: underline; }
  .chip.learning { border-color: rgba(127,255,127,0.2); }
  .chip.learning .icon { color: var(--accent3); }
  .chip.working { border-color: rgba(0,212,255,0.2); }
  .chip.working .icon { color: var(--accent); }
  .chip.contact { border-color: rgba(255,107,53,0.2); }
  .chip.contact .icon { color: var(--accent2); }

  /* ---- FOOTER ---- */
  .footer {
    margin-top: 72px;
    padding-top: 24px;
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: gap;
    gap: 8px;
  }
  .footer span {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--muted);
  }
  .footer .accent { color: var(--accent); }

  /* ---- ANIMATIONS ---- */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-16px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }
  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }

  .cursor {
    display: inline-block;
    width: 8px; height: 14px;
    background: var(--accent);
    vertical-align: middle;
    margin-left: 4px;
    animation: blink 1s infinite;
  }
</style>
</head>
<body>

<div class="container">

  <!-- HERO -->
  <div class="hero">
    <div class="badge">Full Stack Developer</div>
    <h1>Md. <span class="highlight">Sadman</span> Sakib</h1>
    <p class="role">Passionate <span>Laravel</span> Engineer · PHP · JavaScript · MySQL</p>
    <div class="views-badge">
      <span class="dot"></span>
      <span>Open to collaborations</span>
    </div>
  </div>

  <!-- STATUS CHIPS -->
  <div class="status-row">
    <div class="chip working">
      <span class="icon">🔭</span>
      <span>Working on <a href="https://samadhan24.com/" target="_blank">Samadhan</a></span>
    </div>
    <div class="chip learning">
      <span class="icon">🌱</span>
      <span>Learning Python · Vue · React</span>
    </div>
    <div class="chip contact">
      <span class="icon">📫</span>
      <a href="mailto:saadman0000@gmail.com">saadman0000@gmail.com</a>
    </div>
  </div>

  <!-- TERMINAL -->
  <div class="terminal">
    <div class="terminal-bar">
      <div class="dot"></div><div class="dot"></div><div class="dot"></div>
      <span class="title">sadman@portfolio ~ whoami</span>
    </div>
    <div class="terminal-body">
      <div class="line">
        <span class="prompt">$</span>
        <span class="cmd">cat</span>
        <span class="val">about.json</span>
      </div>
      <div class="line" style="margin-top:8px; padding-left:16px;">
        <span class="comment"># name:</span>
        <span class="val">"Md. Sadman Sakib"</span>
      </div>
      <div class="line" style="padding-left:16px;">
        <span class="comment"># role:</span>
        <span class="val">"Full Stack Laravel Developer"</span>
      </div>
      <div class="line" style="padding-left:16px;">
        <span class="comment"># ask_me_about:</span>
        <span style="color:var(--accent3);">"Laravel, PHP, MySQL, APIs"</span>
      </div>
      <div class="line" style="padding-left:16px;">
        <span class="comment"># currently_building:</span>
        <a href="https://samadhan24.com/" class="link" target="_blank">"https://samadhan24.com"</a>
      </div>
      <div class="line" style="padding-left:16px;">
        <span class="comment"># learning_next:</span>
        <span style="color:var(--accent2);">["Python", "Vue.js", "React"]</span>
      </div>
      <div class="line" style="margin-top:8px;">
        <span class="prompt">$</span><span class="cursor"></span>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section-header">
    <span class="num">01</span>
    <h2>Connect</h2>
  </div>
  <div class="connect-row">
    <a href="https://linkedin.com/in/md-sadman-sakib-661641154" target="_blank" class="connect-btn">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      LinkedIn
    </a>
    <a href="https://www.facebook.com/s.sakib.47" target="_blank" class="connect-btn fb">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/></svg>
      Facebook
    </a>
    <a href="mailto:saadman0000@gmail.com" class="connect-btn">
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
      Email
    </a>
  </div>

  <!-- SKILLS -->
  <div class="section-header">
    <span class="num">02</span>
    <h2>Languages &amp; Tools</h2>
  </div>
  <div class="skill-grid">
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/laravel/laravel-plain-wordmark.svg" alt="Laravel">
      <span>Laravel</span>
    </div>
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="PHP">
      <span>PHP</span>
    </div>
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL">
      <span>MySQL</span>
    </div>
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="JavaScript">
      <span>JS</span>
    </div>
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vuejs/vuejs-original-wordmark.svg" alt="Vue.js">
      <span>Vue.js</span>
    </div>
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="HTML5">
      <span>HTML5</span>
    </div>
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="CSS3">
      <span>CSS3</span>
    </div>
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain-wordmark.svg" alt="Bootstrap">
      <span>Bootstrap</span>
    </div>
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="Docker">
      <span>Docker</span>
    </div>
    <div class="skill-item">
      <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="Git">
      <span>Git</span>
    </div>
    <div class="skill-item">
      <img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" alt="Postman">
      <span>Postman</span>
    </div>
    <div class="skill-item">
      <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="Firebase">
      <span>Firebase</span>
    </div>
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="Linux">
      <span>Linux</span>
    </div>
    <div class="skill-item">
      <img src="https://www.vectorlogo.zone/logos/figma/figma-icon.svg" alt="Figma">
      <span>Figma</span>
    </div>
    <div class="skill-item">
      <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="TensorFlow">
      <span>TF</span>
    </div>
    <div class="skill-item">
      <img src="https://cdn.worldvectorlogo.com/logos/arduino-1.svg" alt="Arduino">
      <span>Arduino</span>
    </div>
    <div class="skill-item">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="Java">
      <span>Java</span>
    </div>
    <div class="skill-item">
      <img src="https://www.vectorlogo.zone/logos/adobe_illustrator/adobe_illustrator-icon.svg" alt="Illustrator">
      <span>Ai</span>
    </div>
  </div>

  <!-- STATS -->
  <div class="section-header">
    <span class="num">03</span>
    <h2>GitHub Stats</h2>
  </div>
  <div class="stats-grid">
    <div class="stats-card">
      <img src="https://github-readme-stats.vercel.app/api/top-langs?username=sakib9644&show_icons=true&locale=en&layout=compact&theme=transparent&title_color=00d4ff&text_color=c8dff0&border_color=1a3050&bg_color=101e2e&hide_border=false" alt="Top Languages">
    </div>
    <div class="stats-card">
      <img src="https://github-readme-stats.vercel.app/api?username=sakib9644&show_icons=true&locale=en&theme=transparent&title_color=00d4ff&text_color=c8dff0&icon_color=ff6b35&border_color=1a3050&bg_color=101e2e" alt="GitHub Stats">
    </div>
    <div class="stats-card full">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=sakib9644&theme=transparent&title_color=00d4ff&ring=00d4ff&fire=ff6b35&currStreakLabel=c8dff0&sideLabels=c8dff0&dates=4a6a8a&border=1a3050&background=101e2e" alt="GitHub Streak">
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <span>// <span class="accent">sakib9644</span> · GitHub Profile</span>
    <span>Made with <span class="accent">♥</span> &amp; Laravel</span>
  </div>

</div>
</body>
</html>
