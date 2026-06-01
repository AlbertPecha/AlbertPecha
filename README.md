<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Albert Pecharromán – Profile</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --blue: #0A66C2;
      --blue-light: #E8F0FA;
      --blue-mid: #B5D4F4;
      --text: #1a1a1a;
      --text-muted: #555;
      --text-faint: #888;
      --border: rgba(0,0,0,0.09);
      --bg: #ffffff;
      --surface: #f7f7f5;
      --radius: 12px;
      --radius-sm: 8px;
    }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      align-items: flex-start;
      justify-content: center;
      padding: 3rem 1.5rem;
    }

    .card {
      width: 100%;
      max-width: 640px;
      background: var(--bg);
      border: 1px solid var(--border);
      border-radius: 18px;
      overflow: hidden;
      box-shadow: 0 2px 24px rgba(0,0,0,0.06);
      animation: fadeUp 0.5s ease both;
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(16px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* ── Top stripe ── */
    .stripe {
      height: 6px;
      background: linear-gradient(90deg, #0A66C2 0%, #06B6D4 55%, #10B981 100%);
    }

    /* ── Header ── */
    .header {
      padding: 2rem 2rem 1.25rem;
      display: flex;
      align-items: flex-start;
      gap: 1.25rem;
    }

    .avatar {
      width: 68px;
      height: 68px;
      border-radius: 50%;
      background: var(--blue-light);
      border: 2px solid var(--blue-mid);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'DM Mono', monospace;
      font-size: 18px;
      font-weight: 500;
      color: var(--blue);
      flex-shrink: 0;
      letter-spacing: -0.5px;
    }

    .header-text { flex: 1; }

    .location {
      display: flex;
      align-items: center;
      gap: 4px;
      font-size: 12px;
      color: var(--text-faint);
      margin-bottom: 5px;
      font-family: 'DM Mono', monospace;
      letter-spacing: 0.04em;
    }

    .location svg { flex-shrink: 0; }

    h1 {
      font-size: 20px;
      font-weight: 600;
      color: var(--text);
      line-height: 1.25;
      margin-bottom: 8px;
    }

    .bio {
      font-size: 14px;
      color: var(--text-muted);
      line-height: 1.65;
    }

    /* ── Divider ── */
    .divider {
      height: 1px;
      background: var(--border);
      margin: 0 2rem;
    }

    /* ── Section ── */
    .section {
      padding: 1.25rem 2rem;
    }

    .section-label {
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--text-faint);
      font-family: 'DM Mono', monospace;
      margin-bottom: 0.75rem;
    }

    /* ── Skills ── */
    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 7px;
    }

    .chip {
      display: flex;
      align-items: center;
      gap: 6px;
      padding: 5px 11px;
      border-radius: 20px;
      border: 1px solid var(--border);
      background: var(--surface);
      font-size: 13px;
      font-weight: 500;
      color: var(--text);
      transition: border-color 0.15s, background 0.15s;
    }

    .chip:hover {
      border-color: rgba(0,0,0,0.18);
      background: #f0f0ee;
    }

    .dot {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      flex-shrink: 0;
    }

    /* ── Links ── */
    .links {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
      gap: 8px;
    }

    .link-card {
      display: flex;
      align-items: center;
      gap: 9px;
      padding: 9px 12px;
      border-radius: var(--radius-sm);
      border: 1px solid var(--border);
      background: var(--bg);
      text-decoration: none;
      color: var(--text);
      font-size: 13px;
      font-weight: 500;
      transition: background 0.15s, border-color 0.15s, transform 0.12s;
    }

    .link-card:hover {
      background: var(--surface);
      border-color: rgba(0,0,0,0.15);
      transform: translateY(-1px);
    }

    .link-icon {
      width: 28px;
      height: 28px;
      border-radius: 6px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
    }

    .link-icon svg { display: block; }

    /* ── Footer ── */
    .footer {
      padding: 1rem 2rem 1.5rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .footer-mono {
      font-family: 'DM Mono', monospace;
      font-size: 11px;
      color: var(--text-faint);
    }

    .open-to-work {
      display: flex;
      align-items: center;
      gap: 6px;
      font-size: 12px;
      color: #10B981;
      font-weight: 500;
    }

    .open-dot {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: #10B981;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.4; }
    }
  </style>
</head>
<body>

<div class="card">
  <div class="stripe"></div>

  <!-- Header -->
  <div class="header">
    <div class="avatar">AP</div>
    <div class="header-text">
      <p class="location">
        <svg width="11" height="11" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M21 10c0 7-9 13-9 13S3 17 3 10a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
        Barcelona, Spain 🇪🇸
      </p>
      <h1>Hi! My name is Albert Pecharromán</h1>
      <p class="bio">Passionate developer focused on building clean and efficient digital solutions. I care about well-structured code and modern, responsive interfaces.</p>
    </div>
  </div>

  <div class="divider"></div>

  <!-- Technologies -->
  <div class="section">
    <p class="section-label">Technologies</p>
    <div class="skills">
      <div class="chip"><span class="dot" style="background:#F7DF1E;outline:1px solid #d4bc00;outline-offset:0"></span>JavaScript</div>
      <div class="chip"><span class="dot" style="background:#3776AB"></span>Python</div>
      <div class="chip"><span class="dot" style="background:#E34F26"></span>HTML5</div>
      <div class="chip"><span class="dot" style="background:#1572B6"></span>CSS3</div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- Connect -->
  <div class="section">
    <p class="section-label">Connect</p>
    <div class="links">

      <a class="link-card" href="https://www.linkedin.com/in/albert-pecharroman-vilamitjana/" target="_blank">
        <div class="link-icon" style="background:#0A66C2">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="white"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z"/><circle cx="4" cy="4" r="2" fill="white"/></svg>
        </div>
        LinkedIn
      </a>

      <a class="link-card" href="https://www.instagram.com/albertpecha" target="_blank">
        <div class="link-icon" style="background:#E4405F">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="2" width="20" height="20" rx="5"/><path d="M16 11.37A4 4 0 1112.63 8 4 4 0 0116 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
        </div>
        Instagram
      </a>

      <a class="link-card" href="mailto:albertpecharromanvilamitjana@gmail.com">
        <div class="link-icon" style="background:#EA4335">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        </div>
        Gmail
      </a>

      <a class="link-card" href="https://discordapp.com/users/337181042796101633" target="_blank">
        <div class="link-icon" style="background:#5865F2">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="white"><path d="M20.317 4.37a19.791 19.791 0 00-4.885-1.515.074.074 0 00-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 00-5.487 0 12.64 12.64 0 00-.617-1.25.077.077 0 00-.079-.037A19.736 19.736 0 003.677 4.37a.07.07 0 00-.032.027C.533 9.046-.32 13.58.099 18.057a.082.082 0 00.031.057 19.9 19.9 0 005.993 3.03.078.078 0 00.084-.028c.462-.63.874-1.295 1.226-1.994a.076.076 0 00-.041-.106 13.107 13.107 0 01-1.872-.892.077.077 0 01-.008-.128 10.2 10.2 0 00.372-.292.074.074 0 01.077-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 01.078.01c.12.098.246.198.373.292a.077.077 0 01-.006.127 12.299 12.299 0 01-1.873.892.077.077 0 00-.041.107c.36.698.772 1.362 1.225 1.993a.076.076 0 00.084.028 19.839 19.839 0 006.002-3.03.077.077 0 00.032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 00-.031-.03z"/></svg>
        </div>
        Discord
      </a>

    </div>
  </div>

  <!-- Footer -->
  <div class="footer">
    <span class="footer-mono">albert-pecharroman.dev</span>
    <div class="open-to-work">
      <span class="open-dot"></span>
      Open to work
    </div>
  </div>
</div>

</body>
</html>
