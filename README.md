<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
<title>Yakkzz Official — Links</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  * { margin:0; padding:0; box-sizing:border-box; -webkit-tap-highlight-color:transparent; }
  html, body { height:100%; }
  body {
    font-family:'Inter', system-ui, sans-serif;
    background: #1a1a1d;
    color:#fff;
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    padding:24px 16px;
    position:relative;
    overflow-x:hidden;
    -webkit-font-smoothing:antialiased;
  }

  /* ===== BACKGROUND GRID ===== */
  .bg-gradient {
    position:fixed;
    inset:0;
    background:
      radial-gradient(circle at 20% 20%, #2a2a30 0%, transparent 55%),
      radial-gradient(circle at 80% 80%, #25252b 0%, transparent 55%),
      linear-gradient(135deg, #141416 0%, #1c1c20 50%, #16161a 100%);
    z-index:0;
  }
  .bg-grid {
    position:fixed;
    inset:-2px;
    background-image:
      linear-gradient(to right, rgba(255,255,255,0.035) 1px, transparent 1px),
      linear-gradient(to bottom, rgba(255,255,255,0.035) 1px, transparent 1px);
    background-size: 48px 48px;
    z-index:1;
    animation: gridShift 40s linear infinite;
    pointer-events:none;
  }
  @keyframes gridShift {
    0%   { background-position: 0 0, 0 0; }
    100% { background-position: 48px 48px, 48px 48px; }
  }
  .bg-vignette {
    position:fixed;
    inset:0;
    background: radial-gradient(circle at center, transparent 30%, rgba(0,0,0,0.55) 100%);
    z-index:2;
    pointer-events:none;
  }

  /* ===== CARD ===== */
  .card {
    position:relative;
    z-index:10;
    width:100%;
    max-width: 460px;
    background: rgba(38, 38, 44, 0.55);
    border: 1px solid rgba(200, 200, 210, 0.14);
    border-radius: 24px;
    padding: 32px 24px 24px;
    backdrop-filter: blur(18px);
    -webkit-backdrop-filter: blur(18px);
    box-shadow:
      0 20px 60px rgba(0,0,0,0.55),
      0 0 0 1px rgba(255,255,255,0.03) inset,
      0 1px 0 rgba(255,255,255,0.06) inset;
    animation: cardIn 0.7s cubic-bezier(0.16, 1, 0.3, 1) both;
  }
  @keyframes cardIn {
    from { opacity:0; transform: translateY(24px) scale(0.97); }
    to   { opacity:1; transform: translateY(0) scale(1); }
  }

  /* ===== PROFILE ===== */
  .profile {
    display:flex;
    flex-direction:column;
    align-items:center;
    text-align:center;
    margin-bottom: 26px;
  }
  .avatar-wrap {
    position:relative;
    width:104px;
    height:104px;
    margin-bottom:16px;
  }
  .avatar-ring {
    position:absolute;
    inset:-4px;
    border-radius:50%;
    background: conic-gradient(from 180deg, #8a8a94, #d4d4dc, #6c6c76, #b8b8c2, #8a8a94);
    animation: spinRing 8s linear infinite;
    opacity:0.55;
  }
  @keyframes spinRing {
    to { transform: rotate(360deg); }
  }
  .avatar-ring::after {
    content:'';
    position:absolute;
    inset:2px;
    border-radius:50%;
    background: #1c1c20;
  }
  .avatar {
    position:relative;
    width:100%;
    height:100%;
    border-radius:50%;
    object-fit:cover;
    border: 3px solid rgba(40,40,46,0.9);
    display:block;
    z-index:1;
  }
  .name {
    font-size: 22px;
    font-weight: 800;
    letter-spacing: -0.02em;
    background: linear-gradient(180deg, #ffffff, #c8c8d0);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
  }
  .username {
    font-size: 13.5px;
    color: #9a9aa6;
    font-weight: 500;
    margin-top: 4px;
  }
  .username::before { content:'@'; opacity:0.7; }
  .bio {
    font-size: 13px;
    line-height: 1.6;
    color: #b8b8c2;
    margin-top: 14px;
    max-width: 340px;
    font-weight: 400;
  }

  /* ===== DIVIDER ===== */
  .divider {
    height:1px;
    background: linear-gradient(to right, transparent, rgba(200,200,210,0.16), transparent);
    margin: 22px 0 18px;
  }

  /* ===== LINKS ===== */
  .links {
    display:flex;
    flex-direction:column;
    gap:12px;
  }
  .link-btn {
    display:flex;
    align-items:center;
    gap:14px;
    width:100%;
    padding: 15px 18px;
    background: linear-gradient(180deg, rgba(58,58,66,0.7), rgba(42,42,48,0.7));
    border: 1px solid rgba(200,200,210,0.12);
    border-radius: 16px;
    color:#ececf1;
    text-decoration:none;
    font-size: 14px;
    font-weight: 600;
    letter-spacing: -0.01em;
    transition: transform .22s cubic-bezier(0.16,1,0.3,1), background .22s ease, border-color .22s ease, box-shadow .22s ease;
    position:relative;
    overflow:hidden;
    cursor:pointer;
  }
  .link-btn::before {
    content:'';
    position:absolute;
    inset:0;
    background: linear-gradient(120deg, transparent 30%, rgba(255,255,255,0.07) 50%, transparent 70%);
    transform: translateX(-100%);
    transition: transform .6s ease;
    pointer-events:none;
  }
  .link-btn:hover::before { transform: translateX(100%); }
  .link-btn:hover {
    transform: translateY(-2px) scale(1.015);
    background: linear-gradient(180deg, rgba(72,72,82,0.85), rgba(52,52,60,0.85));
    border-color: rgba(220,220,230,0.22);
    box-shadow: 0 10px 26px rgba(0,0,0,0.4), 0 0 0 1px rgba(255,255,255,0.05) inset;
  }
  .link-btn:active { transform: translateY(0) scale(0.995); }
  .link-icon {
    width: 38px;
    height: 38px;
    flex-shrink:0;
    border-radius: 11px;
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.07);
    display:flex;
    align-items:center;
    justify-content:center;
    transition: background .22s ease;
  }
  .link-btn:hover .link-icon { background: rgba(255,255,255,0.11); }
  .link-icon svg { width:19px; height:19px; }
  .link-text {
    flex:1;
    display:flex;
    flex-direction:column;
    gap:2px;
    text-align:left;
  }
  .link-title { font-size:14px; font-weight:600; color:#f0f0f4; line-height:1.2; }
  .link-sub { font-size:11.5px; font-weight:400; color:#8e8e9a; line-height:1.2; }
  .link-arrow {
    opacity:0.35;
    transition: opacity .22s ease, transform .22s ease;
    flex-shrink:0;
  }
  .link-btn:hover .link-arrow { opacity:0.75; transform: translateX(2px); }

  /* ===== FOOTER ===== */
  .footer {
    text-align:center;
    margin-top: 22px;
    font-size: 11.5px;
    color: #6a6a76;
    font-weight: 500;
    letter-spacing: 0.02em;
  }
  .footer-dot { opacity:0.5; margin: 0 6px; }

  /* ===== RESPONSIVE ===== */
  @media (max-width: 480px) {
    body { padding: 20px 14px; align-items: flex-start; }
    .card { padding: 28px 18px 20px; border-radius: 22px; }
    .avatar-wrap { width:92px; height:92px; }
    .name { font-size:20px; }
    .bio { font-size:12.5px; }
    .link-btn { padding: 14px 15px; gap:12px; }
    .link-icon { width:36px; height:36px; border-radius:10px; }
    .link-title { font-size:13.5px; }
    .link-sub { font-size:11px; }
  }
  @media (min-width: 768px) {
    .card { padding: 40px 32px 28px; }
    .avatar-wrap { width:116px; height:116px; }
    .name { font-size:24px; }
  }
</style>
</head>
<body>

<div class="bg-gradient"></div>
<div class="bg-grid"></div>
<div class="bg-vignette"></div>

<main class="card">

  <!-- PROFILE -->
  <section class="profile">
    <div class="avatar-wrap">
      <div class="avatar-ring"></div>
      <img
        class="avatar"
        src="https://files.catbox.moe/r5awec.png"
        alt="Yakkzz Official"
        onerror="this.style.background='linear-gradient(135deg,#3a3a42,#22222a)'; this.src='data:image/svg+xml;utf8,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text x=%2250%22 y=%2268%22 font-size=%2250%22 text-anchor=%22middle%22 fill=%22%23999%22 font-family=%22Inter%22 font-weight=%22700%22>Y</text></svg>';"
      />
    </div>
    <h1 class="name">Yakkzz Official</h1>
    <p class="username">yakkzzstore</p>
    <p class="bio">
      HAI KENALIN AKU ADALAH YAKKZZSTORE PENJUAL AKUN FF,ML DAN OPEN JOKI ROBLOX. TESTI AKU SUDA NYAMPE 350 DI JAMIN TRUST, JANGAN LUPA SV NO AKU YAA
    </p>
  </section>

  <div class="divider"></div>

  <!-- LINKS -->
  <section class="links">

    <!-- INSTAGRAM -->
    <a class="link-btn" href="https://www.instagram.com/arrrryaaa.brr" target="_blank" rel="noopener">
      <span class="link-icon" style="color:#e1306c;">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="2" y="2" width="20" height="20" rx="5" ry="5"/>
          <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/>
          <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/>
        </svg>
      </span>
      <span class="link-text">
        <span class="link-title">Instagram</span>
        <span class="link-sub">@arrrryaaa.brr</span>
      </span>
      <span class="link-arrow">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 18l6-6-6-6"/></svg>
      </span>
    </a>

    <!-- TIKTOK -->
    <a class="link-btn" href="https://www.tiktok.com/@bang_aryaa1" target="_blank" rel="noopener">
      <span class="link-icon" style="color:#eaeaea;">
        <svg viewBox="0 0 24 24" fill="currentColor">
          <path d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 0 1-5.2 1.74 2.89 2.89 0 0 1 2.31-4.64 2.93 2.93 0 0 1 .88.13V9.4a6.84 6.84 0 0 0-1-.05A6.33 6.33 0 0 0 5.8 20.1a6.34 6.34 0 0 0 10.86-4.43v-7a8.16 8.16 0 0 0 4.77 1.52v-3.4a4.85 4.85 0 0 1-1.84-.1z"/>
        </svg>
      </span>
      <span class="link-text">
        <span class="link-title">TikTok</span>
        <span class="link-sub">@bang_aryaa1</span>
      </span>
      <span class="link-arrow">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 18l6-6-6-6"/></svg>
      </span>
    </a>

    <!-- WHATSAPP KONTAK -->
    <a class="link-btn" href="https://wa.me/+62895622759784" target="_blank" rel="noopener">
      <span class="link-icon" style="color:#25d366;">
        <svg viewBox="0 0 24 24" fill="currentColor">
          <path d="M17.47 14.38c-.3-.15-1.76-.87-2.03-.97-.27-.1-.47-.15-.67.15-.2.3-.77.97-.94 1.17-.17.2-.35.22-.65.07-.3-.15-1.26-.46-2.4-1.48-.89-.79-1.49-1.77-1.66-2.07-.17-.3-.02-.46.13-.61.13-.13.3-.35.45-.52.15-.17.2-.3.3-.5.1-.2.05-.37-.02-.52-.07-.15-.67-1.62-.92-2.22-.24-.58-.49-.5-.67-.51l-.57-.01c-.2 0-.52.07-.79.37-.27.3-1.04 1.02-1.04 2.48 0 1.46 1.07 2.88 1.22 3.08.15.2 2.1 3.2 5.08 4.49.71.31 1.26.49 1.69.62.71.23 1.36.19 1.87.12.57-.09 1.76-.72 2.01-1.41.25-.7.25-1.29.17-1.42-.07-.13-.27-.2-.57-.35zM12.05 21.5h-.01a9.4 9.4 0 0 1-4.79-1.31l-.34-.2-3.56.93.95-3.47-.22-.36a9.38 9.38 0 0 1-1.44-5.02c0-5.19 4.23-9.41 9.42-9.41 2.52 0 4.88.98 6.66 2.76a9.35 9.35 0 0 1 2.76 6.66c0 5.19-4.23 9.42-9.43 9.42zm8.01-17.43A11.36 11.36 0 0 0 12.05 0.75C5.79.75.69 5.85.69 12.11c0 2 .52 3.95 1.52 5.68L.6 23.25l5.59-1.47a11.35 11.35 0 0 0 5.86 1.6h.01c6.26 0 11.36-5.1 11.36-11.36 0-3.04-1.18-5.89-3.33-8.03z"/>
        </svg>
      </span>
      <span class="link-text">
        <span class="link-title">WhatsApp</span>
        <span class="link-sub">Chat / Order</span>
      </span>
      <span class="link-arrow">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 18l6-6-6-6"/></svg>
      </span>
    </a>

    <!-- LINK TAMBAHAN 1 -->
    <a class="link-btn" href="https://whatsapp.com/channel/0029VbAVjDXHgZWVGTVHH30r" target="_blank" rel="noopener">
      <span class="link-icon" style="color:#25d366;">
        <svg viewBox="0 0 24 24" fill="currentColor">
          <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 15v-4H8l4-7v4h3l-4 7z"/>
        </svg>
      </span>
      <span class="link-text">
        <span class="link-title">Channel SL Yakkzz DKK</span>
        <span class="link-sub">Info & Testi</span>
      </span>
      <span class="link-arrow">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 18l6-6-6-6"/></svg>
      </span>
    </a>

    <!-- LINK TAMBAHAN 2 -->
    <a class="link-btn" href="https://whatsapp.com/channel/0029VbCrUP5JUM2bTRtxgA1S" target="_blank" rel="noopener">
      <span class="link-icon" style="color:#25d366;">
        <svg viewBox="0 0 24 24" fill="currentColor">
          <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 15v-4H8l4-7v4h3l-4 7z"/>
        </svg>
      </span>
      <span class="link-text">
        <span class="link-title">Cek Keamanan</span>
        <span class="link-sub">Bukti Testi</span>
      </span>
      <span class="link-arrow">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 18l6-6-6-6"/></svg>
      </span>
    </a>

  </section>

  <!-- FOOTER -->
  <div class="footer">
    © 2026 yakkzzstore
  </div>

</main>

</body>
</html>
