<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Storm Lounge | Home</title>
  <meta name="description" content="Storm Lounge — a friendly Discord community for creators. Assets, tools, and learning resources for Unreal/UEFN, game dev, and more." />
  <meta property="og:title" content="Storm Lounge — Home" />
  <meta property="og:description" content="A warm, creator-friendly hub for assets, tools, and help." />
  <meta property="og:type" content="website" />
  <meta name="theme-color" content="#6D28D9" />
  
  <!-- Tailwind CSS via CDN for a simple GitHub Pages setup -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    // Tailwind config tweaks
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: { display: ['Inter', 'ui-sans-serif', 'system-ui'], body: ['Inter', 'ui-sans-serif', 'system-ui'] },
          colors: { storm: { 50:'#f5f3ff', 200:'#ddd6fe', 400:'#a78bfa', 600:'#7c3aed', 700:'#6d28d9', 900:'#1f1441' } },
          boxShadow: { soft: '0 10px 30px rgba(0,0,0,0.25)' },
          backgroundImage: {
            stormy: 'radial-gradient(1200px 600px at 20% -10%, rgba(124,58,237,.25), transparent 60%), radial-gradient(1000px 600px at 120% 10%, rgba(59,130,246,.18), transparent 60%), linear-gradient(180deg, #0b1020, #0b0f1a)'
          }
        }
      }
    }
  </script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
</head>
<body class="font-body text-slate-100 bg-stormy min-h-screen selection:bg-storm-600/60 selection:text-white">
  <!-- Nav -->
  <header class="sticky top-0 z-50 backdrop-blur supports-[backdrop-filter]:bg-slate-900/40 bg-slate-900/60 border-b border-white/10">
    <div class="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
      <a href="#home" class="flex items-center gap-2 group">
        <span aria-hidden class="inline-flex h-8 w-8 rounded-xl bg-gradient-to-br from-violet-500 to-indigo-600 shadow-soft items-center justify-center">⚡</span>
        <span class="font-display font-semibold tracking-wide group-hover:text-white/90">Storm Lounge</span>
      </a>
      <nav class="hidden md:flex items-center gap-6 text-sm">
        <a href="#about" class="hover:text-white">About</a>
        <a href="#provide" class="hover:text-white">What We Provide</a>
        <a href="#assets" class="hover:text-white">Assets</a>
        <a href="#tools" class="hover:text-white">Tools</a>
        <a href="#links" class="hover:text-white">Links</a>
        <a href="#join" class="inline-flex items-center gap-2 px-3 py-1.5 rounded-lg bg-violet-600 hover:bg-violet-500 transition shadow-soft">Join</a>
      </nav>
      <button id="menuBtn" class="md:hidden inline-flex items-center justify-center h-10 w-10 rounded-lg bg-white/5 hover:bg-white/10">☰</button>
    </div>
    <div id="mobileMenu" class="md:hidden hidden border-t border-white/10">
      <div class="px-4 py-3 grid gap-2 text-sm">
        <a class="py-2" href="#about">About</a>
        <a class="py-2" href="#provide">What We Provide</a>
        <a class="py-2" href="#assets">Assets</a>
        <a class="py-2" href="#tools">Tools</a>
        <a class="py-2" href="#links">Links</a>
        <a class="py-2" href="#join">Join</a>
      </div>
    </div>
  </header>

  <!-- Hero -->
  <section id="home" class="relative overflow-hidden">
    <div class="max-w-6xl mx-auto px-4 py-20 md:py-28">
      <div class="grid md:grid-cols-2 items-center gap-10">
        <div>
          <p class="text-violet-300/90 font-medium uppercase tracking-widest">Welcome</p>
          <h1 class="mt-3 font-display text-4xl md:text-5xl font-extrabold leading-tight">
            A warm place in the storm for creators
          </h1>
          <p class="mt-4 text-slate-300/90 leading-relaxed max-w-xl">
            Storm Lounge is a friendly Discord hub for builders, designers, and game devs. Share and discover assets, swap tips, test ideas, and get help—without the drama.
          </p>
          <div class="mt-6 flex flex-wrap gap-3">
            <a href="#join" class="px-5 py-3 rounded-xl bg-violet-600 hover:bg-violet-500 font-semibold shadow-soft">Join the Discord</a>
            <a href="#assets" class="px-5 py-3 rounded-xl bg-white/10 hover:bg-white/20 font-semibold">Browse Assets</a>
            <a href="#links" class="px-5 py-3 rounded-xl bg-white/10 hover:bg-white/20 font-semibold">Quick Links</a>
          </div>
        </div>
        <div class="relative">
          <div class="aspect-[4/3] rounded-2xl bg-gradient-to-br from-indigo-500/20 via-fuchsia-500/20 to-violet-600/20 border border-white/10 p-1">
            <div class="h-full w-full rounded-xl bg-[radial-gradient(ellipse_at_top_right,rgba(99,102,241,0.35),transparent_40%),radial-gradient(ellipse_at_bottom_left,rgba(236,72,153,0.35),transparent_45%)] flex items-center justify-center">
              <div class="text-center p-8">
                <div class="text-6xl">🌩️</div>
                <p class="mt-4 text-lg text-slate-200">“Ride the storm. Build something great.”</p>
                <p class="mt-2 text-sm text-slate-400">UEFN • Unreal • Blender • Game Design • Community</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="border-t border-white/10">
    <div class="max-w-6xl mx-auto px-4 py-16">
      <div class="grid md:grid-cols-3 gap-10">
        <div class="md:col-span-1">
          <h2 class="text-2xl font-bold">About this place</h2>
          <p class="mt-2 text-slate-300">Clear rules, good vibes, and practical help for creators.</p>
        </div>
        <div class="md:col-span-2 grid gap-6">
          <p class="text-slate-300/95">We built Storm Lounge so creators have a calm, focused space to learn, collaborate, and level up. Whether you’re prototyping in UEFN, sculpting in Blender, or tuning materials in Unreal, you’ll find support here.</p>
          <ul class="grid sm:grid-cols-2 gap-4">
            <li class="p-5 rounded-xl bg-white/5 border border-white/10">
              <h3 class="font-semibold">Respect & Safety</h3>
              <p class="mt-1 text-sm text-slate-300">Moderated channels, ticket-based support, and zero tolerance for harassment.</p>
            </li>
            <li class="p-5 rounded-xl bg-white/5 border border-white/10">
              <h3 class="font-semibold">Constructive Feedback</h3>
              <p class="mt-1 text-sm text-slate-300">Get real feedback on maps, materials, blueprints/Verse, and UX flow.</p>
            </li>
            <li class="p-5 rounded-xl bg-white/5 border border-white/10">
              <h3 class="font-semibold">Learning by Doing</h3>
              <p class="mt-1 text-sm text-slate-300">Hands-on guides and examples you can remix. Beginner friendly, expert approved.</p>
            </li>
            <li class="p-5 rounded-xl bg-white/5 border border-white/10">
              <h3 class="font-semibold">Credit & IP Respect</h3>
              <p class="mt-1 text-sm text-slate-300">We promote ethical use of assets. Credit creators and follow platform rules.</p>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- What we provide -->
  <section id="provide" class="border-t border-white/10">
    <div class="max-w-6xl mx-auto px-4 py-16">
      <h2 class="text-2xl font-bold">What we provide</h2>
      <p class="mt-2 text-slate-300">Practical resources to speed up your workflow.</p>
      <div class="mt-8 grid md:grid-cols-3 gap-6">
        <article class="p-6 rounded-2xl bg-white/5 border border-white/10">
          <h3 class="font-semibold">Curated Assets</h3>
          <p class="mt-1 text-sm text-slate-300">Materials, textures, blueprints/Verse snippets, and UI kits with clear usage notes.</p>
          <a href="#assets" class="mt-3 inline-block text-violet-300 hover:text-violet-200">Explore assets →</a>
        </article>
        <article class="p-6 rounded-2xl bg-white/5 border border-white/10">
          <h3 class="font-semibold">Tools & Templates</h3>
          <p class="mt-1 text-sm text-slate-300">Starter projects, scene presets, material functions, Niagara setups, and CLI tips.</p>
          <a href="#tools" class="mt-3 inline-block text-violet-300 hover:text-violet-2 00">See tools →</a>
        </article>
        <article class="p-6 rounded-2xl bg-white/5 border border-white/10">
          <h3 class="font-semibold">Guides & Help</h3>
          <p class="mt-1 text-sm text-slate-300">Step-by-step guides, code walkthroughs, and friendly Q&A in Discord.</p>
          <a href="#links" class="mt-3 inline-block text-violet-300 hover:text-violet-200">Read guides →</a>
        </article>
      </div>
    </div>
  </section>

  <!-- Assets -->
  <section id="assets" class="border-t border-white/10">
    <div class="max-w-6xl mx-auto px-4 py-16">
      <div class="flex items-end justify-between gap-4 flex-wrap">
        <div>
          <h2 class="text-2xl font-bold">Assets</h2>
          <p class="mt-2 text-slate-300">A tidy, growing library with clear categories and notes.</p>
        </div>
        <a href="#" class="px-4 py-2 rounded-xl bg-white/10 hover:bg-white/20">View GitHub folder</a>
      </div>
      <div class="mt-6 overflow-hidden rounded-xl border border-white/10">
        <table class="min-w-full text-sm">
          <thead class="bg-white/5">
            <tr class="text-left text-slate-300">
              <th class="py-3 px-4">Category</th>
              <th class="py-3 px-4">Examples</th>
              <th class="py-3 px-4">Notes</th>
            </tr>
          </thead>
          <tbody class="divide-y divide-white/10">
            <tr>
              <td class="py-3 px-4">Materials</td>
              <td class="py-3 px-4">Landscape blends, stylized metal, storm FX</td>
              <td class="py-3 px-4">UEFN/UE compatible · Usage notes in README</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Textures</td>
              <td class="py-3 px-4">Noise packs, tiling grounds, decals</td>
              <td class="py-3 px-4">Includes ORM & normals where applicable</td>
            </tr>
            <tr>
              <td class="py-3 px-4">Code Snippets</td>
              <td class="py-3 px-4">Verse utilities, blueprint macros</td>
              <td class="py-3 px-4">MIT/Permissive licenses where possible</td>
            </tr>
            <tr>
              <td class="py-3 px-4">UI / HUD</td>
              <td class="py-3 px-4">Scoreboards, badges, icon sets</td>
              <td class="py-3 px-4">SVG + PNG variants</td>
            </tr>
          </tbody>
        </table>
      </div>
      <p class="mt-3 text-xs text-slate-400">We respect creators and platform rules. Please review any included license before use and follow applicable ToS.</p>
    </div>
  </section>

  <!-- Tools -->
  <section id="tools" class="border-t border-white/10">
    <div class="max-w-6xl mx-auto px-4 py-16">
      <h2 class="text-2xl font-bold">Tools & Templates</h2>
      <p class="mt-2 text-slate-300">Grab-and-go setups to ship faster.</p>
      <div class="mt-8 grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- Card 1 -->
        <div class="p-6 rounded-2xl bg-white/5 border border-white/10">
          <div class="text-3xl">🧱</div>
          <h3 class="mt-2 font-semibold">Material Function Pack</h3>
          <p class="mt-1 text-sm text-slate-300">Re-usable blends, masks, and utility functions for clean node graphs.</p>
          <a class="mt-3 inline-block text-violet-300 hover:text-violet-200" href="#">Open folder →</a>
        </div>
        <!-- Card 2 -->
        <div class="p-6 rounded-2xl bg-white/5 border border-white/10">
          <div class="text-3xl">🌪️</div>
          <h3 class="mt-2 font-semibold">Niagara Storm Presets</h3>
          <p class="mt-1 text-sm text-slate-300">Starter emitters and systems for wind, rain streaks, and flash FX.</p>
          <a class="mt-3 inline-block text-violet-300 hover:text-violet-200" href="#">Open folder →</a>
        </div>
        <!-- Card 3 -->
        <div class="p-6 rounded-2xl bg-white/5 border border-white/10">
          <div class="text-3xl">🧩</div>
          <h3 class="mt-2 font-semibold">UI Badge & Icon Set</h3>
          <p class="mt-1 text-sm text-slate-300">SVG/PNG badges that fit stormy, neon-accented themes.</p>
          <a class="mt-3 inline-block text-violet-300 hover:text-violet-200" href="#">Open folder →</a>
        </div>
        <!-- Card 4 -->
        <div class="p-6 rounded-2xl bg-white/5 border border-white/10">
          <div class="text-3xl">🧭</div>
          <h3 class="mt-2 font-semibold">Project Templates</h3>
          <p class="mt-1 text-sm text-slate-300">Opinionated UEFN/UE project setup with folders, naming, and scripts.</p>
          <a class="mt-3 inline-block text-violet-300 hover:text-violet-200" href="#">Open folder →</a>
        </div>
        <!-- Card 5 -->
        <div class="p-6 rounded-2xl bg-white/5 border border-white/10">
          <div class="text-3xl">📦</div>
          <h3 class="mt-2 font-semibold">CLI Helpers</h3>
          <p class="mt-1 text-sm text-slate-300">Batch import/rename, texture packing, and thumbnail automation.</p>
          <a class="mt-3 inline-block text-violet-300 hover:text-violet-200" href="#">Open folder →</a>
        </div>
        <!-- Card 6 -->
        <div class="p-6 rounded-2xl bg-white/5 border border-white/10">
          <div class="text-3xl">📘</div>
          <h3 class="mt-2 font-semibold">Guides & Checklists</h3>
          <p class="mt-1 text-sm text-slate-300">Material optimization, memory budgeting, and submission prep.</p>
          <a class="mt-3 inline-block text-violet-300 hover:text-violet-200" href="#">Open folder →</a>
        </div>
      </div>
    </div>
  </section>

  <!-- Links / Useful refs -->
  <section id="links" class="border-t border-white/10">
    <div class="max-w-6xl mx-auto px-4 py-16">
      <h2 class="text-2xl font-bold">Quick Links</h2>
      <p class="mt-2 text-slate-300">Jump straight to what you need.</p>
      <div class="mt-6 grid md:grid-cols-2 gap-4">
        <a class="group p-5 rounded-xl bg-white/5 border border-white/10 hover:bg-white/10 flex items-center justify-between" href="#">
          <span><strong>Discord</strong> — Announcements, help, and chat</span>
          <span aria-hidden class="opacity-60 group-hover:opacity-90">→</span>
        </a>
        <a class="group p-5 rounded-xl bg-white/5 border border-white/10 hover:bg-white/10 flex items-center justify-between" href="#">
          <span><strong>GitHub Assets</strong> — All public packs</span>
          <span aria-hidden class="opacity-60 group-hover:opacity-90">→</span>
        </a>
        <a class="group p-5 rounded-xl bg-white/5 border border-white/10 hover:bg-white/10 flex items-center justify-between" href="#">
          <span><strong>Guides</strong> — Step-by-step tutorials</span>
          <span aria-hidden class="opacity-60 group-hover:opacity-90">→</span>
        </a>
        <a class="group p-5 rounded-xl bg-white/5 border border-white/10 hover:bg-white/10 flex items-center justify-between" href="#">
          <span><strong>Issues</strong> — Request help or report a bug</span>
          <span aria-hidden class="opacity-60 group-hover:opacity-90">→</span>
        </a>
      </div>
    </div>
  </section>

  <!-- Join -->
  <section id="join" class="border-t border-white/10">
    <div class="max-w-6xl mx-auto px-4 py-16 text-center">
      <h2 class="text-3xl font-extrabold">Come in out of the storm ☔</h2>
      <p class="mt-3 text-slate-300 max-w-2xl mx-auto">We’d love to have you. Bring your projects, your questions, and your curiosity.</p>
      <div class="mt-6 flex flex-wrap gap-3 justify-center">
        <a href="#" class="px-6 py-3 rounded-xl bg-violet-600 hover:bg-violet-500 font-semibold shadow-soft">Join Storm Lounge</a>
        <a href="#" class="px-6 py-3 rounded-xl bg-white/10 hover:bg-white/20 font-semibold">View the Repo</a>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="border-t border-white/10">
    <div class="max-w-6xl mx-auto px-4 py-10 text-sm text-slate-400 flex flex-col md:flex-row items-center justify-between gap-3">
      <p>© <span id="year"></span> Storm Lounge. All rights reserved.</p>
      <p class="opacity-80">Built with ❤ for creators.</p>
    </div>
  </footer>

  <script>
    // Tiny helpers
    document.getElementById('year').textContent = new Date().getFullYear();
    const menuBtn = document.getElementById('menuBtn');
    const mobileMenu = document.getElementById('mobileMenu');
    menuBtn?.addEventListener('click', () => mobileMenu.classList.toggle('hidden'));
  </script>
</body>
</html>
