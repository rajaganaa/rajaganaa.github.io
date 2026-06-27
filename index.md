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

body::after {
  content: '';
  position: fixed; inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.035'/%3E%3C/svg%3E");
  pointer-events: none; z-index: 9999; opacity: 0.5;
}

.f-display { font-family: 'Bebas Neue', sans-serif; letter-spacing: 0.01em; }
.f-sans    { font-family: 'DM Sans', sans-serif; }
.f-mono    { font-family: 'DM Mono', monospace; }

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

.proj-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
  gap: 1px;
  background: var(--border);
}

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
  cursor: pointer;
  text-decoration: none; color: inherit;
}
.cert-card:hover { background: var(--bg3); }
.cert-card:hover .cert-verify { opacity: 1; }
.cert-verify {
  margin-left: auto; align-self: center; flex-shrink: 0;
  font-family: 'DM Mono', monospace;
  font-size: 9px; letter-spacing: 0.08em;
  color: var(--green); opacity: 0;
  transition: opacity 0.15s;
}
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

/* ── NEW: RESEARCH SECTION ── */
.research-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1px;
  background: var(--border);
  margin-bottom: 4rem;
}
.research-card {
  background: var(--bg);
  padding: 2.5rem;
  position: relative;
  transition: background 0.15s;
}
.research-card:hover { background: var(--bg3); }
.research-card.featured {
  border: 1px solid rgba(184,240,80,0.2);
  background: var(--bg2);
}
.research-label {
  font-family: 'DM Mono', monospace;
  font-size: 9px; letter-spacing: 0.22em;
  color: var(--green); margin-bottom: 1rem;
  display: flex; align-items: center; gap: 0.5rem;
}
.research-label::before {
  content: '';
  width: 5px; height: 5px; border-radius: 50%;
  background: var(--green);
  box-shadow: 0 0 8px rgba(184,240,80,0.6);
  flex-shrink: 0;
}
.research-title {
  font-family: 'DM Sans', sans-serif;
  font-size: 1.1rem; font-weight: 600;
  color: var(--text); line-height: 1.4; margin-bottom: 0.75rem;
}
.research-authors {
  font-family: 'DM Mono', monospace;
  font-size: 10px; color: var(--text-3);
  margin-bottom: 0.75rem; letter-spacing: 0.04em;
}
.research-authors strong { color: var(--green); }
.research-venue {
  font-family: 'DM Mono', monospace;
  font-size: 10px; color: var(--blue);
  margin-bottom: 1rem; letter-spacing: 0.06em;
}
.research-abstract {
  font-family: 'DM Sans', sans-serif;
  font-size: 12.5px; font-weight: 300;
  color: var(--text-2); line-height: 1.85;
  margin-bottom: 1.5rem;
}
.research-links { display: flex; gap: 0.6rem; flex-wrap: wrap; }
.research-link {
  font-family: 'DM Mono', monospace;
  font-size: 10px; letter-spacing: 0.08em;
  padding: 0.4rem 1rem;
  border: 1px solid var(--border-md);
  color: var(--text-2); text-decoration: none;
  transition: all 0.15s;
  display: inline-flex; align-items: center; gap: 0.35rem;
}
.research-link:hover { border-color: var(--text); color: var(--text); }
.research-link.green { border-color: rgba(184,240,80,0.4); color: var(--green); }
.research-link.green:hover { background: rgba(184,240,80,0.07); }
.research-link.blue { border-color: rgba(80,200,240,0.4); color: var(--blue); }

/* ── NEW: RESEARCHER IDs PANEL ── */
.researcher-ids {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1px;
  background: var(--border);
  margin-bottom: 2rem;
}
.rid-card {
  background: var(--bg2);
  padding: 1.75rem;
  text-decoration: none;
  transition: background 0.15s;
  display: flex; align-items: flex-start; gap: 1rem;
}
.rid-card:hover { background: var(--bg3); }
.rid-card:hover .rid-arrow { transform: translate(3px, -3px); }
.rid-icon {
  width: 36px; height: 36px; border-radius: 4px;
  display: flex; align-items: center; justify-content: center;
  font-size: 14px; flex-shrink: 0;
  border: 1px solid var(--border-md);
}
.rid-icon.orcid { background: rgba(166,206,57,0.1); border-color: rgba(166,206,57,0.4); }
.rid-icon.scholar { background: rgba(66,133,244,0.1); border-color: rgba(66,133,244,0.4); }
.rid-icon.hf { background: rgba(255,160,0,0.1); border-color: rgba(255,160,0,0.4); }
.rid-icon.gs { background: rgba(80,200,240,0.1); border-color: rgba(80,200,240,0.4); }
.rid-label {
  font-family: 'DM Mono', monospace;
  font-size: 9px; letter-spacing: 0.18em; margin-bottom: 4px;
}
.rid-label.orcid { color: #a6ce39; }
.rid-label.scholar { color: #4285f4; }
.rid-label.hf { color: var(--orange); }
.rid-label.gs { color: var(--blue); }
.rid-value {
  font-family: 'DM Mono', monospace;
  font-size: 11px; color: var(--text-2);
  word-break: break-all; line-height: 1.5;
}
.rid-arrow {
  margin-left: auto; font-size: 12px;
  color: var(--text-3); flex-shrink: 0;
  transition: transform 0.15s; align-self: center;
}

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

footer {
  border-top: 1px solid var(--border);
  padding: 2rem 3rem;
  display: flex; justify-content: space-between; align-items: center;
}
footer p {
  font-family: 'DM Mono', monospace;
  font-size: 11px; color: var(--text-3); letter-spacing: 0.06em;
}

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(22px); }
  to   { opacity: 1; transform: translateY(0); }
}
.reveal {
  opacity: 0; transform: translateY(18px);
  transition: opacity 0.65s ease, transform 0.65s ease;
}
.reveal.visible { opacity: 1; transform: none; }

@media (max-width: 768px) {
  nav { padding: 0 1.5rem; }
  .nav-links { display: none; }
  .hero { padding: calc(var(--nav-h) + 3rem) 1.5rem 3rem; }
  .hero-name, .hero-name-accent { font-size: clamp(4rem, 16vw, 6rem); }
  section { padding: 4.5rem 1.5rem; }
  .about-grid, .contact-grid, .proj-featured, .research-grid { grid-template-columns: 1fr; }
  .feat-left { border-right: none; border-bottom: 1px solid rgba(184,240,80,0.1); }
  .hero-stats { display: none; }
  .hero-scroll { left: 1.5rem; }
  footer { padding: 1.5rem; flex-direction: column; gap: 0.5rem; text-align: center; }
}

.cv-modal-overlay {
  display: none; position: fixed; inset: 0;
  background: rgba(0,0,0,0.85); z-index: 600;
  align-items: flex-start; justify-content: center;
  padding: 2rem 1rem; overflow-y: auto;
  backdrop-filter: blur(12px);
}
.cv-modal-overlay.open { display: flex; }
.cv-modal {
  background: var(--bg2); border: 1px solid rgba(184,240,80,0.2);
  max-width: 860px; width: 100%; position: relative;
  box-shadow: 0 0 80px rgba(184,240,80,0.06);
  animation: fadeUp 0.3s ease forwards;
}
.cv-modal-bar {
  display: flex; align-items: center; justify-content: space-between;
  padding: 1rem 1.5rem;
  background: var(--bg); border-bottom: 1px solid var(--border);
  position: sticky; top: 0; z-index: 10;
  flex-wrap: wrap; gap: 0.5rem;
}
.cv-modal-bar-left {
  font-family: 'DM Mono', monospace;
  font-size: 11px; letter-spacing: 0.14em; color: var(--green);
  display: flex; align-items: center; gap: 0.75rem;
}
.cv-modal-bar-left::before {
  content: ''; display: block; width: 6px; height: 6px;
  background: var(--green); border-radius: 50%;
  box-shadow: 0 0 8px rgba(184,240,80,0.6);
}
.cv-modal-actions { display: flex; gap: 0.5rem; flex-wrap: wrap; }
.cv-btn-dl {
  font-family: 'DM Mono', monospace;
  font-size: 11px; letter-spacing: 0.08em;
  padding: 0.45rem 1.1rem;
  background: var(--green); color: #080808;
  border: none; cursor: pointer; font-weight: 500;
  transition: all 0.15s;
}
.cv-btn-dl:hover { background: #ccff55; transform: translateY(-1px); }
.cv-btn-print {
  font-family: 'DM Mono', monospace;
  font-size: 11px; letter-spacing: 0.08em;
  padding: 0.45rem 1.1rem;
  background: var(--blue); color: #080808;
  border: none; cursor: pointer; font-weight: 500;
  transition: all 0.15s;
}
.cv-btn-print:hover { background: #7adcff; transform: translateY(-1px); }
.cv-btn-close {
  font-family: 'DM Mono', monospace;
  font-size: 11px; letter-spacing: 0.08em;
  padding: 0.45rem 1rem;
  background: none; border: 1px solid var(--border-md);
  color: var(--text-2); cursor: pointer;
  transition: all 0.15s;
}
.cv-btn-close:hover { border-color: var(--text); color: var(--text); }
.cv-modal-inner {
  padding: 3rem 4rem;
  background: #fff; color: #18180f;
  font-family: 'DM Sans', sans-serif;
}
.cv-h1 { font-size: 2.2rem; font-weight: 700; letter-spacing: -0.02em; margin-bottom: 0.2rem; color: #18180f; }
.cv-sub { font-family: 'DM Mono', monospace; font-size: 11px; color: #4a9400; letter-spacing: 0.1em; margin-bottom: 0.75rem; }
.cv-bar { font-family: 'DM Mono', monospace; font-size: 11px; color: #5a5750; display: flex; flex-wrap: wrap; gap: 1.25rem; margin-bottom: 1.5rem; padding-bottom: 1rem; border-bottom: 2px solid #18180f; }
.cv-bdg { display: inline-flex; gap: 0.5rem; flex-wrap: wrap; margin-bottom: 1.5rem; }
.cv-b { font-family: 'DM Mono', monospace; font-size: 10px; border: 1px solid #4a9400; color: #4a9400; padding: 2px 9px; }
.cv-h2 { font-family: 'DM Mono', monospace; font-size: 10px; font-weight: 500; letter-spacing: 0.18em; color: #4a9400; margin: 1.5rem 0 0.6rem; padding-bottom: 3px; border-bottom: 1px solid #e0ddd6; }
.cv-sum { font-size: 13px; font-weight: 300; color: #3a3830; line-height: 1.85; }
.cv-ei { margin-bottom: 1rem; }
.cv-eh { display: flex; justify-content: space-between; align-items: baseline; }
.cv-er { font-weight: 600; font-size: 14px; color: #18180f; }
.cv-ed { font-family: 'DM Mono', monospace; font-size: 10px; color: #5a5750; }
.cv-eo { font-family: 'DM Mono', monospace; font-size: 11px; color: #5a5750; margin-bottom: 3px; }
.cv-ex { font-size: 12px; font-weight: 300; color: #5a5750; line-height: 1.75; }
.cv-pg { display: grid; grid-template-columns: 1fr 1fr; gap: 0.75rem; }
.cv-pi { border: 1px solid #e0ddd6; padding: 0.75rem; }
.cv-pn { font-weight: 600; font-size: 13px; margin-bottom: 2px; color: #18180f; }
.cv-pt { font-family: 'DM Mono', monospace; font-size: 10px; color: #5a5750; }
.cv-sc { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem; }
.cv-sg { font-weight: 600; font-size: 12px; margin-bottom: 4px; color: #18180f; }
.cv-sl { font-family: 'DM Mono', monospace; font-size: 11px; font-weight: 300; color: #5a5750; line-height: 1.85; }
.cv-cl { display: grid; grid-template-columns: 1fr 1fr; gap: 4px; }
.cv-ce { font-family: 'DM Mono', monospace; font-size: 11px; font-weight: 300; color: #5a5750; }
.cv-ce span { color: #18180f; font-weight: 500; }
.cv-ft { margin-top: 2rem; padding-top: 1rem; border-top: 1px solid #e0ddd6; font-family: 'DM Mono', monospace; font-size: 10px; color: #9a9890; display: flex; justify-content: space-between; }
@media (max-width: 768px) {
  .cv-modal-inner { padding: 1.5rem; }
  .cv-pg, .cv-sc, .cv-cl { grid-template-columns: 1fr; }
  .cv-modal-bar { flex-direction: column; align-items: flex-start; }
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
    <li><a href="#research">research</a></li>
    <li><a href="#certifications">certs</a></li>
    <li><a href="#blog">blog</a></li>
    <li><a href="#resume">resume</a></li>
    <li><a href="#contact">contact</a></li>
    <li><a href="https://youtube.com/@rajaganaaAI" target="_blank" style="color:var(--green);">▶ youtube</a></li>
    <li><a href="https://anbuclinic.me" target="_blank" style="color:var(--green);font-weight:600;border:1px solid rgba(184,240,80,0.4);padding:2px 8px;">🏥 live</a></li>
  </ul>
  <div class="nav-right">
    <button class="btn-nav" id="themeToggle">☀ light</button>
    <button class="btn-nav" onclick="openCVModal()">↓ cv</button>
    <a class="btn-nav btn-nav-accent" href="#contact">contact →</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-grid"></div>
  <div class="hero-glow"></div>
  <div class="hero-glow2"></div>

  <div class="hero-eyebrow">ai/ml engineer · founder, ai vision · 2+ yrs freelance · 9+ yrs engineering · live product: anbuclinic.me</div>

  <h1 class="hero-name">
    Raja Ganapathy M
    <span class="hero-name-accent"></span>
  </h1>

  <p class="hero-title">AI / ML ENGINEER &nbsp;·&nbsp; LLM SYSTEMS &nbsp;·&nbsp; AGENTIC AI &nbsp;·&nbsp; RAG</p>

  <p class="hero-tagline">
    I spent nine years engineering systems where <strong>failure wasn't an option.</strong>
    Then two years building real AI products for real clients —
    <strong>anbuclinic.me is live today,</strong> billed and running in Tamil Nadu.
    A filed patent and an IEEE paper are the research proof.
  </p>

  <div class="hero-badges">
    <span class="badge badge-g" style="font-weight:700;font-size:11px;padding:0.45rem 1.1rem;">🏥 anbuclinic.me · LIVE PRODUCT · BILLED</span>
    <span class="badge badge-g">⚡ Patent Filed · Apr 2026</span>
    <span class="badge badge-b">📄 IEEE Paper · Submitted</span>
    <span class="badge badge-g">🎓 M.Tech AI · Graduated May 2026 · 9.6 CGPA</span>
    <span class="badge" style="border-color:rgba(240,160,50,0.6);color:#f0a040;background:rgba(240,160,50,0.07);">🏢 AI Vision · Founder · Freelance AIML · 2+ Yrs</span>
    <span class="badge" style="border-color:rgba(255,160,50,0.5);color:#f0a040;background:rgba(255,160,50,0.05);">🤗 3 Models Live · HuggingFace</span>
    <span class="badge" style="border-color:rgba(255,80,80,0.5);color:#ff8080;background:rgba(255,80,80,0.05);">▶ Conscious AI · YouTube</span>
    <span class="badge" style="border-color:rgba(0,212,255,0.5);color:#00d4ff;background:rgba(0,212,255,0.05);">🌐 Conscious AI Browser · Chromium Source</span>
    <span class="badge" style="border-color:rgba(166,206,57,0.5);color:#a6ce39;background:rgba(166,206,57,0.05);">🆔 ORCID · 0009-0006-9701-7942</span>
    <span class="badge" style="border-color:rgba(66,133,244,0.5);color:#4285f4;background:rgba(66,133,244,0.05);">📚 Google Scholar · Verified Profile</span>
    <span class="badge">LLMs · Agentic AI · RAG</span>
    <span class="badge">Multi-Agent Systems</span>
    <span class="badge">Computer Vision</span>
  </div>

  <div class="hero-actions">
    <a class="btn-primary" href="https://anbuclinic.me" target="_blank">🏥 live product →</a>
    <a class="btn-outline" href="#projects">view all work →</a>
    <a class="btn-outline" href="https://rajaganaa.github.io/antahkarana-frontend/" target="_blank">⚡ demo ↗</a>
    <a class="btn-outline" href="https://huggingface.co/RajGana" target="_blank" style="border-color:rgba(255,160,50,0.6);color:#f0a040;">🤗 huggingface ↗</a>
    <a class="btn-outline" href="https://orcid.org/0009-0006-9701-7942" target="_blank" style="border-color:rgba(166,206,57,0.6);color:#a6ce39;">🆔 orcid ↗</a>
    <button class="btn-outline" onclick="openCVModal()">↓ view & download cv</button>
    <a class="btn-outline" href="#contact">contact me →</a>
  </div>

  <div class="hero-scroll">scroll</div>

  <div class="hero-stats">
    <div class="stat"><div class="stat-num">9+</div><div class="stat-label">YRS ENGINEERING</div></div>
    <div class="stat"><div class="stat-num">2+</div><div class="stat-label">YRS FREELANCE AIML</div></div>
    <div class="stat"><div class="stat-num">1</div><div class="stat-label">LIVE BILLED PRODUCT</div></div>
    <div class="stat"><div class="stat-num">9.6</div><div class="stat-label">M.TECH CGPA</div></div>
  </div>
</section>

<!-- TICKER -->
<div class="ticker-wrap">
  <div class="ticker-inner">
    &nbsp;&nbsp;&nbsp;🏥 ANBUCLINIC.ME · LIVE AI PRODUCT · BILLED · JUNE 2026
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🏢 AI VISION · FOUNDER · FREELANCE AIML ENGINEER · 2+ YEARS
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ⚡ PATENT FILED · APP NO. 202641043947
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    📄 IEEE CONFERENCE PAPER SUBMITTED · SRM INSTITUTE
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🎓 M.TECH AI · GRADUATED MAY 2026 · 9.6 CGPA
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🆔 ORCID · 0009-0006-9701-7942
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    📚 GOOGLE SCHOLAR · ANTAHKARANA · 2026
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🚀 ANTAHKARANA AI — LIVE DEMO DEPLOYED
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🤗 3 LIVE MODELS ON HUGGINGFACE · LLM · VLM · CODELLAMA FINE-TUNE
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ▶ CONSCIOUS AI — YOUTUBE CHANNEL · @rajaganaaAI
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🌐 CONSCIOUS AI BROWSER · CHROMIUM FROM SOURCE · LLAMA 3.3 70B
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🛠 13 PRODUCTION AI SYSTEMS
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🏭 9+ YEARS SAFETY-CRITICAL ENGINEERING
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ☁️ AWS SOLUTIONS ARCHITECT CERTIFIED · 2025
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    📍 OPEN TO ROLES IN CHENNAI · BANGALORE · HYDERABAD
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🏥 ANBUCLINIC.ME · LIVE AI PRODUCT · BILLED · JUNE 2026
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🏢 AI VISION · FOUNDER · FREELANCE AIML ENGINEER · 2+ YEARS
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ⚡ PATENT FILED · APP NO. 202641043947
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    📄 IEEE CONFERENCE PAPER SUBMITTED · SRM INSTITUTE
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🎓 M.TECH AI · GRADUATED MAY 2026 · 9.6 CGPA
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🆔 ORCID · 0009-0006-9701-7942
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    📚 GOOGLE SCHOLAR · ANTAHKARANA · 2026
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🚀 ANTAHKARANA AI — LIVE DEMO DEPLOYED
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🤗 3 LIVE MODELS ON HUGGINGFACE · LLM · VLM · CODELLAMA FINE-TUNE
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ▶ CONSCIOUS AI — YOUTUBE CHANNEL · @rajaganaaAI
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🌐 CONSCIOUS AI BROWSER · CHROMIUM FROM SOURCE · LLAMA 3.3 70B
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🛠 13 PRODUCTION AI SYSTEMS
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🏭 9+ YEARS SAFETY-CRITICAL ENGINEERING
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ☁️ AWS SOLUTIONS ARCHITECT CERTIFIED · 2025
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    📍 OPEN TO ROLES IN CHENNAI · BANGALORE · HYDERABAD
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
          <div class="tl-role" style="color:var(--orange);">Founder & AI/ML Freelance Engineer — AI Vision <span style="font-family:'DM Mono',monospace;font-size:10px;border:1px solid rgba(240,160,64,0.5);padding:1px 7px;margin-left:6px;vertical-align:middle;">Udyam Reg: UDYAM-TN-02-0483528</span></div>
          <div class="tl-org" style="color:var(--text-2);">Built & billed real AI products for clients · Invoice AIV-2026-001 issued · Anbu Clinic, Ariyalur District, TN</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">2024 – May 2026</div>
          <div class="tl-role">M.Tech Artificial Intelligence · 9.6 CGPA · <span style="color:var(--green);">Graduated ✓</span></div>
          <div class="tl-org">SRM Institute of Science & Technology</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">Jun 2026</div>
          <div class="tl-role" style="color:var(--green);">Anbu Health AI — LIVE at anbuclinic.me</div>
          <div class="tl-org">React 19 · Groq LLaMA 3.3 70B · GPT-4o · Qdrant · Supabase · Sarvam Tamil TTS · Azure · Terraform · DPDP compliant</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">Apr 2026</div>
          <div class="tl-role">Indian Patent Filed · Antahkarana System</div>
          <div class="tl-org">App No. 202641043947 · IEEE Paper Submitted</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">May 2026</div>
          <div class="tl-role">ORCID Registered · Google Scholar Profile Live</div>
          <div class="tl-org">ORCID: 0009-0006-9701-7942 · Antahkarana paper indexed</div>
        </div>
      </div>
    </div>

    <div class="about-body reveal">
      <p>
        I am an <strong>AI/ML Engineer</strong> and the founder of <strong>AI Vision</strong>
        (Udyam Reg: UDYAM-TN-02-0483528) — a registered freelance AI practice I've been running
        for 2+ years alongside my M.Tech. I don't just build AI systems as projects.
        <em>I build them for paying clients, invoice them, and keep them running in production.</em>
      </p>
      <p>
        My most recent work is <strong>Anbu Health AI</strong> — live today at
        <a href="https://anbuclinic.me" target="_blank" style="color:var(--green);text-decoration:none;font-weight:600;">anbuclinic.me</a>.
        It's a real AI doctor assistant for village clinic patients in Ariyalur District, Tamil Nadu —
        Tamil voice + text, medicine image analysis (GPT-4o), lab PDF parsing, Groq LLaMA 3.3 70B,
        Qdrant RAG, Sarvam Tamil TTS, Azure Container Apps, full DPDP Act compliance.
        Invoice AIV-2026-001 issued to Anbu Clinic in June 2026. <em>This is paid freelance work.</em>
      </p>
      <p>
        My flagship research project, <strong>Antahkarana</strong>, is a cognitively-inspired adaptive
        reasoning framework for LLMs and VLMs — drawing on Vedantic cognitive architecture.
        It earned a <em>filed Indian patent</em> and a <em>submitted IEEE Conference paper</em>
        now indexed on <em>Google Scholar</em> and linked to my <em>ORCID</em> researcher identity.
      </p>
      <p>
        What I bring that most candidates don't: 9 years of safety-critical engineering discipline,
        2+ years of real freelance delivery, a live billed product, a patent, and an IEEE paper —
        all built while completing an M.Tech with a <strong>9.6 CGPA.</strong>
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
          <span class="badge" style="border-color:rgba(66,133,244,0.4);color:#4285f4;">Google Scholar</span>
          <span class="badge" style="border-color:rgba(166,206,57,0.4);color:#a6ce39;">ORCID Linked</span>
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
          <div class="ach-icon">📚</div>
          <div>
            <div class="ach-title">Google Scholar · ORCID Indexed</div>
            <div class="ach-body">Paper live on Google Scholar — linked to ORCID 0009-0006-9701-7942</div>
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
          <a class="btn-feat-secondary" href="https://scholar.google.com/citations?user=93hagOEAAAAJ" target="_blank" style="border-color:rgba(66,133,244,0.35);color:#4285f4;">scholar ↗</a>
        </div>
      </div>
    </div>

    <!-- P.002 — ANBU HEALTH AI — LIVE PRODUCT -->
    <div class="proj-featured reveal" style="border-color:rgba(184,240,80,0.35);margin-top:1px;">
      <div class="feat-left">
        <div class="feat-num">P.002 · LIVE FREELANCE PRODUCT · BILLED</div>
        <h2 class="feat-title">Anbu Health<span>AI — anbuclinic.me</span></h2>
        <p class="feat-desc">
          A real AI doctor assistant for village clinic patients in Ariyalur District, Tamil Nadu —
          built under AI Vision (my registered freelance company) and billed to Anbu Clinic.
          Invoice AIV-2026-001 · ₹21,500 · June 2026. Tamil voice + text, medicine image analysis,
          lab PDF parsing, appointment booking. DPDP Act 2023 compliant. Running in production today.
        </p>
        <div class="feat-tags">
          <span class="badge badge-g" style="font-size:11px;">LIVE · anbuclinic.me</span>
          <span class="badge" style="border-color:rgba(240,160,50,0.5);color:#f0a040;">Freelance · Billed · AI Vision</span>
          <span class="badge badge-b">Azure Container Apps</span>
          <span class="badge">React 19 · FastAPI</span>
          <span class="badge">Groq · LLaMA 3.3 70B</span>
          <span class="badge">GPT-4o Vision</span>
          <span class="badge">Qdrant RAG</span>
          <span class="badge">Supabase · Redis</span>
          <span class="badge">Sarvam Tamil TTS</span>
          <span class="badge">Firebase OTP</span>
          <span class="badge">Terraform IaC</span>
          <span class="badge">Prometheus · Grafana</span>
          <span class="badge">DPDP Act 2023</span>
        </div>
      </div>
      <div class="feat-right">
        <div class="ach-item">
          <div class="ach-icon">🏥</div>
          <div>
            <div class="ach-title">Live Product — anbuclinic.me</div>
            <div class="ach-body">Deployed on Azure Central India · serving Anbu Clinic patients · Pappakudi, Ariyalur District, Tamil Nadu</div>
          </div>
        </div>
        <div class="ach-item">
          <div class="ach-icon">🧾</div>
          <div>
            <div class="ach-title">Invoice AIV-2026-001 · ₹21,500 · Jun 2026</div>
            <div class="ach-body">AI Vision (Udyam Reg: UDYAM-TN-02-0483528) · Billed to Anbu Clinic · Dr. Raghul M.D · Dr. Rajeswari M.D</div>
          </div>
        </div>
        <div class="ach-item">
          <div class="ach-icon">🗣️</div>
          <div>
            <div class="ach-title">Tamil Voice + Multilingual AI</div>
            <div class="ach-body">Sarvam AI Bulbul TTS · Web Speech API Tamil voice input · serves patients with no English literacy</div>
          </div>
        </div>
        <div class="ach-item">
          <div class="ach-icon">🔬</div>
          <div>
            <div class="ach-title">Multimodal — Image + PDF + Voice + Text</div>
            <div class="ach-body">Medicine strip photo → drug info (GPT-4o) · Lab PDF parsing (PyMuPDF) · Dosage calculator · Schedule H1 drug blocking</div>
          </div>
        </div>
        <div class="ach-item">
          <div class="ach-icon">🛡️</div>
          <div>
            <div class="ach-title">Full Compliance Stack</div>
            <div class="ach-body">DPDP Act 2023 · IT Rules 2021 · PHI redaction · Consent management · Grievance Officer · Right to erasure</div>
          </div>
        </div>
        <div class="feat-links">
          <a class="btn-feat-primary" href="https://anbuclinic.me" target="_blank">🏥 live product →</a>
          <a class="btn-feat-secondary" href="https://github.com/rajaganaa/anbu-health-ai" target="_blank">frontend ↗</a>
          <a class="btn-feat-secondary" href="https://github.com/rajaganaa/anbu-health-ai-api" target="_blank">api ↗</a>
        </div>
      </div>
    </div>

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

    <!-- P.009 -->
    <a class="proj-card reveal" href="https://huggingface.co/RajGana" target="_blank">
      <div class="proj-top"><span class="proj-num">P.009</span><span class="proj-arrow">↗</span></div>
      <div class="proj-tags">
        <span class="proj-tag proj-tag-g">From Scratch</span>
        <span class="proj-tag">LLM</span>
        <span class="proj-tag">VLM</span>
        <span class="proj-tag">HuggingFace</span>
      </div>
      <h3 class="proj-title">TinyLLaMA & Mini-VLM — Built from Scratch in 1 Day</h3>
      <p class="proj-desc">Built and trained a full LLM and Vision-Language Model from scratch in a single day. Transformer theory → LLM (loss 8.9→0.33) → VLM (loss 17→1.17) → LoRA fine-tune (loss 1.6→1.01) → published live on HuggingFace. Both models public at RajGana/tinyllama-alpaca-finetuned and RajGana/mini-vlm-scratch.</p>
      <div class="proj-metric" style="display:flex;justify-content:space-between;flex-wrap:wrap;gap:4px;">
        <span>⚡ 2 live models (LLM + VLM) · ~$10 compute · Day 1 build</span>
        <span style="display:flex;gap:8px;">
          <a href="https://huggingface.co/RajGana/tinyllama-alpaca-finetuned" target="_blank" onclick="event.stopPropagation()" style="color:var(--orange);text-decoration:none;font-size:10px;">🤗 LLM ↗</a>
          <a href="https://huggingface.co/RajGana/mini-vlm-scratch" target="_blank" onclick="event.stopPropagation()" style="color:var(--orange);text-decoration:none;font-size:10px;">🤗 VLM ↗</a>
        </span>
      </div>
    </a>

    <!-- P.010 -->
    <a class="proj-card reveal" href="https://conscious-ai-webapp.vercel.app" target="_blank">
      <div class="proj-top"><span class="proj-num">P.010</span><span class="proj-arrow">↗</span></div>
      <div class="proj-tags">
        <span class="proj-tag proj-tag-g">Chromium Source</span>
        <span class="proj-tag">LLaMA 3.3 70B</span>
        <span class="proj-tag">AI Browser</span>
        <span class="proj-tag">Vercel</span>
      </div>
      <h3 class="proj-title">Conscious AI Browser — Built from Chromium Source</h3>
      <p class="proj-desc">Compiled Chromium from source (26,000 build steps) on GCP. Custom branded browser with built-in AI sidebar powered by LLaMA 3.3 70B — summarizes and explains any webpage in real-time. Packaged as Linux .deb installer. Same architecture as Brave and Arc browser.</p>
      <div class="proj-metric" style="display:flex;justify-content:space-between;flex-wrap:wrap;gap:4px;">
        <span>⚡ 26,000 build steps · LLaMA 3.3 70B · Linux .deb</span>
        <span style="display:flex;gap:8px;">
          <a href="https://conscious-ai-webapp.vercel.app" target="_blank" onclick="event.stopPropagation()" style="color:var(--green);text-decoration:none;font-size:10px;">Live Demo ↗</a>
          <a href="https://github.com/rajaganaa/conscious-ai-browser" target="_blank" onclick="event.stopPropagation()" style="color:var(--blue);text-decoration:none;font-size:10px;">GitHub ↗</a>
        </span>
      </div>
    </a>

    <!-- P.011 -->
    <a class="proj-card reveal" href="https://huggingface.co/spaces/RajGana/codellama-demo" target="_blank">
      <div class="proj-top"><span class="proj-num">P.011</span><span class="proj-arrow">↗</span></div>
      <div class="proj-tags">
        <span class="proj-tag proj-tag-g">Live Demo</span>
        <span class="proj-tag">QLoRA Fine-tune</span>
        <span class="proj-tag">AWS SageMaker</span>
        <span class="proj-tag">HuggingFace</span>
      </div>
      <h3 class="proj-title">CodeLlama Coding Assistant — Fine-tuned on AWS SageMaker</h3>
      <p class="proj-desc">Fine-tuned CodeLlama-7B with QLoRA (4-bit) on CodeAlpaca-20K using AWS SageMaker ml.g4dn.xlarge. Full MLOps pipeline: SageMaker → S3 → HuggingFace Hub → Gradio Space → Groq inference API. Live demo supports code completion, debugging, and explanation in real time.</p>
      <div class="proj-metric" style="display:flex;justify-content:space-between;flex-wrap:wrap;gap:4px;">
        <span>⚡ CodeLlama-7B · QLoRA · SageMaker · Groq API</span>
        <span style="display:flex;gap:8px;">
          <a href="https://huggingface.co/spaces/RajGana/codellama-demo" target="_blank" onclick="event.stopPropagation()" style="color:var(--green);text-decoration:none;font-size:10px;">Live Demo ↗</a>
          <a href="https://huggingface.co/RajGana/codellama-coding-assistant" target="_blank" onclick="event.stopPropagation()" style="color:var(--orange);text-decoration:none;font-size:10px;">🤗 Model ↗</a>
          <a href="https://github.com/rajaganaa/codellama-coding-assistant" target="_blank" onclick="event.stopPropagation()" style="color:var(--blue);text-decoration:none;font-size:10px;">GitHub ↗</a>
        </span>
      </div>
    </a>

  </div>
</section>

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

<!-- ✅ NEW: RESEARCH & PUBLICATIONS SECTION -->
<section id="research" style="background:var(--bg2);">
  <div class="sec-label">04 · RESEARCH &amp; PUBLICATIONS</div>

  <!-- Researcher IDs panel -->
  <div class="researcher-ids reveal" style="margin-bottom:3rem;">
    <a class="rid-card" href="https://orcid.org/0009-0006-9701-7942" target="_blank">
      <div class="rid-icon orcid">🆔</div>
      <div style="flex:1;">
        <div class="rid-label orcid">ORCID</div>
        <div class="rid-value">0009-0006-9701-7942</div>
      </div>
      <div class="rid-arrow">↗</div>
    </a>
    <a class="rid-card" href="https://scholar.google.com/citations?user=93hagOEAAAAJ" target="_blank">
      <div class="rid-icon scholar">📚</div>
      <div style="flex:1;">
        <div class="rid-label scholar">GOOGLE SCHOLAR</div>
        <div class="rid-value">RAJA GANAPATHY M<br/><span style="font-size:9px;">AI Fellow · SRM Institute</span></div>
      </div>
      <div class="rid-arrow">↗</div>
    </a>
    <a class="rid-card" href="https://huggingface.co/RajGana" target="_blank">
      <div class="rid-icon hf">🤗</div>
      <div style="flex:1;">
        <div class="rid-label hf">HUGGINGFACE</div>
        <div class="rid-value">RajGana<br/><span style="font-size:9px;">3 live models · LLM · VLM · CodeLlama</span></div>
      </div>
      <div class="rid-arrow">↗</div>
    </a>
    <a class="rid-card" href="https://github.com/rajaganaa" target="_blank">
      <div class="rid-icon gs">⌥</div>
      <div style="flex:1;">
        <div class="rid-label gs">GITHUB</div>
        <div class="rid-value">rajaganaa<br/><span style="font-size:9px;">10+ AI repositories</span></div>
      </div>
      <div class="rid-arrow">↗</div>
    </a>
  </div>

  <!-- Publications -->
  <div class="research-grid reveal">

    <!-- Paper 1 — flagship -->
    <div class="research-card featured">
      <div class="research-label">CONFERENCE PAPER · 2026 · UNDER REVIEW</div>
      <h3 class="research-title">Antahkarana: Cognitively-Inspired Adaptive Reasoning for LLMs and VLMs</h3>
      <div class="research-authors"><strong>Raja Ganapathy M</strong>, RG Karthikeyan</div>
      <div class="research-venue">📍 IEEE Conference — SRM Institute of Science &amp; Technology, Kattankulathur · 2026</div>
      <p class="research-abstract">
        Introduces a modular conditional reasoning framework for large language models and vision-language models,
        inspired by Vedantic cognitive architecture (antahkarana). The system routes complex queries through
        four specialised cognitive stages — manas (perception), buddhi (discrimination), chitta (memory),
        and ahamkara (integration) — validated across 2,500+ LLM and multimodal samples.
        Accompanied by Indian Patent Application No. 202641043947.
      </p>
      <div class="research-links">
        <a class="research-link green" href="https://scholar.google.com/citations?user=93hagOEAAAAJ" target="_blank">📚 Google Scholar ↗</a>
        <a class="research-link" href="https://orcid.org/0009-0006-9701-7942" target="_blank" style="border-color:rgba(166,206,57,0.35);color:#a6ce39;">🆔 ORCID ↗</a>
        <a class="research-link" href="https://github.com/rajaganaa/antahkarana-reasoning-framework" target="_blank">⌥ Code ↗</a>
        <a class="research-link blue" href="https://rajaganaa.github.io/antahkarana-frontend/" target="_blank">⚡ Live Demo ↗</a>
      </div>
    </div>

    <!-- Patent card -->
    <div class="research-card" style="border:1px solid rgba(240,160,64,0.2);background:var(--bg);">
      <div class="research-label" style="color:var(--orange);">INDIAN PATENT · FILED APR 2026</div>
      <h3 class="research-title">Antahkarana — Adaptive AI Reasoning System</h3>
      <div class="research-authors" style="color:var(--orange);opacity:0.8;">Application No. 202641043947</div>
      <div class="research-venue" style="color:var(--orange);opacity:0.7;">📍 Indian Patent Office · Filed April 3, 2026 · Under Examination</div>
      <p class="research-abstract">
        Patent protects the system architecture of the Antahkarana cognitively-inspired reasoning engine —
        specifically the multi-stage query routing mechanism, the Vedantic cognitive stage mapping to neural
        processing pipelines, and the multimodal integration layer for LLM and VLM joint reasoning.
        First Indian patent in the space of Vedanta-inspired AI cognitive architectures.
      </p>
      <div class="research-links">
        <span class="research-link" style="border-color:rgba(240,160,64,0.35);color:var(--orange);cursor:default;">⚡ Patent Pending</span>
        <a class="research-link" href="https://github.com/rajaganaa/antahkarana-reasoning-framework" target="_blank">⌥ Implementation ↗</a>
      </div>
    </div>

  </div>

  <!-- Research highlights -->
  <div class="reveal" style="margin-top:3rem;padding:2.5rem;background:var(--bg);border:1px solid var(--border);">
    <div style="font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.22em;color:var(--text-3);margin-bottom:1.5rem;">RESEARCH IMPACT SUMMARY</div>
    <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:2rem;">
      <div style="text-align:center;">
        <div style="font-family:'Bebas Neue',sans-serif;font-size:3.5rem;color:var(--green);line-height:1;">1</div>
        <div style="font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.14em;color:var(--text-3);margin-top:4px;">PATENT FILED</div>
      </div>
      <div style="text-align:center;">
        <div style="font-family:'Bebas Neue',sans-serif;font-size:3.5rem;color:var(--blue);line-height:1;">1</div>
        <div style="font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.14em;color:var(--text-3);margin-top:4px;">IEEE SUBMISSION</div>
      </div>
      <div style="text-align:center;">
        <div style="font-family:'Bebas Neue',sans-serif;font-size:3.5rem;color:#a6ce39;line-height:1;">1</div>
        <div style="font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.14em;color:var(--text-3);margin-top:4px;">ORCID PROFILE</div>
      </div>
      <div style="text-align:center;">
        <div style="font-family:'Bebas Neue',sans-serif;font-size:3.5rem;color:#4285f4;line-height:1;">1</div>
        <div style="font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.14em;color:var(--text-3);margin-top:4px;">SCHOLAR PROFILE</div>
      </div>
      <div style="text-align:center;">
        <div style="font-family:'Bebas Neue',sans-serif;font-size:3.5rem;color:var(--orange);line-height:1;">2.5K</div>
        <div style="font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.14em;color:var(--text-3);margin-top:4px;">VALIDATION SAMPLES</div>
      </div>
      <div style="text-align:center;">
        <div style="font-family:'Bebas Neue',sans-serif;font-size:3.5rem;color:var(--text);line-height:1;">3</div>
        <div style="font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.14em;color:var(--text-3);margin-top:4px;">HF LIVE MODELS</div>
      </div>
    </div>
  </div>
</section>

<!-- CERTIFICATIONS -->
<section id="certifications">
  <div class="sec-label">05 · CERTIFICATIONS</div>
  <div class="certs-grid reveal">

    <a class="cert-card" href="https://guvi.in/verify-certificate?id=Xd67z1F22po7eP2299" target="_blank" style="text-decoration:none;"><div class="cert-icon">🎓</div><div><div class="cert-name">AI & ML Professional Program</div><div class="cert-issuer">GUVI · IIT-M · May 2024</div></div><span class="cert-verify">verify ↗</span></a>
    <a class="cert-card" href="https://ude.my/UC-b6b0e72b-8ff0-4ffc-844b-1cadaa967220" target="_blank" style="text-decoration:none;"><div class="cert-icon">☁️</div><div><div class="cert-name">AWS Certified Solutions Architect Associate</div><div class="cert-issuer">Udemy · Oct 2025</div></div><span class="cert-verify">verify ↗</span></a>
    <a class="cert-card" href="https://ude.my/UC-7719c7f3-162d-424a-b60c-7663580edfd6" target="_blank" style="text-decoration:none;"><div class="cert-icon">⚙️</div><div><div class="cert-name">DevOps Beginners to Advanced with Projects</div><div class="cert-issuer">Udemy · Jul 2025</div></div><span class="cert-verify">verify ↗</span></a>
    <a class="cert-card" href="https://nptel.ac.in/noc/E_Certificate/NPTEL25CS147S10539027271075509" target="_blank" style="text-decoration:none;"><div class="cert-icon">🔗</div><div><div class="cert-name">Introduction to Internet of Things</div><div class="cert-issuer">NPTEL · Oct 2025</div></div><span class="cert-verify">verify ↗</span></a>
    <a class="cert-card" href="https://digitalskills.iitmpravartak.org.in/verify/cert/Xd67z1F22po7eP2299" target="_blank" style="text-decoration:none;"><div class="cert-icon">🖥️</div><div><div class="cert-name">Certificate Professional — Advanced Programming</div><div class="cert-issuer">IIT-M · May 2024</div></div><span class="cert-verify">verify ↗</span></a>
    <a class="cert-card" href="https://courses.opencv.org/certificates/412c33237d8c4a73bf0d810bda6612dd" target="_blank" style="text-decoration:none;"><div class="cert-icon">👁️</div><div><div class="cert-name">OpenCV Certification</div><div class="cert-issuer">OpenCV University · Mar 2025</div></div><span class="cert-verify">verify ↗</span></a>
    <a class="cert-card" href="https://simpli-web.app.link/e/oQY4qjHgo3b" target="_blank" style="text-decoration:none;"><div class="cert-icon">🔥</div><div><div class="cert-name">PyTorch for Deep Learning</div><div class="cert-issuer">Simplilearn · Nov 2024</div></div><span class="cert-verify">verify ↗</span></a>
    <a class="cert-card" href="https://simpli-web.app.link/e/NFDsQUbho3b" target="_blank" style="text-decoration:none;"><div class="cert-icon">🧠</div><div><div class="cert-name">TensorFlow for Beginners</div><div class="cert-issuer">Simplilearn · Nov 2024</div></div><span class="cert-verify">verify ↗</span></a>
    <a class="cert-card" href="https://guvi.in/verify-certificate?id=H1Ow9I851C8XvA9755" target="_blank" style="text-decoration:none;"><div class="cert-icon">🐍</div><div><div class="cert-name">Advanced Python Course</div><div class="cert-issuer">GUVI · IIT-M · Feb 2024</div></div><span class="cert-verify">verify ↗</span></a>
    <a class="cert-card" href="https://simpli-web.app.link/e/9iRW7Ttgo3b" target="_blank" style="text-decoration:none;"><div class="cert-icon">📊</div><div><div class="cert-name">DSA · Data Structures & Algorithms</div><div class="cert-issuer">Simplilearn · Nov 2024</div></div><span class="cert-verify">verify ↗</span></a>

  </div>
</section>

<!-- BLOG -->
<section id="blog">
  <div class="sec-label">06 · BLOG</div>
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

<!-- CONSCIOUS AI — YOUTUBE -->
<section id="youtube" style="background:var(--bg2);">
  <div class="sec-label">07 · CONSCIOUS AI — YOUTUBE</div>

  <div style="display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:center;" class="reveal">

    <div>
      <div style="font-family:'DM Mono',monospace;font-size:10px;letter-spacing:0.2em;color:#ff8080;margin-bottom:1rem;">▶ @rajaganaaAI</div>
      <h2 style="font-family:'Bebas Neue',sans-serif;font-size:clamp(2.5rem,4vw,3.8rem);line-height:0.95;color:var(--text);margin-bottom:1.25rem;">
        Conscious AI<br/><span style="color:#ff8080;"></span>
      </h2>
      <p style="font-family:'DM Sans',sans-serif;font-size:14px;font-weight:300;color:var(--text-2);line-height:1.9;margin-bottom:1.5rem;">
        A YouTube channel dedicated to understanding Artificial Intelligence — from fundamentals
        to advanced concepts like Machine Learning, Deep Learning, NLP, Reinforcement Learning,
        LLMs, Computer Vision, and Intelligent Agents.
      </p>
      <p style="font-family:'DM Sans',sans-serif;font-size:14px;font-weight:300;color:var(--text-2);line-height:1.9;margin-bottom:2rem;">
        This channel explores AI not just as technology, but as a step toward
        <strong style="color:var(--text);font-weight:500;">human-like reasoning, cognition, and consciousness.</strong>
        The same philosophy behind the Antahkarana framework — taught publicly.
      </p>
      <p style="font-family:'DM Mono',monospace;font-size:12px;letter-spacing:0.06em;color:#ff8080;font-style:italic;margin-bottom:2rem;">
        "Learn AI deeply. Think consciously."
      </p>
      <a href="https://youtube.com/@rajaganaaAI" target="_blank"
        style="font-family:'DM Mono',monospace;font-size:12px;letter-spacing:0.08em;
               padding:0.8rem 1.75rem;background:#ff4040;color:#fff;
               text-decoration:none;display:inline-flex;align-items:center;gap:0.5rem;
               transition:all 0.15s;border:1px solid #ff4040;font-weight:500;"
        onmouseover="this.style.background='#ff2020'"
        onmouseout="this.style.background='#ff4040'">
        ▶ Visit the Channel →
      </a>
    </div>

    <div style="border:1px solid rgba(255,80,80,0.15);background:var(--bg);padding:2.5rem;">
      <div style="font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.2em;color:#ff8080;margin-bottom:1.5rem;">WHAT YOU'LL FIND HERE</div>

      <div style="display:flex;flex-direction:column;gap:1px;background:rgba(255,80,80,0.08);">
        <div style="background:var(--bg);padding:1rem 1.25rem;border-left:2px solid #ff8080;">
          <div style="font-family:'DM Sans',sans-serif;font-size:13px;font-weight:600;color:var(--text);margin-bottom:3px;">AI Fundamentals to Advanced</div>
          <div style="font-family:'DM Mono',monospace;font-size:11px;color:var(--text-3);">ML · DL · NLP · Computer Vision · RL</div>
        </div>
        <div style="background:var(--bg);padding:1rem 1.25rem;border-left:2px solid rgba(255,128,128,0.5);">
          <div style="font-family:'DM Sans',sans-serif;font-size:13px;font-weight:600;color:var(--text);margin-bottom:3px;">LLMs & Intelligent Agents</div>
          <div style="font-family:'DM Mono',monospace;font-size:11px;color:var(--text-3);">Agentic AI · RAG · Multi-Agent Systems</div>
        </div>
        <div style="background:var(--bg);padding:1rem 1.25rem;border-left:2px solid rgba(255,128,128,0.5);">
          <div style="font-family:'DM Sans',sans-serif;font-size:13px;font-weight:600;color:var(--text);margin-bottom:3px;">Tamil Language AI Content</div>
          <div style="font-family:'DM Mono',monospace;font-size:11px;color:var(--text-3);">Making AI education accessible in Tamil Nadu</div>
        </div>
        <div style="background:var(--bg);padding:1rem 1.25rem;border-left:2px solid rgba(255,128,128,0.5);">
          <div style="font-family:'DM Sans',sans-serif;font-size:13px;font-weight:600;color:var(--text);margin-bottom:3px;">Cognition & Consciousness in AI</div>
          <div style="font-family:'DM Mono',monospace;font-size:11px;color:var(--text-3);">The philosophy behind Antahkarana — explained</div>
        </div>
      </div>

      <div style="margin-top:1.5rem;padding-top:1.25rem;border-top:1px solid var(--border);
                  font-family:'DM Mono',monospace;font-size:10px;color:var(--text-3);
                  display:flex;justify-content:space-between;">
        <span>youtube.com/@rajaganaaAI</span>
        <span style="color:#ff8080;">▶ ACTIVE</span>
      </div>
    </div>

  </div>
</section>

<!-- THE EDGE -->
<section id="edge" style="background:var(--bg2);">
  <div class="sec-label">08 · THE EDGE</div>
  <div class="edge-grid">

    <div class="edge-card reveal">
      <div class="edge-label">NOT A STUDENT PROJECT — A BILLED PRODUCT</div>
      <h3 class="edge-heading">Live. Billed. <em>Running today.</em></h3>
      <p class="edge-body">Anbu Health AI is live at <strong>anbuclinic.me</strong> — serving real patients in Ariyalur District, Tamil Nadu. Invoice AIV-2026-001 for ₹21,500 was issued to Anbu Clinic in June 2026 under AI Vision (Udyam Reg: UDYAM-TN-02-0483528). This is not a demo. It is a paid, production-deployed product with a real client and a maintenance contract.</p>
    </div>

    <div class="edge-card reveal">
      <div class="edge-label">WHAT MOST CANDIDATES DON'T HAVE</div>
      <h3 class="edge-heading">A filed patent <em>and</em> a live product.</h3>
      <p class="edge-body">Most M.Tech graduates build class projects. Rajaganapathy filed an Indian patent (App. 202641043947), submitted an IEEE paper, ran a 2-year freelance AI practice under AI Vision, and deployed a live billed product — all while graduating with a 9.6 CGPA in May 2026.</p>
    </div>

    <div class="edge-card reveal">
      <div class="edge-label">THE ENGINEERING MINDSET</div>
      <h3 class="edge-heading">9 yrs engineering. <em>2 yrs AI delivery.</em></h3>
      <p class="edge-body">Nine years maintaining 500 kVA transformers and 400 kW motors in live industrial environments. Then two years building and shipping real AI products for paying clients. The discipline of both is in every line of code — and recruiters can verify it with a live URL and an invoice number.</p>
    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="sec-label">09 · CONTACT</div>
  <div class="contact-grid">
    <div class="reveal">
      <h2 class="contact-heading">Ready to build<br/>at <span>Google scale.</span></h2>
      <p class="contact-sub">
        Most candidates bring a degree. I bring 9+ years of engineering under real-world pressure,
        2+ years of freelance AI delivery under <strong>AI Vision</strong> (Udyam Reg: UDYAM-TN-02-0483528),
        a live billed product at <strong>anbuclinic.me</strong>,
        a filed patent, an IEEE paper under review, an ORCID researcher identity,
        and a Google Scholar profile — all while completing an M.Tech in AI with a 9.6 CGPA.
        <br/><br/>
        <em style="color:var(--green);">You can verify the product right now: anbuclinic.me is live.</em>
      </p>
      <div style="display:flex;gap:1rem;flex-wrap:wrap;">
        <a class="btn-primary" href="mailto:rajaganaa@gmail.com">send me an email →</a>
        <a class="btn-outline" href="https://www.linkedin.com/in/raja-ganapathy-36b00658" target="_blank">linkedin ↗</a>
      </div>
    </div>
    <div class="contact-links reveal">
      <a class="contact-link" href="https://anbuclinic.me" target="_blank" style="color:var(--green);background:rgba(184,240,80,0.04);border-bottom:1px solid rgba(184,240,80,0.15);">
        <span>🏥 Live Product</span><span class="contact-link-val" style="color:var(--green);">anbuclinic.me · Invoice AIV-2026-001</span>
      </a>
      <a class="contact-link" href="mailto:rajaganaa@gmail.com">
        <span>✉ Email</span><span class="contact-link-val">rajaganaa@gmail.com</span>
      </a>
      <a class="contact-link" href="tel:+919176631419">
        <span>📞 Phone</span><span class="contact-link-val">+91 9176631419</span>
      </a>
      <div class="contact-link" style="cursor:default;">
        <span>🏢 Company</span><span class="contact-link-val" style="color:#f0a040;">AI Vision · Udyam Reg: UDYAM-TN-02-0483528</span>
      </div>
      <a class="contact-link" href="https://www.linkedin.com/in/raja-ganapathy-36b00658" target="_blank">
        <span>in LinkedIn</span><span class="contact-link-val">raja-ganapathy-36b00658</span>
      </a>
      <a class="contact-link" href="https://orcid.org/0009-0006-9701-7942" target="_blank" style="color:#a6ce39;">
        <span>🆔 ORCID</span><span class="contact-link-val" style="color:#a6ce39;">0009-0006-9701-7942</span>
      </a>
      <a class="contact-link" href="https://scholar.google.com/citations?user=93hagOEAAAAJ" target="_blank" style="color:#4285f4;">
        <span>📚 Google Scholar</span><span class="contact-link-val" style="color:#4285f4;">Raja Ganapathy M · AI Fellow</span>
      </a>
      <a class="contact-link" href="https://huggingface.co/RajGana" target="_blank" style="color:var(--orange);">
        <span>🤗 HuggingFace</span><span class="contact-link-val" style="color:var(--orange);">RajGana · 3 live models</span>
      </a>
      <a class="contact-link" href="https://github.com/rajaganaa" target="_blank">
        <span>⌥ GitHub</span><span class="contact-link-val">github.com/rajaganaa</span>
      </a>
      <a class="contact-link" href="https://x.com/rajaganaa" target="_blank">
        <span>𝕏 Twitter / X</span><span class="contact-link-val">@rajaganaa</span>
      </a>
      <a class="contact-link" href="https://youtube.com/@rajaganaaAI" target="_blank" style="color:#ff8080;">
        <span>▶ YouTube</span><span class="contact-link-val" style="color:#ff6060;">@rajaganaaAI · Conscious AI</span>
      </a>
      <div class="contact-link" style="cursor:default;">
        <span>📍 Location</span><span class="contact-link-val">Chennai · Open to Bangalore / Hyderabad</span>
      </div>
    </div>
  </div>
</section>

<!-- RESUME SECTION -->
<section id="resume" style="background:var(--bg2);">
  <div class="sec-label">10 · RESUME</div>
  <div class="reveal" style="display:flex;flex-direction:column;align-items:center;gap:1.5rem;padding:2rem 0;text-align:center;">
    <p style="font-family:'DM Mono',monospace;font-size:11px;letter-spacing:0.18em;color:var(--text-3);">
      CLICK TO VIEW · PRINT · OR DOWNLOAD AS PDF
    </p>
    <div style="display:flex;gap:0.75rem;flex-wrap:wrap;justify-content:center;">
      <button class="btn-primary" onclick="openCVModal()">↓ open resume →</button>
      <a class="btn-outline" href="?resume=1" onclick="event.preventDefault();openCVModal()">🔗 shareable link</a>
    </div>
    <p style="font-family:'DM Mono',monospace;font-size:10px;color:var(--text-3);">
      Share <code style="color:var(--green);">rajaganaa.github.io/?resume=1</code> with recruiters — auto-opens the resume
    </p>
  </div>
</section>

<!-- RESUME MODAL -->
<div class="cv-modal-overlay" id="cvModal" onclick="closeCVOnOverlay(event)">
  <div class="cv-modal">
    <div class="cv-modal-bar">
      <div class="cv-modal-bar-left">RAJAGANAPATHY M — CURRICULUM VITAE</div>
      <div class="cv-modal-actions">
        <button class="cv-btn-dl" onclick="downloadCV()">↓ download</button>
        <button class="cv-btn-print" onclick="printCV()">⎙ print / pdf</button>
        <button class="cv-btn-close" onclick="closeCVModal()">✕ close</button>
      </div>
    </div>
    <div class="cv-modal-inner" id="cvContent">
      <h1 class="cv-h1">Rajaganapathy M</h1>
      <div class="cv-sub">AI / ML ENGINEER · LLM · AGENTIC AI · RAG · MULTI-AGENT SYSTEMS</div>
      <div class="cv-bar">
        <span>✉ rajaganaa@gmail.com</span><span>📞 +91 9176631419</span>
        <span>🌐 rajaganaa.github.io</span><span>🏥 anbuclinic.me</span>
        <span>in raja-ganapathy-36b00658</span><span>⌥ github.com/rajaganaa</span>
        <span>🤗 huggingface.co/RajGana</span>
        <span>🆔 orcid.org/0009-0006-9701-7942</span>
        <span>📚 scholar.google.com · Raja Ganapathy M</span>
        <span>📍 Chennai · Bangalore · Hyderabad</span>
      </div>
      <div class="cv-bdg">
        <span class="cv-b" style="border-color:#4a9400;color:#4a9400;font-weight:700;">🏥 anbuclinic.me · LIVE PRODUCT · BILLED</span>
        <span class="cv-b" style="border-color:#b05000;color:#b05000;">🏢 AI Vision · Freelance AIML · 2+ Yrs · Udyam Reg: UDYAM-TN-02-0483528</span>
        <span class="cv-b">⚡ PATENT FILED · APR 2026</span>
        <span class="cv-b">📄 IEEE PAPER SUBMITTED</span>
        <span class="cv-b">🎓 M.TECH AI · GRADUATED MAY 2026 · 9.6 CGPA</span>
        <span class="cv-b">🤗 3 LIVE MODELS · HUGGINGFACE</span>
        <span class="cv-b" style="border-color:#a6ce39;color:#a6ce39;">🆔 ORCID REGISTERED</span>
        <span class="cv-b" style="border-color:#4285f4;color:#4285f4;">📚 GOOGLE SCHOLAR VERIFIED</span>
        <span class="cv-b">9+ YRS ENGINEERING</span>
      </div>

      <div class="cv-h2">PROFILE</div>
      <p class="cv-sum">AI/ML Engineer and founder of AI Vision (Udyam Reg: UDYAM-TN-02-0483528) — a registered freelance AI practice active for 2+ years. Delivered and billed a live production AI product: Anbu Health AI at anbuclinic.me (Invoice AIV-2026-001, ₹21,500, June 2026) — a multilingual Tamil/English AI doctor assistant for village clinic patients in Ariyalur District, Tamil Nadu. Graduated M.Tech in Artificial Intelligence from SRM Institute (May 2026, CGPA 9.6/10). Filed Indian Patent No. 202641043947 for Antahkarana; IEEE Conference paper submitted and indexed on Google Scholar. ORCID: 0009-0006-9701-7942. Built and published 3 live models on HuggingFace. 9+ years prior safety-critical electrical engineering experience.</p>

      <div class="cv-h2">FREELANCE EXPERIENCE — AI VISION</div>
      <div class="cv-ei">
        <div class="cv-eh"><span class="cv-er">Founder & AI/ML Engineer</span><span class="cv-ed">2024 – Present</span></div>
        <div class="cv-eo">AI Vision · Udyam Reg: UDYAM-TN-02-0483528 · Chennai, Tamil Nadu</div>
        <div class="cv-ex">Registered freelance AI practice. Built and delivered Anbu Health AI (anbuclinic.me) — a live, billed, production-grade AI health product. Invoice AIV-2026-001 issued June 2026 to Anbu Clinic, Pappakudi, Ariyalur District (Dr. Raghul M.D, Dr. Rajeswari M.D). Stack: React 19 · FastAPI · Groq LLaMA 3.3 70B · GPT-4o · Qdrant · Supabase · Sarvam Tamil TTS · Azure Container Apps · Terraform · Prometheus · DPDP Act 2023 compliant. Monthly maintenance ₹1,500/month from July 2026.</div>
      </div>

      <div class="cv-h2">RESEARCH &amp; INTELLECTUAL PROPERTY</div>
      <div class="cv-ei">
        <div class="cv-eh"><span class="cv-er">Antahkarana: Cognitively-Inspired Adaptive Reasoning for LLMs and VLMs</span></div>
        <div class="cv-eo">IEEE Conference Paper · SRM Institute · 2026 · Under Review · Google Scholar Indexed</div>
        <div class="cv-ex">Modular conditional reasoning framework inspired by Vedantic cognitive architecture. Validated on 2,500+ multimodal samples. Authors: Raja Ganapathy M, RG Karthikeyan.</div>
      </div>
      <div class="cv-ei">
        <div class="cv-eh"><span class="cv-er">Indian Patent — Antahkarana Adaptive AI Reasoning System</span><span class="cv-ed">Filed Apr 3, 2026</span></div>
        <div class="cv-eo">Application No. 202641043947 · Indian Patent Office · Under Examination</div>
      </div>

      <div class="cv-h2">EDUCATION</div>
      <div class="cv-ei">
        <div class="cv-eh"><span class="cv-er">M.Tech — Artificial Intelligence</span><span class="cv-ed">2024 – May 2026</span></div>
        <div class="cv-eo">SRM Institute of Science &amp; Technology · Chennai · CGPA: 9.6 / 10 · <strong style="color:#4a9400;">Graduated</strong></div>
      </div>
      <div class="cv-ei">
        <div class="cv-eh"><span class="cv-er">B.E — Electrical & Electronics Engineering</span><span class="cv-ed">2013</span></div>
        <div class="cv-eo">Thangavelu Engineering College · Chennai</div>
      </div>

      <div class="cv-h2">KEY PROJECTS</div>
      <div class="cv-pg">
        <div class="cv-pi" style="border-color:#4a9400;background:#f8fff4;"><div class="cv-pn" style="color:#2a6000;">Anbu Health AI — anbuclinic.me (LIVE · BILLED)</div><div class="cv-pt">React 19 · Groq LLaMA 3.3 70B · GPT-4o · Qdrant · Supabase · Azure · Sarvam TTS · DPDP · Invoice AIV-2026-001 ₹21,500</div></div>
        <div class="cv-pi"><div class="cv-pn">Antahkarana Reasoning Framework</div><div class="cv-pt">Python · Qwen · BLIP-3 · Patent filed · IEEE submitted · Scholar indexed</div></div>
        <div class="cv-pi"><div class="cv-pn">TinyLLaMA & Mini-VLM (HuggingFace)</div><div class="cv-pt">Built from scratch · LoRA fine-tune · 2 live public models</div></div>
        <div class="cv-pi"><div class="cv-pn">MML Smart Campus Security</div><div class="cv-pt">OpenAI CLIP · Salesforce BLIP · PyTorch · Voice Biometrics</div></div>
        <div class="cv-pi"><div class="cv-pn">AgentNet Enterprise Support</div><div class="cv-pt">Multi-agent · LLM-as-Judge · RAG · Vertex AI</div></div>
        <div class="cv-pi"><div class="cv-pn">Conscious AI Browser (Chromium)</div><div class="cv-pt">26,000 build steps · LLaMA 3.3 70B · Linux .deb · Vercel</div></div>
      </div>

      <div class="cv-h2">PROFESSIONAL EXPERIENCE</div>
      <div class="cv-ei">
        <div class="cv-eh"><span class="cv-er">Electrical Construction Site Engineer</span><span class="cv-ed">Jan 2017 – Jun 2023</span></div>
        <div class="cv-eo">SR Electrical Works · Chennai</div>
        <div class="cv-ex">Large-scale electrical systems for construction projects. Led budget estimation, resource allocation, site supervision, and cross-team coordination under hard safety constraints.</div>
      </div>
      <div class="cv-ei">
        <div class="cv-eh"><span class="cv-er">Electrical Maintenance Engineer</span><span class="cv-ed">Dec 2014 – Dec 2016</span></div>
        <div class="cv-eo">Mod Forge Pvt. Ltd. · ISO/TS 16949 Certified · Chennai</div>
        <div class="cv-ex">O&amp;M of 500 kVA transformer, 250 kVA DG, motors up to 400 kW, power factor correction panels and automation under C-certificate supervision.</div>
      </div>

      <div class="cv-h2">TECHNICAL SKILLS</div>
      <div class="cv-sc">
        <div><div class="cv-sg">Generative AI / LLMs</div><div class="cv-sl">LLM Orchestration<br/>RAG · FAISS · Vector DBs<br/>Prompt Engineering<br/>Agentic Workflows<br/>LangChain · HuggingFace</div></div>
        <div><div class="cv-sg">ML / Deep Learning</div><div class="cv-sl">PyTorch · TensorFlow<br/>scikit-learn · XGBoost<br/>CNN · LSTM · Transformers<br/>NLP · Embeddings<br/>Computer Vision · OpenCV</div></div>
        <div><div class="cv-sg">Cloud / DevOps / Data</div><div class="cv-sl">AWS · Azure · Docker<br/>Git · GitHub Actions CI/CD<br/>Python · SQL · MongoDB<br/>Streamlit · Plotly<br/>Linux · Bash · R</div></div>
      </div>

      <div class="cv-h2">CERTIFICATIONS</div>
      <div class="cv-cl">
        <div class="cv-ce"><span>AWS</span> Solutions Architect Associate · Udemy 2025</div>
        <div class="cv-ce"><span>GUVI</span> AI &amp; ML Professional Program · IIT-M 2024</div>
        <div class="cv-ce"><span>Kaggle</span> 5-Day AI Agents Intensive with Google · 2025</div>
        <div class="cv-ce"><span>DevOps</span> Beginners to Advanced · Udemy 2025</div>
        <div class="cv-ce"><span>NPTEL</span> Introduction to Internet of Things · 2025</div>
        <div class="cv-ce"><span>IIT-M</span> Certificate Professional · Advanced Programming 2024</div>
        <div class="cv-ce"><span>OpenCV</span> OpenCV University Certification · 2025</div>
        <div class="cv-ce"><span>Simplilearn</span> PyTorch · TensorFlow · DSA · GIT · MongoDB</div>
      </div>

      <div class="cv-ft">
        <span>rajaganaa.github.io · orcid.org/0009-0006-9701-7942 · scholar.google.com</span>
        <span id="cvGenDate">Generated May 2026</span>
      </div>
    </div>
  </div>
</div>

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
  <p>© 2026 Rajaganapathy M — AI Engineer · AI Vision (Udyam Reg: UDYAM-TN-02-0483528) · Chennai, India</p>
  <p>Live Product: anbuclinic.me · Patent pending · IEEE under review · ORCID: 0009-0006-9701-7942 · Open to world-class opportunities</p>
</footer>

<script>
const observer = new IntersectionObserver((entries) => {
  entries.forEach((e, i) => {
    if (e.isIntersecting) {
      setTimeout(() => e.target.classList.add('visible'), (i % 4) * 90);
      observer.unobserve(e.target);
    }
  });
}, { threshold: 0.08 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

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
toggle.addEventListener('click', () => {
  light = !light;
  toggle.textContent = light ? '☾ dark' : '☀ light';
  if (light) {
    const s = document.createElement('style');
    s.id = 'light-override'; s.textContent = lightCSS;
    document.head.appendChild(s);
  } else { document.getElementById('light-override')?.remove(); }
});

function downloadCV() {
  const genDate = new Date().toLocaleDateString('en-GB', {month:'long', year:'numeric'});
  const html = `<!DOCTYPE html><html><head><meta charset="UTF-8"/>
<title>Rajaganapathy M — CV</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:'DM Sans',sans-serif;color:#18180f;background:#fff;font-size:14px;line-height:1.65;padding:3rem 4rem;}
@media print{body{padding:1.5rem 2rem;}}
h1{font-family:'DM Sans',sans-serif;font-size:2.4rem;font-weight:700;letter-spacing:-0.02em;margin-bottom:0.2rem;}
.sub{font-family:'DM Mono',monospace;font-size:11px;color:#4a9400;letter-spacing:0.1em;margin-bottom:0.75rem;}
.bar{font-family:'DM Mono',monospace;font-size:11px;color:#5a5750;display:flex;flex-wrap:wrap;gap:1rem;margin-bottom:1.5rem;padding-bottom:1rem;border-bottom:2px solid #18180f;}
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
.ft{margin-top:2rem;padding-top:1rem;border-top:1px solid #e0ddd6;font-family:'DM Mono',monospace;font-size:10px;color:#9a9890;display:flex;justify-content:space-between;flex-wrap:wrap;gap:0.5rem;}
</style></head><body>
<h1>Rajaganapathy M</h1>
<div class="sub">AI / ML ENGINEER · LLM · AGENTIC AI · RAG · MULTI-AGENT SYSTEMS</div>
<div class="bar">
  <span>✉ rajaganaa@gmail.com</span><span>📞 +91 9176631419</span>
  <span>🌐 rajaganaa.github.io</span><span>in raja-ganapathy-36b00658</span>
  <span>⌥ github.com/rajaganaa</span>
  <span>🆔 orcid.org/0009-0006-9701-7942</span>
  <span>📚 Google Scholar · Raja Ganapathy M</span>
  <span>📍 Chennai, India</span>
</div>
<div class="bdg">
  <span class="b">⚡ PATENT FILED · APR 2026</span>
  <span class="b">📄 IEEE PAPER SUBMITTED</span>
  <span class="b">🎓 M.TECH AI · MAY 2026 · 9.6 CGPA</span>
  <span class="b">🤗 3 LIVE MODELS · HUGGINGFACE</span>
  <span class="b" style="border-color:#a6ce39;color:#a6ce39;">🆔 ORCID REGISTERED</span>
  <span class="b" style="border-color:#4285f4;color:#4285f4;">📚 GOOGLE SCHOLAR</span>
  <span class="b">9+ YRS ENGINEERING</span>
</div>
<h2>PROFILE</h2>
<p class="sum">AI/ML Engineer with 9+ years of prior industry experience in safety-critical engineering. Graduated M.Tech in Artificial Intelligence from SRM Institute of Science &amp; Technology, Chennai (May 2026, CGPA 9.6/10). Filed Indian Patent (No. 202641043947) for Antahkarana — a cognitively-inspired reasoning framework for LLMs and VLMs; IEEE Conference paper submitted, indexed on Google Scholar. ORCID: 0009-0006-9701-7942. Built and published 3 live models on HuggingFace (LLM + VLM from scratch; CodeLlama-7B fine-tuned with QLoRA on AWS SageMaker).</p>
<h2>RESEARCH &amp; IP</h2>
<div class="ei"><div class="er">Antahkarana: Cognitively-Inspired Adaptive Reasoning for LLMs and VLMs</div><div class="eo">IEEE Conference Paper · 2026 · Under Review · Google Scholar Indexed · Authors: Raja Ganapathy M, RG Karthikeyan</div></div>
<div class="ei"><div class="eh"><span class="er">Indian Patent — Antahkarana Adaptive AI Reasoning System</span><span class="ed">Filed Apr 3, 2026</span></div><div class="eo">Application No. 202641043947 · Indian Patent Office</div></div>
<h2>EDUCATION</h2>
<div class="ei"><div class="eh"><span class="er">M.Tech — Artificial Intelligence</span><span class="ed">2024 – May 2026</span></div><div class="eo">SRM Institute of Science &amp; Technology · Chennai · CGPA: 9.6 / 10 · <strong>Graduated</strong></div></div>
<div class="ei"><div class="eh"><span class="er">B.E — Electrical & Electronics Engineering</span><span class="ed">2013</span></div><div class="eo">Thangavelu Engineering College · Chennai</div></div>
<h2>KEY PROJECTS</h2>
<div class="pg">
  <div class="pi"><div class="pn">Antahkarana Reasoning Framework</div><div class="pt">Python · Qwen · BLIP-3 · Patent · IEEE · Scholar</div></div>
  <div class="pi"><div class="pn">Antahkarana Medical AI (Live)</div><div class="pt">Azure · GitHub Actions CI/CD · Multimodal</div></div>
  <div class="pi"><div class="pn">MML Smart Campus Security</div><div class="pt">OpenAI CLIP · BLIP · PyTorch · Voice Biometrics</div></div>
  <div class="pi"><div class="pn">AgentNet Enterprise Support</div><div class="pt">Multi-agent · LLM-as-Judge · RAG · Vertex AI</div></div>
  <div class="pi"><div class="pn">Hospital Readmission Predictor</div><div class="pt">XGBoost · Streamlit · Healthcare analytics</div></div>
  <div class="pi"><div class="pn">Conscious AI Browser (Chromium)</div><div class="pt">26,000 build steps · LLaMA 3.3 70B · Linux .deb</div></div>
</div>
<h2>PROFESSIONAL EXPERIENCE</h2>
<div class="ei"><div class="eh"><span class="er">Electrical Construction Site Engineer</span><span class="ed">Jan 2017 – Jun 2023</span></div><div class="eo">SR Electrical Works · Chennai</div><div class="ex">Large-scale electrical systems. Budget estimation, resource allocation, site supervision under hard safety constraints.</div></div>
<div class="ei"><div class="eh"><span class="er">Electrical Maintenance Engineer</span><span class="ed">Dec 2014 – Dec 2016</span></div><div class="eo">Mod Forge Pvt. Ltd. · ISO/TS 16949 · Chennai</div><div class="ex">O&M of 500 kVA transformer, 250 kVA DG, motors up to 400 kW under C-certificate supervision.</div></div>
<h2>TECHNICAL SKILLS</h2>
<div class="sc">
  <div><div class="sg">Generative AI / LLMs</div><div class="sl">LLM Orchestration<br/>RAG · FAISS · Vector DBs<br/>Prompt Engineering<br/>Agentic Workflows<br/>LangChain · HuggingFace</div></div>
  <div><div class="sg">ML / Deep Learning</div><div class="sl">PyTorch · TensorFlow<br/>scikit-learn · XGBoost<br/>CNN · LSTM · Transformers<br/>NLP · Embeddings<br/>Computer Vision · OpenCV</div></div>
  <div><div class="sg">Cloud / DevOps / Data</div><div class="sl">AWS · Azure · Docker<br/>Git · GitHub Actions CI/CD<br/>Python · SQL · MongoDB<br/>Streamlit · Plotly<br/>Linux · Bash · R</div></div>
</div>
<h2>CERTIFICATIONS</h2>
<div class="cl">
  <div class="ce"><span>AWS</span> Solutions Architect Associate · 2025</div>
  <div class="ce"><span>GUVI</span> AI &amp; ML Professional Program · IIT-M 2024</div>
  <div class="ce"><span>Kaggle</span> 5-Day AI Agents Intensive with Google · 2025</div>
  <div class="ce"><span>DevOps</span> Beginners to Advanced · Udemy 2025</div>
  <div class="ce"><span>NPTEL</span> Introduction to Internet of Things · 2025</div>
  <div class="ce"><span>IIT-M</span> Certificate Professional · Advanced Programming 2024</div>
</div>
<div class="ft">
  <span>rajaganaa.github.io · orcid.org/0009-0006-9701-7942 · scholar.google.com</span>
  <span>Generated ${genDate}</span>
</div>
</body></html>`;
  const blob = new Blob([html], {type:'text/html'});
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url; a.download = 'Rajaganapathy_M_CV.html';
  a.click(); URL.revokeObjectURL(url);
}

const blogs = [
  {
    tag: 'CAREER · AI',
    date: 'May 2026 · 6 min read',
    title: 'From Electrical Engineer to AI Engineer — What Really Transfers',
    body: `<p>In June 2023, after nine years of working on electrical systems across industrial sites in Chennai, I quit my job. Not because I was failing — I was good at it. I quit because I wanted to build a different kind of system.</p>
<h3>What I thought would transfer</h3>
<p>I assumed the engineering fundamentals would carry over: systems thinking, problem decomposition, reading technical documentation. I was right about those. What surprised me was <em>how much deeper</em> that transfer went.</p>
<p>In industrial electrical work, you build things that operate continuously under unpredictable conditions. A 500 kVA transformer doesn't get to fail at 3am because the load spiked. You design for failure modes before they happen. You think about what the system does when something unexpected occurs — not just what it does when everything is normal.</p>
<p>That mindset is rare in AI engineering. Most ML practitioners optimise for the happy path. My instinct is always: <strong>what happens at the edge cases?</strong></p>
<h3>What actually doesn't transfer</h3>
<p>Mathematics. I had to rebuild from scratch — linear algebra, probability theory, calculus. This took six months of uncomfortable work before I could read ML papers without feeling lost.</p>
<h3>The unexpected advantage</h3>
<p>The biggest transfer no one talks about: <em>project management in safety-critical environments</em>. When you've coordinated electrical installation across a live construction site, running a complex ML project feels almost straightforward by comparison.</p>
<p>I don't regret the nine years. They made me a better AI engineer than I would have been if I'd started at 22.</p>`
  },
  {
    tag: 'LLM · RESEARCH',
    date: 'April 2026 · 9 min read',
    title: 'How I Built Antahkarana — A Cognitively-Inspired Reasoning Framework',
    body: `<p>Most LLM pipelines are, at their core, sophisticated prompt chains. You send a query, you get a response. Maybe you add retrieval. Maybe you add a tool call. But the fundamental architecture is linear: input → model → output.</p>
<p>Antahkarana is different. It routes complex queries through specialised cognitive stages — each responsible for a distinct aspect of reasoning — before synthesising a final response. The inspiration came from an unlikely source: Vedantic philosophy.</p>
<h3>The cognitive architecture</h3>
<p>In Vedantic thought, the <em>antahkarana</em> is the inner instrument of the mind — four distinct functions: <strong>manas</strong> (perception and doubt), <strong>buddhi</strong> (discrimination and decision), <strong>chitta</strong> (memory and conditioning), and <strong>ahamkara</strong> (the ego that integrates everything).</p>
<p>I mapped these directly to LLM reasoning stages. The result earned an Indian patent filing and a submitted IEEE paper — now indexed on Google Scholar and linked to my ORCID researcher identity.</p>
<h3>Why it works better</h3>
<p>The key insight is that different reasoning tasks require different cognitive postures. By routing explicitly, Antahkarana applies the right tool to the right task — and the 2,500-sample validation showed measurable improvements in coherence on complex multimodal queries.</p>`
  },
  {
    tag: 'AGENTIC AI',
    date: 'March 2026 · 7 min read',
    title: 'RAG vs Fine-Tuning: Lessons from Building a Medical AI Assistant',
    body: `<p>When I started building the Antahkarana medical AI assistant, I had to make the RAG vs. fine-tuning decision for every sub-task. After months of building and testing, here's the framework I arrived at.</p>
<h3>The question is wrong</h3>
<p>The industry frames this as a binary choice. It isn't. The real question is: <em>what is the nature of the knowledge this task requires?</em></p>
<p><strong>RAG wins</strong> when the knowledge is: external and updatable (medical guidelines change), verifiable (you need citations), or domain-specific and voluminous.</p>
<p><strong>Fine-tuning wins</strong> when the task requires: a specific output format the base model can't reliably produce, internalised reasoning patterns (not facts), or latency-critical inference where retrieval overhead is unacceptable.</p>
<h3>The biggest lesson</h3>
<p><em>Don't fine-tune to fix retrieval problems.</em> If your RAG pipeline is returning poor context, fine-tuning the generator won't help — it'll just learn to hallucinate more confidently. Fix the retrieval first.</p>
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

function openCVModal() {
  document.getElementById('cvModal').classList.add('open');
  document.body.style.overflow = 'hidden';
  document.getElementById('cvGenDate').textContent =
    'Generated ' + new Date().toLocaleDateString('en-GB', {month:'long', year:'numeric'});
}
function closeCVModal() {
  document.getElementById('cvModal').classList.remove('open');
  document.body.style.overflow = '';
  const url = new URL(window.location);
  if (url.searchParams.has('resume')) {
    url.searchParams.delete('resume');
    history.replaceState({}, '', url);
  }
}
function closeCVOnOverlay(e) {
  if (e.target === document.getElementById('cvModal')) closeCVModal();
}
function printCV() {
  const content = document.getElementById('cvContent').innerHTML;
  const win = window.open('', '_blank', 'width=900,height=700');
  win.document.write(`<!DOCTYPE html><html><head><meta charset="UTF-8"/>
<title>Rajaganapathy M — CV</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:'DM Sans',sans-serif;color:#18180f;background:#fff;font-size:14px;line-height:1.65;padding:2.5rem 3.5rem;}
.cv-h1{font-size:2.2rem;font-weight:700;letter-spacing:-0.02em;margin-bottom:0.2rem;color:#18180f;}
.cv-sub{font-family:'DM Mono',monospace;font-size:11px;color:#4a9400;letter-spacing:0.1em;margin-bottom:0.75rem;}
.cv-bar{font-family:'DM Mono',monospace;font-size:11px;color:#5a5750;display:flex;flex-wrap:wrap;gap:1rem;margin-bottom:1.5rem;padding-bottom:1rem;border-bottom:2px solid #18180f;}
.cv-bdg{display:inline-flex;gap:0.5rem;flex-wrap:wrap;margin-bottom:1.5rem;}
.cv-b{font-family:'DM Mono',monospace;font-size:10px;border:1px solid #4a9400;color:#4a9400;padding:2px 9px;}
.cv-h2{font-family:'DM Mono',monospace;font-size:10px;font-weight:500;letter-spacing:0.18em;color:#4a9400;margin:1.5rem 0 0.6rem;padding-bottom:3px;border-bottom:1px solid #e0ddd6;}
.cv-sum{font-size:13px;font-weight:300;color:#3a3830;line-height:1.85;}
.cv-ei{margin-bottom:1rem;}
.cv-eh{display:flex;justify-content:space-between;align-items:baseline;}
.cv-er{font-weight:600;font-size:14px;color:#18180f;}
.cv-ed{font-family:'DM Mono',monospace;font-size:10px;color:#5a5750;}
.cv-eo{font-family:'DM Mono',monospace;font-size:11px;color:#5a5750;margin-bottom:3px;}
.cv-ex{font-size:12px;font-weight:300;color:#5a5750;line-height:1.75;}
.cv-pg{display:grid;grid-template-columns:1fr 1fr;gap:0.75rem;}
.cv-pi{border:1px solid #e0ddd6;padding:0.75rem;}
.cv-pn{font-weight:600;font-size:13px;margin-bottom:2px;color:#18180f;}
.cv-pt{font-family:'DM Mono',monospace;font-size:10px;color:#5a5750;}
.cv-sc{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem;}
.cv-sg{font-weight:600;font-size:12px;margin-bottom:4px;color:#18180f;}
.cv-sl{font-family:'DM Mono',monospace;font-size:11px;font-weight:300;color:#5a5750;line-height:1.85;}
.cv-cl{display:grid;grid-template-columns:1fr 1fr;gap:4px;}
.cv-ce{font-family:'DM Mono',monospace;font-size:11px;font-weight:300;color:#5a5750;}
.cv-ce span{color:#18180f;font-weight:500;}
.cv-ft{margin-top:2rem;padding-top:1rem;border-top:1px solid #e0ddd6;font-family:'DM Mono',monospace;font-size:10px;color:#9a9890;display:flex;justify-content:space-between;flex-wrap:wrap;gap:0.5rem;}
</style></head><body>${content}</body></html>`);
  win.document.close();
  win.focus();
  setTimeout(() => win.print(), 600);
}
window.addEventListener('DOMContentLoaded', () => {
  if (new URLSearchParams(window.location.search).get('resume') === '1') {
    setTimeout(openCVModal, 400);
  }
});
document.addEventListener('keydown', e => {
  if (e.key === 'Escape') { closeBlog(); closeCVModal(); }
});
</script>

</body>
</html>
