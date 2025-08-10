import { useState } from "react";
import { motion, AnimatePresence } from "framer-motion";

// Simple client-side tabs for a multi-page feel
const TABS = [
  { key: "home", label: "Home" },
  { key: "assets", label: "Assets" },
  { key: "tools", label: "Tools" },
  { key: "guides", label: "Guides" },
  { key: "community", label: "Community" },
  { key: "contact", label: "Contact" },
];

function Shell({ children }) {
  return (
    <div className="min-h-screen bg-[radial-gradient(1200px_600px_at_20%_-10%,rgba(124,58,237,.25),transparent_60%),radial-gradient(1000px_600px_at_120%_10%,rgba(59,130,246,.18),transparent_60%),linear-gradient(180deg,#0b1020,#0b0f1a)] text-slate-100">
      {children}
    </div>
  );
}

function Header({ active, onChange }) {
  return (
    <header className="sticky top-0 z-50 backdrop-blur supports-[backdrop-filter]:bg-slate-900/40 bg-slate-900/60 border-b border-white/10">
      <div className="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
        <button onClick={() => onChange("home")} className="flex items-center gap-2 group">
          <span aria-hidden className="inline-flex h-8 w-8 rounded-xl bg-gradient-to-br from-violet-500 to-indigo-600 items-center justify-center shadow">⚡</span>
          <span className="font-semibold tracking-wide group-hover:text-white/90">Storm Lounge</span>
        </button>
        <nav className="hidden md:flex items-center gap-5 text-sm">
          {TABS.map((t) => (
            <button
              key={t.key}
              onClick={() => onChange(t.key)}
              className={`pb-1 hover:text-white ${
                active === t.key ? "text-white border-b-2 border-violet-500" : "text-slate-300"
              }`}
            >
              {t.label}
            </button>
          ))}
          <a
            href="#join"
            onClick={(e) => {
              e.preventDefault();
              onChange("contact");
            }}
            className="inline-flex items-center gap-2 px-3 py-1.5 rounded-lg bg-violet-600 hover:bg-violet-500 transition shadow"
          >
            Join
          </a>
        </nav>
      </div>
    </header>
  );
}

function Hero() {
  return (
    <section className="max-w-6xl mx-auto px-4 py-16 md:py-24">
      <div className="grid md:grid-cols-2 items-center gap-10">
        <motion.div initial={{ opacity: 0, y: 20 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.5 }}>
          <p className="text-violet-300/90 font-medium uppercase tracking-widest">Welcome</p>
          <h1 className="mt-3 text-4xl md:text-5xl font-extrabold leading-tight">
            A warm place in the storm for creators
          </h1>
          <p className="mt-4 text-slate-300/90 leading-relaxed max-w-xl">
            Storm Lounge is a friendly Discord hub for builders, designers, and game devs. Share and discover assets, swap tips, test ideas, and get help—without the drama.
          </p>
          <div className="mt-6 flex flex-wrap gap-3">
            <a href="#" className="px-5 py-3 rounded-xl bg-violet-600 hover:bg-violet-500 font-semibold shadow">Join the Discord</a>
            <a href="#" className="px-5 py-3 rounded-xl bg-white/10 hover:bg-white/20 font-semibold">Browse Assets</a>
            <a href="#" className="px-5 py-3 rounded-xl bg-white/10 hover:bg-white/20 font-semibold">Quick Links</a>
          </div>
        </motion.div>
        <motion.div initial={{ opacity: 0, scale: 0.98 }} animate={{ opacity: 1, scale: 1 }} transition={{ duration: 0.5, delay: 0.1 }}>
          <div className="aspect-[4/3] rounded-2xl bg-gradient-to-br from-indigo-500/20 via-fuchsia-500/20 to-violet-600/20 border border-white/10 p-1">
            <div className="h-full w-full rounded-xl bg-[radial-gradient(ellipse_at_top_right,rgba(99,102,241,0.35),transparent_40%),radial-gradient(ellipse_at_bottom_left,rgba(236,72,153,0.35),transparent_45%)] flex items-center justify-center">
              <div className="text-center p-8">
                <div className="text-6xl">🌩️</div>
                <p className="mt-4 text-lg text-slate-200">“Ride the storm. Build something great.”</p>
                <p className="mt-2 text-sm text-slate-400">UEFN • Unreal • Blender • Game Design • Community</p>
              </div>
            </div>
          </div>
        </motion.div>
      </div>
    </section>
  );
}

function Section({ title, subtitle, children }) {
  return (
    <section className="border-t border-white/10">
      <div className="max-w-6xl mx-auto px-4 py-14">
        <h2 className="text-2xl font-bold">{title}</h2>
        {subtitle && <p className="mt-2 text-slate-300">{subtitle}</p>}
        <div className="mt-8">{children}</div>
      </div>
    </section>
  );
}

function Cards({ items }) {
  return (
    <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
      {items.map((it, i) => (
        <motion.article
          key={i}
          initial={{ opacity: 0, y: 10 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.3, delay: i * 0.05 }}
          className="p-6 rounded-2xl bg-white/5 border border-white/10"
        >
          <div className="text-3xl">{it.emoji}</div>
          <h3 className="mt-2 font-semibold">{it.title}</h3>
          <p className="mt-1 text-sm text-slate-300">{it.text}</p>
          {it.link && (
            <a className="mt-3 inline-block text-violet-300 hover:text-violet-200" href={it.href || "#"}>
              {it.link} →
            </a>
          )}
        </motion.article>
      ))}
    </div>
  );
}

function Table() {
  return (
    <div className="overflow-hidden rounded-xl border border-white/10">
      <table className="min-w-full text-sm">
        <thead className="bg-white/5">
          <tr className="text-left text-slate-300">
            <th className="py-3 px-4">Category</th>
            <th className="py-3 px-4">Examples</th>
            <th className="py-3 px-4">Notes</th>
          </tr>
        </thead>
        <tbody className="divide-y divide-white/10">
          <tr>
            <td className="py-3 px-4">Materials</td>
            <td className="py-3 px-4">Landscape blends, stylized metal, storm FX</td>
            <td className="py-3 px-4">UEFN/UE compatible · Usage notes in README</td>
          </tr>
          <tr>
            <td className="py-3 px-4">Textures</td>
            <td className="py-3 px-4">Noise packs, tiling grounds, decals</td>
            <td className="py-3 px-4">Includes ORM & normals where applicable</td>
          </tr>
          <tr>
            <td className="py-3 px-4">Code Snippets</td>
            <td className="py-3 px-4">Verse utilities, blueprint macros</td>
            <td className="py-3 px-4">MIT/Permissive licenses where possible</td>
          </tr>
          <tr>
            <td className="py-3 px-4">UI / HUD</td>
            <td className="py-3 px-4">Scoreboards, badges, icon sets</td>
            <td className="py-3 px-4">SVG + PNG variants</td>
          </tr>
        </tbody>
      </table>
    </div>
  );
}

function FAQ() {
  const QS = [
    { q: "How do I join the Discord?", a: "Use the Join button above or your invite link here. Once inside, read the rules and pick your roles." },
    { q: "Can I use the assets commercially?", a: "Each folder includes a LICENSE file. Respect the terms, attribute when required, and follow Epic/UEFN ToS." },
    { q: "Do you offer project feedback?", a: "Yes—share screenshots or a short clip in #feedback. For deeper help, open a ticket." },
  ];
  const [open, setOpen] = useState(null);
  return (
    <div className="grid gap-3">
      {QS.map((item, i) => (
        <div key={i} className="rounded-xl border border-white/10 bg-white/5">
          <button
            onClick={() => setOpen(open === i ? null : i)}
            className="w-full text-left px-5 py-4 flex items-center justify-between"
          >
            <span className="font-medium">{item.q}</span>
            <span className="opacity-60">{open === i ? "−" : "+"}</span>
          </button>
          <AnimatePresence initial={false}>
            {open === i && (
              <motion.div initial={{ height: 0, opacity: 0 }} animate={{ height: "auto", opacity: 1 }} exit={{ height: 0, opacity: 0 }} className="px-5 pb-4 text-slate-300">
                {item.a}
              </motion.div>
            )}
          </AnimatePresence>
        </div>
      ))}
    </div>
  );
}

function Footer() {
  return (
    <footer className="border-t border-white/10">
      <div className="max-w-6xl mx-auto px-4 py-10 text-sm text-slate-400 flex flex-col md:flex-row items-center justify-between gap-3">
        <p>© {new Date().getFullYear()} Storm Lounge. All rights reserved.</p>
        <p className="opacity-80">Built with ❤ for creators.</p>
      </div>
    </footer>
  );
}

function HomePage() {
  return (
    <>
      <Hero />
      <Section title="About this place" subtitle="Clear rules, good vibes, and practical help for creators.">
        <div className="grid md:grid-cols-2 gap-6">
          <p className="text-slate-300/95">
            We built Storm Lounge so creators have a calm, focused space to learn, collaborate, and level up. Whether you’re prototyping in UEFN, sculpting in Blender, or tuning materials in Unreal, you’ll find support here.
          </p>
          <ul className="grid gap-3">
            {["Respect & Safety", "Constructive Feedback", "Learning by Doing", "Credit & IP Respect"].map((t) => (
              <li key={t} className="p-4 rounded-xl bg-white/5 border border-white/10">{t}</li>
            ))}
          </ul>
        </div>
      </Section>
      <Section title="What we provide" subtitle="Practical resources to speed up your workflow.">
        <Cards
          items={[
            { emoji: "🧱", title: "Curated Assets", text: "Materials, textures, code, and UI kits with clear usage notes.", link: "Explore assets" },
            { emoji: "🌪️", title: "Niagara Presets", text: "Starter emitters for wind, rain streaks, and flash FX.", link: "Open presets" },
            { emoji: "🧩", title: "UI Badge Set", text: "SVG/PNG badges that fit stormy, neon-accented themes.", link: "View icons" },
          ]}
        />
      </Section>
      <Section title="FAQ" subtitle="New here? Start with these.">
        <FAQ />
      </Section>
    </>
  );
}

function AssetsPage() {
  return (
    <>
      <Section title="Assets" subtitle="A tidy, growing library with clear categories and notes.">
        <div className="flex items-end justify-between gap-4 flex-wrap mb-6">
          <a href="#" className="px-4 py-2 rounded-xl bg-white/10 hover:bg-white/20">View GitHub folder</a>
        </div>
        <Table />
        <p className="mt-3 text-xs text-slate-400">Review included licenses and follow platform ToS.</p>
      </Section>
    </>
  );
}

function ToolsPage() {
  return (
    <Section title="Tools & Templates" subtitle="Grab-and-go setups to ship faster.">
      <Cards
        items={[
          { emoji: "🧱", title: "Material Function Pack", text: "Re-usable blends, masks, and utility functions for clean graphs.", link: "Open folder" },
          { emoji: "🧭", title: "Project Templates", text: "Opinionated UEFN/UE setup with folders, naming, and scripts.", link: "Open template" },
          { emoji: "📦", title: "CLI Helpers", text: "Batch import/rename, texture packing, thumbnails.", link: "Open scripts" },
          { emoji: "📘", title: "Guides & Checklists", text: "Optimization, memory budgeting, submission prep.", link: "Read guides" },
        ]}
      />
    </Section>
  );
}

function GuidesPage() {
  return (
    <Section title="Guides" subtitle="Step-by-step tutorials and best practices.">
      <div className="grid gap-4">
        {[
          { title: "Landscape Materials 101", desc: "Blend layers cleanly with runtime virtual textures." },
          { title: "Niagara Storm FX", desc: "Rain streaks, fog sheets, lightning flashes." },
          { title: "UEFN Memory Budgeting", desc: "Keep your project under control with profiling tips." },
        ].map((g, i) => (
          <div key={i} className="p-5 rounded-xl bg-white/5 border border-white/10">
            <h3 className="font-semibold">{g.title}</h3>
            <p className="text-sm text-slate-300">{g.desc}</p>
            <a href="#" className="mt-2 inline-block text-violet-300 hover:text-violet-200">Open guide →</a>
          </div>
        ))}
      </div>
    </Section>
  );
}

function CommunityPage() {
  return (
    <Section title="Community" subtitle="Hop in, say hi, and share what you're building.">
      <div className="grid md:grid-cols-2 gap-6">
        <div className="p-6 rounded-2xl bg-white/5 border border-white/10">
          <h3 className="font-semibold">Discord</h3>
          <p className="mt-1 text-sm text-slate-300">Announcements, help, and chat. Read rules, then pick roles.</p>
          <a className="mt-3 inline-block text-violet-300 hover:text-violet-200" href="#">Join →</a>
        </div>
        <div className="p-6 rounded-2xl bg-white/5 border border-white/10">
          <h3 className="font-semibold">Issues / Tickets</h3>
          <p className="mt-1 text-sm text-slate-300">Request help, report bugs, or propose features.</p>
          <a className="mt-3 inline-block text-violet-300 hover:text-violet-200" href="#">Open issues →</a>
        </div>
      </div>
    </Section>
  );
}

function ContactPage() {
  return (
    <Section title="Contact" subtitle="We’d love to have you. Bring your projects and questions.">
      <form className="grid gap-4 max-w-xl">
        <input className="px-4 py-3 rounded-xl bg-white/10 border border-white/10 focus:outline-none" placeholder="Your name" />
        <input className="px-4 py-3 rounded-xl bg-white/10 border border-white/10 focus:outline-none" placeholder="Email or Discord handle" />
        <textarea rows={5} className="px-4 py-3 rounded-xl bg-white/10 border border-white/10 focus:outline-none" placeholder="What can we help with?" />
        <button type="button" className="px-5 py-3 rounded-xl bg-violet-600 hover:bg-violet-500 font-semibold w-fit">Send</button>
        <p className="text-xs text-slate-400">Tip: For repo issues, please use GitHub Issues instead of this form.</p>
      </form>
    </Section>
  );
}

export default function App() {
  const [active, setActive] = useState("home");
  const Page = {
    home: <HomePage />,
    assets: <AssetsPage />,
    tools: <ToolsPage />,
    guides: <GuidesPage />,
    community: <CommunityPage />,
    contact: <ContactPage />,
  }[active];

  return (
    <Shell>
      <Header active={active} onChange={setActive} />
      <main>
        <AnimatePresence mode="wait">
          <motion.div key={active} initial={{ opacity: 0, y: 8 }} animate={{ opacity: 1, y: 0 }} exit={{ opacity: 0, y: -8 }} transition={{ duration: 0.22 }}>
            {Page}
          </motion.div>
        </AnimatePresence>
      </main>
      <Footer />
    </Shell>
  );
}
