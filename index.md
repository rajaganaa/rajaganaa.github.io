---
layout: none
permalink: /
---
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Rajaganapathy M — AI Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,300&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --bg:        #080808;
  --bg2:       #0f0f0f;
  --bg3:       #161616;
  --bg4:       #1e1e1e;
  --border:    rgba(255,255,255,0.07);
  --border-md: rgba(255,255,255,0.12);
  --border-hi: rgba(255,255,255,0.20);
  --text:      #f2efea;
  --text-2:    #a8a49e;
  --text-3:    #5a5650;
  --green:     #b8f050;
  --blue:      #50c8f0;
  --orange:    #f0a040;
  --nav-h:     72px;
}

/* ─── RESET / BASE ─── */
html { scroll-behavior: smooth; font-size: 16px; }
body {
  background: var(--bg);
  color: var(--text);
  font-family: 'DM Sans', sans-serif;
  line-height: 1.6;
  overflow-x: hidden;
  -webkit-font-smoothing: antialiased;
}
::selection { background: var(--green); color: #080808; }
::-webkit-scrollbar { width: 3px; }
::-webkit-scrollbar-track { background: var(--bg); }
::-webkit-scrollbar-thumb { background: var(--border-hi); }

/* ─── NOISE GRAIN ─── */
body::after {
  content: '';
  position: fixed; inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.035'/%3E%3C/svg%3E");
  pointer-events: none; z-index: 9999; opacity: 0.5;
}

/* ─── TYPOGRAPHY ─── */
.f-display { font-family: 'Bebas Neue', sans-serif; letter-spacing: 0.01em; }
.f-sans    { font-family: 'DM Sans', sans-serif; }
.f-mono    { font-family: 'DM Mono', monospace; }

/* ─── NAV ─── */
nav {
  position: fixed; top: 0; left: 0; right: 0;
  height: var(--nav-h);
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 3rem;
  background: rgba(8,8,8,0.92);
  backdrop-filter: blur(24px);
  border-bottom: 1px solid var(--border);
  z-index: 200;
}
.nav-logo {
  font-family: 'DM Mono', monospace;
  font-size: 13px; font-weight: 400;
  color: var(--green);
  letter-spacing: 0.06em;
  text-decoration: none;
}
.nav-links { display: flex; gap: 2rem; list-style: none; }
.nav-links a {
  font-family: 'DM Mono', monospace;
  font-size: 11px; letter-spacing: 0.1em;
  color: var(--text-2); text-decoration: none;
  transition: color 0.15s;
}
.nav-links a:hover { color: var(--text); }
.nav-right { display: flex; align-items: center; gap: 0.75rem; }
.btn-nav {
  font-family: 'DM Mono', monospace;
  font-size: 11px; letter-spacing: 0.08em;
  padding: 0.45rem 1.1rem;
  border: 1px solid var(--border-md);
  color: var(--text-2);
  text-decoration: none;
  transition: all 0.15s;
  cursor: pointer; background: none;
}
.btn-nav:hover { border-color: var(--text); color: var(--text); }
.btn-nav-accent {
  border-color: var(--green); color: var(--green);
}
.btn-nav-accent:hover { background: var(--green); color: #080808; }

/* ─── HERO ─── */
.hero {
  min-height: 100vh;
  padding: calc(var(--nav-h) + 6rem) 3rem 5rem;
  display: flex; flex-direction: column; justify-content: center;
  position: relative; overflow: hidden;
}
.hero-grid {
  position: absolute; inset: 0;
  background-image:
    linear-gradient(rgba(255,255,255,0.018) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255,255,255,0.018) 1px, transparent 1px);
  background-size: 72px 72px;
  mask-image: radial-gradient(ellipse 90% 90% at 50% 50%, black 30%, transparent 100%);
}
.hero-glow {
  position: absolute;
  width: 800px; height: 800px; border-radius: 50%;
  background: radial-gradient(circle, rgba(184,240,80,0.04) 0%, transparent 65%);
  top: -300px; right: -200px; pointer-events: none;
}
.hero-glow2 {
  position: absolute;
  width: 500px; height: 500px; border-radius: 50%;
  background: radial-gradient(circle, rgba(80,200,240,0.03) 0%, transparent 65%);
  bottom: -100px; left: -100px; pointer-events: none;
}

.hero-eyebrow {
  font-family: 'DM Mono', monospace;
  font-size: 11px; letter-spacing: 0.2em;
  color: var(--green);
  display: flex; align-items: center; gap: 1rem;
  margin-bottom: 2rem;
  opacity: 0; animation: fadeUp 0.7s 0.05s forwards;
}
.hero-eyebrow::before {
  content: '';
  display: block; width: 40px; height: 1px; background: var(--green);
}

/* THE BIG NAME */
.hero-name {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(5rem, 13vw, 11rem);
  line-height: 0.88;
  letter-spacing: 0.01em;
  color: var(--text);
  margin-bottom: 0.15em;
  opacity: 0; animation: fadeUp 0.8s 0.15s forwards;
}
.hero-name-accent {
  display: block;
  color: var(--green);
  font-size: clamp(5rem, 13vw, 11rem);
}

.hero-title {
  font-family: 'DM Mono', monospace;
  font-size: clamp(0.8rem, 1.4vw, 1rem);
  letter-spacing: 0.18em;
  color: var(--text-2);
  margin-bottom: 2.5rem;
  opacity: 0; animation: fadeUp 0.7s 0.28s forwards;
}

.hero-tagline {
  font-family: 'DM Sans', sans-serif;
  font-size: clamp(1.05rem, 1.8vw, 1.3rem);
  font-weight: 300;
  font-style: italic;
  color: var(--text-2);
  max-width: 620px;
  line-height: 1.75;
  margin-bottom: 3rem;
  opacity: 0; animation: fadeUp 0.7s 0.38s forwards;
}
.hero-tagline strong { color: var(--text); font-weight: 500; font-style: normal; }

.hero-badges {
  display: flex; flex-wrap: wrap; gap: 0.6rem;
  margin-bottom: 3rem;
  opacity: 0; animation: fadeUp 0.7s 0.5s forwards;
}
.badge {
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.08em;
  padding: 0.35rem 0.9rem;
  border: 1px solid var(--border-md);
  color: var(--text-3);
  white-space: nowrap;
}
.badge-g  { border-color: rgba(184,240,80,0.5); color: var(--green); background: rgba(184,240,80,0.05); }
.badge-b  { border-color: rgba(80,200,240,0.5); color: var(--blue);  background: rgba(80,200,240,0.05); }

.hero-actions {
  display: flex; gap: 0.9rem; flex-wrap: wrap;
  opacity: 0; animation: fadeUp 0.7s 0.6s forwards;
}
.btn-primary {
  font-family: 'DM Mono', monospace;
  font-size: 12px; letter-spacing: 0.1em;
  padding: 0.85rem 2rem;
  background: var(--green); color: #080808;
  text-decoration: none; font-weight: 500;
  transition: all 0.15s;
  display: inline-flex; align-items: center; gap: 0.5rem;
  border: 1px solid var(--green);
}
.btn-primary:hover { background: #ccff55; transform: translateY(-1px); }
.btn-outline {
  font-family: 'DM Mono', monospace;
  font-size: 12px; letter-spacing: 0.1em;
  padding: 0.85rem 1.8rem;
  border: 1px solid var(--border-md);
  color: var(--text-2); text-decoration: none;
  transition: all 0.15s;
  display: inline-flex; align-items: center; gap: 0.5rem;
  background: none; cursor: pointer;
}
.btn-outline:hover { border-color: var(--text); color: var(--text); }

.hero-scroll {
  position: absolute; bottom: 2.5rem; left: 3rem;
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.15em; color: var(--text-3);
  display: flex; align-items: center; gap: 0.75rem;
  opacity: 0; animation: fadeUp 0.7s 1s forwards;
}
.hero-scroll::after {
  content: '';
  display: block; width: 1px; height: 52px;
  background: linear-gradient(to bottom, var(--text-3), transparent);
}

.hero-stats {
  position: absolute; bottom: 2.5rem; right: 3rem;
  display: flex; gap: 3rem;
  opacity: 0; animation: fadeUp 0.7s 0.75s forwards;
}
.stat { text-align: right; }
.stat-num {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 2.6rem; line-height: 1; color: var(--text);
}
.stat-label {
  font-family: 'DM Mono', monospace;
  font-size: 9px; letter-spacing: 0.14em;
  color: var(--text-3); margin-top: 4px;
}

/* ─── TICKER ─── */
.ticker-wrap {
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
  background: var(--bg2);
  overflow: hidden; white-space: nowrap;
  padding: 0.7rem 0;
}
.ticker-inner {
  display: inline-block;
  animation: ticker 40s linear infinite;
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.14em; color: var(--text-3);
}
@keyframes ticker {
  from { transform: translateX(0); }
  to   { transform: translateX(-50%); }
}

/* ─── SECTION BASE ─── */
section {
  padding: 7rem 3rem;
  border-top: 1px solid var(--border);
}
.sec-label {
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.22em;
  color: var(--text-3);
  margin-bottom: 4rem;
  display: flex; align-items: center; gap: 1rem;
}
.sec-label::after {
  content: ''; flex: 1; height: 1px;
  background: var(--border); max-width: 100px;
}

/* ─── ABOUT ─── */
.about-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 6rem;
  align-items: start;
}
.about-statement {
  font-family: 'DM Sans', sans-serif;
  font-size: clamp(1.4rem, 2.4vw, 1.95rem);
  font-weight: 300;
  line-height: 1.55; color: var(--text);
}
.about-statement em { color: var(--green); font-style: italic; }
.about-statement strong { font-weight: 600; color: var(--text); font-style: normal; }

.timeline { padding-left: 1.5rem; margin-top: 3.5rem; position: relative; }
.timeline::before {
  content: ''; position: absolute;
  left: 0; top: 6px; bottom: 0; width: 1px;
  background: linear-gradient(to bottom, var(--green), transparent);
}
.tl-item { position: relative; padding-bottom: 2.25rem; padding-left: 1.5rem; }
.tl-item::before {
  content: ''; position: absolute;
  left: -1.5rem; top: 6px;
  width: 6px; height: 6px; border-radius: 50%;
  background: var(--green);
  box-shadow: 0 0 10px rgba(184,240,80,0.5);
}
.tl-year {
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.1em;
  color: var(--green); margin-bottom: 3px;
}
.tl-role {
  font-family: 'DM Sans', sans-serif;
  font-size: 14px; font-weight: 600; color: var(--text);
  margin-bottom: 2px;
}
.tl-org {
  font-family: 'DM Mono', monospace;
  font-size: 11px; color: var(--text-3);
}

.about-body p {
  font-family: 'DM Sans', sans-serif;
  font-size: 14px; font-weight: 300;
  color: var(--text-2); line-height: 1.9;
  margin-bottom: 1.5rem;
}
.about-body p strong { color: var(--text); font-weight: 500; }
.about-body p em { color: var(--green); font-style: normal; font-weight: 500; }

/* ─── PROJECTS ─── */
.proj-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
  gap: 1px;
  background: var(--border);
}

/* Featured spans full width */
.proj-featured {
  grid-column: 1 / -1;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0;
  background: var(--bg);
  position: relative;
  border: 1px solid rgba(184,240,80,0.18);
}
.proj-featured::before {
  content: 'FLAGSHIP PROJECT';
  position: absolute; top: 1.5rem; right: 1.5rem;
  font-family: 'DM Mono', monospace;
  font-size: 9px; letter-spacing: 0.22em;
  color: var(--green); border: 1px solid rgba(184,240,80,0.3);
  padding: 3px 10px;
}
.feat-left {
  padding: 3rem;
  border-right: 1px solid rgba(184,240,80,0.1);
}
.feat-right {
  padding: 3rem;
  display: flex; flex-direction: column; gap: 1.5rem;
}
.feat-num {
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.18em;
  color: var(--text-3); margin-bottom: 1rem;
}
.feat-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 3rem; line-height: 0.95;
  color: var(--text); margin-bottom: 1.25rem;
}
.feat-title span { color: var(--green); display: block; }
.feat-desc {
  font-family: 'DM Sans', sans-serif;
  font-size: 13px; font-weight: 300;
  color: var(--text-2); line-height: 1.85;
  font-style: italic;
}
.feat-tags {
  display: flex; flex-wrap: wrap; gap: 6px; margin-top: 1.25rem;
}
.feat-links {
  display: flex; gap: 0.75rem; margin-top: auto; flex-wrap: wrap;
}
.btn-feat-primary {
  font-family: 'DM Mono', monospace;
  font-size: 11px; letter-spacing: 0.08em;
  padding: 0.6rem 1.4rem;
  background: var(--green); color: #080808;
  text-decoration: none; font-weight: 500;
  display: inline-flex; align-items: center; gap: 0.4rem;
  transition: all 0.15s;
}
.btn-feat-primary:hover { background: #ccff55; }
.btn-feat-secondary {
  font-family: 'DM Mono', monospace;
  font-size: 11px; letter-spacing: 0.08em;
  padding: 0.6rem 1.4rem;
  border: 1px solid rgba(184,240,80,0.35);
  color: var(--green); text-decoration: none;
  display: inline-flex; align-items: center; gap: 0.4rem;
  transition: all 0.15s;
}
.btn-feat-secondary:hover { background: rgba(184,240,80,0.07); }

.ach-item {
  display: flex; align-items: flex-start; gap: 1rem;
  padding: 1rem 1.25rem;
  border: 1px solid var(--border);
  background: var(--bg2);
}
.ach-icon { font-size: 1.1rem; flex-shrink: 0; line-height: 1; margin-top: 2px; }
.ach-title {
  font-family: 'DM Sans', sans-serif;
  font-size: 13px; font-weight: 600;
  color: var(--text); margin-bottom: 3px;
}
.ach-body {
  font-family: 'DM Mono', monospace;
  font-size: 11px; color: var(--text-3); line-height: 1.65;
}

/* regular project cards */
.proj-card {
  background: var(--bg);
  padding: 2rem;
  display: flex; flex-direction: column; gap: 1rem;
  text-decoration: none; color: inherit;
  transition: background 0.15s;
}
.proj-card:hover { background: var(--bg3); }
.proj-card:hover .proj-arrow { transform: translate(3px, -3px); }

.proj-top {
  display: flex; justify-content: space-between; align-items: flex-start;
}
.proj-num {
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.1em; color: var(--text-3);
}
.proj-arrow {
  font-size: 16px; color: var(--text-3); transition: transform 0.15s;
}
.proj-tags { display: flex; flex-wrap: wrap; gap: 5px; }
.proj-tag {
  font-family: 'DM Mono', monospace;
  font-size: 9px; letter-spacing: 0.06em;
  padding: 3px 8px;
  background: var(--bg3); color: var(--text-3);
  border: 1px solid var(--border);
}
.proj-tag-g { border-color: rgba(184,240,80,0.25); color: rgba(184,240,80,0.65); }
.proj-title {
  font-family: 'DM Sans', sans-serif;
  font-size: 1.05rem; font-weight: 600;
  color: var(--text); line-height: 1.35;
}
.proj-desc {
  font-family: 'DM Sans', sans-serif;
  font-size: 12.5px; font-weight: 300;
  color: var(--text-2); line-height: 1.8; flex: 1;
}
.proj-metric {
  font-family: 'DM Mono', monospace;
  font-size: 10px; color: var(--green);
  padding-top: 0.75rem;
  border-top: 1px solid var(--border);
}

/* ─── SKILLS ─── */
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 2.5rem;
}
.skill-group-title {
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.18em;
  color: var(--green);
  padding-bottom: 0.6rem;
  border-bottom: 1px solid var(--border);
  margin-bottom: 1rem;
}
.skill-item {
  display: flex; align-items: center;
  justify-content: space-between;
  padding: 0.55rem 0;
  border-bottom: 1px solid rgba(255,255,255,0.025);
}
.skill-name {
  font-family: 'DM Sans', sans-serif;
  font-size: 13px; font-weight: 300; color: var(--text-2);
}
.skill-dots { display: flex; gap: 3px; }
.dot { width: 5px; height: 5px; border-radius: 50%; background: var(--bg4); }
.dot.on { background: var(--green); }

/* ─── CERTS ─── */
.certs-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 1px; background: var(--border);
}
.cert-card {
  background: var(--bg);
  padding: 1.5rem;
  display: flex; gap: 1rem; align-items: flex-start;
  transition: background 0.15s;
}
.cert-card:hover { background: var(--bg3); }
.cert-icon {
  width: 34px; height: 34px; flex-shrink: 0;
  display: flex; align-items: center; justify-content: center;
  border: 1px solid var(--border-md); font-size: 13px;
}
.cert-name {
  font-family: 'DM Sans', sans-serif;
  font-size: 13px; font-weight: 500;
  color: var(--text); line-height: 1.4; margin-bottom: 4px;
}
.cert-issuer {
  font-family: 'DM Mono', monospace;
  font-size: 10px; color: var(--text-3); letter-spacing: 0.06em;
}

/* ─── BLOG ─── */
.blog-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1px; background: var(--border);
}
.blog-card {
  background: var(--bg);
  padding: 2rem;
  display: flex; flex-direction: column; gap: 0.75rem;
  cursor: pointer; transition: background 0.15s;
}
.blog-card:hover { background: var(--bg3); }
.blog-card:hover .blog-arrow { transform: translate(3px, -3px); }
.blog-meta { display: flex; justify-content: space-between; align-items: center; }
.blog-date {
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.1em; color: var(--text-3);
}
.blog-arrow { font-size: 14px; color: var(--text-3); transition: transform 0.15s; }
.blog-tag {
  font-family: 'DM Mono', monospace;
  font-size: 9px; letter-spacing: 0.08em;
  padding: 3px 9px;
  border: 1px solid rgba(184,240,80,0.25);
  color: var(--green); background: rgba(184,240,80,0.04);
  width: fit-content;
}
.blog-title {
  font-family: 'DM Sans', sans-serif;
  font-size: 1rem; font-weight: 600;
  color: var(--text); line-height: 1.4;
}
.blog-excerpt {
  font-family: 'DM Sans', sans-serif;
  font-size: 12.5px; font-weight: 300;
  color: var(--text-2); line-height: 1.8; flex: 1;
}
.blog-readtime {
  font-family: 'DM Mono', monospace;
  font-size: 10px; color: var(--text-3);
  padding-top: 0.75rem; border-top: 1px solid var(--border);
}

/* ─── BLOG MODAL ─── */
.modal-overlay {
  display: none; position: fixed; inset: 0;
  background: rgba(0,0,0,0.75); z-index: 500;
  align-items: flex-start; justify-content: center;
  padding: 4rem 1rem; overflow-y: auto;
  backdrop-filter: blur(6px);
}
.modal-overlay.open { display: flex; }
.modal {
  background: var(--bg2); border: 1px solid var(--border-md);
  max-width: 720px; width: 100%; padding: 3rem; position: relative;
}
.modal-close {
  position: absolute; top: 1.5rem; right: 1.5rem;
  background: none; border: 1px solid var(--border);
  color: var(--text-2); font-family: 'DM Mono', monospace;
  font-size: 11px; padding: 4px 12px; cursor: pointer;
  letter-spacing: 0.06em; transition: all 0.15s;
}
.modal-close:hover { border-color: var(--text); color: var(--text); }
.modal-tag {
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.12em;
  color: var(--green); margin-bottom: 0.75rem;
}
.modal-title {
  font-family: 'DM Sans', sans-serif;
  font-size: 1.7rem; font-weight: 700;
  color: var(--text); line-height: 1.2; margin-bottom: 0.5rem;
}
.modal-date {
  font-family: 'DM Mono', monospace;
  font-size: 11px; color: var(--text-3);
  margin-bottom: 2rem; padding-bottom: 1.5rem;
  border-bottom: 1px solid var(--border);
}
.modal-body {
  font-family: 'DM Sans', sans-serif;
  font-size: 14.5px; font-weight: 300;
  color: var(--text-2); line-height: 1.9;
}
.modal-body p { margin-bottom: 1.25rem; }
.modal-body h3 {
  font-size: 1rem; font-weight: 600; color: var(--text);
  margin: 2rem 0 0.75rem;
}
.modal-body strong { color: var(--text); font-weight: 500; }
.modal-body em { color: var(--green); font-style: normal; }

/* ─── THE EDGE ─── */
.edge-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1px; background: var(--border);
}
.edge-card {
  background: var(--bg2);
  padding: 2.5rem;
}
.edge-label {
  font-family: 'DM Mono', monospace;
  font-size: 9px; letter-spacing: 0.22em;
  color: var(--green); margin-bottom: 1.25rem;
}
.edge-heading {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 2.1rem; line-height: 1;
  color: var(--text); margin-bottom: 1rem;
}
.edge-heading em { color: var(--green); font-style: normal; }
.edge-body {
  font-family: 'DM Sans', sans-serif;
  font-size: 13px; font-weight: 300;
  color: var(--text-2); line-height: 1.85;
}

/* ─── CONTACT ─── */
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 6rem; align-items: center;
}
.contact-heading {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(2.8rem, 5vw, 4.5rem);
  line-height: 0.95; letter-spacing: 0.01em;
  color: var(--text); margin-bottom: 1.5rem;
}
.contact-heading span { color: var(--green); }
.contact-sub {
  font-family: 'DM Sans', sans-serif;
  font-size: 13.5px; font-weight: 300;
  color: var(--text-2); line-height: 1.9; margin-bottom: 2.5rem;
}
.contact-links { border: 1px solid var(--border); }
.contact-link {
  display: flex; align-items: center;
  justify-content: space-between;
  padding: 1rem 1.5rem;
  border-bottom: 1px solid var(--border);
  text-decoration: none; color: var(--text-2);
  transition: all 0.15s;
  font-family: 'DM Mono', monospace; font-size: 12px;
}
.contact-link:last-child { border-bottom: none; }
.contact-link:hover { background: var(--bg3); color: var(--text); }
.contact-link-val { font-size: 11px; color: var(--text-3); }

/* ─── FOOTER ─── */
footer {
  border-top: 1px solid var(--border);
  padding: 2rem 3rem;
  display: flex; justify-content: space-between; align-items: center;
}
footer p {
  font-family: 'DM Mono', monospace;
  font-size: 11px; color: var(--text-3); letter-spacing: 0.06em;
}

/* ─── ANIMATIONS ─── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(22px); }
  to   { opacity: 1; transform: translateY(0); }
}
.reveal {
  opacity: 0; transform: translateY(18px);
  transition: opacity 0.65s ease, transform 0.65s ease;
}
.reveal.visible { opacity: 1; transform: none; }

/* ─── RESPONSIVE ─── */
@media (max-width: 768px) {
  nav { padding: 0 1.5rem; }
  .nav-links { display: none; }
  .hero { padding: calc(var(--nav-h) + 3rem) 1.5rem 3rem; }
  .hero-name, .hero-name-accent { font-size: clamp(4rem, 16vw, 6rem); }
  section { padding: 4.5rem 1.5rem; }
  .about-grid, .contact-grid, .proj-featured { grid-template-columns: 1fr; }
  .feat-left { border-right: none; border-bottom: 1px solid rgba(184,240,80,0.1); }
  .hero-stats { display: none; }
  .hero-scroll { left: 1.5rem; }
  footer { padding: 1.5rem; flex-direction: column; gap: 0.5rem; text-align: center; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">RM_AI</a>
  <ul class="nav-links">
    <li><a href="#about">about</a></li>
    <li><a href="#projects">projects</a></li>
    <li><a href="#skills">skills</a></li>
    <li><a href="#certifications">certs</a></li>
    <li><a href="#blog">blog</a></li>
    <li><a href="#contact">contact</a></li>
  </ul>
  <div class="nav-right">
    <button class="btn-nav" id="themeToggle">☀ light</button>
    <button class="btn-nav" onclick="downloadCV(event)">↓ cv</button>
    <a class="btn-nav btn-nav-accent" href="mailto:rajaganaa@gmail.com">hire me →</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-grid"></div>
  <div class="hero-glow"></div>
  <div class="hero-glow2"></div>

  <div class="hero-eyebrow">available for ai/ml roles · chennai, india</div>

  <h1 class="hero-name">
    Rajaganapathy
    <span class="hero-name-accent">M.</span>
  </h1>

  <p class="hero-title">AI / ML ENGINEER &nbsp;·&nbsp; LLM SYSTEMS &nbsp;·&nbsp; AGENTIC AI &nbsp;·&nbsp; RAG</p>

  <p class="hero-tagline">
    I spent nine years engineering systems where <strong>failure wasn't an option.</strong>
    Now I build AI with that same discipline —
    a filed patent and an IEEE paper are the proof.
  </p>

  <div class="hero-badges">
    <span class="badge badge-g">⚡ Patent Filed · Apr 2026</span>
    <span class="badge badge-b">📄 IEEE Paper · Submitted</span>
    <span class="badge badge-g">🎓 M.Tech AI · 9.6 CGPA</span>
    <span class="badge">LLMs · Agentic AI · RAG</span>
    <span class="badge">Multi-Agent Systems</span>
    <span class="badge">Computer Vision</span>
  </div>

  <div class="hero-actions">
    <a class="btn-primary" href="#projects">view my work →</a>
    <a class="btn-outline" href="https://rajaganaa.github.io/antahkarana-frontend/" target="_blank">⚡ live demo ↗</a>
    <button class="btn-outline" onclick="downloadCV(event)">↓ download cv</button>
    <a class="btn-outline" href="https://github.com/rajaganaa" target="_blank">github ↗</a>
    <a class="btn-outline" href="https://www.linkedin.com/in/raja-ganapathy-36b00658" target="_blank">linkedin ↗</a>
  </div>

  <div class="hero-scroll">scroll</div>

  <div class="hero-stats">
    <div class="stat"><div class="stat-num">9+</div><div class="stat-label">YRS ENGINEERING</div></div>
    <div class="stat"><div class="stat-num">13+</div><div class="stat-label">PROJECTS BUILT</div></div>
    <div class="stat"><div class="stat-num">9.6</div><div class="stat-label">M.TECH CGPA</div></div>
  </div>
</section>

<!-- TICKER -->
<div class="ticker-wrap">
  <div class="ticker-inner">
    &nbsp;&nbsp;&nbsp;⚡ PATENT FILED · APP NO. 202641043947
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    📄 IEEE CONFERENCE PAPER SUBMITTED · SRM INSTITUTE
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🎓 M.TECH ARTIFICIAL INTELLIGENCE · 9.6 CGPA
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🚀 ANTAHKARANA AI — LIVE DEMO DEPLOYED
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🛠 8 PRODUCTION AI SYSTEMS
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🏭 9+ YEARS SAFETY-CRITICAL ENGINEERING
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ☁️ AWS SOLUTIONS ARCHITECT CERTIFIED · 2025
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🤖 KAGGLE AI AGENTS INTENSIVE WITH GOOGLE · 2025
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ⚡ PATENT FILED · APP NO. 202641043947
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    📄 IEEE CONFERENCE PAPER SUBMITTED · SRM INSTITUTE
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🎓 M.TECH ARTIFICIAL INTELLIGENCE · 9.6 CGPA
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🚀 ANTAHKARANA AI — LIVE DEMO DEPLOYED
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🛠 8 PRODUCTION AI SYSTEMS
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🏭 9+ YEARS SAFETY-CRITICAL ENGINEERING
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ☁️ AWS SOLUTIONS ARCHITECT CERTIFIED · 2025
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🤖 KAGGLE AI AGENTS INTENSIVE WITH GOOGLE · 2025
    &nbsp;&nbsp;&nbsp;&nbsp;
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="sec-label">01 · ABOUT</div>
  <div class="about-grid">
    <div>
      <p class="about-statement reveal">
        Most AI engineers understand models.<br/>
        I understand <em>failure</em> — the real kind,
        in 400 kW industrial systems where downtime
        costs money and <strong>safety.</strong>
        That discipline is in every line of AI code I write.
      </p>

      <div class="timeline reveal" style="margin-top:3.5rem;">
        <div class="tl-item">
          <div class="tl-year">2013</div>
          <div class="tl-role">B.E. Electrical & Electronics Engineering</div>
          <div class="tl-org">Thangavelu Engineering College, Chennai</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">2014 – 2016</div>
          <div class="tl-role">Electrical Maintenance Engineer</div>
          <div class="tl-org">Mod Forge Pvt. Ltd. · ISO/TS 16949 Certified</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">2017 – 2023</div>
          <div class="tl-role">Electrical Construction Site Engineer</div>
          <div class="tl-org">SR Electrical Works · Chennai</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">2023</div>
          <div class="tl-role">Deliberate pivot to Artificial Intelligence</div>
          <div class="tl-org">After 9+ years of production engineering</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">2024 – Present</div>
          <div class="tl-role">M.Tech Artificial Intelligence · 9.6 CGPA</div>
          <div class="tl-org">SRM Institute of Science & Technology</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">Apr 2026</div>
          <div class="tl-role">Indian Patent Filed · Antahkarana System</div>
          <div class="tl-org">App No. 202641043947 · IEEE Paper Submitted</div>
        </div>
      </div>
    </div>

    <div class="about-body reveal">
      <p>
        I am an <strong>AI/ML Engineer</strong> specialising in LLMs, Agentic AI, RAG pipelines,
        and multi-agent systems. After nine years as a practising electrical engineer,
        I made a deliberate leap into AI in 2023 — and spent the next two years proving
        it was the right decision.
      </p>
      <p>
        My flagship project, <strong>Antahkarana</strong>, is a cognitively-inspired adaptive
        reasoning framework for LLMs and VLMs — drawing on Vedantic cognitive architecture.
        It earned a <em>filed Indian patent</em> and a <em>submitted IEEE Conference paper</em>:
        outputs typically associated with full research teams, not individual M.Tech students.
      </p>
      <p>
        What I bring that most candidates don't: the discipline of a practising engineer who
        has operated under hard constraints in safety-critical environments. I think about
        AI the way production engineers think about infrastructure —
        <strong>reliably, at scale, with failure modes already mapped.</strong>
      </p>
      <p>
        <strong>CGPA 9.6/10</strong> · AWS Solutions Architect · DevOps · GUVI AIML Professional
        · IIT-M Advanced Programming · NPTEL IoT · Kaggle AI Agents (Google)
      </p>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="sec-label">02 · PROJECTS</div>

  <div class="proj-grid">

    <!-- FLAGSHIP -->
    <div class="proj-featured reveal">
      <div class="feat-left">
        <div class="feat-num">P.001 · FLAGSHIP</div>
        <h2 class="feat-title">Antahkarana<span>Reasoning Framework</span></h2>
        <p class="feat-desc">
          A cognitively-inspired, modular conditional reasoning framework for LLMs and VLMs.
          Inspired by Vedantic cognitive architecture, Antahkarana routes complex queries
          through specialised stages — perception, discrimination, memory, and integration —
          to produce coherent, grounded responses at scale.
        </p>
        <div class="feat-tags">
          <span class="badge badge-g">Patent Filed</span>
          <span class="badge badge-b">IEEE Submitted</span>
          <span class="badge">Python 3.8+</span>
          <span class="badge">Apache 2.0</span>
          <span class="badge">BLIP-3 · VLM</span>
          <span class="badge">Qwen 0.5</span>
        </div>
      </div>
      <div class="feat-right">
        <div class="ach-item">
          <div class="ach-icon">⚡</div>
          <div>
            <div class="ach-title">Indian Patent Filed · Apr 2026</div>
            <div class="ach-body">App No. 202641043947 — system design protected under Indian IP law</div>
          </div>
        </div>
        <div class="ach-item">
          <div class="ach-icon">📄</div>
          <div>
            <div class="ach-title">IEEE Conference Submission</div>
            <div class="ach-body">SRM Institute of Science & Technology, Kattankulathur — under review</div>
          </div>
        </div>
        <div class="ach-item">
          <div class="ach-icon">🧠</div>
          <div>
            <div class="ach-title">2,500+ Sample Validation</div>
            <div class="ach-body">Multimodal pipeline tested across LLM querying, VQA tasks, and patent e-filing workflows</div>
          </div>
        </div>
        <div class="feat-links">
          <a class="btn-feat-primary" href="https://rajaganaa.github.io/antahkarana-frontend/" target="_blank">⚡ live demo →</a>
          <a class="btn-feat-secondary" href="https://github.com/rajaganaa/antahkarana-reasoning-framework" target="_blank">github ↗</a>
        </div>
      </div>
    </div>

    <!-- P.002 -->
    <a class="proj-card reveal" href="https://github.com/rajaganaa/antahkarana-product" target="_blank">
      <div class="proj-top"><span class="proj-num">P.002</span><span class="proj-arrow">↗</span></div>
      <div class="proj-tags">
        <span class="proj-tag proj-tag-g">Agentic AI</span>
        <span class="proj-tag">Azure</span>
        <span class="proj-tag">Multimodal</span>
      </div>
      <h3 class="proj-title">Antahkarana Medical AI — Unified Reasoning Engine</h3>
      <p class="proj-desc">Full-stack medical AI assistant built on the Antahkarana framework. Deployed on Azure with a live frontend. Multimodal — processes text, images, and documents. CI/CD via GitHub Actions.</p>
      <div class="proj-metric">⚡ Deployed on Azure · CI/CD · 16 commits</div>
    </a>

    <!-- P.003 -->
    <a class="proj-card reveal" href="https://github.com/rajaganaa/MML_smart_campus_security_system" target="_blank">
      <div class="proj-top"><span class="proj-num">P.003</span><span class="proj-arrow">↗</span></div>
      <div class="proj-tags">
        <span class="proj-tag">Computer Vision</span>
        <span class="proj-tag">VLM</span>
        <span class="proj-tag">Multimodal</span>
      </div>
      <h3 class="proj-title">Multimodal Smart Campus Security System</h3>
      <p class="proj-desc">AI-driven surveillance and threat detection using Vision-Language Models (CLIP, BLIP) and Voice Biometrics. Solves the challenge of monitoring hundreds of CCTV feeds simultaneously.</p>
      <div class="proj-metric">⚡ OpenAI CLIP · Salesforce BLIP · PyTorch</div>
    </a>

    <!-- P.004 -->
    <a class="proj-card reveal" href="https://github.com/rajaganaa/AgentNet-Enterprise-Support" target="_blank">
      <div class="proj-top"><span class="proj-num">P.004</span><span class="proj-arrow">↗</span></div>
      <div class="proj-tags">
        <span class="proj-tag proj-tag-g">Multi-Agent</span>
        <span class="proj-tag">LLM-as-Judge</span>
        <span class="proj-tag">RAG</span>
      </div>
      <h3 class="proj-title">AgentNet — Enterprise Multi-Agent Support System</h3>
      <p class="proj-desc">Autonomous, self-correcting support system using multi-agent orchestration. Agents triage, respond, and self-grade output quality using LLM-as-a-Judge. Vector retrieval memory for contextual recall.</p>
      <div class="proj-metric">⚡ Self-reflection loop · Custom trace logging · Vertex AI</div>
    </a>

    <!-- P.005 -->
    <a class="proj-card reveal" href="https://github.com/rajaganaa/Hospital-Readmission-Predictor" target="_blank">
      <div class="proj-top"><span class="proj-num">P.005</span><span class="proj-arrow">↗</span></div>
      <div class="proj-tags">
        <span class="proj-tag">ML · XGBoost</span>
        <span class="proj-tag">Healthcare</span>
      </div>
      <h3 class="proj-title">Hospital Readmission Risk Predictor</h3>
      <p class="proj-desc">Predicts 30-day hospital readmission risk using AI-driven A1C imputation. Targets the $41B annual cost of preventable US readmissions. Clinical feature engineering + XGBoost pipeline.</p>
      <div class="proj-metric">⚡ Production-ready · Streamlit dashboard · Healthcare analytics</div>
    </a>

    <!-- P.006 -->
    <a class="proj-card reveal" href="https://github.com/rajaganaa/YouTube-Data-ETL-Pipeline" target="_blank">
      <div class="proj-top"><span class="proj-num">P.006</span><span class="proj-arrow">↗</span></div>
      <div class="proj-tags">
        <span class="proj-tag">Data Engineering</span>
        <span class="proj-tag">ETL · SQL</span>
      </div>
      <h3 class="proj-title">YouTube Data Harvesting & Warehousing Pipeline</h3>
      <p class="proj-desc">Automated ETL pipeline ingesting, cleaning, transforming, and loading YouTube creator data into a structured MySQL warehouse. Analytics-ready output for engagement trend analysis.</p>
      <div class="proj-metric">⚡ YouTube API · MySQL · pandas · Production ready</div>
    </a>

    <!-- P.007 -->
    <a class="proj-card reveal" href="https://github.com/rajaganaa/Industrial-HR-Geo-Dashboard" target="_blank">
      <div class="proj-top"><span class="proj-num">P.007</span><span class="proj-arrow">↗</span></div>
      <div class="proj-tags">
        <span class="proj-tag">Geo-Spatial</span>
        <span class="proj-tag">NLP</span>
        <span class="proj-tag">Streamlit</span>
      </div>
      <h3 class="proj-title">Industrial HR Geo-Visualisation Dashboard</h3>
      <p class="proj-desc">Geo-spatial + NLP dashboard mapping India's industrial workforce distribution across sectors. Combines choropleth visualisation with natural language querying for policy planning.</p>
      <div class="proj-metric">⚡ Research-prototype · Plotly · Folium · NLP queries</div>
    </a>

    <!-- P.008 -->
    <a class="proj-card reveal" href="https://github.com/rajaganaa/PhonePe-Transaction-Visualizer" target="_blank">
      <div class="proj-top"><span class="proj-num">P.008</span><span class="proj-arrow">↗</span></div>
      <div class="proj-tags">
        <span class="proj-tag">Data Viz</span>
        <span class="proj-tag">Fintech</span>
        <span class="proj-tag">MySQL</span>
      </div>
      <h3 class="proj-title">PhonePe Pulse Data Visualisation Dashboard</h3>
      <p class="proj-desc">Comprehensive analysis of India's digital payment ecosystem using PhonePe Pulse data. Visualises state-level adoption, transaction volumes, and payment category trends.</p>
      <div class="proj-metric">⚡ 100% Python · Streamlit · MySQL · Production ready</div>
    </a>

  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="sec-label">03 · SKILLS</div>
  <div class="skills-grid reveal">

    <div>
      <div class="skill-group-title">GENERATIVE AI · LLMs</div>
      <div class="skill-item"><span class="skill-name">LLM Orchestration</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div></div></div>
      <div class="skill-item"><span class="skill-name">RAG Pipelines · FAISS</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div></div></div>
      <div class="skill-item"><span class="skill-name">Prompt Engineering</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div></div></div>
      <div class="skill-item"><span class="skill-name">Agentic Workflows</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">LangChain · HuggingFace</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div></div></div>
    </div>

    <div>
      <div class="skill-group-title">MACHINE LEARNING · DL</div>
      <div class="skill-item"><span class="skill-name">PyTorch · TensorFlow</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">scikit-learn · XGBoost</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div></div></div>
      <div class="skill-item"><span class="skill-name">CNN · LSTM · Transformers</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">NLP · Embeddings</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">Computer Vision · OpenCV</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div></div></div>
    </div>

    <div>
      <div class="skill-group-title">DATA · ENGINEERING</div>
      <div class="skill-item"><span class="skill-name">Python</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div></div></div>
      <div class="skill-item"><span class="skill-name">SQL · MySQL · MongoDB</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">ETL Pipelines</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">Streamlit · Plotly</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div></div></div>
      <div class="skill-item"><span class="skill-name">pandas · NumPy</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div></div></div>
    </div>

    <div>
      <div class="skill-group-title">CLOUD · DEVOPS</div>
      <div class="skill-item"><span class="skill-name">AWS Solutions Architect</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">Azure · Docker</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div><div class="dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">Git · GitHub Actions</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">Linux · Bash</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div><div class="dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">R · SQL · NoSQL</span><div class="skill-dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot"></div><div class="dot"></div></div></div>
    </div>

  </div>
</section>

<!-- CERTIFICATIONS -->
<section id="certifications">
  <div class="sec-label">04 · CERTIFICATIONS</div>
  <div class="certs-grid reveal">

    <div class="cert-card"><div class="cert-icon">🎓</div><div><div class="cert-name">AI & ML Professional Program</div><div class="cert-issuer">GUVI · IIT-M · May 2024</div></div></div>
    <div class="cert-card"><div class="cert-icon">☁️</div><div><div class="cert-name">AWS Certified Solutions Architect Associate</div><div class="cert-issuer">Udemy · Oct 2025</div></div></div>
    <div class="cert-card"><div class="cert-icon">🤖</div><div><div class="cert-name">5-Day AI Agents Intensive with Google</div><div class="cert-issuer">Kaggle · Dec 2025</div></div></div>
    <div class="cert-card"><div class="cert-icon">⚙️</div><div><div class="cert-name">DevOps Beginners to Advanced with Projects</div><div class="cert-issuer">Udemy · Jul 2025</div></div></div>
    <div class="cert-card"><div class="cert-icon">🔗</div><div><div class="cert-name">Introduction to Internet of Things</div><div class="cert-issuer">NPTEL · Oct 2025</div></div></div>
    <div class="cert-card"><div class="cert-icon">🖥️</div><div><div class="cert-name">Certificate Professional — Advanced Programming</div><div class="cert-issuer">IIT-M · May 2024</div></div></div>
    <div class="cert-card"><div class="cert-icon">👁️</div><div><div class="cert-name">OpenCV Certification</div><div class="cert-issuer">OpenCV University · Mar 2025</div></div></div>
    <div class="cert-card"><div class="cert-icon">🔥</div><div><div class="cert-name">PyTorch & TensorFlow for Deep Learning</div><div class="cert-issuer">Simplilearn · Nov 2024</div></div></div>
    <div class="cert-card"><div class="cert-icon">🐍</div><div><div class="cert-name">Advanced Python Course</div><div class="cert-issuer">GUVI · IIT-M · Feb 2024</div></div></div>
    <div class="cert-card"><div class="cert-icon">📊</div><div><div class="cert-name">DSA · Data Structures & Algorithms</div><div class="cert-issuer">Simplilearn · Nov 2024</div></div></div>

  </div>
</section>

<!-- BLOG -->
<section id="blog">
  <div class="sec-label">05 · BLOG</div>
  <div class="blog-grid reveal">

    <div class="blog-card" onclick="openBlog(0)">
      <div class="blog-meta"><span class="blog-date">MAY 2026</span><span class="blog-arrow">↗</span></div>
      <span class="blog-tag">CAREER · AI</span>
      <h3 class="blog-title">From Electrical Engineer to AI Engineer — What Really Transfers</h3>
      <p class="blog-excerpt">Nine years of high-voltage systems taught me things no AI course ever could. Here's what actually crosses over — and what doesn't.</p>
      <div class="blog-readtime">⏱ 6 min read</div>
    </div>

    <div class="blog-card" onclick="openBlog(1)">
      <div class="blog-meta"><span class="blog-date">APR 2026</span><span class="blog-arrow">↗</span></div>
      <span class="blog-tag">LLM · RESEARCH</span>
      <h3 class="blog-title">How I Built Antahkarana — A Cognitively-Inspired Reasoning Framework</h3>
      <p class="blog-excerpt">Most LLM pipelines are glorified prompt chains. Antahkarana is different — it routes queries through Vedantic cognitive stages. Here's the architecture and why it works.</p>
      <div class="blog-readtime">⏱ 9 min read</div>
    </div>

    <div class="blog-card" onclick="openBlog(2)">
      <div class="blog-meta"><span class="blog-date">MAR 2026</span><span class="blog-arrow">↗</span></div>
      <span class="blog-tag">AGENTIC AI</span>
      <h3 class="blog-title">RAG vs Fine-Tuning: Lessons from Building a Medical AI Assistant</h3>
      <p class="blog-excerpt">When building Antahkarana's medical reasoning engine, I had to choose between RAG and fine-tuning for every sub-task. Here's the decision framework I developed.</p>
      <div class="blog-readtime">⏱ 7 min read</div>
    </div>

  </div>
</section>

<!-- THE EDGE -->
<section id="edge" style="background:var(--bg2);">
  <div class="sec-label">06 · THE EDGE</div>
  <div class="edge-grid">

    <div class="edge-card reveal">
      <div class="edge-label">WHAT MOST CANDIDATES DON'T HAVE</div>
      <h3 class="edge-heading">A filed patent <em>and</em> a live product.</h3>
      <p class="edge-body">Most M.Tech students build class projects. Rajaganapathy filed an Indian patent (App. 202641043947), submitted an IEEE paper, and deployed a live medical AI product on Azure — in the same academic cycle.</p>
    </div>

    <div class="edge-card reveal">
      <div class="edge-label">THE ENGINEERING MINDSET</div>
      <h3 class="edge-heading">Builds AI that <em>can't fail.</em></h3>
      <p class="edge-body">9 years maintaining 500 kVA transformers and 400 kW motors in live industrial environments teaches you one thing: systems must work under every condition. That discipline is rare in AI — and it shows.</p>
    </div>

    <div class="edge-card reveal">
      <div class="edge-label">THE RESEARCH PROOF</div>
      <h3 class="edge-heading">2,500 samples. <em>Novel contribution.</em></h3>
      <p class="edge-body">Antahkarana's Vedantic cognitive routing was validated across 2,500 LLM/VLM samples — earning both a patent filing and an IEEE conference submission. Not a class project. Original research.</p>
    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="sec-label">07 · CONTACT</div>
  <div class="contact-grid">
    <div class="reveal">
      <h2 class="contact-heading">Ready to build<br/>at <span>Google scale.</span></h2>
      <p class="contact-sub">
        Most candidates bring a degree. I bring 9+ years of engineering under real-world pressure,
        a filed patent, a live Azure deployment, and an IEEE paper under review —
        all from a 2-year M.Tech programme.
        If you're building infrastructure that has to work at scale, I already think that way.
      </p>
      <div style="display:flex;gap:1rem;flex-wrap:wrap;">
        <a class="btn-primary" href="mailto:rajaganaa@gmail.com">send me an email →</a>
        <a class="btn-outline" href="https://www.linkedin.com/in/raja-ganapathy-36b00658" target="_blank">linkedin ↗</a>
      </div>
    </div>
    <div class="contact-links reveal">
      <a class="contact-link" href="mailto:rajaganaa@gmail.com">
        <span>✉ Email</span><span class="contact-link-val">rajaganaa@gmail.com</span>
      </a>
      <a class="contact-link" href="tel:+919176631419">
        <span>📞 Phone</span><span class="contact-link-val">+91 9176631419</span>
      </a>
      <a class="contact-link" href="https://www.linkedin.com/in/raja-ganapathy-36b00658" target="_blank">
        <span>in LinkedIn</span><span class="contact-link-val">raja-ganapathy-36b00658</span>
      </a>
      <a class="contact-link" href="https://github.com/rajaganaa" target="_blank">
        <span>⌥ GitHub</span><span class="contact-link-val">github.com/rajaganaa</span>
      </a>
      <a class="contact-link" href="https://x.com/rajaganaa" target="_blank">
        <span>𝕏 Twitter / X</span><span class="contact-link-val">@rajaganaa</span>
      </a>
      <div class="contact-link" style="cursor:default;">
        <span>📍 Location</span><span class="contact-link-val">Chennai, India · Open to remote</span>
      </div>
    </div>
  </div>
</section>

<!-- BLOG MODAL -->
<div class="modal-overlay" id="blogModal" onclick="closeOnOverlay(event)">
  <div class="modal">
    <button class="modal-close" onclick="closeBlog()">✕ close</button>
    <div class="modal-tag" id="modalTag"></div>
    <h2 class="modal-title" id="modalTitle"></h2>
    <div class="modal-date" id="modalDate"></div>
    <div class="modal-body" id="modalBody"></div>
  </div>
</div>

<footer>
  <p>© 2026 Rajaganapathy M — AI Engineer · Chennai, India</p>
  <p>Patent pending · IEEE under review · Open to world-class opportunities</p>
</footer>

<script>
// ── SCROLL REVEAL ──
const observer = new IntersectionObserver((entries) => {
  entries.forEach((e, i) => {
    if (e.isIntersecting) {
      setTimeout(() => e.target.classList.add('visible'), (i % 4) * 90);
      observer.unobserve(e.target);
    }
  });
}, { threshold: 0.08 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

// ── THEME TOGGLE ──
const toggle = document.getElementById('themeToggle');
let light = false;

const lightCSS = `
  body { --bg:#f4f2ed; --bg2:#ece9e2; --bg3:#e2dfd8; --bg4:#d8d5ce;
    --border:rgba(0,0,0,0.07); --border-md:rgba(0,0,0,0.13); --border-hi:rgba(0,0,0,0.22);
    --text:#18180f; --text-2:#5a5750; --text-3:#9a9890;
    --green:#4a9400; --blue:#006ea0; --nav-h:72px; }
  nav { background: rgba(244,242,237,0.92) !important; }
  .hero-grid { background-image: linear-gradient(rgba(0,0,0,0.03) 1px,transparent 1px),linear-gradient(90deg,rgba(0,0,0,0.03) 1px,transparent 1px) !important; }
  .dot { background: var(--bg4) !important; }
`;
let lightStyle = null;

toggle.addEventListener('click', () => {
  light = !light;
  toggle.textContent = light ? '☾ dark' : '☀ light';
  if (light) {
    lightStyle = document.createElement('style');
    lightStyle.id = 'light-override';
    lightStyle.textContent = lightCSS;
    document.head.appendChild(lightStyle);
  } else {
    document.getElementById('light-override')?.remove();
  }
});

// ── CV DOWNLOAD ──
function downloadCV(e) {
  if (e) e.preventDefault();
  const genDate = new Date().toLocaleDateString('en-GB', {month:'long', year:'numeric'});
  const html = `<!DOCTYPE html>
<html><head><meta charset="UTF-8"/>
<title>Rajaganapathy M — CV</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:'DM Sans',sans-serif;color:#18180f;background:#fff;font-size:14px;line-height:1.65;padding:3rem 4rem;}
@media print{body{padding:1.5rem 2rem;}}
h1{font-family:'DM Sans',sans-serif;font-size:2.4rem;font-weight:700;letter-spacing:-0.02em;margin-bottom:0.2rem;}
.sub{font-family:'DM Mono',monospace;font-size:11px;color:#4a9400;letter-spacing:0.1em;margin-bottom:0.75rem;}
.bar{font-family:'DM Mono',monospace;font-size:11px;color:#5a5750;display:flex;flex-wrap:wrap;gap:1.25rem;margin-bottom:1.5rem;padding-bottom:1rem;border-bottom:2px solid #18180f;}
.bdg{display:inline-flex;gap:0.5rem;flex-wrap:wrap;margin-bottom:1.5rem;}
.b{font-family:'DM Mono',monospace;font-size:10px;border:1px solid #4a9400;color:#4a9400;padding:2px 9px;}
h2{font-family:'DM Mono',monospace;font-size:10px;font-weight:500;letter-spacing:0.18em;color:#4a9400;margin:1.5rem 0 0.6rem;padding-bottom:3px;border-bottom:1px solid #e0ddd6;}
.sum{font-size:13px;font-weight:300;color:#3a3830;line-height:1.85;}
.ei{margin-bottom:1rem;}
.eh{display:flex;justify-content:space-between;align-items:baseline;}
.er{font-weight:600;font-size:14px;}
.ed{font-family:'DM Mono',monospace;font-size:10px;color:#5a5750;}
.eo{font-family:'DM Mono',monospace;font-size:11px;color:#5a5750;margin-bottom:3px;}
.ex{font-size:12px;font-weight:300;color:#5a5750;line-height:1.75;}
.pg{display:grid;grid-template-columns:1fr 1fr;gap:0.75rem;}
.pi{border:1px solid #e0ddd6;padding:0.75rem;}
.pn{font-weight:600;font-size:13px;margin-bottom:2px;}
.pt{font-family:'DM Mono',monospace;font-size:10px;color:#5a5750;}
.sc{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem;}
.sg{font-weight:600;font-size:12px;margin-bottom:4px;}
.sl{font-family:'DM Mono',monospace;font-size:11px;font-weight:300;color:#5a5750;line-height:1.85;}
.cl{display:grid;grid-template-columns:1fr 1fr;gap:4px;}
.ce{font-family:'DM Mono',monospace;font-size:11px;font-weight:300;color:#5a5750;}
.ce span{color:#18180f;font-weight:500;}
.ft{margin-top:2rem;padding-top:1rem;border-top:1px solid #e0ddd6;font-family:'DM Mono',monospace;font-size:10px;color:#9a9890;display:flex;justify-content:space-between;}
</style></head><body>
<h1>Rajaganapathy M</h1>
<div class="sub">AI / ML ENGINEER · LLM · AGENTIC AI · RAG · MULTI-AGENT SYSTEMS</div>
<div class="bar">
  <span>✉ rajaganaa@gmail.com</span><span>📞 +91 9176631419</span>
  <span>🌐 rajaganaa.github.io</span><span>in raja-ganapathy-36b00658</span>
  <span>⌥ github.com/rajaganaa</span><span>📍 Chennai, India</span>
</div>
<div class="bdg">
  <span class="b">⚡ PATENT FILED · APR 2026</span>
  <span class="b">📄 IEEE PAPER SUBMITTED</span>
  <span class="b">🎓 M.TECH AI · 9.6 CGPA</span>
  <span class="b">9+ YRS ENGINEERING</span>
</div>
<h2>PROFILE</h2>
<p class="sum">Engineering professional with 9+ years of industry experience now specialising in AI/ML. M.Tech Artificial Intelligence at SRM Institute (CGPA 9.6/10). Filed Indian Patent (No. 202641043947) for the Antahkarana cognitively-inspired reasoning framework; IEEE Conference paper submitted. Skills span LLMs, Agentic AI, RAG pipelines, multi-agent systems, computer vision, and data engineering. Brings production engineering discipline — safety-critical systems, project management, hard-constraint delivery — to every AI build.</p>
<h2>EDUCATION</h2>
<div class="ei"><div class="eh"><span class="er">M.Tech — Artificial Intelligence</span><span class="ed">2024 – Present</span></div><div class="eo">SRM Institute of Science & Technology · Chennai · CGPA: 9.6 / 10</div></div>
<div class="ei"><div class="eh"><span class="er">B.E — Electrical & Electronics Engineering</span><span class="ed">2013</span></div><div class="eo">Thangavelu Engineering College · Chennai</div></div>
<h2>RESEARCH & IP</h2>
<div class="ei"><div class="er">Indian Patent Filed — Antahkarana System</div><div class="eo">Application No. 202641043947 · Filed April 3, 2026</div><div class="ex">Cognitively-inspired adaptive reasoning framework for LLMs and VLMs. System design protected under Indian IP law.</div></div>
<div class="ei"><div class="er">IEEE Conference Paper — Submitted</div><div class="eo">SRM Institute of Science & Technology, Kattankulathur</div><div class="ex">Antahkarana: Cognitively-Inspired Adaptive Reasoning for LLMs and VLMs. Under review.</div></div>
<h2>KEY PROJECTS</h2>
<div class="pg">
  <div class="pi"><div class="pn">Antahkarana Reasoning Framework</div><div class="pt">Python · Qwen · BLIP-3 · Patent filed · IEEE submitted</div></div>
  <div class="pi"><div class="pn">Antahkarana Medical AI (Live)</div><div class="pt">Azure · GitHub Actions CI/CD · Multimodal · Full-stack</div></div>
  <div class="pi"><div class="pn">MML Smart Campus Security</div><div class="pt">OpenAI CLIP · Salesforce BLIP · PyTorch · Voice Biometrics</div></div>
  <div class="pi"><div class="pn">AgentNet Enterprise Support</div><div class="pt">Multi-agent · LLM-as-Judge · RAG · Vertex AI</div></div>
  <div class="pi"><div class="pn">Hospital Readmission Predictor</div><div class="pt">XGBoost · Streamlit · Healthcare analytics</div></div>
  <div class="pi"><div class="pn">YouTube Data ETL Pipeline</div><div class="pt">Python · MySQL · YouTube API · Production ready</div></div>
</div>
<h2>PROFESSIONAL EXPERIENCE</h2>
<div class="ei"><div class="eh"><span class="er">Electrical Construction Site Engineer</span><span class="ed">Jan 2017 – Jun 2023</span></div><div class="eo">SR Electrical Works · Chennai</div><div class="ex">Large-scale electrical systems for construction projects. Led budget estimation, resource allocation, site supervision, and cross-team coordination under hard safety constraints.</div></div>
<div class="ei"><div class="eh"><span class="er">Electrical Maintenance Engineer</span><span class="ed">Dec 2014 – Dec 2016</span></div><div class="eo">Mod Forge Pvt. Ltd. · ISO/TS 16949 Certified · Chennai</div><div class="ex">O&M of 500 kVA transformer, 250 kVA DG, motors up to 400 kW, power factor correction panels and automation under C-certificate supervision.</div></div>
<h2>TECHNICAL SKILLS</h2>
<div class="sc">
  <div><div class="sg">Generative AI / LLMs</div><div class="sl">LLM Orchestration<br/>RAG · FAISS · Vector DBs<br/>Prompt Engineering<br/>Agentic Workflows<br/>LangChain · HuggingFace</div></div>
  <div><div class="sg">ML / Deep Learning</div><div class="sl">PyTorch · TensorFlow<br/>scikit-learn · XGBoost<br/>CNN · LSTM · Transformers<br/>NLP · Embeddings<br/>Computer Vision · OpenCV</div></div>
  <div><div class="sg">Cloud / DevOps / Data</div><div class="sl">AWS · Azure · Docker<br/>Git · GitHub Actions CI/CD<br/>Python · SQL · MongoDB<br/>Streamlit · Plotly<br/>Linux · Bash · R</div></div>
</div>
<h2>CERTIFICATIONS</h2>
<div class="cl">
  <div class="ce"><span>AWS</span> Solutions Architect Associate · Udemy 2025</div>
  <div class="ce"><span>GUVI</span> AI &amp; ML Professional Program · IIT-M 2024</div>
  <div class="ce"><span>Kaggle</span> 5-Day AI Agents Intensive with Google · 2025</div>
  <div class="ce"><span>DevOps</span> Beginners to Advanced · Udemy 2025</div>
  <div class="ce"><span>NPTEL</span> Introduction to Internet of Things · 2025</div>
  <div class="ce"><span>IIT-M</span> Certificate Professional · Advanced Programming 2024</div>
  <div class="ce"><span>OpenCV</span> OpenCV University Certification · 2025</div>
  <div class="ce"><span>Simplilearn</span> PyTorch · TensorFlow · DSA · GIT · MongoDB</div>
</div>
<div class="ft"><span>rajaganaa.github.io · github.com/rajaganaa</span><span>Generated ${genDate}</span></div>
</body></html>`;

  const blob = new Blob([html], {type:'text/html'});
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url; a.download = 'Rajaganapathy_M_CV.html';
  a.click(); URL.revokeObjectURL(url);
}

// ── BLOG MODAL ──
const blogs = [
  {
    tag: 'CAREER · AI',
    date: 'May 2026 · 6 min read',
    title: 'From Electrical Engineer to AI Engineer — What Really Transfers',
    body: `<p>In June 2023, after nine years of working on electrical systems across industrial sites in Chennai, I quit my job. Not because I was failing — I was good at it. I quit because I wanted to build a different kind of system.</p>
<h3>What I thought would transfer</h3>
<p>I assumed the engineering fundamentals would carry over: systems thinking, problem decomposition, reading technical documentation. I was right about those. What surprised me was <em>how much deeper</em> that transfer went.</p>
<p>In industrial electrical work, you build things that operate continuously under unpredictable conditions. A 500 kVA transformer doesn't get to fail at 3am because the load spiked. You design for failure modes before they happen. You think about what the system does when something unexpected occurs — not just what it does when everything is normal.</p>
<p>That mindset is rare in AI engineering. Most ML practitioners optimise for the happy path. They tune accuracy on the test set and ship. My instinct is always: <strong>what happens at the edge cases?</strong></p>
<h3>What actually doesn't transfer</h3>
<p>Mathematics. I had to rebuild from scratch — linear algebra, probability theory, calculus. This took six months of uncomfortable work before I could read ML papers without feeling lost.</p>
<h3>The unexpected advantage</h3>
<p>The biggest transfer no one talks about: <em>project management in safety-critical environments</em>. When you've coordinated electrical installation across a live construction site — managing contractors, clients, timelines, and regulations simultaneously — running a complex ML project feels almost straightforward by comparison. The stakes are different, but the discipline is the same.</p>
<p>I don't regret the nine years. They made me a better AI engineer than I would have been if I'd started at 22.</p>`
  },
  {
    tag: 'LLM · RESEARCH',
    date: 'April 2026 · 9 min read',
    title: 'How I Built Antahkarana — A Cognitively-Inspired Reasoning Framework',
    body: `<p>Most LLM pipelines are, at their core, sophisticated prompt chains. You send a query, you get a response. Maybe you add retrieval. Maybe you add a tool call. But the fundamental architecture is linear: input → model → output.</p>
<p>Antahkarana is different. It routes complex queries through specialised cognitive stages — each responsible for a distinct aspect of reasoning — before synthesising a final response. The inspiration came from an unlikely source: Vedantic philosophy.</p>
<h3>The cognitive architecture</h3>
<p>In Vedantic thought, the <em>antahkarana</em> is the inner instrument of the mind — four distinct functions: <strong>manas</strong> (perception and doubt), <strong>buddhi</strong> (discrimination and decision), <strong>chitta</strong> (memory and conditioning), and <strong>ahamkara</strong> (the ego that integrates everything into a coherent self).</p>
<p>I mapped these directly to LLM reasoning stages. Manas handles initial query parsing and ambiguity detection. Buddhi routes the query to the appropriate specialised module. Chitta manages retrieval memory via FAISS vector search. The integration layer synthesises outputs without the "ego" problem — no single module dominates; the best answer wins.</p>
<h3>Why it works better</h3>
<p>The key insight is that different reasoning tasks require different cognitive postures. A factual retrieval query should not be processed the same way as a complex multi-step inference problem. By routing explicitly, Antahkarana applies the right tool to the right task — and the 2,500-sample validation showed measurable improvements in coherence on complex multimodal queries.</p>
<p>The patent covers the routing and decision architecture. The IEEE paper covers the full experimental methodology. The framework is at github.com/rajaganaa/antahkarana-reasoning-framework.</p>`
  },
  {
    tag: 'AGENTIC AI',
    date: 'March 2026 · 7 min read',
    title: 'RAG vs Fine-Tuning: Lessons from Building a Medical AI Assistant',
    body: `<p>When I started building the Antahkarana medical AI assistant, I had to make the RAG vs. fine-tuning decision for every sub-task. After months of building and testing, here's the framework I arrived at.</p>
<h3>The question is wrong</h3>
<p>The industry frames this as a binary choice. It isn't. The real question is: <em>what is the nature of the knowledge this task requires?</em></p>
<p><strong>RAG wins</strong> when the knowledge is: external and updatable (medical guidelines change), verifiable (you need citations), or domain-specific and voluminous. For the medical assistant, this was almost everything.</p>
<p><strong>Fine-tuning wins</strong> when the task requires: a specific output format the base model can't reliably produce, internalised reasoning patterns (not facts), or latency-critical inference where retrieval overhead is unacceptable.</p>
<h3>What I actually did</h3>
<p>The Antahkarana medical system uses RAG for factual retrieval and prompting for output formatting and clinical tone. The retrieval runs against a FAISS index of structured medical knowledge.</p>
<p>The biggest lesson: <em>don't fine-tune to fix retrieval problems</em>. If your RAG pipeline is returning poor context, fine-tuning the generator won't help — it'll just learn to hallucinate more confidently. Fix the retrieval first.</p>
<p>The live system is deployed at rajaganaa.github.io/antahkarana-frontend. It's multimodal — accepts text, images, and documents. Backend on Azure Container Instances. CI/CD via GitHub Actions.</p>`
  }
];

function openBlog(i) {
  const b = blogs[i];
  document.getElementById('modalTag').textContent = b.tag;
  document.getElementById('modalTitle').textContent = b.title;
  document.getElementById('modalDate').textContent = b.date;
  document.getElementById('modalBody').innerHTML = b.body;
  document.getElementById('blogModal').classList.add('open');
  document.body.style.overflow = 'hidden';
}
function closeBlog() {
  document.getElementById('blogModal').classList.remove('open');
  document.body.style.overflow = '';
}
function closeOnOverlay(e) {
  if (e.target === document.getElementById('blogModal')) closeBlog();
}
document.addEventListener('keydown', e => { if (e.key === 'Escape') closeBlog(); });
</script>

</body>
</html>
