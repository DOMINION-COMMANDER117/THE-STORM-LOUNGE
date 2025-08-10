<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Storm Lounge — Home</title>
  <meta name="description" content="Storm Lounge: a calm, creator‑friendly Discord hub. Assets, tools, and guides for Unreal/UEFN and game dev." />
  <meta name="theme-color" content="#0d1117" />
  <!-- Pure HTML + CSS. Drop this file in your repo as index.html for GitHub Pages. -->
  <style>
    :root{
      --bg:#0d1117;       /* GitHub dark */
      --panel:#0b0f1a;    /* slightly darker */
      --card:#111826;     /* card surface */
      --ink:#e6edf3;      /* text */
      --muted:#8b949e;    /* secondary text */
      --brand:#7c3aed;    /* violet */
      --brand-2:#6366f1;  /* indigo */
      --line:#1f2430;     /* borders */
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{margin:0; color:var(--ink); background:radial-gradient(1200px 600px at -10% -20%, rgba(124,58,237,.12), transparent 60%),radial-gradient(900px 600px at 120% -10%, rgba(99,102,241,.10), transparent 55%), linear-gradient(180deg,var(--bg), #0b1220);}    
    a{color:#b4b9ff; text-decoration:none}
    a:hover{color:#fff}
    .container{max-width:1180px; margin-inline:auto; padding:0 20px}

    /* ===== NAV ===== */
    header{position:sticky; top:0; z-index:10; backdrop-filter:saturate(1.1) blur(8px); background:rgba(13,17,23,.72); border-bottom:1px solid var(--line)}
    .nav{display:flex; gap:16px; align-items:center; justify-content:space-between; padding:14px 0}
    .brand{display:flex; align-items:center; gap:10px; font-weight:800; letter-spacing:.2px}
    .badge{display:inline-grid; place-items:center; width:34px; height:34px; border-radius:10px; background:linear-gradient(135deg,var(--brand),var(--brand-2)); box-shadow:0 6px 24px rgba(124,58,237,.35)}
    .links{display:flex; gap:18px; align-items:center}
    .links a{color:#c5d0dd}
    .links a:hover{color:#fff}
    .btn{display:inline-block; padding:10px 14px; border-radius:10px; border:1px solid #ffffff20; background:#ffffff10; color:var(--ink); font-weight:600}
    .btn:hover{background:#ffffff18}
    .btn-primary{background:var(--brand); border-color:transparent; color:#fff}
    .btn-primary:hover{background:#6d28d9}
    .hamburger{display:none; width:42px; height:42px; border-radius:10px; background:#ffffff10; border:1px solid #ffffff20; color:#d0d7de}

    /* ===== HERO ===== */
    .hero{position:relative; border-bottom:1px solid var(--line)}
    .hero-wrap{display:grid; grid-template-columns:1.2fr .8fr; gap:40px; padding:72px 0}
    .eyebrow{color:#c7b8ff; letter-spacing:.14em; text-transform:uppercase; font-size:12px}
    h1{font-size: clamp(36px, 6vw, 64px); line-height:1.05; margin:10px 0 12px}
    .lead{color:var(--muted); font-size: clamp(16px, 2vw, 20px); max-width:680px}
    .cta-row{display:flex; flex-wrap:wrap; gap:12px; margin-top:22px}
    .input{display:flex; gap:10px; background:#0a1220; border:1px solid #1c2230; padding:8px; border-radius:12px; width:min(520px,100%)}
    .input input{flex:1; padding:10px 12px; border:0; outline:0; background:transparent; color:#e6edf3}
    .art{align-self:center; border:1px solid #22283a; border-radius:16px; background:radial-gradient(650px 300px at 80% 10%, rgba(99,102,241,.15), transparent 60%), radial-gradient(500px 280px at 15% 80%, rgba(124,58,237,.18), transparent 55%), linear-gradient(180deg,#0b1220,#0b0f1a); min-height:280px; display:grid; place-items:center}
    .art .glyph{font-size:56px; filter:drop-shadow(0 8px 30px rgba(124,58,237,.55))}

    /* ===== SECTION ===== */
    section{padding:56px 0; border-bottom:1px solid var(--line)}
    h2{font-size:28px; margin:0 0 8px}
    .cards{display:grid; grid-template-columns:repeat(auto-fit,minmax(240px,1fr)); gap:16px; margin-top:16px}
    .card{background:var(--card); border:1px solid var(--line); padding:18px; border-radius:14px}
    .card h3{margin:4px 0 6px}
    .muted{color:var(--muted)}

    /* ===== FOOTER ===== */
    footer{background:#0b0f1a; color:#9fb0c3; text-align:center; padding:22px 16px}

    /* ===== RESPONSIVE ===== */
    @media (max-width: 900px){
      .links{display:none}
      .hamburger{display:inline-grid; place-items:center}
      .hero-wrap{grid-template-columns:1fr; gap:28px; padding:56px 0}
      .art{min-height:220px}
    }
  </style>
</head>
<body>
  <!-- ===== NAV ===== -->
  <header>
    <div class="container nav">
      <div class="brand">
        <span class="badge" aria-hidden>⚡</span>
        <span>Storm Lounge</span>
      </div>
      <nav class="links" aria-label="Primary">
        <a href="#about">About</a>
        <a href="#provide">What We Provide</a>
        <a href="#assets">Assets</a>
        <a href="#links">Links</a>
        <a class="btn-primary" href="REPLACE_WITH_DISCORD_INVITE">Join</a>
      </nav>
      <button class="hamburger" aria-label="Menu">☰</button>
    </div>
  </header>

  <!-- ===== HERO ===== -->
  <section class="hero">
    <div class="container hero-wrap">
      <div>
        <div class="eyebrow">Welcome</div>
        <h1>Build in the storm.</h1>
        <p class="lead">Harnessed for productivity. Designed for collaboration. A calm home for Unreal/UEFN creators. Welcome to the Storm Lounge community.</p>
        <div class="cta-row">
          <div class="input" role="group" aria-label="Join form">
            <input placeholder="Email address (optional)" />
            <a class="btn-primary" href="REPLACE_WITH_DISCORD_INVITE">Join Discord</a>
          </div>
          <a class="btn" href="REPLACE_WITH_REPO_URL">View the GitHub repo →</a>
        </div>
      </div>
      <div class="art" aria-hidden>
        <div class="glyph">🌩️</div>
      </div>
    </div>
  </section>

  <!-- ===== ABOUT ===== -->
  <section id="about">
    <div class="container">
      <h2>About this place</h2>
      <p class="muted">Storm Lounge is a focused, friendly space to learn, share, and ship. Clear rules, good vibes, and practical help—without the noise.</p>
      <div class="cards">
        <div class="card"><h3>Respect & Safety</h3><p class="muted">Moderated channels, ticket support, zero tolerance for harassment.</p></div>
        <div class="card"><h3>Constructive Feedback</h3><p class="muted">Map reviews, material tips, Verse/Blueprint help.</p></div>
        <div class="card"><h3>Learn by Doing</h3><p class="muted">Short guides, examples, and templates you can remix.</p></div>
      </div>
    </div>
  </section>

  <!-- ===== PROVIDE ===== -->
  <section id="provide">
    <div class="container">
      <h2>What we provide</h2>
      <div class="cards">
        <div class="card"><h3>Curated Assets</h3><p class="muted">Materials, textures, UI kits, and code snippets with usage notes.</p></div>
        <div class="card"><h3>Tools & Templates</h3><p class="muted">Project starters, Niagara presets, and CLI helpers.</p></div>
        <div class="card"><h3>Guides & Help</h3><p class="muted">Step‑by‑step write‑ups and friendly Q&A in Discord.</p></div>
      </div>
    </div>
  </section>

  <!-- ===== ASSETS ===== -->
  <section id="assets">
    <div class="container">
      <h2>Assets</h2>
      <p class="muted">A tidy, growing library with clear categories and notes.</p>
      <div class="cards">
        <div class="card"><h3>Materials</h3><p class="muted">Landscape blends, stylized metal, storm FX.</p></div>
        <div class="card"><h3>Textures</h3><p class="muted">Noise packs, tilers, decals (with ORM + normals where applicable).</p></div>
        <div class="card"><h3>Code</h3><p class="muted">Verse utilities, blueprint macros, helpers.</p></div>
        <div class="card"><h3>UI / HUD</h3><p class="muted">Scoreboards, badges, icon sets (SVG + PNG).</p></div>
      </div>
      <p style="margin-top:10px"><a class="btn" href="REPLACE_WITH_ASSETS_FOLDER">Browse assets folder →</a></p>
      <p class="muted" style="margin-top:6px"><small>Please review included licenses and follow Epic/UEFN ToS.</small></p>
    </div>
  </section>

  <!-- ===== LINKS ===== -->
  <section id="links">
    <div class="container">
      <h2>Quick links</h2>
      <div class="cards">
        <a class="card" href="REPLACE_WITH_DISCORD_INVITE"><h3>Discord</h3><p class="muted">Announcements, help, and chat.</p></a>
        <a class="card" href="REPLACE_WITH_REPO_URL"><h3>GitHub Repo</h3><p class="muted">Source, packs, and issues.</p></a>
        <a class="card" href="REPLACE_WITH_GUIDES_URL"><h3>Guides</h3><p class="muted">Step‑by‑step tutorials & checklists.</p></a>
      </div>
    </div>
  </section>

  <!-- ===== FOOTER ===== -->
  <footer>
    <div class="container">© <span id="y"></span> Storm Lounge — Built with ❤ for creators.</div>
  </footer>

  <script>
    // Set year
    document.getElementById('y').textContent = new Date().getFullYear();
  </script>
</body>
</html>
