
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Storm Lounge | Home</title>
  <meta name="description" content="Storm Lounge — a friendly Discord community for creators. Assets, tools, and learning resources for Unreal/UEFN, game dev, and more." />
  <meta name="theme-color" content="#6d28d9" />
  <!-- Pure HTML/CSS. No frameworks. Drop this in your repo as index.html for GitHub Pages. -->
  <style>
    :root{
      --bg:#0b0f1a; --panel:#121628; --panel2:#1a1f35; --ink:#eef2ff; --muted:#b8c1ec; --brand:#7c3aed; --brand2:#6366f1; --line:#232841;
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{margin:0; font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji"; color:var(--ink); background:radial-gradient(1000px 600px at 20% -10%, rgba(124,58,237,.18), transparent 60%), radial-gradient(800px 500px at 120% 10%, rgba(99,102,241,.14), transparent 60%), linear-gradient(180deg,var(--bg),#0a0d18);}    
    a{color:#c7b8ff; text-decoration:none}
    a:hover{color:white}
    .container{max-width:1100px; margin-inline:auto; padding:0 1.25rem}

    /* Header */
    header{position:sticky; top:0; z-index:50; backdrop-filter:saturate(1.1) blur(8px); background:rgba(18,22,40,.7); border-bottom:1px solid var(--line)}
    .nav{display:flex; justify-content:space-between; align-items:center; padding:0.9rem 0}
    .brand{display:flex; align-items:center; gap:.6rem; font-weight:800; letter-spacing:.3px}
    .badge{display:inline-flex; width:32px; height:32px; align-items:center; justify-content:center; border-radius:10px; background:linear-gradient(135deg,var(--brand),var(--brand2));}
    .links{display:flex; gap:1rem; align-items:center}
    .links a{color:#cbd5e1}
    .links a:hover{color:white}
    .cta{padding:.55rem .9rem; border-radius:.75rem; background:var(--brand); color:white}
    .cta:hover{background:#6d28d9}
    .hamburger{display:none; width:40px; height:40px; border-radius:.6rem; background:#ffffff10; border:1px solid #ffffff20; color:#e2e8f0}

    /* Mobile menu */
    #mobile{display:none; border-top:1px solid var(--line); background:var(--panel)}
    #mobile a{display:block; padding:0.9rem 1rem; border-bottom:1px solid #ffffff10; color:#d1d5db}
    #mobile a:last-child{border-bottom:0}

    /* Hero */
