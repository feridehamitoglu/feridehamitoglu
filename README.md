<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Feride Hamitoğlu — README</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #fdf8f5;
    --surface: #fff9f6;
    --border: #f0e6df;
    --accent: #d4896a;
    --accent2: #9b7fa6;
    --soft-pink: #f2cfc4;
    --soft-purple: #d9cfe8;
    --text: #3d2e28;
    --muted: #a8917f;
    --code-bg: #fef4ef;
    --green: #6a9e7f;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    padding: 60px 20px;
    background-image:
      radial-gradient(ellipse at 5% 10%, rgba(212,137,106,0.08) 0%, transparent 50%),
      radial-gradient(ellipse at 95% 90%, rgba(155,127,166,0.08) 0%, transparent 50%);
  }

  .card { width: 100%; max-width: 700px; }

  /* HEADER */
  .header {
    text-align: center;
    padding-bottom: 48px;
    animation: fadeUp 0.7s ease both;
  }

  .petal-ring {
    width: 64px;
    height: 64px;
    margin: 0 auto 20px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--soft-pink), var(--soft-purple));
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 26px;
    box-shadow: 0 8px 24px rgba(212,137,106,0.18);
  }

  h1 {
    font-family: 'DM Serif Display', serif;
    font-size: 2.8rem;
    font-weight: 400;
    color: var(--text);
    margin-bottom: 8px;
    letter-spacing: -0.01em;
  }

  h1 em {
    font-style: italic;
    color: var(--accent);
  }

  .subtitle {
    font-size: 0.8rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
    font-weight: 500;
    margin-bottom: 10px;
  }

  .tagline {
    font-size: 0.88rem;
    color: var(--muted);
    margin-bottom: 26px;
    font-style: italic;
  }

  .badges {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 18px;
    border-radius: 40px;
    font-size: 0.79rem;
    font-family: 'DM Mono', monospace;
    text-decoration: none;
    border: 1.5px solid var(--border);
    background: var(--surface);
    transition: all 0.22s ease;
    color: var(--muted);
    box-shadow: 0 2px 8px rgba(212,137,106,0.06);
  }

  .badge:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 18px rgba(212,137,106,0.14);
  }

  .badge.li:hover { border-color: #0A66C2; color: #0A66C2; }
  .badge.em:hover { border-color: var(--accent); color: var(--accent); }
  .badge svg { width: 13px; height: 13px; flex-shrink: 0; }

  /* SECTION */
  .section {
    padding: 30px 0;
    border-bottom: 1.5px solid var(--border);
    animation: fadeUp 0.7s ease both;
  }

  .section:last-child { border-bottom: none; }

  .section-header {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 20px;
  }

  .section-title {
    font-size: 0.68rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
    font-weight: 500;
    white-space: nowrap;
  }

  .section-line {
    flex: 1;
    height: 1.5px;
    background: var(--border);
    border-radius: 2px;
  }

  /* ABOUT */
  .about-list { display: flex; flex-direction: column; gap: 12px; }

  .about-item {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    font-size: 0.9rem;
    color: #7a6259;
    line-height: 1.65;
  }

  .about-item .ico { flex-shrink: 0; font-size: 1rem; margin-top: 1px; }
  .about-item strong { color: var(--text); font-weight: 500; }

  /* TECH STACK */
  .stack-rows { display: flex; flex-direction: column; gap: 14px; }
  .stack-row { display: flex; align-items: flex-start; gap: 16px; }

  .stack-key {
    font-family: 'DM Mono', monospace;
    font-size: 0.73rem;
    color: var(--accent2);
    min-width: 96px;
    flex-shrink: 0;
    padding-top: 5px;
  }

  .tags { display: flex; flex-wrap: wrap; gap: 7px; }

  .tag {
    padding: 4px 12px;
    background: var(--code-bg);
    border: 1.5px solid var(--border);
    border-radius: 20px;
    font-size: 0.77rem;
    font-family: 'DM Mono', monospace;
    color: #9a8075;
    transition: all 0.18s;
    cursor: default;
  }

  .tag:hover {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(212,137,106,0.06);
  }

  /* CODE BLOCK */
  .code-block {
    background: var(--code-bg);
    border: 1.5px solid var(--border);
    border-radius: 16px;
    overflow: hidden;
    box-shadow: 0 4px 16px rgba(212,137,106,0.06);
  }

  .code-topbar {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 10px 16px;
    background: #fef0ea;
    border-bottom: 1.5px solid var(--border);
  }

  .dot { width: 9px; height: 9px; border-radius: 50%; }
  .dot.r { background: #ffb5a3; }
  .dot.y { background: #ffd6a0; }
  .dot.g { background: #b5ddb5; }

  .code-filename {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
    margin-left: 8px;
  }

  pre {
    padding: 20px;
    font-family: 'DM Mono', monospace;
    font-size: 0.82rem;
    line-height: 1.75;
    overflow-x: auto;
    color: #7a6259;
  }

  .kw { color: var(--accent2); }
  .vr { color: var(--accent); }
  .st { color: var(--green); }
  .ky { color: #b07a9e; }

  /* PROJECTS */
  .project-list { display: flex; flex-direction: column; gap: 10px; }

  .project-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 14px 18px;
    background: var(--surface);
    border: 1.5px solid var(--border);
    border-radius: 14px;
    text-decoration: none;
    transition: all 0.2s;
    cursor: default;
    box-shadow: 0 2px 8px rgba(212,137,106,0.04);
  }

  .project-item:hover {
    border-color: var(--soft-pink);
    transform: translateX(5px);
    box-shadow: 0 4px 16px rgba(212,137,106,0.1);
  }

  .project-left { display: flex; align-items: center; gap: 12px; }
  .project-icon { font-size: 1.05rem; }
  .project-name { font-size: 0.88rem; color: var(--text); font-weight: 400; }

  .project-arrow {
    font-size: 0.75rem;
    color: var(--muted);
    font-family: 'DM Mono', monospace;
    opacity: 0.4;
  }

  /* CONTACT */
  .contact-list { display: flex; flex-direction: column; gap: 10px; }

  .contact-row {
    display: flex;
    align-items: center;
    gap: 14px;
    padding: 13px 18px;
    background: var(--surface);
    border: 1.5px solid var(--border);
    border-radius: 14px;
    text-decoration: none;
    transition: all 0.2s;
    box-shadow: 0 2px 8px rgba(212,137,106,0.04);
  }

  .contact-row:hover {
    border-color: var(--accent);
    transform: translateX(5px);
    box-shadow: 0 4px 16px rgba(212,137,106,0.1);
  }

  .contact-icon { font-size: 1.05rem; flex-shrink: 0; }
  .contact-info { display: flex; flex-direction: column; }

  .contact-platform {
    font-size: 0.66rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    color: var(--muted);
    font-family: 'DM Mono', monospace;
  }

  .contact-value {
    font-size: 0.84rem;
    color: var(--accent);
    font-family: 'DM Mono', monospace;
  }

  /* QUOTE */
  .quote {
    text-align: center;
    padding-top: 36px;
    font-family: 'DM Serif Display', serif;
    font-size: 1.05rem;
    color: var(--muted);
    font-style: italic;
  }

  .quote em { color: var(--accent); }

  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .header               { animation-delay: 0.00s; }
  .section:nth-child(1) { animation-delay: 0.08s; }
  .section:nth-child(2) { animation-delay: 0.16s; }
  .section:nth-child(3) { animation-delay: 0.24s; }
  .section:nth-child(4) { animation-delay: 0.32s; }
  .section:nth-child(5) { animation-delay: 0.40s; }
  .section:nth-child(6) { animation-delay: 0.48s; }
</style>
</head>
<body>
<div class="card">

  <!-- HEADER -->
  <div class="header">
    <div class="petal-ring">🌸</div>
    <h1>Hey, I'm <em>Feride</em> 👋</h1>
    <p class="subtitle">Junior Frontend Developer</p>
    <p class="tagline">HTML · CSS · React — building clean interfaces, one pixel at a time.</p>
    <div class="badges">
      <a href="https://www.linkedin.com/in/feride-hamito%C4%9Flu-0a6041387" target="_blank" class="badge li">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a href="mailto:feridegamidova1590@gmail.com" class="badge em">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 010 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.909 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
        Email
      </a>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-header">
      <span class="section-title">About Me</span>
      <div class="section-line"></div>
    </div>
    <div class="about-list">
      <div class="about-item"><span class="ico">🌱</span><span>Currently learning and improving my skills in <strong>React</strong> and <strong>JavaScript</strong></span></div>
      <div class="about-item"><span class="ico">💻</span><span>Passionate about building <strong>clean, responsive</strong> and user-friendly interfaces</span></div>
      <div class="about-item"><span class="ico">🔄</span><span>Career switcher from <strong>aviation & operations</strong> to software development</span></div>
      <div class="about-item"><span class="ico">🤝</span><span>Strong <strong>communication</strong> and problem-solving skills</span></div>
      <div class="about-item"><span class="ico">📧</span><span>Reach me at: <strong>feridegamidova1590@gmail.com</strong></span></div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-header">
      <span class="section-title">Tech Stack</span>
      <div class="section-line"></div>
    </div>
    <div class="stack-rows">
      <div class="stack-row">
        <span class="stack-key">frontend</span>
        <div class="tags">
          <span class="tag">HTML5</span>
          <span class="tag">CSS3</span>
          <span class="tag">Tailwind CSS</span>
          <span class="tag">JavaScript ES6+</span>
          <span class="tag">React</span>
        </div>
      </div>
      <div class="stack-row">
        <span class="stack-key">tools</span>
        <div class="tags">
          <span class="tag">Git</span>
          <span class="tag">GitHub</span>
          <span class="tag">VS Code</span>
        </div>
      </div>
      <div class="stack-row">
        <span class="stack-key">UI / UX</span>
        <div class="tags">
          <span class="tag">Responsive Design</span>
          <span class="tag">Flexbox</span>
          <span class="tag">CSS Grid</span>
        </div>
      </div>
    </div>
  </div>

  <!-- INTERESTS / CODE BLOCK -->
  <div class="section">
    <div class="section-header">
      <span class="section-title">Interests</span>
      <div class="section-line"></div>
    </div>
    <div class="code-block">
      <div class="code-topbar">
        <div class="dot r"></div>
        <div class="dot y"></div>
        <div class="dot g"></div>
        <span class="code-filename">feride.js</span>
      </div>
      <pre><span class="kw">const</span> <span class="vr">feride</span> = {
  <span class="ky">code</span>:       [<span class="st">"HTML5"</span>, <span class="st">"CSS3"</span>, <span class="st">"Tailwind CSS"</span>, <span class="st">"JavaScript"</span>, <span class="st">"React"</span>],
  <span class="ky">learning</span>:  [<span class="st">"React"</span>, <span class="st">"JavaScript"</span>],
  <span class="ky">languages</span>: [<span class="st">"Turkish 🇹🇷"</span>, <span class="st">"English 🇬🇧"</span>, <span class="st">"Russian 🇷🇺"</span>],
  <span class="ky">background</span>:[<span class="st">"Aviation ✈️"</span>, <span class="st">"Operations"</span>, <span class="st">"Customer Focus"</span>]
};</pre>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section">
    <div class="section-header">
      <span class="section-title">Projects</span>
      <div class="section-line"></div>
    </div>
    <div class="project-list">
      <div class="project-item">
        <div class="project-left"><span class="project-icon">🎨</span><span class="project-name">Responsive Web Interfaces</span></div>
        <span class="project-arrow">→</span>
      </div>
      <div class="project-item">
        <div class="project-left"><span class="project-icon">⚡</span><span class="project-name">Interactive JavaScript Features</span></div>
        <span class="project-arrow">→</span>
      </div>
      <div class="project-item">
        <div class="project-left"><span class="project-icon">⚛️</span><span class="project-name">Component-based React Apps</span></div>
        <span class="project-arrow">→</span>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-header">
      <span class="section-title">Connect</span>
      <div class="section-line"></div>
    </div>
    <div class="contact-list">
      <a href="https://www.linkedin.com/in/feride-hamito%C4%9Flu-0a6041387" target="_blank" class="contact-row">
        <span class="contact-icon">💼</span>
        <div class="contact-info">
          <span class="contact-platform">LinkedIn</span>
          <span class="contact-value">feride-hamitoğlu</span>
        </div>
      </a>
      <a href="mailto:feridegamidova1590@gmail.com" class="contact-row">
        <span class="contact-icon">✉️</span>
        <div class="contact-info">
          <span class="contact-platform">Email</span>
          <span class="contact-value">feridegamidova1590@gmail.com</span>
        </div>
      </a>
    </div>
  </div>

  <div class="quote">✈️ "<em>From the skies to the screen.</em>"</div>

</div>
</body>
</html>
