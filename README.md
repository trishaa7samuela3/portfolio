# portfolio
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Trishaa Samuela T | Strategic Research Analyst</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
–bg: #0B1622;
–surface: #122030;
–surface2: #1A2E45;
–border: #1E3A55;
–gold: #C8972F;
–gold-light: #E5B852;
–gold-faint: rgba(200, 151, 47, 0.08);
–text: #EDF2F7;
–text-muted: #7A9BB8;
–text-dim: #3A5A75;
–green: #4ADE80;
–blue: #60A5FA;
–font-display: ‘Space Grotesk’, system-ui, sans-serif;
–font-body: ‘DM Sans’, system-ui, sans-serif;
–font-mono: ‘JetBrains Mono’, ‘Courier New’, monospace;
}

html { scroll-behavior: smooth; }

body {
background: var(–bg);
color: var(–text);
font-family: var(–font-body);
font-size: 16px;
line-height: 1.65;
overflow-x: hidden;
}

/* ── NAV ── */
nav {
position: fixed; top: 0; left: 0; right: 0; z-index: 100;
display: flex; align-items: center; justify-content: space-between;
padding: 1rem 2.5rem;
background: rgba(11, 22, 34, 0.88);
backdrop-filter: blur(14px);
border-bottom: 1px solid var(–border);
}
.nav-logo {
font-family: var(–font-mono); font-size: 0.8rem;
color: var(–gold); letter-spacing: 0.12em;
}
.nav-links { display: flex; gap: 2rem; list-style: none; }
.nav-links a {
color: var(–text-muted); text-decoration: none;
font-size: 0.85rem; font-weight: 500; letter-spacing: 0.03em;
transition: color 0.2s;
}
.nav-links a:hover { color: var(–text); }

/* ── HERO ── */
#hero {
min-height: 100vh; display: flex; align-items: center;
max-width: 100%; padding: 0; position: relative; overflow: hidden;
}
.hero-bg {
position: absolute; inset: 0;
background:
radial-gradient(ellipse 55% 55% at 72% 50%, rgba(200,151,47,0.07) 0%, transparent 65%),
radial-gradient(ellipse 35% 50% at 18% 30%, rgba(96,165,250,0.04) 0%, transparent 60%);
}
.hero-grid {
position: absolute; inset: 0;
background-image:
linear-gradient(var(–border) 1px, transparent 1px),
linear-gradient(90deg, var(–border) 1px, transparent 1px);
background-size: 60px 60px; opacity: 0.25;
}
.hero-inner {
max-width: 1100px; margin: 0 auto;
padding: 9rem 2rem 5rem;
display: grid; grid-template-columns: 1fr 1fr;
gap: 4rem; align-items: center;
width: 100%; position: relative;
}
.hero-eyebrow {
font-family: var(–font-mono); font-size: 0.75rem;
color: var(–gold); letter-spacing: 0.2em; text-transform: uppercase;
margin-bottom: 1.5rem; display: flex; align-items: center; gap: 0.75rem;
}
.hero-eyebrow::before {
content: ‘’; display: block; width: 2rem; height: 1px; background: var(–gold);
}
.hero-name {
font-family: var(–font-display);
font-size: clamp(2.6rem, 5.5vw, 4.2rem);
font-weight: 700; line-height: 1.04;
letter-spacing: -0.025em; margin-bottom: 1.5rem;
}
.hero-name span { color: var(–gold); }
.hero-desc {
font-size: 1.05rem; color: var(–text-muted);
line-height: 1.75; margin-bottom: 2rem; max-width: 460px;
}
.hero-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-bottom: 2.5rem; }
.htag {
font-family: var(–font-mono); font-size: 0.7rem;
color: var(–text-muted); background: var(–surface);
border: 1px solid var(–border); padding: 0.28rem 0.7rem;
border-radius: 2px; letter-spacing: 0.04em;
}
.hero-cta { display: flex; gap: 1rem; flex-wrap: wrap; }
.btn-primary {
background: var(–gold); color: #0B1622;
padding: 0.75rem 1.75rem; font-family: var(–font-display);
font-weight: 600; font-size: 0.88rem; border: none; cursor: pointer;
text-decoration: none; display: inline-block;
transition: background 0.2s, transform 0.15s; border-radius: 2px; letter-spacing: 0.02em;
}
.btn-primary:hover { background: var(–gold-light); transform: translateY(-1px); }
.btn-outline {
background: transparent; color: var(–text-muted);
padding: 0.75rem 1.75rem; font-family: var(–font-display);
font-weight: 500; font-size: 0.88rem;
border: 1px solid var(–border); cursor: pointer;
text-decoration: none; display: inline-block;
transition: color 0.2s, border-color 0.2s, transform 0.15s; border-radius: 2px;
}
.btn-outline:hover { color: var(–text); border-color: var(–text-muted); transform: translateY(-1px); }

.hero-visual {
position: relative; height: 430px;
display: flex; align-items: center; justify-content: center;
}

/* ── MARQUEE ── */
.marquee-wrap {
overflow: hidden;
background: rgba(200,151,47,0.07);
border-top: 1px solid rgba(200,151,47,0.18);
border-bottom: 1px solid rgba(200,151,47,0.18);
padding: 0.8rem 0;
}
.marquee-track {
display: flex; gap: 2.5rem;
animation: marquee 28s linear infinite; width: max-content;
}
.marquee-track:hover { animation-play-state: paused; }
.mitem {
font-family: var(–font-mono); font-size: 0.72rem;
color: var(–gold); letter-spacing: 0.12em; text-transform: uppercase;
white-space: nowrap; display: flex; align-items: center; gap: 0.75rem;
}
.mitem::after { content: ‘◆’; font-size: 0.45rem; opacity: 0.45; }
@keyframes marquee {
from { transform: translateX(0); } to { transform: translateX(-50%); }
}

/* ── STATS BAND ── */
.stats-band {
background: var(–surface);
border-top: 1px solid var(–border);
border-bottom: 1px solid var(–border);
padding: 2.5rem 2rem;
}
.stats-inner {
max-width: 1100px; margin: 0 auto;
display: grid; grid-template-columns: repeat(4,1fr); gap: 1rem;
}
.stat-item {
text-align: center; padding: 1.25rem;
border-right: 1px solid var(–border);
}
.stat-item:last-child { border-right: none; }
.stat-number {
font-family: var(–font-display); font-size: 2.6rem;
font-weight: 700; color: var(–gold); line-height: 1; margin-bottom: 0.5rem;
}
.stat-label { font-size: 0.82rem; color: var(–text-muted); line-height: 1.45; }

/* ── SECTIONS ── */
section {
max-width: 1100px; margin: 0 auto; padding: 5rem 2rem;
}
.section-label {
font-family: var(–font-mono); font-size: 0.72rem;
color: var(–gold); letter-spacing: 0.18em; text-transform: uppercase; margin-bottom: 0.75rem;
}
h2 {
font-family: var(–font-display); font-size: 2rem;
font-weight: 600; color: var(–text); margin-bottom: 2.5rem; line-height: 1.2;
}
.section-divider { border-top: 1px solid var(–border); }

/* ── EXPERTISE CARDS ── */
.expertise-grid {
display: grid; grid-template-columns: repeat(3,1fr); gap: 1.5rem;
}
.expertise-card {
background: var(–surface); border: 1px solid var(–border);
padding: 1.75rem; border-radius: 3px;
transition: border-color 0.25s, transform 0.2s; position: relative; overflow: hidden;
}
.expertise-card::after {
content: ‘’; position: absolute; top: 0; left: 0; right: 0; height: 2px;
background: var(–gold); transform: scaleX(0); transform-origin: left;
transition: transform 0.3s;
}
.expertise-card:hover::after { transform: scaleX(1); }
.expertise-card:hover { border-color: rgba(200,151,47,0.5); transform: translateY(-2px); }
.card-icon { font-size: 1.4rem; margin-bottom: 1rem; }
.card-title {
font-family: var(–font-display); font-size: 0.95rem;
font-weight: 600; color: var(–text); margin-bottom: 0.5rem;
}
.card-desc { font-size: 0.855rem; color: var(–text-muted); line-height: 1.65; }

/* ── EXPERIENCE ── */
.exp-timeline { position: relative; padding-left: 2.25rem; }
.exp-timeline::before {
content: ‘’; position: absolute; left: 0; top: 0.6rem; bottom: 0; width: 1px;
background: linear-gradient(to bottom, var(–gold), var(–border) 70%, transparent);
}
.exp-item { position: relative; margin-bottom: 3rem; }
.exp-dot {
position: absolute; left: -2.6rem; top: 0.55rem;
width: 9px; height: 9px; border-radius: 50%; background: var(–gold);
border: 2px solid var(–bg); box-shadow: 0 0 0 3px rgba(200,151,47,0.2);
}
.exp-header {
display: flex; justify-content: space-between;
align-items: flex-start; margin-bottom: 0.4rem; flex-wrap: wrap; gap: 0.4rem;
}
.exp-role {
font-family: var(–font-display); font-size: 1.05rem;
font-weight: 600; color: var(–text);
}
.exp-company { font-size: 0.88rem; color: var(–gold); font-weight: 500; margin-top: 0.15rem; }
.exp-date {
font-family: var(–font-mono); font-size: 0.72rem;
color: var(–text-dim); letter-spacing: 0.05em;
}
.exp-bullets { list-style: none; margin-top: 1rem; }
.exp-bullets li {
font-size: 0.875rem; color: var(–text-muted); line-height: 1.65;
margin-bottom: 0.55rem; padding-left: 1.3rem; position: relative;
}
.exp-bullets li::before {
content: ‘→’; position: absolute; left: 0;
color: var(–gold); font-size: 0.7rem; top: 0.25rem;
}
.hi { color: var(–green); font-family: var(–font-mono); font-size: 0.85em; font-weight: 500; }

/* ── PROJECTS ── */
.projects-grid { display: grid; grid-template-columns: repeat(2,1fr); gap: 1.5rem; }
.project-card {
background: var(–surface); border: 1px solid var(–border);
padding: 2rem; border-radius: 3px; transition: border-color 0.2s;
}
.project-card.featured {
grid-column: span 2; display: grid;
grid-template-columns: 1fr 1fr; gap: 2rem;
}
.project-card:hover { border-color: rgba(200,151,47,0.4); }
.project-type {
font-family: var(–font-mono); font-size: 0.68rem; letter-spacing: 0.12em;
color: var(–gold); text-transform: uppercase; margin-bottom: 0.75rem;
}
.project-title {
font-family: var(–font-display); font-size: 1.15rem;
font-weight: 600; color: var(–text); margin-bottom: 0.75rem; line-height: 1.3;
}
.project-desc {
font-size: 0.865rem; color: var(–text-muted);
line-height: 1.68; margin-bottom: 1.25rem;
}
.pill-row { display: flex; flex-wrap: wrap; gap: 0.4rem; }
.pill {
font-family: var(–font-mono); font-size: 0.68rem;
color: var(–text-dim); background: rgba(30,58,85,0.4);
border: 1px solid var(–border); padding: 0.2rem 0.6rem; border-radius: 2px;
}
.impact-box {
background: var(–bg); border: 1px solid var(–border);
border-radius: 3px; padding: 1.1rem; display: flex; flex-direction: column; gap: 1rem;
}
.impact-label {
font-family: var(–font-mono); font-size: 0.65rem; color: var(–text-dim);
text-transform: uppercase; letter-spacing: 0.12em; margin-bottom: 0.35rem;
}
.impact-val { font-size: 0.855rem; color: var(–text-muted); }
.impact-val.green { color: var(–green); }

/* ── SKILLS ── */
.skills-layout { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; }
.skill-group-title {
font-family: var(–font-display); font-size: 0.8rem; font-weight: 600;
color: var(–text-muted); text-transform: uppercase; letter-spacing: 0.1em;
margin-bottom: 0.85rem; padding-bottom: 0.5rem; border-bottom: 1px solid var(–border);
margin-top: 1.75rem;
}
.skill-group-title:first-child { margin-top: 0; }
.stags { display: flex; flex-wrap: wrap; gap: 0.45rem; }
.stag {
font-size: 0.8rem; color: var(–text-muted); background: var(–surface);
border: 1px solid var(–border); padding: 0.3rem 0.8rem;
border-radius: 3px; transition: color 0.18s, border-color 0.18s;
}
.stag:hover { color: var(–text); border-color: var(–gold); }
.stag.p { color: var(–gold); border-color: rgba(200,151,47,0.35); background: var(–gold-faint); }

/* ── CONTACT ── */
.contact-box {
text-align: center; background: var(–surface);
border: 1px solid var(–border); border-radius: 6px;
padding: 4.5rem 2rem; position: relative; overflow: hidden;
}
.contact-box::before {
content: ‘’; position: absolute; top: 0; left: 50%; transform: translateX(-50%);
width: 45%; height: 1px;
background: linear-gradient(to right, transparent, var(–gold), transparent);
}
.contact-title {
font-family: var(–font-display); font-size: 1.9rem;
font-weight: 700; margin-bottom: 0.85rem;
}
.contact-sub {
color: var(–text-muted); margin-bottom: 2.25rem;
max-width: 440px; margin-left: auto; margin-right: auto; font-size: 0.95rem;
}
.contact-links { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; }
.contact-item {
display: flex; align-items: center; gap: 0.55rem;
color: var(–text-muted); font-size: 0.875rem; text-decoration: none;
transition: color 0.2s, border-color 0.2s;
padding: 0.55rem 1.1rem; border: 1px solid var(–border); border-radius: 3px;
}
.contact-item:hover { color: var(–gold); border-color: var(–gold); }

/* ── FOOTER ── */
footer {
text-align: center; padding: 2rem;
border-top: 1px solid var(–border);
font-family: var(–font-mono); font-size: 0.7rem; color: var(–text-dim);
}

/* ── SCROLL FADE ── */
.fi { opacity: 0; transform: translateY(22px); transition: opacity 0.6s ease, transform 0.6s ease; }
.fi.vis { opacity: 1; transform: translateY(0); }
.fi:nth-child(2) { transition-delay: 0.07s; }
.fi:nth-child(3) { transition-delay: 0.14s; }
.fi:nth-child(4) { transition-delay: 0.21s; }
.fi:nth-child(5) { transition-delay: 0.28s; }
.fi:nth-child(6) { transition-delay: 0.35s; }

/* ── RESPONSIVE ── */
@media (max-width: 900px) {
.hero-inner { grid-template-columns: 1fr; }
.hero-visual { display: none; }
.expertise-grid { grid-template-columns: repeat(2,1fr); }
.projects-grid { grid-template-columns: 1fr; }
.project-card.featured { grid-column: span 1; grid-template-columns: 1fr; }
.skills-layout { grid-template-columns: 1fr; }
}
@media (max-width: 600px) {
nav { padding: 0.9rem 1.25rem; }
.nav-links { gap: 1rem; }
.nav-links li:nth-child(4), .nav-links li:nth-child(5) { display: none; }
.stats-inner { grid-template-columns: repeat(2,1fr); }
.stat-item:nth-child(2) { border-right: none; }
.expertise-grid { grid-template-columns: 1fr; }
}
</style>

</head>
<body>

<!-- NAV -->

<nav>
  <div class="nav-logo">TST // STRATEGIC RESEARCH</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Work</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- ── HERO ── -->

<section id="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-inner">
    <div>
      <div class="hero-eyebrow">Strategic Research Analyst</div>
      <h1 class="hero-name">Trishaa<br>Samuela <span>T.</span></h1>
      <p class="hero-desc">
        Market intelligence that earns boardroom trust. Eight country-level reports. Ten-plus competitors decoded. Five emerging B2B export markets mapped — all delivered into live executive strategy within one year.
      </p>
      <div class="hero-tags">
        <span class="htag">MENA Markets</span>
        <span class="htag">South Asia</span>
        <span class="htag">Competitive Intelligence</span>
        <span class="htag">B2B Export Research</span>
        <span class="htag">Go-To-Market Strategy</span>
      </div>
      <div class="hero-cta">
        <a href="mailto:trishaatsamuela@gmail.com" class="btn-primary">Get in Touch</a>
        <a href="https://linkedin.com/in/trishaa-samuelat/" target="_blank" class="btn-outline">LinkedIn ↗</a>
      </div>
    </div>

```
<!-- ANIMATED INTELLIGENCE MAP -->
<div class="hero-visual">
  <svg viewBox="0 0 400 360" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" style="max-width:430px;" aria-hidden="true">
    <defs>
      <pattern id="dotgrid" x="0" y="0" width="18" height="18" patternUnits="userSpaceOnUse">
        <circle cx="9" cy="9" r="0.9" fill="#1E3A55" opacity="0.9"/>
      </pattern>
      <radialGradient id="gGold" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stop-color="#C8972F" stop-opacity="0.5"/>
        <stop offset="100%" stop-color="#C8972F" stop-opacity="0"/>
      </radialGradient>
      <radialGradient id="gBlue" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stop-color="#60A5FA" stop-opacity="0.45"/>
        <stop offset="100%" stop-color="#60A5FA" stop-opacity="0"/>
      </radialGradient>
      <filter id="blur3"><feGaussianBlur stdDeviation="4"/></filter>
    </defs>

    <rect width="400" height="360" fill="url(#dotgrid)"/>

    <!-- Glow halos -->
    <circle cx="196" cy="180" r="32" fill="url(#gGold)" filter="url(#blur3)"/>
    <circle cx="278" cy="228" r="22" fill="url(#gBlue)" filter="url(#blur3)" opacity="0.7"/>

    <!-- Connection lines from HQ -->
    <g opacity="0.35" stroke-dasharray="3,4">
      <line x1="196" y1="180" x2="148" y2="140" stroke="#C8972F" stroke-width="0.6"/>
      <line x1="196" y1="180" x2="100" y2="160" stroke="#C8972F" stroke-width="0.6"/>
      <line x1="196" y1="180" x2="248" y2="128" stroke="#C8972F" stroke-width="0.6"/>
      <line x1="196" y1="180" x2="310" y2="148" stroke="#C8972F" stroke-width="0.6"/>
      <line x1="196" y1="180" x2="322" y2="196" stroke="#C8972F" stroke-width="0.6"/>
      <line x1="196" y1="180" x2="278" y2="228" stroke="#60A5FA" stroke-width="0.6"/>
      <!-- Cross links -->
      <line x1="248" y1="128" x2="310" y2="148" stroke="#C8972F" stroke-width="0.3" opacity="0.5"/>
      <line x1="310" y1="148" x2="322" y2="196" stroke="#C8972F" stroke-width="0.3" opacity="0.5"/>
      <line x1="148" y1="140" x2="248" y2="128" stroke="#C8972F" stroke-width="0.3" opacity="0.5"/>
      <line x1="100" y1="160" x2="148" y2="140" stroke="#C8972F" stroke-width="0.3" opacity="0.5"/>
    </g>

    <!-- ALGERIA -->
    <g transform="translate(148,140)">
      <circle r="20" fill="rgba(200,151,47,0.09)" stroke="#C8972F" stroke-width="0.7"/>
      <circle r="4.5" fill="#C8972F"/>
      <circle r="4.5" fill="#C8972F" opacity="0.35">
        <animate attributeName="r" values="4.5;14;4.5" dur="3.2s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.35;0;0.35" dur="3.2s" repeatCount="indefinite"/>
      </circle>
      <text y="32" text-anchor="middle" font-family="JetBrains Mono, monospace" font-size="8" fill="#C8972F" letter-spacing="0.06em">DZA</text>
    </g>

    <!-- MOROCCO -->
    <g transform="translate(100,160)">
      <circle r="16" fill="rgba(200,151,47,0.07)" stroke="#C8972F" stroke-width="0.5" opacity="0.75"/>
      <circle r="3.5" fill="#C8972F" opacity="0.9"/>
      <circle r="3.5" fill="#C8972F" opacity="0.25">
        <animate attributeName="r" values="3.5;11;3.5" dur="4s" begin="1.5s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.25;0;0.25" dur="4s" begin="1.5s" repeatCount="indefinite"/>
      </circle>
      <text y="27" text-anchor="middle" font-family="JetBrains Mono, monospace" font-size="7.5" fill="#7A9BB8" letter-spacing="0.05em">MAR</text>
    </g>

    <!-- LIBYA -->
    <g transform="translate(248,128)">
      <circle r="17" fill="rgba(200,151,47,0.08)" stroke="#C8972F" stroke-width="0.6" opacity="0.8"/>
      <circle r="4" fill="#C8972F" opacity="0.95"/>
      <circle r="4" fill="#C8972F" opacity="0.3">
        <animate attributeName="r" values="4;13;4" dur="3.8s" begin="0.8s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.3;0;0.3" dur="3.8s" begin="0.8s" repeatCount="indefinite"/>
      </circle>
      <text y="28" text-anchor="middle" font-family="JetBrains Mono, monospace" font-size="7.5" fill="#C8972F" letter-spacing="0.05em">LBY</text>
    </g>

    <!-- UAE -->
    <g transform="translate(310,148)">
      <circle r="22" fill="rgba(200,151,47,0.12)" stroke="#C8972F" stroke-width="1"/>
      <circle r="5.5" fill="#C8972F"/>
      <circle r="5.5" fill="#C8972F" opacity="0.35">
        <animate attributeName="r" values="5.5;18;5.5" dur="3.5s" begin="0.4s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.35;0;0.35" dur="3.5s" begin="0.4s" repeatCount="indefinite"/>
      </circle>
      <text y="34" text-anchor="middle" font-family="JetBrains Mono, monospace" font-size="8" fill="#C8972F" letter-spacing="0.06em" font-weight="500">UAE</text>
    </g>

    <!-- OMAN -->
    <g transform="translate(322,196)">
      <circle r="16" fill="rgba(200,151,47,0.07)" stroke="#C8972F" stroke-width="0.5" opacity="0.7"/>
      <circle r="3.5" fill="#C8972F" opacity="0.85"/>
      <text y="27" text-anchor="middle" font-family="JetBrains Mono, monospace" font-size="7.5" fill="#7A9BB8" letter-spacing="0.05em">OMN</text>
    </g>

    <!-- NEPAL (South Asia blue) -->
    <g transform="translate(278,228)">
      <circle r="19" fill="rgba(96,165,250,0.1)" stroke="#60A5FA" stroke-width="0.7"/>
      <circle r="4.5" fill="#60A5FA"/>
      <circle r="4.5" fill="#60A5FA" opacity="0.3">
        <animate attributeName="r" values="4.5;15;4.5" dur="4.2s" begin="2s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.3;0;0.3" dur="4.2s" begin="2s" repeatCount="indefinite"/>
      </circle>
      <text y="31" text-anchor="middle" font-family="JetBrains Mono, monospace" font-size="7.5" fill="#60A5FA" letter-spacing="0.05em">NPL</text>
    </g>

    <!-- HQ / INDIA -->
    <g transform="translate(196,180)">
      <circle r="30" fill="rgba(200,151,47,0.05)" stroke="#C8972F" stroke-width="0.8"/>
      <circle r="13" fill="rgba(200,151,47,0.14)" stroke="#C8972F" stroke-width="0.5"/>
      <circle r="5.5" fill="#C8972F"/>
      <text y="44" text-anchor="middle" font-family="JetBrains Mono, monospace" font-size="7.5" fill="#C8972F" letter-spacing="0.08em" font-weight="500">IND ◆ HQ</text>
    </g>

    <!-- Header text -->
    <text x="10" y="18" font-family="JetBrains Mono, monospace" font-size="7" fill="#2A4A65" letter-spacing="0.12em">MARKET COVERAGE — FY2024/25</text>
    <text x="10" y="30" font-family="JetBrains Mono, monospace" font-size="6.5" fill="#2A4A65" letter-spacing="0.08em">MENA + SOUTH ASIA EXPORT INTELLIGENCE</text>

    <!-- Legend -->
    <g transform="translate(10, 330)">
      <circle cx="5" cy="5" r="3.5" fill="#C8972F"/>
      <text x="14" y="9" font-family="JetBrains Mono, monospace" font-size="7" fill="#5A7A99">MENA MARKETS</text>
      <circle cx="102" cy="5" r="3.5" fill="#60A5FA"/>
      <text x="111" y="9" font-family="JetBrains Mono, monospace" font-size="7" fill="#5A7A99">SOUTH ASIA</text>
    </g>

    <!-- Scan line -->
    <rect x="0" y="0" width="400" height="1.5" fill="rgba(200,151,47,0.12)">
      <animateTransform attributeName="transform" type="translate"
        values="0,0;0,360;0,0" dur="9s" repeatCount="indefinite"/>
    </rect>
  </svg>
</div>
```

  </div>
</section>

<!-- MARQUEE TICKER -->

<div class="marquee-wrap">
  <div class="marquee-track">
    <span class="mitem">Market Intelligence</span>
    <span class="mitem">MENA Export Research</span>
    <span class="mitem">Competitive Benchmarking</span>
    <span class="mitem">Porter's Five Forces</span>
    <span class="mitem">B2B Trade Data</span>
    <span class="mitem">Go-To-Market Strategy</span>
    <span class="mitem">Country Intelligence</span>
    <span class="mitem">Demand Forecasting</span>
    <span class="mitem">Board-Ready Reporting</span>
    <span class="mitem">South Asian Markets</span>
    <span class="mitem">OSINT Research</span>
    <span class="mitem">ITC Trade Map</span>
    <span class="mitem">Market Intelligence</span>
    <span class="mitem">MENA Export Research</span>
    <span class="mitem">Competitive Benchmarking</span>
    <span class="mitem">Porter's Five Forces</span>
    <span class="mitem">B2B Trade Data</span>
    <span class="mitem">Go-To-Market Strategy</span>
    <span class="mitem">Country Intelligence</span>
    <span class="mitem">Demand Forecasting</span>
    <span class="mitem">Board-Ready Reporting</span>
    <span class="mitem">South Asian Markets</span>
    <span class="mitem">OSINT Research</span>
    <span class="mitem">ITC Trade Map</span>
  </div>
</div>

<!-- STATS -->

<div class="stats-band">
  <div class="stats-inner">
    <div class="stat-item fi">
      <div class="stat-number" data-target="8">0</div>
      <div class="stat-label">Country intelligence reports integrated into FY2026–27 executive strategy</div>
    </div>
    <div class="stat-item fi">
      <div class="stat-number" data-target="10" data-suffix="+">0</div>
      <div class="stat-label">Competitors benchmarked with SWOT & Porter's Five Forces analysis</div>
    </div>
    <div class="stat-item fi">
      <div class="stat-number" data-target="5">0</div>
      <div class="stat-label">Emerging B2B export markets researched and reported</div>
    </div>
    <div class="stat-item fi">
      <div class="stat-number" data-target="6">0</div>
      <div class="stat-label">MENA countries covered — Algeria, Morocco, UAE, Libya, Nepal, Oman</div>
    </div>
  </div>
</div>

<!-- EXPERTISE -->

<section id="about">
  <p class="section-label">What I Do</p>
  <h2>Intelligence that earns a seat at the table</h2>
  <div class="expertise-grid">
    <div class="expertise-card fi">
      <div class="card-icon">🌍</div>
      <div class="card-title">Country Market Intelligence</div>
      <div class="card-desc">End-to-end market entry research across MENA and South Asia — regulatory landscape, demand sizing, competitive positioning, risk frameworks. Built for executive decisions, not slide decoration.</div>
    </div>
    <div class="expertise-card fi">
      <div class="card-icon">⚔️</div>
      <div class="card-title">Competitive Intelligence</div>
      <div class="card-desc">Structured competitor benchmarking using SWOT and Porter's Five Forces. Identifies pricing gaps, capability weaknesses, and whitespace opportunities that translate directly into strategy.</div>
    </div>
    <div class="expertise-card fi">
      <div class="card-icon">📊</div>
      <div class="card-title">B2B Trade Data Analysis</div>
      <div class="card-desc">Trade flow analysis, demand forecasting, and export opportunity mapping using ITC Trade Map, Volza, and Refinitiv — converted into stakeholder-ready intelligence reports.</div>
    </div>
    <div class="expertise-card fi">
      <div class="card-icon">🎯</div>
      <div class="card-title">Go-To-Market Strategy</div>
      <div class="card-desc">Market feasibility assessments and GTM frameworks for industrial B2B expansion into new geographies — bridging research outputs directly to revenue and expansion decisions.</div>
    </div>
    <div class="expertise-card fi">
      <div class="card-icon">📋</div>
      <div class="card-title">Executive-Level Reporting</div>
      <div class="card-desc">Monthly market activity reports and intelligence briefings supporting ABP planning cycles. Translating complex multi-source data into clear, concise executive narratives.</div>
    </div>
    <div class="expertise-card fi">
      <div class="card-icon">🔍</div>
      <div class="card-title">OSINT & Deep Research</div>
      <div class="card-desc">PESTLE analysis, multi-database synthesis across industry publications, regulatory portals, trade data platforms, and financial databases — structured into actionable intelligence.</div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->

<div class="section-divider"></div>
<section id="experience">
  <p class="section-label">Career Timeline</p>
  <h2>Work Experience</h2>
  <div class="exp-timeline">

```
<div class="exp-item fi">
  <div class="exp-dot"></div>
  <div class="exp-header">
    <div>
      <div class="exp-role">Strategic Research Analyst</div>
      <div class="exp-company">Texmo Industries — Taro Pumps</div>
    </div>
    <div class="exp-date">JUL 2024 – PRESENT · COIMBATORE</div>
  </div>
  <ul class="exp-bullets">
    <li>Developed <span class="hi">8 country-level market entry reports</span> across Algeria, Morocco, UAE, Libya, Nepal, and Oman — covering market potential, regulatory landscape, and GTM strategy; directly adopted into FY2026–27 executive strategic planning.</li>
    <li>Conducted competitive intelligence and benchmarking for <span class="hi">10+ competitors</span> using SWOT and Porter's Five Forces; surfaced market gaps that enhanced strategic positioning across key product lines.</li>
    <li>Published monthly market activity reports supporting ABP 2026–27 planning; delivered demand forecasting and trend analysis improving leadership decision visibility across <span class="hi">5 emerging B2B export markets</span>.</li>
    <li>Revised ISO 9001 QMS documentation for audit compliance; collaborated cross-functionally with sales, product, and executive teams to align research outputs with organizational strategy.</li>
  </ul>
</div>

<div class="exp-item fi">
  <div class="exp-dot"></div>
  <div class="exp-header">
    <div>
      <div class="exp-role">Procurement & Supply Chain Intern</div>
      <div class="exp-company">Aditya Birla Fashion & Retail · Tata Trent</div>
    </div>
    <div class="exp-date">FEB – APR 2024</div>
  </div>
  <ul class="exp-bullets">
    <li>Built Excel-based demand forecasting models improving inventory turnover by <span class="hi">15%</span>; cost-benefit analysis identified efficiencies generating annual savings of <span class="hi">₹1.8L</span>.</li>
    <li>Prepared budget variance and KPI performance reports supporting data-driven operational decisions.</li>
  </ul>
</div>

<div class="exp-item fi">
  <div class="exp-dot"></div>
  <div class="exp-header">
    <div>
      <div class="exp-role">Operations Intern</div>
      <div class="exp-company">Marks & Spencer India</div>
    </div>
    <div class="exp-date">MAY – JUN 2023</div>
  </div>
  <ul class="exp-bullets">
    <li>Prepared variance analysis reports, managed accounts payable workflows, and supported financial and operational reporting across the department.</li>
  </ul>
</div>

<div class="exp-item fi">
  <div class="exp-dot"></div>
  <div class="exp-header">
    <div>
      <div class="exp-role">Market Research Associate</div>
      <div class="exp-company">Lessburn</div>
    </div>
    <div class="exp-date">JAN – JUL 2022</div>
  </div>
  <ul class="exp-bullets">
    <li>Conducted market research and competitor benchmarking to support pricing strategy; recommendations directly influenced business decisions across multiple product categories.</li>
  </ul>
</div>
```

  </div>
</section>

<!-- PROJECTS -->

<div class="section-divider"></div>
<section id="projects">
  <p class="section-label">Featured Work</p>
  <h2>Key Projects</h2>
  <div class="projects-grid">

```
<!-- FLAGSHIP FEATURED -->
<div class="project-card featured fi">
  <div>
    <div class="project-type">Flagship Project · 2024 – Present</div>
    <div class="project-title">MENA & South Asia Export Market Intelligence Program</div>
    <div class="project-desc">
      Built a structured intelligence program from the ground up — 8 country reports covering market size, demand trends, regulatory frameworks, competitive landscape, and GTM strategy across MENA and South Asian markets. Outputs directly adopted into Taro Pumps' FY2026–27 Annual Business Plan.
    </div>
    <div class="pill-row">
      <span class="pill">Algeria</span><span class="pill">Morocco</span><span class="pill">UAE</span>
      <span class="pill">Libya</span><span class="pill">Nepal</span><span class="pill">Oman</span>
      <span class="pill">SWOT</span><span class="pill">Porter's Five Forces</span>
      <span class="pill">PESTLE</span><span class="pill">Executive Reporting</span>
    </div>
  </div>
  <div class="impact-box">
    <div>
      <div class="impact-label">Deliverable Type</div>
      <div class="impact-val">Country Intelligence Reports → ABP Strategic Integration</div>
    </div>
    <div>
      <div class="impact-label">Research Tools</div>
      <div class="impact-val">ITC Trade Map · Volza · Refinitiv · PESTLE · Desk Research</div>
    </div>
    <div>
      <div class="impact-label">Business Impact</div>
      <div class="impact-val green">Adopted into FY2026–27 executive strategic planning</div>
    </div>
    <div>
      <div class="impact-label">Scope</div>
      <div class="impact-val">8 countries · 10+ competitor profiles · 5 emerging markets</div>
    </div>
  </div>
</div>

<div class="project-card fi">
  <div class="project-type">Competitive Intelligence · 2024 – Present</div>
  <div class="project-title">Integrated Competitor Dossier Program</div>
  <div class="project-desc">
    Built comprehensive competitive dossiers for 10+ pump manufacturers covering production capacity, financials, R&D signals, talent trends, and field activity — structured for ongoing monthly intelligence cycles.
  </div>
  <div class="pill-row">
    <span class="pill">KSB</span><span class="pill">Kirloskar Brothers</span>
    <span class="pill">Grundfos</span><span class="pill">CRI Pumps</span>
    <span class="pill">Lubi</span><span class="pill">OSINT</span><span class="pill">Benchmarking</span>
  </div>
</div>

<div class="project-card fi">
  <div class="project-type">MBA Dissertation · 2024</div>
  <div class="project-title">Supply Chain Optimization Study — Apparel Retail</div>
  <div class="project-desc">
    6-month comparative study on supply chain operations at Aditya Birla Fashion & Tata Trent. Recommendations were validated during subsequent internships at both organizations.
  </div>
  <div class="pill-row">
    <span class="pill">15% Inventory Turnover ↑</span>
    <span class="pill">Aditya Birla</span><span class="pill">Tata Trent</span>
    <span class="pill">Supply Chain</span><span class="pill">Benchmarking</span>
  </div>
</div>

<div class="project-card fi">
  <div class="project-type">Compliance & Process · 2024</div>
  <div class="project-title">ISO 9001 QMS Documentation Revision</div>
  <div class="project-desc">
    Revised QMS documentation for the sales team, validated procedures cross-functionally, and supported successful internal quality audits — demonstrating cross-functional breadth beyond a typical research scope.
  </div>
  <div class="pill-row">
    <span class="pill">ISO 9001</span><span class="pill">QMS</span>
    <span class="pill">Cross-Functional</span><span class="pill">Audit Compliance</span>
  </div>
</div>
```

  </div>
</section>

<!-- SKILLS -->

<div class="section-divider"></div>
<section id="skills">
  <p class="section-label">Capabilities</p>
  <h2>Skills & Tools</h2>
  <div class="skills-layout">
    <div>
      <div class="skill-group-title">Core Research & Strategy</div>
      <div class="stags">
        <span class="stag p">Market Intelligence</span>
        <span class="stag p">Competitive Intelligence</span>
        <span class="stag p">Country-Level Research</span>
        <span class="stag p">Go-To-Market Strategy</span>
        <span class="stag">SWOT Analysis</span>
        <span class="stag">Porter's Five Forces</span>
        <span class="stag">PESTLE Analysis</span>
        <span class="stag">Demand Forecasting</span>
        <span class="stag">Trade Data Analysis</span>
        <span class="stag">OSINT / Deep Web Research</span>
        <span class="stag">Secondary & Desk Research</span>
        <span class="stag">B2B Export Research</span>
        <span class="stag">Market Sizing (TAM/SAM/SOM)</span>
        <span class="stag">Risk Assessment</span>
        <span class="stag">Stakeholder Reporting</span>
      </div>

```
  <div class="skill-group-title">Research Databases & Platforms</div>
  <div class="stags">
    <span class="stag p">ITC Trade Map</span>
    <span class="stag p">Volza</span>
    <span class="stag">Refinitiv / LSEG</span>
    <span class="stag">S&P Capital IQ</span>
    <span class="stag">Factiva</span>
    <span class="stag">EMIS</span>
    <span class="stag">Power BI</span>
  </div>
</div>
<div>
  <div class="skill-group-title">Analytics & Business Tools</div>
  <div class="stags">
    <span class="stag p">Advanced Excel</span>
    <span class="stag">SPSS</span>
    <span class="stag">SQL (query-level)</span>
    <span class="stag">SAP FICO</span>
    <span class="stag">Tally ERP</span>
    <span class="stag">MS Office Suite</span>
    <span class="stag">FP&A Modelling</span>
    <span class="stag">Financial Statement Analysis</span>
  </div>

  <div class="skill-group-title">Education</div>
  <div class="stags">
    <span class="stag p">MBA — Central University of Tamil Nadu (2024)</span>
    <span class="stag">B.Com — Bharathiar University (2021)</span>
  </div>

  <div class="skill-group-title">Certifications</div>
  <div class="stags">
    <span class="stag">FP&A Modelling & Valuation — Udemy</span>
    <span class="stag">SAP FICO — Alison</span>
    <span class="stag">Business Analysis & PM — Coursera</span>
    <span class="stag">Data Analysis Excel — Novitech</span>
    <span class="stag">Financial Analyst: FSA — Udemy</span>
  </div>

  <div class="skill-group-title">Languages</div>
  <div class="stags">
    <span class="stag">English (Fluent)</span>
    <span class="stag">Tamil (Native)</span>
    <span class="stag">Hindi (Intermediate)</span>
  </div>
</div>
```

  </div>
</section>

<!-- CONTACT -->

<div class="section-divider"></div>
<section id="contact">
  <div class="contact-box">
    <p class="section-label" style="justify-content:center; display:flex;">Let's Connect</p>
    <h2 class="contact-title">Open to new opportunities</h2>
    <p class="contact-sub">Available for market research, KPO, and strategic research roles. Remote, hybrid, or onsite in Bangalore, Chennai, Coimbatore, or Kerala. Floor: 6 LPA.</p>
    <div class="contact-links">
      <a href="mailto:trishaatsamuela@gmail.com" class="contact-item">✉ trishaatsamuela@gmail.com</a>
      <a href="tel:+918300665144" class="contact-item">📱 +91 83006 65144</a>
      <a href="https://linkedin.com/in/trishaa-samuelat/" target="_blank" class="contact-item">in LinkedIn Profile ↗</a>
    </div>
  </div>
</section>

<footer>Trishaa Samuela T · Strategic Research Analyst · Coimbatore, India · 2025</footer>

<script>
  // Scroll-triggered fade-in
  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('vis'); });
  }, { threshold: 0.08, rootMargin: '0px 0px -40px 0px' });
  document.querySelectorAll('.fi').forEach(el => io.observe(el));

  // Animated counters
  function animCounter(el, target, suffix) {
    let start = null;
    const dur = 1400;
    const run = (ts) => {
      if (!start) start = ts;
      const p = Math.min((ts - start) / dur, 1);
      const ease = 1 - Math.pow(1 - p, 3);
      el.textContent = Math.floor(ease * target) + suffix;
      if (p < 1) requestAnimationFrame(run);
    };
    requestAnimationFrame(run);
  }

  const statsObs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.querySelectorAll('.stat-number').forEach(el => {
          animCounter(el, parseInt(el.dataset.target), el.dataset.suffix || '');
        });
        statsObs.unobserve(e.target);
      }
    });
  }, { threshold: 0.3 });

  const band = document.querySelector('.stats-band');
  if (band) statsObs.observe(band);
</script>

</body>
</html>