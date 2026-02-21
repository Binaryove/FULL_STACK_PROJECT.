<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NEXUS — Advanced Web Experience</title>
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Syne:wght@400;600;700;800&family=JetBrains+Mono:wght@300;400;500&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #030508;
      --bg2: #080c14;
      --cyan: #00f5ff;
      --magenta: #ff0080;
      --yellow: #ffe600;
      --white: #f0f4ff;
      --dim: rgba(240,244,255,0.45);
      --glass: rgba(255,255,255,0.03);
      --border: rgba(0,245,255,0.12);
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; font-size: 16px; }

    body {
      background: var(--bg);
      color: var(--white);
      font-family: 'Syne', sans-serif;
      overflow-x: hidden;
      cursor: none;
    }

    /* ── CUSTOM CURSOR ── */
    #cursor {
      position: fixed;
      width: 12px; height: 12px;
      background: var(--cyan);
      border-radius: 50%;
      pointer-events: none;
      z-index: 99999;
      transform: translate(-50%,-50%);
      transition: transform 0.08s, width 0.2s, height 0.2s, background 0.2s;
      mix-blend-mode: difference;
    }

    #cursor-ring {
      position: fixed;
      width: 40px; height: 40px;
      border: 1px solid rgba(0,245,255,0.5);
      border-radius: 50%;
      pointer-events: none;
      z-index: 99998;
      transform: translate(-50%,-50%);
      transition: transform 0.18s ease, width 0.3s, height 0.3s, border-color 0.3s;
    }

    body:has(a:hover) #cursor, body:has(button:hover) #cursor {
      width: 20px; height: 20px;
      background: var(--magenta);
    }

    body:has(a:hover) #cursor-ring, body:has(button:hover) #cursor-ring {
      width: 60px; height: 60px;
      border-color: rgba(255,0,128,0.5);
    }

    /* ── CANVAS BACKGROUND ── */
    #particles-canvas {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      z-index: 0;
      pointer-events: none;
    }

    /* ── LOADER ── */
    #loader {
      position: fixed;
      inset: 0;
      background: var(--bg);
      z-index: 9000;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 24px;
      transition: opacity 0.6s, visibility 0.6s;
    }

    #loader.hidden { opacity: 0; visibility: hidden; }

    .loader-text {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 64px;
      letter-spacing: 0.15em;
      color: var(--cyan);
      text-shadow: 0 0 40px rgba(0,245,255,0.6);
      animation: glitch 0.5s infinite;
    }

    .loader-bar-wrap {
      width: 300px;
      height: 2px;
      background: rgba(255,255,255,0.08);
      overflow: hidden;
    }

    .loader-bar {
      height: 100%;
      width: 0%;
      background: linear-gradient(to right, var(--cyan), var(--magenta));
      transition: width 2s cubic-bezier(0.4,0,0.2,1);
      box-shadow: 0 0 20px var(--cyan);
    }

    .loader-percent {
      font-family: 'JetBrains Mono', monospace;
      font-size: 13px;
      color: var(--dim);
      letter-spacing: 0.1em;
    }

    /* ── NAV ── */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 1000;
      padding: 24px 60px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      backdrop-filter: blur(20px);
      background: rgba(3,5,8,0.7);
      border-bottom: 1px solid var(--border);
      transform: translateY(-100%);
      transition: transform 0.6s cubic-bezier(0.16,1,0.3,1);
    }

    nav.visible { transform: translateY(0); }

    .nav-logo {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 28px;
      letter-spacing: 0.2em;
      color: var(--cyan);
      text-shadow: 0 0 20px rgba(0,245,255,0.5);
    }

    .nav-links {
      display: flex;
      gap: 40px;
      list-style: none;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--dim);
      font-size: 12px;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      font-family: 'JetBrains Mono', monospace;
      position: relative;
      transition: color 0.2s;
    }

    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: -4px; left: 0;
      width: 0; height: 1px;
      background: var(--cyan);
      transition: width 0.3s;
    }

    .nav-links a:hover { color: var(--cyan); }
    .nav-links a:hover::after { width: 100%; }

    .nav-cta {
      background: transparent;
      border: 1px solid var(--cyan);
      color: var(--cyan);
      padding: 10px 24px;
      font-family: 'JetBrains Mono', monospace;
      font-size: 12px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      cursor: none;
      transition: background 0.2s, color 0.2s, box-shadow 0.2s;
    }

    .nav-cta:hover {
      background: var(--cyan);
      color: var(--bg);
      box-shadow: 0 0 30px rgba(0,245,255,0.4);
    }

    /* ── HERO ── */
    #hero {
      position: relative;
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 0 60px;
      z-index: 1;
      overflow: hidden;
    }

    .hero-content { max-width: 900px; }

    .hero-eyebrow {
      font-family: 'JetBrains Mono', monospace;
      font-size: 12px;
      letter-spacing: 0.3em;
      color: var(--cyan);
      text-transform: uppercase;
      margin-bottom: 24px;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeUp 0.8s 2.2s forwards;
    }

    .hero-eyebrow span {
      display: inline-block;
      width: 30px;
      height: 1px;
      background: var(--cyan);
      vertical-align: middle;
      margin-right: 12px;
    }

    .hero-title {
      font-family: 'Bebas Neue', sans-serif;
      font-size: clamp(72px, 12vw, 180px);
      line-height: 0.88;
      letter-spacing: 0.02em;
      margin-bottom: 32px;
      opacity: 0;
      transform: translateY(30px);
      animation: fadeUp 0.9s 2.4s forwards;
    }

    .hero-title .line1 { color: var(--white); }
    .hero-title .line2 {
      color: transparent;
      -webkit-text-stroke: 1px var(--cyan);
      text-shadow: none;
    }
    .hero-title .line3 {
      color: var(--magenta);
      text-shadow: 0 0 60px rgba(255,0,128,0.4);
    }

    .hero-desc {
      font-size: 16px;
      line-height: 1.8;
      color: var(--dim);
      max-width: 480px;
      font-weight: 400;
      margin-bottom: 48px;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeUp 0.8s 2.6s forwards;
    }

    .hero-buttons {
      display: flex;
      gap: 16px;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeUp 0.8s 2.8s forwards;
    }

    .btn-primary {
      padding: 16px 40px;
      background: var(--cyan);
      color: var(--bg);
      border: none;
      font-family: 'Syne', sans-serif;
      font-weight: 700;
      font-size: 14px;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      cursor: none;
      position: relative;
      overflow: hidden;
      transition: box-shadow 0.3s;
    }

    .btn-primary::before {
      content: '';
      position: absolute;
      inset: 0;
      background: var(--magenta);
      transform: translateX(-100%);
      transition: transform 0.3s cubic-bezier(0.4,0,0.2,1);
    }

    .btn-primary:hover::before { transform: translateX(0); }
    .btn-primary:hover { box-shadow: 0 0 40px rgba(255,0,128,0.5); }
    .btn-primary span { position: relative; z-index: 1; }

    .btn-secondary {
      padding: 16px 40px;
      background: transparent;
      color: var(--white);
      border: 1px solid rgba(255,255,255,0.15);
      font-family: 'Syne', sans-serif;
      font-weight: 600;
      font-size: 14px;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      cursor: none;
      transition: border-color 0.3s, color 0.3s;
    }

    .btn-secondary:hover { border-color: var(--white); color: var(--cyan); }

    /* Scroll indicator */
    .scroll-indicator {
      position: absolute;
      bottom: 48px;
      left: 60px;
      display: flex;
      align-items: center;
      gap: 16px;
      opacity: 0;
      animation: fadeUp 0.8s 3s forwards;
    }

    .scroll-indicator .line {
      width: 60px; height: 1px;
      background: linear-gradient(to right, var(--cyan), transparent);
      animation: scrollPulse 2s infinite;
    }

    .scroll-indicator span {
      font-family: 'JetBrains Mono', monospace;
      font-size: 10px;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--dim);
    }

    /* Stats row */
    .stats-row {
      position: absolute;
      bottom: 48px;
      right: 60px;
      display: flex;
      gap: 48px;
      opacity: 0;
      animation: fadeUp 0.8s 3.1s forwards;
    }

    .stat { text-align: right; }

    .stat-num {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 40px;
      color: var(--cyan);
      letter-spacing: 0.05em;
      line-height: 1;
    }

    .stat-label {
      font-family: 'JetBrains Mono', monospace;
      font-size: 10px;
      letter-spacing: 0.15em;
      color: var(--dim);
      text-transform: uppercase;
    }

    /* Hero grid lines */
    .hero-grid {
      position: absolute;
      inset: 0;
      background-image:
        linear-gradient(rgba(0,245,255,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(0,245,255,0.03) 1px, transparent 1px);
      background-size: 80px 80px;
      pointer-events: none;
    }

    /* ── SECTION BASE ── */
    .section {
      position: relative;
      z-index: 1;
      padding: 120px 60px;
      max-width: 1400px;
      margin: 0 auto;
    }

    .section-label {
      font-family: 'JetBrains Mono', monospace;
      font-size: 11px;
      letter-spacing: 0.3em;
      text-transform: uppercase;
      color: var(--cyan);
      margin-bottom: 16px;
    }

    .section-heading {
      font-family: 'Bebas Neue', sans-serif;
      font-size: clamp(48px, 6vw, 88px);
      line-height: 0.95;
      letter-spacing: 0.04em;
      margin-bottom: 64px;
      color: var(--white);
    }

    /* ── FEATURES BENTO ── */
    .bento {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      grid-template-rows: auto;
      gap: 2px;
      background: rgba(0,245,255,0.05);
      border: 1px solid var(--border);
    }

    .bento-item {
      background: var(--bg2);
      padding: 48px 40px;
      position: relative;
      overflow: hidden;
      transition: background 0.3s;
      opacity: 0;
      transform: translateY(30px);
    }

    .bento-item.visible {
      animation: fadeUp 0.7s forwards;
    }

    .bento-item:hover { background: rgba(0,245,255,0.04); }

    .bento-item::before {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 1px;
      background: linear-gradient(to right, var(--cyan), transparent);
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.4s;
    }

    .bento-item:hover::before { transform: scaleX(1); }

    .bento-item.wide { grid-column: span 4; }
    .bento-item.tall { grid-row: span 2; }
    .bento-item.half { grid-column: span 3; }
    .bento-item.small { grid-column: span 2; }

    .bento-icon {
      font-size: 36px;
      margin-bottom: 20px;
      display: block;
    }

    .bento-num {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 80px;
      color: rgba(0,245,255,0.08);
      position: absolute;
      top: 16px;
      right: 24px;
      line-height: 1;
      letter-spacing: -0.02em;
    }

    .bento-title {
      font-size: 18px;
      font-weight: 700;
      color: var(--white);
      margin-bottom: 12px;
      letter-spacing: -0.01em;
    }

    .bento-text {
      font-size: 13px;
      line-height: 1.8;
      color: var(--dim);
      font-weight: 400;
    }

    .bento-tag {
      display: inline-block;
      margin-top: 24px;
      font-family: 'JetBrains Mono', monospace;
      font-size: 10px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--cyan);
      border: 1px solid rgba(0,245,255,0.25);
      padding: 4px 12px;
    }

    /* ── MARQUEE ── */
    .marquee-wrap {
      position: relative;
      z-index: 1;
      overflow: hidden;
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      padding: 20px 0;
      background: var(--bg2);
    }

    .marquee {
      display: flex;
      gap: 60px;
      white-space: nowrap;
      animation: marquee 20s linear infinite;
    }

    .marquee span {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 40px;
      letter-spacing: 0.1em;
      color: transparent;
      -webkit-text-stroke: 1px rgba(0,245,255,0.3);
      flex-shrink: 0;
    }

    .marquee span.filled {
      color: var(--white);
      -webkit-text-stroke: 0;
    }

    /* ── SKILLS COUNTER ── */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 1px;
      background: var(--border);
      border: 1px solid var(--border);
    }

    .skill-item {
      background: var(--bg2);
      padding: 48px 32px;
      text-align: center;
      position: relative;
      overflow: hidden;
      transition: background 0.3s;
      opacity: 0;
    }

    .skill-item.visible { animation: fadeUp 0.6s forwards; }
    .skill-item:hover { background: rgba(0,245,255,0.05); }

    .skill-pct {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 64px;
      color: var(--cyan);
      line-height: 1;
      text-shadow: 0 0 30px rgba(0,245,255,0.4);
    }

    .skill-name {
      font-family: 'JetBrains Mono', monospace;
      font-size: 11px;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--dim);
      margin-top: 8px;
    }

    .skill-bar {
      position: absolute;
      bottom: 0; left: 0;
      height: 2px;
      background: linear-gradient(to right, var(--cyan), var(--magenta));
      width: 0%;
      transition: width 1.5s cubic-bezier(0.4,0,0.2,1);
      box-shadow: 0 0 10px var(--cyan);
    }

    .skill-item.visible .skill-bar { width: var(--skill-w); }

    /* ── TIMELINE / PROCESS ── */
    .process {
      display: grid;
      grid-template-columns: 1fr;
      gap: 0;
    }

    .process-item {
      display: grid;
      grid-template-columns: 100px 1fr;
      gap: 40px;
      padding: 48px 0;
      border-bottom: 1px solid var(--border);
      position: relative;
      opacity: 0;
      transform: translateX(-30px);
      transition: opacity 0.7s, transform 0.7s;
    }

    .process-item.visible { opacity: 1; transform: translateX(0); }

    .process-num {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 80px;
      color: rgba(0,245,255,0.12);
      line-height: 1;
      text-align: right;
      transition: color 0.3s;
    }

    .process-item:hover .process-num { color: rgba(0,245,255,0.35); }

    .process-content { padding-top: 12px; }

    .process-title {
      font-size: 22px;
      font-weight: 700;
      color: var(--white);
      margin-bottom: 12px;
    }

    .process-desc {
      font-size: 14px;
      line-height: 1.8;
      color: var(--dim);
    }

    .process-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 16px;
    }

    .tag {
      font-family: 'JetBrains Mono', monospace;
      font-size: 10px;
      letter-spacing: 0.15em;
      padding: 4px 12px;
      border: 1px solid var(--border);
      color: var(--dim);
      text-transform: uppercase;
      transition: border-color 0.2s, color 0.2s;
    }

    .process-item:hover .tag { border-color: rgba(0,245,255,0.3); color: var(--cyan); }

    /* ── CONTACT / CTA ── */
    .cta-section {
      position: relative;
      z-index: 1;
      overflow: hidden;
      background: var(--bg2);
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
    }

    .cta-inner {
      max-width: 1400px;
      margin: 0 auto;
      padding: 120px 60px;
      text-align: center;
    }

    .cta-title {
      font-family: 'Bebas Neue', sans-serif;
      font-size: clamp(60px, 10vw, 140px);
      line-height: 0.9;
      color: var(--white);
      letter-spacing: 0.04em;
      margin-bottom: 32px;
    }

    .cta-title .accent { color: var(--cyan); text-shadow: 0 0 60px rgba(0,245,255,0.5); }

    .cta-sub {
      font-size: 16px;
      color: var(--dim);
      margin-bottom: 48px;
      font-weight: 400;
    }

    /* ── FORM ── */
    .contact-form {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
      max-width: 700px;
      margin: 0 auto 24px;
    }

    .form-input {
      background: rgba(255,255,255,0.03);
      border: 1px solid var(--border);
      color: var(--white);
      padding: 16px 20px;
      font-family: 'Syne', sans-serif;
      font-size: 14px;
      outline: none;
      transition: border-color 0.2s, background 0.2s;
      grid-column: span 1;
    }

    .form-input.full { grid-column: span 2; }

    .form-input::placeholder { color: rgba(255,255,255,0.2); }
    .form-input:focus { border-color: var(--cyan); background: rgba(0,245,255,0.03); }

    .form-submit {
      width: 100%;
      max-width: 700px;
      margin: 0 auto;
      display: block;
      padding: 18px;
      background: var(--cyan);
      color: var(--bg);
      border: none;
      font-family: 'Syne', sans-serif;
      font-weight: 800;
      font-size: 15px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      cursor: none;
      transition: box-shadow 0.3s, background 0.3s;
      position: relative;
      overflow: hidden;
    }

    .form-submit:hover {
      background: var(--magenta);
      box-shadow: 0 0 50px rgba(255,0,128,0.5);
    }

    .form-success {
      display: none;
      font-family: 'JetBrains Mono', monospace;
      font-size: 14px;
      color: var(--cyan);
      letter-spacing: 0.1em;
      margin-top: 16px;
    }

    /* ── FOOTER ── */
    footer {
      position: relative;
      z-index: 1;
      padding: 48px 60px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-top: 1px solid var(--border);
      background: var(--bg);
    }

    .footer-logo {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 32px;
      letter-spacing: 0.2em;
      color: var(--cyan);
      text-shadow: 0 0 20px rgba(0,245,255,0.4);
    }

    .footer-links {
      display: flex;
      gap: 32px;
      list-style: none;
    }

    .footer-links a {
      text-decoration: none;
      font-family: 'JetBrains Mono', monospace;
      font-size: 11px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--dim);
      transition: color 0.2s;
    }

    .footer-links a:hover { color: var(--cyan); }

    .footer-copy {
      font-family: 'JetBrains Mono', monospace;
      font-size: 10px;
      letter-spacing: 0.15em;
      color: rgba(255,255,255,0.2);
    }

    /* ── FLOATING ORBS ── */
    .orb {
      position: fixed;
      border-radius: 50%;
      filter: blur(80px);
      pointer-events: none;
      z-index: 0;
      opacity: 0.15;
      animation: float 8s ease-in-out infinite;
    }

    .orb1 { width: 400px; height: 400px; background: var(--cyan); top: -100px; right: -100px; animation-delay: 0s; }
    .orb2 { width: 300px; height: 300px; background: var(--magenta); bottom: 20%; left: -50px; animation-delay: 3s; }
    .orb3 { width: 200px; height: 200px; background: var(--yellow); top: 50%; right: 10%; animation-delay: 5s; opacity: 0.08; }

    /* ── ANIMATIONS ── */
    @keyframes fadeUp {
      to { opacity: 1; transform: translateY(0) translateX(0); }
    }

    @keyframes glitch {
      0%,100% { text-shadow: 0 0 40px rgba(0,245,255,0.6); transform: translate(0); }
      20% { text-shadow: -3px 0 var(--magenta), 3px 0 var(--cyan); transform: tr
