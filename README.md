[index.html](https://github.com/user-attachments/files/33361159/Alchemy.Systems.IT.html)
# alchemysystemsit.com
Alchemy Systems IT website
<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Alchemy Systems IT</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=IBM+Plex+Sans:wght@400;500&family=IBM+Plex+Mono:wght@400;500&display=swap">

<style>
/* =====================================================
   ALCHEMY SYSTEMS IT — Dark-first design
   Layout: Single column, section-stacked, full-bleed hero
   ===================================================== */

/* --- Tokens: dark (default) --- */
:root {
  --bg:          #0b110b;
  --bg-card:     #111a11;
  --bg-subtle:   #162016;
  --fg:          #ddeedd;
  --fg-muted:    #7a9a7a;
  --fg-dim:      #3d5c3d;
  --accent:      #4ade80;
  --accent-mid:  #22c55e;
  --accent-dark: #15803d;
  --border:      #1e301e;
  --border-hi:   #2d4a2d;
  --glow:        rgba(74, 222, 128, 0.12);
  color-scheme: dark;
}

/* --- Tokens: light --- */
@media (prefers-color-scheme: light) {
  :root:not([data-theme="dark"]) {
    --bg:          #f2f7f2;
    --bg-card:     #ffffff;
    --bg-subtle:   #e8f2e8;
    --fg:          #0d1a0d;
    --fg-muted:    #3d6040;
    --fg-dim:      #a0bca0;
    --accent:      #16a34a;
    --accent-mid:  #15803d;
    --accent-dark: #14532d;
    --border:      #c8dfc8;
    --border-hi:   #a8cca8;
    --glow:        rgba(22, 163, 74, 0.08);
    color-scheme: light;
  }
}
:root[data-theme="light"] {
  --bg:          #f2f7f2;
  --bg-card:     #ffffff;
  --bg-subtle:   #e8f2e8;
  --fg:          #0d1a0d;
  --fg-muted:    #3d6040;
  --fg-dim:      #a0bca0;
  --accent:      #16a34a;
  --accent-mid:  #15803d;
  --accent-dark: #14532d;
  --border:      #c8dfc8;
  --border-hi:   #a8cca8;
  --glow:        rgba(22, 163, 74, 0.08);
  color-scheme: light;
}
:root[data-theme="dark"] {
  --bg:          #0b110b;
  --bg-card:     #111a11;
  --bg-subtle:   #162016;
  --fg:          #ddeedd;
  --fg-muted:    #7a9a7a;
  --fg-dim:      #3d5c3d;
  --accent:      #4ade80;
  --accent-mid:  #22c55e;
  --accent-dark: #15803d;
  --border:      #1e301e;
  --border-hi:   #2d4a2d;
  --glow:        rgba(74, 222, 128, 0.12);
  color-scheme: dark;
}

/* --- Reset & Base --- */
*, *::before, *::after { box-sizing: border-box; }

body {
  margin: 0;
  padding-inline: 0;
  background: var(--bg);
  color: var(--fg);
  font-family: 'IBM Plex Sans', system-ui, sans-serif;
  font-size: 1rem;
  line-height: 1.65;
}

/* --- Circuit grid background texture --- */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: 0;
  background-image:
    linear-gradient(var(--border) 1px, transparent 1px),
    linear-gradient(90deg, var(--border) 1px, transparent 1px);
  background-size: 40px 40px;
  opacity: 0.4;
}

/* --- Layout wrapper --- */
.page {
  position: relative;
  z-index: 1;
  max-width: 900px;
  margin-inline: auto;
  padding-inline: 24px;
}

/* --- Type scale --- */
h1, h2, h3, h4 {
  font-family: 'Syne', sans-serif;
  text-wrap: balance;
  margin: 0;
  line-height: 1.15;
}

.mono {
  font-family: 'IBM Plex Mono', monospace;
}

/* =====================================================
   NAV / HEADER
   ===================================================== */
nav {
  position: sticky;
  top: env(safe-area-inset-top, 0px);
  z-index: 100;
  background: color-mix(in srgb, var(--bg) 85%, transparent);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border);
  padding-block: 0;
}

.nav-inner {
  max-width: 900px;
  margin-inline: auto;
  padding-inline: 24px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-logo {
  display: flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
}

.nav-logo-mark {
  width: 32px;
  height: 32px;
  flex-shrink: 0;
}

.nav-brand {
  font-family: 'Syne', sans-serif;
  font-weight: 700;
  font-size: 1rem;
  color: var(--fg);
  letter-spacing: -0.01em;
}

.nav-brand span {
  color: var(--accent);
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 28px;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-links a {
  color: var(--fg-muted);
  text-decoration: none;
  font-size: 0.875rem;
  font-weight: 500;
  transition: color 0.15s;
}

.nav-links a:hover { color: var(--accent); }

.nav-cta {
  background: var(--accent);
  color: var(--bg) !important;
  padding: 6px 16px;
  border-radius: 4px;
  font-weight: 600 !important;
  font-size: 0.85rem !important;
}

.nav-cta:hover { opacity: 0.88; }

/* =====================================================
   HERO
   ===================================================== */
.hero {
  padding-block: 80px 72px;
  border-bottom: 1px solid var(--border);
}

.hero-eyebrow {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.75rem;
  color: var(--accent);
  letter-spacing: 0.12em;
  text-transform: uppercase;
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.hero-eyebrow::before {
  content: '';
  display: block;
  width: 28px;
  height: 1px;
  background: var(--accent);
}

.hero h1 {
  font-size: clamp(2.4rem, 6vw, 3.8rem);
  font-weight: 800;
  letter-spacing: -0.03em;
  color: var(--fg);
  margin-bottom: 24px;
  max-width: 18ch;
}

.hero h1 em {
  font-style: normal;
  color: var(--accent);
}

.hero-sub {
  font-size: 1.1rem;
  color: var(--fg-muted);
  max-width: 52ch;
  margin-bottom: 40px;
  line-height: 1.7;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  align-items: center;
}

.btn-primary {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: var(--accent);
  color: var(--bg);
  font-family: 'IBM Plex Sans', sans-serif;
  font-weight: 600;
  font-size: 0.95rem;
  padding: 12px 24px;
  border-radius: 4px;
  text-decoration: none;
  transition: opacity 0.15s;
}

.btn-primary:hover { opacity: 0.88; }

.btn-secondary {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: transparent;
  color: var(--fg);
  font-family: 'IBM Plex Sans', sans-serif;
  font-weight: 500;
  font-size: 0.95rem;
  padding: 12px 24px;
  border-radius: 4px;
  border: 1px solid var(--border-hi);
  text-decoration: none;
  transition: border-color 0.15s, color 0.15s;
}

.btn-secondary:hover {
  border-color: var(--accent);
  color: var(--accent);
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  margin-top: 36px;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.78rem;
  color: var(--fg-dim);
  letter-spacing: 0.04em;
}

.hero-badge-dot {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: var(--accent);
  animation: pulse 2.4s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.3; }
}

@media (prefers-reduced-motion: reduce) {
  .hero-badge-dot { animation: none; }
}

/* =====================================================
   SECTION SHARED
   ===================================================== */
section {
  padding-block: 64px;
  border-bottom: 1px solid var(--border);
}

.section-label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.72rem;
  color: var(--accent);
  letter-spacing: 0.12em;
  text-transform: uppercase;
  margin-bottom: 10px;
}

.section-title {
  font-size: clamp(1.5rem, 4vw, 2rem);
  font-weight: 700;
  letter-spacing: -0.02em;
  color: var(--fg);
  margin-bottom: 8px;
}

.section-sub {
  color: var(--fg-muted);
  font-size: 1rem;
  max-width: 56ch;
  margin-bottom: 44px;
}

/* =====================================================
   SERVICES
   ===================================================== */
.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 16px;
}

.service-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 6px;
  padding: 28px 24px;
  transition: border-color 0.2s, box-shadow 0.2s;
}

.service-card:hover {
  border-color: var(--border-hi);
  box-shadow: 0 0 0 1px var(--border-hi), 0 4px 24px var(--glow);
}

.service-icon {
  width: 40px;
  height: 40px;
  margin-bottom: 18px;
  color: var(--accent);
}

.service-card h3 {
  font-size: 1.05rem;
  font-weight: 700;
  color: var(--fg);
  margin-bottom: 8px;
  letter-spacing: -0.01em;
}

.service-card p {
  font-size: 0.9rem;
  color: var(--fg-muted);
  margin: 0 0 16px;
  line-height: 1.6;
}

.service-tag {
  display: inline-block;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.72rem;
  font-weight: 500;
  color: var(--accent);
  background: var(--bg-subtle);
  border: 1px solid var(--border-hi);
  border-radius: 3px;
  padding: 3px 8px;
  letter-spacing: 0.04em;
}

/* =====================================================
   FREE CALL CALLOUT
   ===================================================== */
.callout {
  background: var(--bg-subtle);
  border: 1px solid var(--border-hi);
  border-left: 3px solid var(--accent);
  border-radius: 6px;
  padding: 28px 32px;
  margin-top: 28px;
  display: flex;
  gap: 20px;
  align-items: flex-start;
}

.callout-icon {
  flex-shrink: 0;
  color: var(--accent);
  margin-top: 2px;
}

.callout-title {
  font-family: 'Syne', sans-serif;
  font-weight: 700;
  font-size: 1rem;
  color: var(--fg);
  margin-bottom: 4px;
}

.callout-body {
  font-size: 0.9rem;
  color: var(--fg-muted);
  margin: 0;
  line-height: 1.6;
}

/* =====================================================
   HOURS
   ===================================================== */
.hours-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
}

@media (max-width: 560px) {
  .hours-grid { grid-template-columns: 1fr; }
}

.hours-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 6px;
  overflow: hidden;
}

.hours-card-head {
  background: var(--bg-subtle);
  border-bottom: 1px solid var(--border);
  padding: 14px 20px;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.72rem;
  color: var(--accent);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  font-weight: 500;
}

.hours-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.875rem;
}

.hours-table tr {
  border-bottom: 1px solid var(--border);
}

.hours-table tr:last-child { border-bottom: none; }

.hours-table td {
  padding: 11px 20px;
  vertical-align: middle;
}

.hours-table td:first-child {
  color: var(--fg);
  font-weight: 500;
  width: 45%;
}

.hours-table td:last-child {
  color: var(--fg-muted);
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.8rem;
}

.hours-closed {
  color: var(--fg-dim) !important;
  font-style: italic;
}

.hours-note {
  margin-top: 20px;
  font-size: 0.82rem;
  color: var(--fg-muted);
  font-family: 'IBM Plex Mono', monospace;
  display: flex;
  align-items: flex-start;
  gap: 8px;
}

.hours-note-icon { color: var(--accent); flex-shrink: 0; margin-top: 1px; }

/* =====================================================
   ABOUT / WHY
   ===================================================== */
.about-inner {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 52px;
  align-items: start;
}

@media (max-width: 620px) {
  .about-inner { grid-template-columns: 1fr; gap: 32px; }
}

.about-body {
  font-size: 0.95rem;
  color: var(--fg-muted);
  line-height: 1.75;
}

.about-body p { margin: 0 0 16px; }
.about-body p:last-child { margin: 0; }

.about-points {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.about-point {
  display: flex;
  gap: 14px;
  align-items: flex-start;
}

.about-point-check {
  flex-shrink: 0;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background: var(--bg-subtle);
  border: 1px solid var(--border-hi);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 2px;
  color: var(--accent);
}

.about-point-text strong {
  display: block;
  font-weight: 600;
  color: var(--fg);
  font-size: 0.9rem;
  margin-bottom: 2px;
}

.about-point-text span {
  font-size: 0.85rem;
  color: var(--fg-muted);
}

/* =====================================================
   CONTACT
   ===================================================== */
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}

@media (max-width: 560px) {
  .contact-grid { grid-template-columns: 1fr; }
}

.contact-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 6px;
  padding: 24px;
}

.contact-card-label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.7rem;
  color: var(--fg-muted);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  margin-bottom: 8px;
}

.contact-card-value {
  font-size: 1rem;
  font-weight: 600;
  color: var(--fg);
  font-family: 'Syne', sans-serif;
  word-break: break-all;
}

.contact-card-note {
  font-size: 0.8rem;
  color: var(--fg-muted);
  margin-top: 6px;
}

/* =====================================================
   FOOTER
   ===================================================== */
footer {
  padding-block: 36px;
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  justify-content: space-between;
  align-items: center;
}

.footer-brand {
  font-family: 'Syne', sans-serif;
  font-weight: 700;
  font-size: 0.9rem;
  color: var(--fg-muted);
}

.footer-brand span { color: var(--accent); }

.footer-copy {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 0.72rem;
  color: var(--fg-dim);
}

/* =====================================================
   UTILITY
   ===================================================== */
.sr-only {
  position: absolute; width: 1px; height: 1px;
  padding: 0; margin: -1px; overflow: hidden;
  clip: rect(0,0,0,0); white-space: nowrap; border: 0;
}

a:focus-visible {
  outline: 2px solid var(--accent);
  outline-offset: 3px;
  border-radius: 2px;
}

</style>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <a href="#" class="nav-logo" aria-label="Alchemy Systems IT home">
      <svg class="nav-logo-mark" viewBox="0 0 32 32" fill="none" aria-hidden="true">
        <rect width="32" height="32" rx="4" fill="var(--bg-subtle)"/>
        <rect x="1" y="1" width="30" height="30" rx="3" fill="none" stroke="var(--border-hi)" stroke-width="1"/>
        <!-- circuit lines -->
        <line x1="8" y1="16" x2="14" y2="16" stroke="var(--accent)" stroke-width="1.5" stroke-linecap="round"/>
        <line x1="18" y1="16" x2="24" y2="16" stroke="var(--accent)" stroke-width="1.5" stroke-linecap="round"/>
        <line x1="16" y1="8" x2="16" y2="14" stroke="var(--accent)" stroke-width="1.5" stroke-linecap="round"/>
        <line x1="16" y1="18" x2="16" y2="24" stroke="var(--accent)" stroke-width="1.5" stroke-linecap="round"/>
        <circle cx="16" cy="16" r="2.5" fill="var(--accent)"/>
        <circle cx="8" cy="16" r="1.5" fill="none" stroke="var(--accent-mid)" stroke-width="1"/>
        <circle cx="24" cy="16" r="1.5" fill="none" stroke="var(--accent-mid)" stroke-width="1"/>
        <circle cx="16" cy="8" r="1.5" fill="none" stroke="var(--accent-mid)" stroke-width="1"/>
        <circle cx="16" cy="24" r="1.5" fill="none" stroke="var(--accent-mid)" stroke-width="1"/>
      </svg>
      <span class="nav-brand">Alchemy <span>Systems</span></span>
    </a>
    <ul class="nav-links">
      <li><a href="#services">Services</a></li>
      <li><a href="#hours">Hours</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#contact" class="nav-cta">Contact</a></li>
    </ul>
  </div>
</nav>

<!-- HERO -->
<div class="page">
  <section class="hero" aria-labelledby="hero-heading">
    <p class="hero-eyebrow">Milton-Freewater &amp; Walla Walla</p>
    <h1 id="hero-heading">IT Support for <em>Home &amp; Business</em></h1>
    <p class="hero-sub">Fast, honest tech help — by phone, remote session, or on-site. No jargon, no runaround. Your first call is always free.</p>
    <div class="hero-actions">
      <a href="#contact" class="btn-primary">
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none" aria-hidden="true">
          <path d="M2 3.5C2 2.67 2.67 2 3.5 2h2.618c.329 0 .62.214.724.527l.96 2.88a.75.75 0 0 1-.173.782L6.37 7.44a8.001 8.001 0 0 0 3.19 3.19l1.25-1.26a.75.75 0 0 1 .782-.173l2.88.96c.313.104.528.395.528.724V12.5A1.5 1.5 0 0 1 13.5 14C6.596 14 1 8.404 1 1.5A1.5 1.5 0 0 1 2.5 0h.5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
        </svg>
        Get Free Help
      </a>
      <a href="#services" class="btn-secondary">See What We Fix →</a>
    </div>
    <p class="hero-badge">
      <span class="hero-badge-dot" aria-hidden="true"></span>
      Accepting new clients — no contract required
    </p>
  </section>

  <!-- SERVICES -->
  <section id="services" aria-labelledby="services-heading">
    <p class="section-label">What We Do</p>
    <h2 class="section-title" id="services-heading">Practical IT Help, Done Right</h2>
    <p class="section-sub">From a quick phone fix to a full on-site visit, we handle the tech so you don't have to.</p>

    <div class="services-grid">
      <div class="service-card">
        <svg class="service-icon" viewBox="0 0 40 40" fill="none" aria-hidden="true">
          <path d="M8 14C8 10.686 10.686 8 14 8h12c3.314 0 6 2.686 6 6v8c0 3.314-2.686 6-6 6h-1l-4 4-4-4h-1c-3.314 0-6-2.686-6-6v-8z" stroke="currentColor" stroke-width="1.5"/>
          <path d="M14 17h12M14 22h8" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
        </svg>
        <h3>Free Help Desk Call</h3>
        <p>Call us with your tech problem. We'll diagnose it over the phone, walk you through a fix if we can, or point you to the right resource if we can't.</p>
        <span class="service-tag">Always Free</span>
      </div>

      <div class="service-card">
        <svg class="service-icon" viewBox="0 0 40 40" fill="none" aria-hidden="true">
          <rect x="6" y="10" width="28" height="18" rx="3" stroke="currentColor" stroke-width="1.5"/>
          <path d="M14 28l-2 4h16l-2-4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M18 19l3-3-3-3M22 13l3 3-3 3" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        <h3>Remote Support</h3>
        <p>We connect securely to your computer and fix the problem while you watch. Most issues — slow PCs, software installs, virus removal — can be handled remotely in minutes.</p>
        <span class="service-tag">By Appointment</span>
      </div>

      <div class="service-card">
        <svg class="service-icon" viewBox="0 0 40 40" fill="none" aria-hidden="true">
          <path d="M10 30V18l10-10 10 10v12" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          <rect x="15" y="22" width="10" height="8" rx="1" stroke="currentColor" stroke-width="1.5"/>
          <path d="M20 22v8" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
        </svg>
        <h3>On-Site Service</h3>
        <p>We come to you — home or office. Hardware installs, network setup, printer nightmares, new device configuration. We handle what remote can't.</p>
        <span class="service-tag">$75 first hour · $50/hr after</span>
      </div>

      <div class="service-card">
        <svg class="service-icon" viewBox="0 0 40 40" fill="none" aria-hidden="true">
          <circle cx="20" cy="15" r="6" stroke="currentColor" stroke-width="1.5"/>
          <path d="M10 32c0-5.523 4.477-10 10-10s10 4.477 10 10" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
          <path d="M28 20l4-4m0 0l-2-2m2 2l-2 2" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        <h3>Vendor Referral</h3>
        <p>Out of our area? Need a hardware repair we can't handle remotely? We'll find a reputable local shop, call ahead for pricing, and get you connected to the right help.</p>
        <span class="service-tag">Always Free</span>
      </div>
    </div>

    <div class="callout">
      <svg class="callout-icon" width="20" height="20" viewBox="0 0 20 20" fill="none" aria-hidden="true">
        <path d="M10 2a8 8 0 1 0 0 16A8 8 0 0 0 10 2zm0 4v4m0 4h.01" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
      </svg>
      <div>
        <p class="callout-title">Nonprofits, youth organizations, and community groups</p>
        <p class="callout-body">Ask about free or reduced-rate IT support. Serving the community is part of how we operate.</p>
      </div>
    </div>
  </section>

  <!-- HOURS -->
  <section id="hours" aria-labelledby="hours-heading">
    <p class="section-label">Availability</p>
    <h2 class="section-title" id="hours-heading">Business Hours</h2>
    <p class="section-sub">We keep structured hours so you know when to expect us. After-hours messages are returned within 24 business hours.</p>

    <div class="hours-grid">
      <div class="hours-card">
        <div class="hours-card-head">Weekday Hours</div>
        <table class="hours-table">
          <tbody>
            <tr>
              <td>Monday</td>
              <td>2:00 pm – 5:15 pm</td>
            </tr>
            <tr>
              <td>Tuesday</td>
              <td class="hours-closed">Closed</td>
            </tr>
            <tr>
              <td>Wednesday</td>
              <td>8:00 am – 11:00 am<br>12:00 pm – 5:00 pm</td>
            </tr>
            <tr>
              <td>Thursday</td>
              <td>2:00 pm – 5:15 pm</td>
            </tr>
            <tr>
              <td>Friday</td>
              <td>2:00 pm – 10:00 pm</td>
            </tr>
          </tbody>
        </table>
      </div>

      <div class="hours-card">
        <div class="hours-card-head">Weekend Hours</div>
        <table class="hours-table">
          <tbody>
            <tr>
              <td>Saturday</td>
              <td>By appointment</td>
            </tr>
            <tr>
              <td>Sunday</td>
              <td>By appointment<br><span style="font-size:0.75rem;color:var(--fg-dim)">Closed by 4:00 pm</span></td>
            </tr>
          </tbody>
        </table>
        <div style="padding:20px;border-top:1px solid var(--border)">
          <p class="callout-body" style="margin:0;font-size:0.82rem;">Weekend appointments are available for existing clients and time-sensitive issues. Contact us to schedule.</p>
        </div>
      </div>
    </div>

    <p class="hours-note">
      <svg class="hours-note-icon" width="14" height="14" viewBox="0 0 14 14" fill="none" aria-hidden="true">
        <circle cx="7" cy="7" r="6" stroke="currentColor" stroke-width="1.2"/>
        <path d="M7 4v3l2 2" stroke="currentColor" stroke-width="1.2" stroke-linecap="round"/>
      </svg>
      Phone calls may be returned outside listed hours. Leave a voicemail and we will get back to you on the next business day.
    </p>
  </section>

  <!-- ABOUT -->
  <section id="about" aria-labelledby="about-heading">
    <p class="section-label">Who We Are</p>
    <h2 class="section-title" id="about-heading">Local Tech Help, No Runaround</h2>

    <div class="about-inner">
      <div class="about-body">
        <p>Alchemy Systems IT was built for the Walla Walla Valley. We know what it's like to call a help line and get bounced between departments, or to take a machine to a shop and wait two weeks. That's not how we work.</p>
        <p>You talk to a real person. We tell you what's actually wrong. We tell you what it will actually cost. If we can fix it for free over the phone, we do that first. If we can't help, we say so and find someone who can.</p>
        <p>We serve home users, small businesses, nonprofits, and anyone in between. No job too small.</p>
      </div>

      <div class="about-points">
        <div class="about-point">
          <span class="about-point-check" aria-hidden="true">
            <svg width="10" height="10" viewBox="0 0 10 10" fill="none"><path d="M2 5l2.5 2.5L8 3" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </span>
          <div class="about-point-text">
            <strong>Honest pricing, up front</strong>
            <span>No surprises. You know the rate before we start.</span>
          </div>
        </div>
        <div class="about-point">
          <span class="about-point-check" aria-hidden="true">
            <svg width="10" height="10" viewBox="0 0 10 10" fill="none"><path d="M2 5l2.5 2.5L8 3" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </span>
          <div class="about-point-text">
            <strong>Free first call</strong>
            <span>Phone diagnosis costs nothing. Always.</span>
          </div>
        </div>
        <div class="about-point">
          <span class="about-point-check" aria-hidden="true">
            <svg width="10" height="10" viewBox="0 0 10 10" fill="none"><path d="M2 5l2.5 2.5L8 3" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </span>
          <div class="about-point-text">
            <strong>No contract required</strong>
            <span>Pay per service. Use us when you need us.</span>
          </div>
        </div>
        <div class="about-point">
          <span class="about-point-check" aria-hidden="true">
            <svg width="10" height="10" viewBox="0 0 10 10" fill="none"><path d="M2 5l2.5 2.5L8 3" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </span>
          <div class="about-point-text">
            <strong>We refer if we can't help</strong>
            <span>Hardware we can't fix remotely? We find you someone who can.</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" aria-labelledby="contact-heading">
    <p class="section-label">Reach Us</p>
    <h2 class="section-title" id="contact-heading">Get in Touch</h2>
    <p class="section-sub">Call, email, or use the live chat below. Your first call is always free — no commitment, no pressure.</p>

    <div class="contact-grid">
      <div class="contact-card">
        <p class="contact-card-label">Phone</p>
        <p class="contact-card-value">(XXX) XXX-XXXX</p>
        <p class="contact-card-note">Call or text during business hours. Leave a voicemail after hours.</p>
      </div>
      <div class="contact-card">
        <p class="contact-card-label">Email</p>
        <p class="contact-card-value">alchemysystemsit<wbr>@gmail.com</p>
        <p class="contact-card-note">Response within one business day.</p>
      </div>
    </div>

    <!-- Tawk.to live chat widget goes here -->
    <!-- TAWK_PLACEHOLDER: Replace this comment block with your Tawk.to embed script -->
    <div style="margin-top:24px;padding:20px 24px;background:var(--bg-subtle);border:1px dashed var(--border-hi);border-radius:6px;text-align:center;">
      <p style="margin:0;font-family:'IBM Plex Mono',monospace;font-size:0.78rem;color:var(--fg-dim);">[ Live chat widget loads here — Tawk.to embed coming soon ]</p>
    </div>

  </section>

  <!-- FOOTER -->
  <footer>
    <p class="footer-brand">Alchemy <span>Systems</span> IT</p>
    <p class="footer-copy">Milton-Freewater, OR &nbsp;·&nbsp; Walla Walla Valley &nbsp;·&nbsp; &copy; 2026</p>
  </footer>
</div>

</body></html>
