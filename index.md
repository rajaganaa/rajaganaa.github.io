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
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=DM+Mono:ital,wght@0,300;0,400;0,500;1,300&family=Lora:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0a0a0a;
    --bg2: #111111;
    --bg3: #181818;
    --border: rgba(255,255,255,0.08);
    --border-strong: rgba(255,255,255,0.15);
    --text: #f0ede8;
    --text-muted: #888880;
    --text-dim: #555550;
    --accent: #c8f064;
    --accent2: #64d4f0;
    --accent3: #f0a064;
    --font-display: 'Syne', sans-serif;
    --font-mono: 'DM Mono', monospace;
    --font-serif: 'Lora', serif;
    --nav-bg: rgba(10,10,10,0.85);
  }

  body.light {
    --bg: #f5f3ee;
    --bg2: #eeebe4;
    --bg3: #e5e2da;
    --border: rgba(0,0,0,0.08);
    --border-strong: rgba(0,0,0,0.18);
    --text: #1a1a18;
    --text-muted: #5a5a52;
    --text-dim: #9a9a90;
    --accent: #6aaa00;
    --accent2: #0088aa;
    --nav-bg: rgba(245,243,238,0.88);
  }

  body.light .hero-grid-bg {
    background-image:
      linear-gradient(rgba(0,0,0,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,0,0,0.04) 1px, transparent 1px);
  }

  body.light .hero-accent-circle {
    background: radial-gradient(circle, rgba(100,170,0,0.08) 0%, transparent 70%);
  }

  body.light nav { background: var(--nav-bg); }

  body.light .skill-dot { background: rgba(0,0,0,0.12); }

  /* THEME TOGGLE */
  .theme-toggle {
    background: none;
    border: 1px solid var(--border-strong);
    color: var(--text-muted);
    font-family: var(--font-mono);
    font-size: 12px;
    padding: 0.4rem 0.8rem;
    cursor: pointer;
    letter-spacing: 0.06em;
    transition: all 0.2s;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .theme-toggle:hover { border-color: var(--accent); color: var(--accent); }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-display);
    font-size: 16px;
    line-height: 1.6;
    overflow-x: hidden;
  }

  ::selection { background: var(--accent); color: #0a0a0a; }

  /* NOISE TEXTURE OVERLAY */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 9999;
    opacity: 0.4;
  }

  /* NAV */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1.25rem 4rem;
    border-bottom: 1px solid var(--border);
    background: var(--nav-bg);
    backdrop-filter: blur(20px);
  }

  .nav-logo {
    font-family: var(--font-mono);
    font-size: 13px;
    color: var(--accent);
    letter-spacing: 0.05em;
    text-decoration: none;
  }

  .nav-links {
    display: flex;
    gap: 2.5rem;
    list-style: none;
  }

  .nav-links a {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--text-muted);
    text-decoration: none;
    letter-spacing: 0.08em;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--text); }

  .nav-cta {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--accent);
    border: 1px solid var(--accent);
    padding: 0.5rem 1.25rem;
    text-decoration: none;
    letter-spacing: 0.08em;
    transition: all 0.2s;
  }

  .nav-cta:hover {
    background: var(--accent);
    color: #0a0a0a;
  }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 8rem 4rem 4rem;
    position: relative;
    overflow: hidden;
  }

  .hero-grid-bg {
    position: absolute;
    inset: 0;
    background-image:
      linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
    background-size: 80px 80px;
    mask-image: radial-gradient(ellipse 80% 80% at 50% 50%, black 40%, transparent 100%);
  }

  .hero-accent-circle {
    position: absolute;
    width: 600px;
    height: 600px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(200,240,100,0.06) 0%, transparent 70%);
    top: -200px;
    right: -100px;
    pointer-events: none;
  }

  .hero-tag {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--accent);
    letter-spacing: 0.15em;
    margin-bottom: 2rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
    opacity: 0;
    animation: fadeUp 0.8s 0.1s forwards;
  }

  .hero-tag::before {
    content: '';
    display: block;
    width: 32px;
    height: 1px;
    background: var(--accent);
  }

  .hero-name {
    font-family: var(--font-display);
    font-size: clamp(3.5rem, 8vw, 7rem);
    font-weight: 800;
    line-height: 0.95;
    letter-spacing: -0.03em;
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fadeUp 0.8s 0.2s forwards;
  }

  .hero-name span {
    color: var(--accent);
    display: block;
  }

  .hero-tagline {
    font-family: var(--font-serif);
    font-style: italic;
    font-size: clamp(1.1rem, 2vw, 1.4rem);
    color: var(--text-muted);
    max-width: 580px;
    line-height: 1.7;
    margin-bottom: 2.5rem;
    opacity: 0;
    animation: fadeUp 0.8s 0.35s forwards;
  }

  .hero-badges {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    margin-bottom: 3rem;
    opacity: 0;
    animation: fadeUp 0.8s 0.5s forwards;
  }

  .badge {
    font-family: var(--font-mono);
    font-size: 11px;
    letter-spacing: 0.08em;
    padding: 0.4rem 1rem;
    border: 1px solid var(--border-strong);
    color: var(--text-muted);
    white-space: nowrap;
  }

  .badge-highlight {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(200,240,100,0.05);
  }

  .badge-blue {
    border-color: var(--accent2);
    color: var(--accent2);
    background: rgba(100,212,240,0.05);
  }

  .hero-actions {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    opacity: 0;
    animation: fadeUp 0.8s 0.65s forwards;
  }

  .btn-primary {
    font-family: var(--font-mono);
    font-size: 13px;
    letter-spacing: 0.08em;
    padding: 0.9rem 2rem;
    background: var(--accent);
    color: #0a0a0a;
    text-decoration: none;
    font-weight: 500;
    transition: all 0.2s;
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
  }

  .btn-primary:hover { background: #d8ff70; transform: translateY(-1px); }

  .btn-secondary {
    font-family: var(--font-mono);
    font-size: 13px;
    letter-spacing: 0.08em;
    padding: 0.9rem 2rem;
    border: 1px solid var(--border-strong);
    color: var(--text);
    text-decoration: none;
    transition: all 0.2s;
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
  }

  .btn-secondary:hover { border-color: var(--text); background: rgba(255,255,255,0.03); }

  .hero-scroll {
    position: absolute;
    bottom: 2rem;
    left: 4rem;
    font-family: var(--font-mono);
    font-size: 11px;
    color: var(--text-dim);
    letter-spacing: 0.1em;
    display: flex;
    align-items: center;
    gap: 0.75rem;
    animation: fadeUp 1s 1s forwards;
    opacity: 0;
  }

  .hero-scroll::after {
    content: '';
    display: block;
    width: 1px;
    height: 48px;
    background: linear-gradient(to bottom, var(--text-dim), transparent);
  }

  .hero-stats {
    position: absolute;
    bottom: 2rem;
    right: 4rem;
    display: flex;
    gap: 2.5rem;
    opacity: 0;
    animation: fadeUp 0.8s 0.8s forwards;
  }

  .hero-stat { text-align: right; }
  .hero-stat-num {
    font-family: var(--font-display);
    font-size: 2rem;
    font-weight: 800;
    color: var(--text);
    line-height: 1;
  }
  .hero-stat-label {
    font-family: var(--font-mono);
    font-size: 10px;
    color: var(--text-dim);
    letter-spacing: 0.1em;
    margin-top: 4px;
  }

  /* SECTIONS */
  section {
    padding: 6rem 4rem;
    border-top: 1px solid var(--border);
  }

  .section-label {
    font-family: var(--font-mono);
    font-size: 11px;
    letter-spacing: 0.2em;
    color: var(--text-dim);
    margin-bottom: 3rem;
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
    max-width: 120px;
  }

  /* ABOUT */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5rem;
    align-items: start;
  }

  .about-statement {
    font-family: var(--font-serif);
    font-size: clamp(1.3rem, 2.2vw, 1.7rem);
    line-height: 1.6;
    color: var(--text);
  }

  .about-statement em {
    color: var(--accent);
    font-style: italic;
  }

  .about-right p {
    font-family: var(--font-mono);
    font-size: 13px;
    color: var(--text-muted);
    line-height: 1.9;
    margin-bottom: 1.5rem;
  }

  .about-right p strong {
    color: var(--text);
    font-weight: 500;
  }

  /* TIMELINE */
  .timeline {
    position: relative;
    padding-left: 2rem;
  }

  .timeline::before {
    content: '';
    position: absolute;
    left: 0;
    top: 8px;
    bottom: 0;
    width: 1px;
    background: linear-gradient(to bottom, var(--accent), transparent);
  }

  .timeline-item {
    position: relative;
    padding-bottom: 2.5rem;
    padding-left: 1.5rem;
  }

  .timeline-item::before {
    content: '';
    position: absolute;
    left: -2rem;
    top: 8px;
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 12px rgba(200,240,100,0.4);
  }

  .timeline-year {
    font-family: var(--font-mono);
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 0.1em;
    margin-bottom: 4px;
  }

  .timeline-role {
    font-family: var(--font-display);
    font-size: 15px;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 2px;
  }

  .timeline-org {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--text-muted);
  }

  /* PROJECTS */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
    gap: 1.5px;
    background: var(--border);
  }

  .project-card {
    background: var(--bg);
    padding: 2rem;
    position: relative;
    transition: background 0.2s;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    text-decoration: none;
    color: inherit;
  }

  .project-card:hover { background: var(--bg3); }

  .project-card:hover .project-arrow { transform: translate(3px, -3px); }

  .project-top {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
  }

  .project-num {
    font-family: var(--font-mono);
    font-size: 11px;
    color: var(--text-dim);
    letter-spacing: 0.1em;
  }

  .project-arrow {
    font-size: 18px;
    color: var(--text-dim);
    transition: transform 0.2s;
    line-height: 1;
  }

  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .project-tag {
    font-family: var(--font-mono);
    font-size: 10px;
    letter-spacing: 0.06em;
    padding: 3px 8px;
    background: var(--bg3);
    color: var(--text-dim);
    border: 1px solid var(--border);
  }

  .project-tag-accent {
    border-color: rgba(200,240,100,0.3);
    color: rgba(200,240,100,0.7);
  }

  .project-title {
    font-family: var(--font-display);
    font-size: 1.2rem;
    font-weight: 700;
    line-height: 1.3;
    color: var(--text);
  }

  .project-desc {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--text-muted);
    line-height: 1.8;
    flex: 1;
  }

  .project-metric {
    font-family: var(--font-mono);
    font-size: 11px;
    color: var(--accent);
    padding-top: 0.75rem;
    border-top: 1px solid var(--border);
  }

  /* FEATURED PROJECT */
  .featured-project {
    grid-column: 1 / -1;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0;
    background: var(--bg);
    border: 1px solid rgba(200,240,100,0.2);
    position: relative;
    overflow: hidden;
  }

  .featured-project::before {
    content: 'FLAGSHIP';
    position: absolute;
    top: 1.5rem;
    right: 1.5rem;
    font-family: var(--font-mono);
    font-size: 10px;
    letter-spacing: 0.2em;
    color: var(--accent);
    border: 1px solid rgba(200,240,100,0.3);
    padding: 3px 10px;
  }

  .featured-left {
    padding: 2.5rem;
    border-right: 1px solid rgba(200,240,100,0.1);
  }

  .featured-right {
    padding: 2.5rem;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .featured-title {
    font-family: var(--font-display);
    font-size: 1.8rem;
    font-weight: 800;
    line-height: 1.2;
    color: var(--text);
    margin-bottom: 1rem;
    margin-top: 2rem;
  }

  .featured-title span { color: var(--accent); }

  .featured-desc {
    font-family: var(--font-serif);
    font-size: 14px;
    color: var(--text-muted);
    line-height: 1.9;
    font-style: italic;
  }

  .featured-badges {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-top: 1rem;
  }

  .achievement-item {
    display: flex;
    align-items: flex-start;
    gap: 1rem;
    padding: 1rem;
    border: 1px solid var(--border);
  }

  .achievement-icon {
    font-size: 1.2rem;
    line-height: 1;
    flex-shrink: 0;
  }

  .achievement-text {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--text-muted);
    line-height: 1.6;
  }

  .achievement-text strong {
    color: var(--text);
    display: block;
    font-size: 13px;
    margin-bottom: 2px;
  }

  /* SKILLS */
  .skills-layout {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 2rem;
  }

  .skill-group { }

  .skill-group-title {
    font-family: var(--font-mono);
    font-size: 11px;
    letter-spacing: 0.15em;
    color: var(--accent);
    margin-bottom: 1rem;
    padding-bottom: 0.5rem;
    border-bottom: 1px solid var(--border);
  }

  .skill-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0.6rem 0;
    border-bottom: 1px solid rgba(255,255,255,0.03);
  }

  .skill-name {
    font-family: var(--font-mono);
    font-size: 13px;
    color: var(--text-muted);
  }

  .skill-level {
    display: flex;
    gap: 3px;
  }

  .skill-dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: var(--border-strong);
  }

  .skill-dot.active { background: var(--accent); }

  /* CERTS */
  .certs-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 1rem;
  }

  .cert-card {
    border: 1px solid var(--border);
    padding: 1.25rem;
    display: flex;
    gap: 1rem;
    align-items: flex-start;
    transition: border-color 0.2s;
  }

  .cert-card:hover { border-color: var(--border-strong); }

  .cert-icon {
    width: 36px;
    height: 36px;
    flex-shrink: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 1px solid var(--border);
    font-size: 14px;
  }

  .cert-name {
    font-family: var(--font-display);
    font-size: 13px;
    font-weight: 600;
    color: var(--text);
    line-height: 1.4;
    margin-bottom: 4px;
  }

  .cert-issuer {
    font-family: var(--font-mono);
    font-size: 11px;
    color: var(--text-dim);
    letter-spacing: 0.06em;
  }

  /* CONTACT */
  .contact-layout {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5rem;
    align-items: center;
  }

  .contact-heading {
    font-family: var(--font-display);
    font-size: clamp(2.5rem, 5vw, 4rem);
    font-weight: 800;
    line-height: 1.1;
    letter-spacing: -0.03em;
    margin-bottom: 1.5rem;
  }

  .contact-heading span { color: var(--accent); }

  .contact-sub {
    font-family: var(--font-mono);
    font-size: 13px;
    color: var(--text-muted);
    line-height: 1.9;
    margin-bottom: 2rem;
  }

  .contact-links {
    display: flex;
    flex-direction: column;
    gap: 0;
    border: 1px solid var(--border);
  }

  .contact-link {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem 1.5rem;
    border-bottom: 1px solid var(--border);
    text-decoration: none;
    color: var(--text-muted);
    transition: all 0.2s;
    font-family: var(--font-mono);
    font-size: 13px;
  }

  .contact-link:last-child { border-bottom: none; }
  .contact-link:hover { background: var(--bg3); color: var(--text); }

  .contact-link-label { letter-spacing: 0.05em; }
  .contact-link-val { color: var(--text-dim); font-size: 12px; }

  /* FOOTER */
  footer {
    border-top: 1px solid var(--border);
    padding: 2rem 4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  footer p {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--text-dim);
    letter-spacing: 0.06em;
  }

  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .reveal {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }

  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* BLOG */
  .blog-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5px;
    background: var(--border);
  }

  .blog-card {
    background: var(--bg);
    padding: 2rem;
    text-decoration: none;
    color: inherit;
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
    transition: background 0.2s;
    cursor: pointer;
  }

  .blog-card:hover { background: var(--bg3); }
  .blog-card:hover .blog-arrow { transform: translate(3px, -3px); }

  .blog-meta {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .blog-date {
    font-family: var(--font-mono);
    font-size: 11px;
    color: var(--text-dim);
    letter-spacing: 0.08em;
  }

  .blog-arrow {
    font-size: 16px;
    color: var(--text-dim);
    transition: transform 0.2s;
  }

  .blog-tag {
    font-family: var(--font-mono);
    font-size: 10px;
    letter-spacing: 0.06em;
    padding: 3px 8px;
    border: 1px solid var(--border);
    color: var(--accent);
    border-color: rgba(200,240,100,0.3);
    background: rgba(200,240,100,0.04);
    width: fit-content;
  }

  body.light .blog-tag {
    color: var(--accent);
    border-color: rgba(100,170,0,0.3);
    background: rgba(100,170,0,0.06);
  }

  .blog-title {
    font-family: var(--font-display);
    font-size: 1.1rem;
    font-weight: 700;
    line-height: 1.35;
    color: var(--text);
  }

  .blog-excerpt {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--text-muted);
    line-height: 1.8;
    flex: 1;
  }

  .blog-readtime {
    font-family: var(--font-mono);
    font-size: 11px;
    color: var(--text-dim);
    padding-top: 0.75rem;
    border-top: 1px solid var(--border);
  }

  /* BLOG MODAL */
  .blog-modal-overlay {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.7);
    z-index: 500;
    align-items: flex-start;
    justify-content: center;
    padding: 4rem 1rem;
    overflow-y: auto;
    backdrop-filter: blur(4px);
  }

  .blog-modal-overlay.open { display: flex; }

  .blog-modal {
    background: var(--bg2);
    border: 1px solid var(--border-strong);
    max-width: 720px;
    width: 100%;
    padding: 3rem;
    position: relative;
  }

  .blog-modal-close {
    position: absolute;
    top: 1.5rem;
    right: 1.5rem;
    background: none;
    border: 1px solid var(--border);
    color: var(--text-muted);
    font-family: var(--font-mono);
    font-size: 12px;
    padding: 4px 12px;
    cursor: pointer;
    letter-spacing: 0.06em;
    transition: all 0.2s;
  }

  .blog-modal-close:hover { border-color: var(--text); color: var(--text); }

  .blog-modal-tag {
    font-family: var(--font-mono);
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 0.1em;
    margin-bottom: 1rem;
  }

  .blog-modal-title {
    font-family: var(--font-display);
    font-size: 1.8rem;
    font-weight: 800;
    line-height: 1.2;
    color: var(--text);
    margin-bottom: 0.5rem;
  }

  .blog-modal-date {
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--text-dim);
    margin-bottom: 2rem;
    padding-bottom: 1.5rem;
    border-bottom: 1px solid var(--border);
  }

  .blog-modal-body {
    font-family: var(--font-serif);
    font-size: 15px;
    color: var(--text-muted);
    line-height: 1.9;
  }

  .blog-modal-body p { margin-bottom: 1.25rem; }
  .blog-modal-body h3 {
    font-family: var(--font-display);
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--text);
    margin: 2rem 0 0.75rem;
  }
  .blog-modal-body strong { color: var(--text); font-style: normal; }
  .blog-modal-body em { color: var(--accent); }

  /* CV DOWNLOAD BUTTON */
  .btn-cv {
    font-family: var(--font-mono);
    font-size: 13px;
    letter-spacing: 0.08em;
    padding: 0.9rem 2rem;
    border: 1px solid var(--accent2);
    color: var(--accent2);
    text-decoration: none;
    transition: all 0.2s;
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    cursor: pointer;
    background: none;
  }

  .btn-cv:hover {
    background: var(--accent2);
    color: #0a0a0a;
  }

  /* SCROLLBAR */
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--border-strong); }

  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    .hero { padding: 6rem 1.5rem 3rem; }
    section { padding: 4rem 1.5rem; }
    .about-grid, .contact-layout, .featured-project { grid-template-columns: 1fr; }
    .featured-left { border-right: none; border-bottom: 1px solid rgba(200,240,100,0.1); }
    .hero-stats { display: none; }
    .hero-scroll { left: 1.5rem; }
    footer { padding: 1.5rem; flex-direction: column; gap: 0.5rem; text-align: center; }
  }
</style>
</head>
<body>

<nav>
  <a class="nav-logo" href="#">RM_AI</a>
  <ul class="nav-links">
    <li><a href="#about">about</a></li>
    <li><a href="#projects">projects</a></li>
    <li><a href="#blog">blog</a></li>
    <li><a href="#skills">skills</a></li>
    <li><a href="#certifications">certs</a></li>
    <li><a href="#contact">contact</a></li>
  </ul>
  <div style="display:flex;align-items:center;gap:0.75rem;">
    <button class="theme-toggle" id="themeToggle" aria-label="Toggle theme">☀ light</button>
    <a class="nav-cta" href="#" id="cvDownloadNav" onclick="downloadCV(event)">↓ cv</a>
    <a class="nav-cta" href="mailto:rajaganaa@gmail.com">hire me →</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-grid-bg"></div>
  <div class="hero-accent-circle"></div>

  <div class="hero-tag">available for ai/ml roles · chennai, india</div>

  <h1 class="hero-name">
    Rajaganapathy<span>M.</span>
  </h1>

  <p class="hero-tagline">
    I spent nine years engineering systems where failure meant real-world consequences.
    Now I build AI with the same discipline — a filed patent and IEEE paper prove it.
  </p>

  <div class="hero-badges">
    <span class="badge badge-highlight">⚡ Patent Filed · Apr 2026</span>
    <span class="badge badge-blue">📄 IEEE Paper · Submitted</span>
    <span class="badge badge-highlight">🎓 M.Tech AI · 9.6 CGPA</span>
    <span class="badge">LLMs · Agentic AI · RAG</span>
    <span class="badge">Multi-Agent Systems</span>
    <span class="badge">Computer Vision</span>
  </div>

  <div class="hero-actions">
    <a class="btn-primary" href="#projects">view my work →</a>
    <button class="btn-cv" onclick="downloadCV(event)">↓ download cv</button>
    <a class="btn-secondary" href="https://github.com/rajaganaa" target="_blank">github ↗</a>
    <a class="btn-secondary" href="https://www.linkedin.com/in/raja-ganapathy-36b00658" target="_blank">linkedin ↗</a>
  </div>

  <div class="hero-scroll">scroll</div>

  <div class="hero-stats">
    <div class="hero-stat">
      <div class="hero-stat-num">9+</div>
      <div class="hero-stat-label">YRS ENGINEERING</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-num">13+</div>
      <div class="hero-stat-label">PROJECTS</div>
    </div>
    <div class="hero-stat">
      <div class="hero-stat-num">96%</div>
      <div class="hero-stat-label">CGPA</div>
    </div>
  </div>
</section>

<!-- TICKER STRIP -->
<div style="border-top:1px solid var(--border);border-bottom:1px solid var(--border);background:var(--bg2);overflow:hidden;white-space:nowrap;padding:0.75rem 0;">
  <div style="display:inline-block;animation:ticker 30s linear infinite;font-family:var(--font-mono);font-size:11px;letter-spacing:0.12em;color:var(--text-dim);">
    &nbsp;&nbsp;&nbsp;⚡ PATENT FILED · APP NO. 202641043947
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    📄 IEEE CONFERENCE PAPER SUBMITTED · SRM INSTITUTE
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🎓 M.TECH AI · 9.6 CGPA · SRM INSTITUTE OF SCIENCE &amp; TECHNOLOGY
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🚀 ANTAHKARANA MEDICAL AI · LIVE ON AZURE
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🛠 8 PRODUCTION AI SYSTEMS DEPLOYED
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🏭 9+ YEARS SAFETY-CRITICAL ENGINEERING EXPERIENCE
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ☁️ AWS SOLUTIONS ARCHITECT CERTIFIED · 2025
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🤖 KAGGLE 5-DAY AI AGENTS INTENSIVE WITH GOOGLE · 2025
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    ⚡ PATENT FILED · APP NO. 202641043947
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    📄 IEEE CONFERENCE PAPER SUBMITTED · SRM INSTITUTE
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🎓 M.TECH AI · 9.6 CGPA · SRM INSTITUTE OF SCIENCE &amp; TECHNOLOGY
    &nbsp;&nbsp;&nbsp;·&nbsp;&nbsp;&nbsp;
    🚀 ANTAHKARANA MEDICAL AI · LIVE ON AZURE
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </div>
</div>
<style>
@keyframes ticker {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}
</style>

<!-- ABOUT -->
<section id="about">
  <div class="section-label">01 · ABOUT</div>

  <div class="about-grid">
    <div>
      <p class="about-statement reveal">
        Most AI engineers understand models.<br/>
        I also understand <em>failure</em> — the real kind,
        in 400 kW industrial systems where downtime costs money
        and lives. That discipline is now in every line of my AI code.
      </p>

      <div style="margin-top: 3rem;">
        <div class="section-label" style="margin-bottom: 1.5rem;">JOURNEY</div>
        <div class="timeline reveal">
          <div class="timeline-item">
            <div class="timeline-year">2013</div>
            <div class="timeline-role">B.E. Electrical & Electronics Engineering</div>
            <div class="timeline-org">Thangavelu Engineering College, Chennai</div>
          </div>
          <div class="timeline-item">
            <div class="timeline-year">2014 – 2016</div>
            <div class="timeline-role">Electrical Maintenance Engineer</div>
            <div class="timeline-org">Mod Forge Pvt. Ltd. · ISO/TS Certified</div>
          </div>
          <div class="timeline-item">
            <div class="timeline-year">2017 – 2023</div>
            <div class="timeline-role">Electrical Construction Site Engineer</div>
            <div class="timeline-org">SR Electrical Works · Chennai</div>
          </div>
          <div class="timeline-item">
            <div class="timeline-year">2023</div>
            <div class="timeline-role">Pivoted to Artificial Intelligence</div>
            <div class="timeline-org">Deliberate career transition after 9+ years</div>
          </div>
          <div class="timeline-item">
            <div class="timeline-year">2024 – Present</div>
            <div class="timeline-role">M.Tech Artificial Intelligence · 9.6 CGPA</div>
            <div class="timeline-org">SRM Institute of Science & Technology</div>
          </div>
          <div class="timeline-item">
            <div class="timeline-year">Apr 2026</div>
            <div class="timeline-role">Indian Patent Filed · Antahkarana System</div>
            <div class="timeline-org">App No. 202641043947 · IEEE Paper Submitted</div>
          </div>
        </div>
      </div>
    </div>

    <div class="about-right reveal">
      <p>
        I am an <strong>AI/ML Engineer</strong> specialising in LLMs, Agentic AI, RAG pipelines, and multi-agent systems. After nine years as a practising electrical engineer, I made a deliberate leap into AI in 2023 — and spent the next two years proving it was the right decision.
      </p>
      <p>
        My flagship project, <strong>Antahkarana</strong>, is a cognitively-inspired adaptive reasoning framework for LLMs and VLMs. It has a <strong>filed Indian patent</strong> and a <strong>submitted IEEE Conference paper</strong> to its name — outputs typically associated with full research teams, not individual M.Tech students.
      </p>
      <p>
        What I bring to an AI role that most candidates don't: the discipline of a practising engineer who has operated in safety-critical environments, managed complex projects under hard constraints, and built things that actually have to work. I think about AI systems the way production engineers think about infrastructure — reliably, at scale, with failure modes already considered.
      </p>
      <p>
        <strong>CGPA: 9.6/10</strong> · AWS Solutions Architect · DevOps · GUVI AIML Professional · IIT-M Advanced Programming · NPTEL IoT · Kaggle AI Agents (Google)
      </p>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-label">02 · PROJECTS</div>

  <div class="projects-grid">

    <!-- FEATURED -->
    <div class="featured-project reveal">
      <div class="featured-left">
        <div class="project-num">P.001 · FLAGSHIP</div>
        <h2 class="featured-title">Antahkarana<br/><span>Reasoning Framework</span></h2>
        <p class="featured-desc">
          A cognitively-inspired, modular conditional reasoning framework for LLMs and VLMs. Inspired by Vedantic cognitive architecture, Antahkarana routes complex queries through specialised reasoning stages — perception, discrimination, memory, and ego-less integration — to produce coherent, grounded responses at scale.
        </p>
        <div class="featured-badges">
          <span class="badge badge-highlight">Patent Filed</span>
          <span class="badge badge-blue">IEEE Submitted</span>
          <span class="badge">Python 3.8+</span>
          <span class="badge">Apache 2.0</span>
          <span class="badge">VLM · BLIP-3</span>
          <span class="badge">Qwen 0.5</span>
        </div>
      </div>
      <div class="featured-right">
        <div class="achievement-item">
          <div class="achievement-icon">⚡</div>
          <div class="achievement-text">
            <strong>Indian Patent Filed · Apr 2026</strong>
            App No. 202641043947 — system design protected under Indian IP law
          </div>
        </div>
        <div class="achievement-item">
          <div class="achievement-icon">📄</div>
          <div class="achievement-text">
            <strong>IEEE Conference Submission</strong>
            SRM Institute of Science & Technology, Kattankulathur — paper under review
          </div>
        </div>
        <div class="achievement-item">
          <div class="achievement-icon">🧠</div>
          <div class="achievement-text">
            <strong>2,500+ sample results validated</strong>
            Multimodal pipeline tested across LLM querying, VQA tasks, and patent e-filing workflows
          </div>
        </div>
        <div style="display:flex;gap:1rem;flex-wrap:wrap;margin-top:auto;">
          <a href="https://rajaganaa.github.io/medassist-frontend" target="_blank" style="font-family:var(--font-mono);font-size:12px;color:#0a0a0a;background:var(--accent);text-decoration:none;display:inline-flex;align-items:center;gap:0.5rem;padding:0.5rem 1.25rem;font-weight:500;">⚡ live demo →</a>
          <a href="https://github.com/rajaganaa/antahkarana-reasoning-framework" target="_blank" style="font-family:var(--font-mono);font-size:12px;color:var(--accent);text-decoration:none;display:inline-flex;align-items:center;gap:0.5rem;border:1px solid rgba(200,240,100,0.4);padding:0.5rem 1.25rem;">github ↗</a>
        </div>
      </div>
    </div>

    <!-- Project Cards -->
    <a class="project-card reveal" href="https://github.com/rajaganaa/antahkarana-product" target="_blank">
      <div class="project-top">
        <span class="project-num">P.002</span>
        <span class="project-arrow">↗</span>
      </div>
      <div class="project-tags">
        <span class="project-tag project-tag-accent">Live Demo</span>
        <span class="project-tag">Agentic AI</span>
        <span class="project-tag">Azure</span>
      </div>
      <h3 class="project-title">Antahkarana Medical AI — Unified Reasoning Engine</h3>
      <p class="project-desc">Full-stack medical AI assistant built on the Antahkarana framework. Deployed on Azure with a live frontend. Multimodal — processes text, images, and documents. Includes CI/CD via GitHub Actions.</p>
      <div class="project-metric">⚡ Live on Azure · <a href="https://rajaganaa.github.io/medassist-frontend" target="_blank" style="color:var(--accent);text-decoration:none;">medassist-frontend ↗</a> · CI/CD deployed</div>
    </a>

    <a class="project-card reveal" href="https://github.com/rajaganaa/MML_smart_campus_security_system" target="_blank">
      <div class="project-top">
        <span class="project-num">P.003</span>
        <span class="project-arrow">↗</span>
      </div>
      <div class="project-tags">
        <span class="project-tag">Computer Vision</span>
        <span class="project-tag">VLM</span>
        <span class="project-tag">Multimodal</span>
      </div>
      <h3 class="project-title">Multimodal Smart Campus Security System</h3>
      <p class="project-desc">AI-driven surveillance and threat detection system leveraging Vision-Language Models (CLIP, BLIP) and Voice Biometrics. Addresses the challenge of manual CCTV monitoring across hundreds of feeds simultaneously.</p>
      <div class="project-metric">⚡ OpenAI CLIP · Salesforce BLIP · PyTorch</div>
    </a>

    <a class="project-card reveal" href="https://github.com/rajaganaa/AgentNet-Enterprise-Support" target="_blank">
      <div class="project-top">
        <span class="project-num">P.004</span>
        <span class="project-arrow">↗</span>
      </div>
      <div class="project-tags">
        <span class="project-tag project-tag-accent">Multi-Agent</span>
        <span class="project-tag">LLM-as-Judge</span>
        <span class="project-tag">RAG</span>
      </div>
      <h3 class="project-title">AgentNet — Enterprise Multi-Agent Support System</h3>
      <p class="project-desc">Autonomous, self-correcting customer support system using multi-agent orchestration. Agents triage, respond, and grade their own output quality using LLM-as-a-Judge methodology. Vector retrieval memory for contextual recall.</p>
      <div class="project-metric">⚡ Self-reflection loop · Custom trace logging · Vertex AI</div>
    </a>

    <a class="project-card reveal" href="https://github.com/rajaganaa/Hospital-Readmission-Predictor" target="_blank">
      <div class="project-top">
        <span class="project-num">P.005</span>
        <span class="project-arrow">↗</span>
      </div>
      <div class="project-tags">
        <span class="project-tag">ML · XGBoost</span>
        <span class="project-tag">Healthcare</span>
      </div>
      <h3 class="project-title">Hospital Readmission Risk Predictor</h3>
      <p class="project-desc">ML model predicting 30-day hospital readmission risk using AI-driven A1C imputation. Targets the $41B annual cost of preventable readmissions. Clinical feature engineering + hyperparameter-tuned XGBoost pipeline.</p>
      <div class="project-metric">⚡ Production-ready · Streamlit dashboard · Healthcare analytics</div>
    </a>

    <a class="project-card reveal" href="https://github.com/rajaganaa/YouTube-Data-ETL-Pipeline" target="_blank">
      <div class="project-top">
        <span class="project-num">P.006</span>
        <span class="project-arrow">↗</span>
      </div>
      <div class="project-tags">
        <span class="project-tag">Data Engineering</span>
        <span class="project-tag">ETL · SQL</span>
      </div>
      <h3 class="project-title">YouTube Data Harvesting & Warehousing Pipeline</h3>
      <p class="project-desc">Automated ETL pipeline ingesting, cleaning, transforming, and loading YouTube creator data into structured MySQL warehouse. Analytics-ready output for engagement trend analysis and channel benchmarking.</p>
      <div class="project-metric">⚡ YouTube API · MySQL · pandas · Production ready</div>
    </a>

    <a class="project-card reveal" href="https://github.com/rajaganaa/Industrial-HR-Geo-Dashboard" target="_blank">
      <div class="project-top">
        <span class="project-num">P.007</span>
        <span class="project-arrow">↗</span>
      </div>
      <div class="project-tags">
        <span class="project-tag">Geo-Spatial</span>
        <span class="project-tag">NLP</span>
        <span class="project-tag">Streamlit</span>
      </div>
      <h3 class="project-title">Industrial HR Geo-Visualisation Dashboard</h3>
      <p class="project-desc">Geo-spatial + NLP dashboard mapping India's industrial workforce distribution across sectors. Combines choropleth visualisation with natural language querying for policy and workforce planning insights.</p>
      <div class="project-metric">⚡ Research-prototype · Plotly · Folium · NLP queries</div>
    </a>

    <a class="project-card reveal" href="https://github.com/rajaganaa/PhonePe-Transaction-Visualizer" target="_blank">
      <div class="project-top">
        <span class="project-num">P.008</span>
        <span class="project-arrow">↗</span>
      </div>
      <div class="project-tags">
        <span class="project-tag">Data Viz</span>
        <span class="project-tag">Fintech</span>
        <span class="project-tag">MySQL</span>
      </div>
      <h3 class="project-title">PhonePe Pulse Data Visualisation Dashboard</h3>
      <p class="project-desc">Comprehensive analysis of India's digital payment ecosystem using PhonePe Pulse data. Visualises state-level adoption, transaction volumes, and growth trends across Peer-to-Peer and merchant categories.</p>
      <div class="project-metric">⚡ 100% Python · Streamlit · MySQL · Production ready</div>
    </a>

  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-label">03 · SKILLS</div>

  <div class="skills-layout reveal">

    <div class="skill-group">
      <div class="skill-group-title">GENERATIVE AI · LLMs</div>
      <div class="skill-item"><span class="skill-name">LLM Orchestration</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div></div></div>
      <div class="skill-item"><span class="skill-name">RAG Pipelines · FAISS</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div></div></div>
      <div class="skill-item"><span class="skill-name">Prompt Engineering</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div></div></div>
      <div class="skill-item"><span class="skill-name">Agentic Workflows</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">LangChain · HuggingFace</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div></div></div>
    </div>

    <div class="skill-group">
      <div class="skill-group-title">MACHINE LEARNING · DL</div>
      <div class="skill-item"><span class="skill-name">PyTorch · TensorFlow</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">scikit-learn · XGBoost</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div></div></div>
      <div class="skill-item"><span class="skill-name">CNN · LSTM · Transformers</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">NLP · Embeddings</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">Computer Vision · OpenCV</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div></div></div>
    </div>

    <div class="skill-group">
      <div class="skill-group-title">DATA · ENGINEERING</div>
      <div class="skill-item"><span class="skill-name">Python</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div></div></div>
      <div class="skill-item"><span class="skill-name">SQL · MySQL · MongoDB</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">ETL Pipelines</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">Streamlit · Plotly</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div></div></div>
      <div class="skill-item"><span class="skill-name">pandas · NumPy</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div></div></div>
    </div>

    <div class="skill-group">
      <div class="skill-group-title">CLOUD · DEVOPS</div>
      <div class="skill-item"><span class="skill-name">AWS Solutions Architect</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">Azure · Docker</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div><div class="skill-dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">Git · GitHub Actions CI/CD</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">Linux · Bash</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div><div class="skill-dot"></div></div></div>
      <div class="skill-item"><span class="skill-name">R · SQL · NoSQL</span><div class="skill-level"><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot active"></div><div class="skill-dot"></div><div class="skill-dot"></div></div></div>
    </div>

  </div>
</section>

<!-- CERTIFICATIONS -->
<section id="certifications">
  <div class="section-label">04 · CERTIFICATIONS</div>

  <div class="certs-grid reveal">

    <div class="cert-card">
      <div class="cert-icon">🎓</div>
      <div>
        <div class="cert-name">AI & ML Professional Program</div>
        <div class="cert-issuer">GUVI · IIT-M · May 2024</div>
      </div>
    </div>

    <div class="cert-card">
      <div class="cert-icon">☁️</div>
      <div>
        <div class="cert-name">AWS Certified Solutions Architect Associate</div>
        <div class="cert-issuer">Udemy · Oct 2025</div>
      </div>
    </div>

    <div class="cert-card">
      <div class="cert-icon">🤖</div>
      <div>
        <div class="cert-name">5-Day AI Agents Intensive with Google</div>
        <div class="cert-issuer">Kaggle · Dec 2025</div>
      </div>
    </div>

    <div class="cert-card">
      <div class="cert-icon">⚙️</div>
      <div>
        <div class="cert-name">DevOps Beginners to Advanced with Projects</div>
        <div class="cert-issuer">Udemy · Jul 2025</div>
      </div>
    </div>

    <div class="cert-card">
      <div class="cert-icon">🔗</div>
      <div>
        <div class="cert-name">Introduction to Internet of Things</div>
        <div class="cert-issuer">NPTEL · Oct 2025</div>
      </div>
    </div>

    <div class="cert-card">
      <div class="cert-icon">🖥️</div>
      <div>
        <div class="cert-name">Certificate Professional — Advanced Programming</div>
        <div class="cert-issuer">IIT-M · May 2024</div>
      </div>
    </div>

    <div class="cert-card">
      <div class="cert-icon">👁️</div>
      <div>
        <div class="cert-name">OpenCV Certification</div>
        <div class="cert-issuer">OpenCV University · Mar 2025</div>
      </div>
    </div>

    <div class="cert-card">
      <div class="cert-icon">🔥</div>
      <div>
        <div class="cert-name">PyTorch & TensorFlow for Deep Learning</div>
        <div class="cert-issuer">Simplilearn · Nov 2024</div>
      </div>
    </div>

    <div class="cert-card">
      <div class="cert-icon">🐍</div>
      <div>
        <div class="cert-name">Advanced Python Course</div>
        <div class="cert-issuer">GUVI · IIT-M · Feb 2024</div>
      </div>
    </div>

    <div class="cert-card">
      <div class="cert-icon">📊</div>
      <div>
        <div class="cert-name">DSA · Data Structures & Algorithms</div>
        <div class="cert-issuer">Simplilearn · Nov 2024</div>
      </div>
    </div>

  </div>
</section>

<!-- BLOG -->
<section id="blog">
  <div class="section-label">05 · BLOG</div>

  <div class="blog-grid reveal">

    <div class="blog-card" onclick="openBlog(0)">
      <div class="blog-meta">
        <span class="blog-date">MAY 2026</span>
        <span class="blog-arrow">↗</span>
      </div>
      <span class="blog-tag">CAREER · AI</span>
      <h3 class="blog-title">From Electrical Engineer to AI Engineer — What Really Transfers</h3>
      <p class="blog-excerpt">Nine years of high-voltage systems, industrial automation, and safety-critical engineering taught me things no AI course ever could. Here's what actually crosses over — and what doesn't.</p>
      <div class="blog-readtime">⏱ 6 min read</div>
    </div>

    <div class="blog-card" onclick="openBlog(1)">
      <div class="blog-meta">
        <span class="blog-date">APR 2026</span>
        <span class="blog-arrow">↗</span>
      </div>
      <span class="blog-tag">LLM · RESEARCH</span>
      <h3 class="blog-title">How I Built Antahkarana — A Cognitively-Inspired Reasoning Framework</h3>
      <p class="blog-excerpt">Most LLM pipelines are glorified prompt chains. Antahkarana is different — it routes queries through specialised cognitive stages inspired by Vedantic philosophy. Here's the architecture and why it works.</p>
      <div class="blog-readtime">⏱ 9 min read</div>
    </div>

    <div class="blog-card" onclick="openBlog(2)">
      <div class="blog-meta">
        <span class="blog-date">MAR 2026</span>
        <span class="blog-arrow">↗</span>
      </div>
      <span class="blog-tag">AGENTIC AI</span>
      <h3 class="blog-title">RAG vs Fine-Tuning: Lessons from Building a Medical AI Assistant</h3>
      <p class="blog-excerpt">When building Antahkarana's medical reasoning engine, I had to choose between RAG and fine-tuning for every sub-task. Here's the decision framework I developed — and where each approach actually wins.</p>
      <div class="blog-readtime">⏱ 7 min read</div>
    </div>

  </div>
</section>

<!-- BLOG MODAL -->
<div class="blog-modal-overlay" id="blogModal" onclick="closeBlogOnOverlay(event)">
  <div class="blog-modal" id="blogModalContent">
    <button class="blog-modal-close" onclick="closeBlog()">✕ close</button>
    <div class="blog-modal-tag" id="modalTag"></div>
    <h2 class="blog-modal-title" id="modalTitle"></h2>
    <div class="blog-modal-date" id="modalDate"></div>
    <div class="blog-modal-body" id="modalBody"></div>
  </div>
</div>

<!-- THE EDGE -->
<section id="edge" style="background:var(--bg2);">
  <div class="section-label">07 · THE EDGE</div>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:1.5px;background:var(--border);">

    <div class="reveal" style="background:var(--bg2);padding:2.5rem;">
      <div style="font-family:var(--font-mono);font-size:10px;letter-spacing:0.2em;color:var(--accent);margin-bottom:1rem;">WHAT MOST CANDIDATES DON'T HAVE</div>
      <h3 style="font-family:var(--font-display);font-size:1.5rem;font-weight:800;color:var(--text);line-height:1.2;margin-bottom:1rem;">A filed patent <em style="color:var(--accent);font-style:normal;">and</em> a deployed product.</h3>
      <p style="font-family:var(--font-mono);font-size:12px;color:var(--text-muted);line-height:1.9;">Most M.Tech students build projects. Rajaganapathy filed an Indian patent (App. No. 202641043947), submitted an IEEE paper, and deployed a live medical AI product on Azure — in the same academic cycle.</p>
    </div>

    <div class="reveal" style="background:var(--bg2);padding:2.5rem;">
      <div style="font-family:var(--font-mono);font-size:10px;letter-spacing:0.2em;color:var(--accent2);margin-bottom:1rem;">THE ENGINEERING MINDSET</div>
      <h3 style="font-family:var(--font-display);font-size:1.5rem;font-weight:800;color:var(--text);line-height:1.2;margin-bottom:1rem;">Builds AI that <em style="color:var(--accent2);font-style:normal;">can't fail.</em></h3>
      <p style="font-family:var(--font-mono);font-size:12px;color:var(--text-muted);line-height:1.9;">9 years maintaining 500 kVA transformers and 400 kW motors in live industrial environments teaches you one thing: systems must work under every condition. That discipline is rare in AI engineering — and it shows in every system I build.</p>
    </div>

    <div class="reveal" style="background:var(--bg2);padding:2.5rem;">
      <div style="font-family:var(--font-mono);font-size:10px;letter-spacing:0.2em;color:var(--accent);margin-bottom:1rem;">THE RESEARCH PROOF</div>
      <h3 style="font-family:var(--font-display);font-size:1.5rem;font-weight:800;color:var(--text);line-height:1.2;margin-bottom:1rem;">2,500 samples. One architecture. <em style="color:var(--accent);font-style:normal;">Novel contribution.</em></h3>
      <p style="font-family:var(--font-mono);font-size:12px;color:var(--text-muted);line-height:1.9;">Antahkarana's Vedantic cognitive routing architecture was validated across 2,500 LLM/VLM samples — a methodology that earned both a patent filing and an IEEE conference submission. Not a class project. Original research.</p>
    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-label">06 · CONTACT</div>

  <div class="contact-layout">
    <div class="reveal">
      <h2 class="contact-heading">Ready to build<br/>at <span>Google scale.</span></h2>
      <p class="contact-sub">
        Most candidates bring a degree. I bring 9+ years of engineering under real-world pressure,
        a filed patent, a live Azure deployment, and an IEEE paper under review — all from a 2-year
        M.Tech programme. If you're building infrastructure that has to work at scale,
        I already think that way. Let's talk.
      </p>
      <div style="display:flex;gap:1rem;flex-wrap:wrap;">
        <a class="btn-primary" href="mailto:rajaganaa@gmail.com">send me an email →</a>
        <a class="btn-secondary" href="https://www.linkedin.com/in/raja-ganapathy-36b00658" target="_blank">connect on linkedin ↗</a>
      </div>
    </div>

    <div class="contact-links reveal">
      <a class="contact-link" href="mailto:rajaganaa@gmail.com">
        <span class="contact-link-label">✉ Email</span>
        <span class="contact-link-val">rajaganaa@gmail.com</span>
      </a>
      <a class="contact-link" href="https://www.linkedin.com/in/raja-ganapathy-36b00658" target="_blank">
        <span class="contact-link-label">in LinkedIn</span>
        <span class="contact-link-val">raja-ganapathy-36b00658</span>
      </a>
      <a class="contact-link" href="https://github.com/rajaganaa" target="_blank">
        <span class="contact-link-label">⌥ GitHub</span>
        <span class="contact-link-val">github.com/rajaganaa</span>
      </a>
      <a class="contact-link" href="https://x.com/rajaganaa" target="_blank">
        <span class="contact-link-label">𝕏 Twitter / X</span>
        <span class="contact-link-val">@rajaganaa</span>
      </a>
      <a class="contact-link" href="https://rajaganaa.github.io" target="_blank">
        <span class="contact-link-label">🌐 Portfolio Site</span>
        <span class="contact-link-val">rajaganaa.github.io</span>
      </a>
      <div class="contact-link" style="cursor: default;">
        <span class="contact-link-label">📍 Location</span>
        <span class="contact-link-val">Chennai, India · Open to remote</span>
      </div>
    </div>
  </div>
</section>

<footer>
  <p>© 2026 Rajaganapathy M — AI Engineer · Chennai, India</p>
  <p>Patent pending · IEEE under review · Open to world-class opportunities</p>
</footer>

<script>
  // SCROLL REVEAL
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('visible'), (i % 4) * 100);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });
  reveals.forEach(el => observer.observe(el));

  // DARK / LIGHT TOGGLE
  const toggleBtn = document.getElementById('themeToggle');
  let isLight = false;
  toggleBtn.addEventListener('click', () => {
    isLight = !isLight;
    document.body.classList.toggle('light', isLight);
    toggleBtn.textContent = isLight ? '☾ dark' : '☀ light';
  });

  // CV DOWNLOAD — generates a printable CV page
  function downloadCV(e) {
    e.preventDefault();
    const genDate = new Date().toLocaleDateString('en-GB', {month:'long',year:'numeric'});
    const cvHTML = `<!DOCTYPE html>
<html><head><meta charset="UTF-8"/>
<title>Rajaganapathy M — CV</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  *{box-sizing:border-box;margin:0;padding:0;}
  body{font-family:'Syne',sans-serif;color:#1a1a18;background:#fff;font-size:14px;line-height:1.6;padding:3rem 4rem;}
  @media print{body{padding:1.5rem 2rem;}}
  h1{font-size:2.2rem;font-weight:800;letter-spacing:-0.03em;margin-bottom:0.25rem;}
  .subtitle{font-family:'DM Mono',monospace;font-size:12px;color:#6aaa00;letter-spacing:0.08em;margin-bottom:0.5rem;}
  .contact-bar{font-family:'DM Mono',monospace;font-size:11px;color:#5a5a52;display:flex;flex-wrap:wrap;gap:1rem;margin-bottom:1.5rem;padding-bottom:1rem;border-bottom:2px solid #1a1a18;}
  .badges{display:flex;gap:0.5rem;flex-wrap:wrap;margin-bottom:1.5rem;}
  .badge{font-family:'DM Mono',monospace;font-size:10px;border:1px solid #6aaa00;color:#6aaa00;padding:2px 8px;}
  h2{font-size:11px;font-weight:600;letter-spacing:0.15em;color:#6aaa00;margin:1.5rem 0 0.75rem;padding-bottom:4px;border-bottom:1px solid #e0e0d8;}
  .summary{font-size:13px;color:#3a3a32;line-height:1.8;margin-bottom:0.5rem;}
  .exp-item{margin-bottom:1rem;}
  .exp-header{display:flex;justify-content:space-between;align-items:baseline;}
  .exp-role{font-weight:700;font-size:14px;}
  .exp-date{font-family:'DM Mono',monospace;font-size:11px;color:#5a5a52;}
  .exp-org{font-family:'DM Mono',monospace;font-size:11px;color:#5a5a52;margin-bottom:4px;}
  .exp-desc{font-size:12px;color:#5a5a52;line-height:1.7;}
  .proj-grid{display:grid;grid-template-columns:1fr 1fr;gap:0.75rem;}
  .proj-item{border:1px solid #e0e0d8;padding:0.75rem;}
  .proj-name{font-weight:700;font-size:13px;margin-bottom:2px;}
  .proj-tech{font-family:'DM Mono',monospace;font-size:10px;color:#5a5a52;}
  .skills-cols{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem;}
  .skill-group-name{font-weight:700;font-size:12px;margin-bottom:4px;}
  .skill-list{font-family:'DM Mono',monospace;font-size:11px;color:#5a5a52;line-height:1.8;}
  .certs-list{display:grid;grid-template-columns:1fr 1fr;gap:4px;}
  .cert-entry{font-family:'DM Mono',monospace;font-size:11px;color:#5a5a52;}
  .cert-entry span{color:#1a1a18;font-weight:600;}
  .footer-cv{margin-top:2rem;padding-top:1rem;border-top:1px solid #e0e0d8;font-family:'DM Mono',monospace;font-size:11px;color:#9a9a90;display:flex;justify-content:space-between;}
</style></head><body>
<h1>Rajaganapathy M</h1>
<div class="subtitle">AI / ML ENGINEER · LLM · AGENTIC AI · RAG · MULTI-AGENT SYSTEMS</div>
<div class="contact-bar">
  <span>✉ rajaganaa@gmail.com</span>
  <span>📞 +91 9176631419</span>
  <span>🌐 rajaganaa.github.io</span>
  <span>in raja-ganapathy-36b00658</span>
  <span>⌥ github.com/rajaganaa</span>
  <span>📍 Chennai, India</span>
</div>
<div class="badges">
  <span class="badge">⚡ PATENT FILED · APR 2026</span>
  <span class="badge">📄 IEEE PAPER SUBMITTED</span>
  <span class="badge">🎓 M.TECH AI · 9.6 CGPA</span>
  <span class="badge">9+ YRS ENGINEERING</span>
</div>

<h2>PROFILE</h2>
<p class="summary">Engineering professional with 9+ years of industry experience transitioning into AI. M.Tech in Artificial Intelligence at SRM Institute (CGPA 9.6/10). Filed Indian Patent (No. 202641043947) for the Antahkarana cognitively-inspired reasoning framework; IEEE Conference paper submitted. Skilled in LLMs, Agentic AI, RAG pipelines, multi-agent systems, computer vision, and data engineering. Brings production engineering discipline — safety-critical systems, project management, cross-team delivery — to every AI build.</p>

<h2>EDUCATION</h2>
<div class="exp-item">
  <div class="exp-header"><span class="exp-role">M.Tech — Artificial Intelligence</span><span class="exp-date">2024 – Present</span></div>
  <div class="exp-org">SRM Institute of Science & Technology · Chennai · CGPA: 9.6 / 10</div>
</div>
<div class="exp-item">
  <div class="exp-header"><span class="exp-role">B.E — Electrical & Electronics Engineering</span><span class="exp-date">2013</span></div>
  <div class="exp-org">Thangavelu Engineering College · Chennai</div>
</div>

<h2>RESEARCH & IP</h2>
<div class="exp-item">
  <div class="exp-role">Indian Patent Filed — Antahkarana System</div>
  <div class="exp-org">Application No. 202641043947 · Filed April 3, 2026</div>
  <div class="exp-desc">Cognitively-inspired adaptive reasoning framework for LLMs and VLMs. System design protected under Indian IP law.</div>
</div>
<div class="exp-item">
  <div class="exp-role">IEEE Conference Paper — Submitted</div>
  <div class="exp-org">SRM Institute of Science & Technology, Kattankulathur</div>
  <div class="exp-desc">Antahkarana: Cognitively-Inspired Adaptive Reasoning for LLMs and VLMs. Under review.</div>
</div>

<h2>KEY PROJECTS</h2>
<div class="proj-grid">
  <div class="proj-item"><div class="proj-name">Antahkarana Reasoning Framework</div><div class="proj-tech">Python · Qwen · BLIP-3 · Apache 2.0 · Patent filed · IEEE submitted</div></div>
  <div class="proj-item"><div class="proj-name">Antahkarana Medical AI (Live)</div><div class="proj-tech">Azure · GitHub Actions CI/CD · Multimodal · Full-stack deployed</div></div>
  <div class="proj-item"><div class="proj-name">MML Smart Campus Security</div><div class="proj-tech">OpenAI CLIP · Salesforce BLIP · PyTorch · Voice Biometrics</div></div>
  <div class="proj-item"><div class="proj-name">AgentNet Enterprise Support</div><div class="proj-tech">Multi-agent · LLM-as-Judge · RAG · Vertex AI · Self-reflection loop</div></div>
  <div class="proj-item"><div class="proj-name">Hospital Readmission Predictor</div><div class="proj-tech">XGBoost · Streamlit · Healthcare analytics · A1C imputation</div></div>
  <div class="proj-item"><div class="proj-name">YouTube Data ETL Pipeline</div><div class="proj-tech">Python · MySQL · YouTube API · Production ready</div></div>
</div>

<h2>PROFESSIONAL EXPERIENCE</h2>
<div class="exp-item">
  <div class="exp-header"><span class="exp-role">Electrical Construction Site Engineer</span><span class="exp-date">Jan 2017 – Jun 2023</span></div>
  <div class="exp-org">SR Electrical Works · Chennai</div>
  <div class="exp-desc">Designed and implemented electrical systems for large-scale construction projects. Led budget estimation, resource allocation, site supervision, and cross-team coordination. Delivered safety-critical systems under hard constraints across multiple simultaneous projects.</div>
</div>
<div class="exp-item">
  <div class="exp-header"><span class="exp-role">Electrical Maintenance Engineer</span><span class="exp-date">Dec 2014 – Dec 2016</span></div>
  <div class="exp-org">Mod Forge Pvt. Ltd. · ISO/TS 16949 Certified · Chennai</div>
  <div class="exp-desc">O&M of 500 kVA transformer, 250 kVA DG, motors up to 400 kW, power factor correction panels, compressors, and automation panels under C-certificate supervision.</div>
</div>

<h2>TECHNICAL SKILLS</h2>
<div class="skills-cols">
  <div><div class="skill-group-name">Generative AI / LLMs</div><div class="skill-list">LLM Orchestration<br/>RAG · FAISS · Vector DBs<br/>Prompt Engineering<br/>Agentic Workflows<br/>LangChain · HuggingFace</div></div>
  <div><div class="skill-group-name">ML / Deep Learning</div><div class="skill-list">PyTorch · TensorFlow<br/>scikit-learn · XGBoost<br/>CNN · LSTM · Transformers<br/>NLP · Embeddings<br/>Computer Vision · OpenCV</div></div>
  <div><div class="skill-group-name">Cloud / DevOps / Data</div><div class="skill-list">AWS · Azure · Docker<br/>Git · GitHub Actions CI/CD<br/>Python · SQL · MongoDB<br/>Streamlit · Plotly<br/>Linux · Bash · R</div></div>
</div>

<h2>CERTIFICATIONS</h2>
<div class="certs-list">
  <div class="cert-entry"><span>AWS</span> Solutions Architect Associate · Udemy 2025</div>
  <div class="cert-entry"><span>GUVI</span> AI & ML Professional Program · IIT-M 2024</div>
  <div class="cert-entry"><span>Kaggle</span> 5-Day AI Agents Intensive with Google · 2025</div>
  <div class="cert-entry"><span>DevOps</span> Beginners to Advanced · Udemy 2025</div>
  <div class="cert-entry"><span>NPTEL</span> Introduction to Internet of Things · 2025</div>
  <div class="cert-entry"><span>IIT-M</span> Certificate Professional · Advanced Programming 2024</div>
  <div class="cert-entry"><span>OpenCV</span> OpenCV University Certification · 2025</div>
  <div class="cert-entry"><span>Simplilearn</span> PyTorch · TensorFlow · DSA · GIT · MongoDB</div>
</div>

<div class="footer-cv">
  <span>rajaganaa.github.io · github.com/rajaganaa</span>
  <span>Generated ${genDate}</span>
</div>
</body></html>`;
    const blob = new Blob([cvHTML], {type: 'text/html'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = 'Rajaganapathy_M_CV.html';
    a.click();
    URL.revokeObjectURL(url);
  }

  // BLOG MODAL DATA
  const blogs = [
    {
      tag: 'CAREER · AI',
      date: 'May 2026 · 6 min read',
      title: 'From Electrical Engineer to AI Engineer — What Really Transfers',
      body: `
        <p>In June 2023, after nine years of working on electrical systems across industrial sites in Chennai, I quit my job. Not because I was failing — I was good at it. I quit because I wanted to build a different kind of system.</p>
        <h3>What I thought would transfer</h3>
        <p>I assumed the engineering fundamentals would carry over: systems thinking, problem decomposition, reading technical documentation. I was right about those. What surprised me was <em>how much deeper</em> that transfer went.</p>
        <p>In industrial electrical work, you build things that operate continuously under unpredictable conditions. A 500 kVA transformer doesn't get to fail at 3am because the load spiked. You design for failure modes before they happen. You think about what the system does when something unexpected occurs — not just what it does when everything is normal.</p>
        <p>That mindset is rare in AI engineering. Most ML practitioners optimise for the happy path. They tune accuracy on the test set and ship. My instinct is always: <strong>what happens at the edge cases? What does the model do when the input is malformed, the context is incomplete, or the query is genuinely ambiguous?</strong></p>
        <h3>What actually doesn't transfer</h3>
        <p>Mathematics. I had to rebuild from scratch — linear algebra, probability theory, calculus of variations. The electrical engineering maths is completely different. This took six months of uncomfortable work before I could read ML papers without feeling lost.</p>
        <p>Speed of iteration. Physical engineering is slow by nature — you can't A/B test a transformer installation. Software moves at a completely different pace, and learning to ship, iterate, and throw things away was genuinely uncomfortable at first.</p>
        <h3>The unexpected advantage</h3>
        <p>The biggest transfer no one talks about: <em>project management in safety-critical environments</em>. When you've coordinated electrical installation across a live construction site — managing contractors, clients, timelines, and regulations simultaneously — running a complex ML project feels almost straightforward by comparison. The stakes are different, but the discipline is the same.</p>
        <p>I don't regret the nine years. They made me a better AI engineer than I would have been if I'd started at 22.</p>
      `
    },
    {
      tag: 'LLM · RESEARCH',
      date: 'April 2026 · 9 min read',
      title: 'How I Built Antahkarana — A Cognitively-Inspired Reasoning Framework',
      body: `
        <p>Most LLM pipelines are, at their core, sophisticated prompt chains. You send a query, you get a response. Maybe you add retrieval. Maybe you add a tool call. But the fundamental architecture is linear: input → model → output.</p>
        <p>Antahkarana is different. It routes complex queries through specialised cognitive stages — each stage responsible for a distinct aspect of reasoning — before synthesising a final response. The inspiration came from an unlikely source: Vedantic philosophy.</p>
        <h3>The cognitive architecture</h3>
        <p>In Vedantic thought, the <em>antahkarana</em> is the inner instrument of the mind — not a single faculty, but four distinct functions: <strong>manas</strong> (perception and doubt), <strong>buddhi</strong> (discrimination and decision), <strong>chitta</strong> (memory and conditioning), and <strong>ahamkara</strong> (the ego that integrates everything into a coherent self).</p>
        <p>I mapped these directly to LLM reasoning stages. Manas handles initial query parsing and ambiguity detection. Buddhi routes the query to the appropriate specialised module. Chitta manages retrieval memory via FAISS vector search. The integration layer synthesises outputs without the "ego" problem — no single module dominates; the best answer wins.</p>
        <h3>Why it works better than a single model</h3>
        <p>The key insight is that different reasoning tasks require different cognitive postures. A factual retrieval query should not be processed the same way as a complex multi-step inference problem. By routing explicitly, Antahkarana applies the right tool to the right task — and the 2,500-sample validation showed measurable improvements in coherence on complex multimodal queries.</p>
        <h3>What's next</h3>
        <p>The patent covers the routing and decision architecture. The IEEE paper covers the full experimental methodology. I'm currently working on open-sourcing a lightweight version — the full framework is at github.com/rajaganaa/antahkarana-reasoning-framework.</p>
      `
    },
    {
      tag: 'AGENTIC AI',
      date: 'March 2026 · 7 min read',
      title: 'RAG vs Fine-Tuning: Lessons from Building a Medical AI Assistant',
      body: `
        <p>When I started building the Antahkarana medical AI assistant, I had to make the RAG vs. fine-tuning decision for every sub-task. After months of building, testing, and occasionally rebuilding from scratch, here's the framework I arrived at.</p>
        <h3>The question is wrong</h3>
        <p>The industry frames this as a binary choice. It isn't. The real question is: <em>what is the nature of the knowledge this task requires?</em></p>
        <p><strong>RAG wins</strong> when the knowledge is: external and updatable (medical guidelines change), verifiable (you need citations), or domain-specific and voluminous (no model has memorised every clinical study). For the medical assistant, this was almost everything — symptom analysis, drug interactions, treatment protocols.</p>
        <p><strong>Fine-tuning wins</strong> when the task requires: a specific output format or tone the base model can't reliably produce, internalised reasoning patterns (not facts), or latency-critical inference where retrieval overhead is unacceptable.</p>
        <h3>What I actually did</h3>
        <p>The Antahkarana medical system uses RAG for factual retrieval and a lightly fine-tuned layer for output formatting and clinical tone. The retrieval runs against a FAISS index of structured medical knowledge. The generation model has been prompted — not fine-tuned — to maintain appropriate clinical caution.</p>
        <p>The biggest lesson: <em>don't fine-tune to fix retrieval problems</em>. If your RAG pipeline is returning poor context, fine-tuning the generator won't help — it'll just learn to hallucinate more confidently. Fix the retrieval first.</p>
        <h3>The live system</h3>
        <p>The full medical assistant is deployed on Azure at rajaganaa.github.io/antahkarana-frontend. It's multimodal — it accepts text, images, and documents. The backend runs on Azure Container Instances. CI/CD via GitHub Actions.</p>
      `
    }
  ];

  function openBlog(index) {
    const b = blogs[index];
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

  function closeBlogOnOverlay(e) {
    if (e.target === document.getElementById('blogModal')) closeBlog();
  }

  document.addEventListener('keydown', (e) => { if (e.key === 'Escape') closeBlog(); });
</script>

</body>
</html> 
