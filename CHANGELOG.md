# Linea Lab Website Refresh — Changelog

**Metadata**
- **Status:** Working — 🧪 experiment, not launched
- **Last updated:** June 24, 2026
- **Owner:** Brandon / David / Emery
- **Update trigger:** Update when the site copy, structure, package ladder, or launch status materially changes.
- **Generated:** yes

---

## 2026-06-24 — Ground-up rebuild (statement-driven, NOBL-energy)

A complete rethink of `index.html`, `styles.css`, and `script.js`. The page is now a bold, client-journey-driven, single-page site for **Linea Lab** (practical AI guidance), built around large statements that each dominate their own screen, with ruthless word economy.

### What changed
- **New positioning headline:** `Make AI make sense.` (hero), supported by "Practical AI guidance for owner-led businesses…". Replaces the prior sparse "Practical AI Guidance" one-pager.
- **Statement-first structure.** Key messages are full-viewport beats that arrive as the sole element with a line-mask rise animation: the hero, "AI is not the hard part. Sorting it is.", "AI that fits how you already work.", and the closing "Start small. Build what is useful."
- **Ruthless de-bloat.** Paragraphs and multi-item bullet lists were cut to single bold statements plus minimal support. The three engagement options dropped their long inclusion lists to one line each. Removed the prior contact form, the hero "question cloud," and the phrase "Senior attention."
- **Brand system applied.** Linen / Smoke / Sage / Cognac / Parchment; Cormorant (display) + Inter (body). Black-on-linen and linen-on-smoke established first; **Sage used sparingly** (Signal Session "Start here" tag + the single Sage-toned closing screen). Cognac reserved for CTAs, numbers, and accents.
- **Graphic elements** (client-supplied) used as full-bleed statement backdrops: `linea-human-eye-hero.png` (Sorting), `linea-lab-hands-keyboard.png` (fits-your-flow), `linea-mountain-route.png` (Process), `linea-ocean-horizon.png` (final CTA).
- **Font system switched** from Adobe Typekit (Orpheus Pro / Adobe Garamond Pro) to **Google Fonts Cormorant + Inter** per `BRAND_GUIDE.md`. This also removes the Typekit-domain-allowlist risk flagged in `LAUNCH_PLAN.md`.
- **Motion:** vanilla-JS IntersectionObserver scroll reveals, line-mask statement entrances, staggered cards, hover states, sticky-header state, full `prefers-reduced-motion` support. No animation libraries.
- **Agent-readability:** semantic landmarks, one `<h1>`, `<h2>` section titles with real service names in text, JSON-LD `ProfessionalService` with `makesOffer` (no prices), plain-text email + location. JSON-LD contains **no** internal-system language.
- **Follow-up tweaks (same day):** removed the "Real work / Practical first steps" recent-work section entirely (team call); team headline changed from "Small team." to **"Human understanding."**; removed the outline on the nav "Start a conversation" link (now a plain bold link); widened the line-mask so large display descenders (y/g) are no longer clipped.

### Why the direction changed
The first pass was clean but read as a wordy "info dump" and didn't carry NOBL's confidence. Direction from the team: bolder, cleaner, fewer words, "more signal, less reassurance syrup," with statements that dominate the screen. Copy was tightened line-by-line per that feedback ("AI is not the hard part. Sorting it is.", "Useful AI inside your business is harder to find.", positive principles trio, etc.).

### Source files that informed the work
- `BRAND_GUIDE.md` — colors, Cormorant + Inter, "more smoke than Sage."
- `BUSINESS_INFO.md`, `SOUL.md` — Linea Lab positioning, audience, taste (unhurried, warm, analog-over-glossy, no purple).
- `01_STRATEGY/Research/Strategy/Linea Lab Website — Agent-Readable Design Spec.md` — semantic HTML + JSON-LD (the lore-laden `llms.txt` draft was intentionally **not** used).
- `VERSION_LOCK.md`, `LAUNCH_PLAN.md` — folder is the kept refresh; contact email `hello@linealab.ai`.
- Client engagement patterns informed the offer ladder **as internal context only** (no client names or details exposed): Signal Session (clarity-first), Clarity Sprint (one-workflow planning), Workflow Build & Enablement (design → train → handoff).

### Reference sites — borrowed the job, not the surface
- **NOBL (nobl.io):** confidence, scale, contrast, sequential scroll storytelling, one bold statement per screen, section momentum, tasteful motion. No layouts, copy, type, or visual system copied.
- **Superadditive (superadd.org):** directness, "why this exists" clarity, a useful FAQ that answers buying anxiety, and simple comparable options. No copy or structure copied.

### Package ladder (no pricing anywhere)
- **The Signal Session — 3 hours.** The obvious first step; "Start here" tag.
- **The Clarity Sprint.** Shape one real workflow into a build-ready plan.
- **Workflow Build & Enablement.** Design it, train the team, hand it over.
All three are framed as tailored, not fixed packages. No prices, ranges, fees, "fixed-fee," or retainer language appear on the page.

### Checks performed
- **Dev server:** `python3 -m http.server 4173 --directory "."` (the Claude preview MCP is pinned to another project at the repo root and 404s this subfolder; the preview browser was pointed at `http://localhost:4173/`).
- **Browser/visual:** every section captured at desktop (1280) and key sections at mobile (390): hero, both image statement screens, sort/principles, about, what-we-help-with, options, process, proof, team, FAQ, final CTA, footer.
- **Responsive:** 0px horizontal overflow at 390 and 1280; options stack with the Signal Session first; team stacks; mobile hamburger nav opens/closes (hamburger ↔ ×).
- **Accessibility:** one `<h1>`; `<h2>` section headings; skip link; `aria-labelledby` on sections; keyboard-focus styles; accordion toggles; alt text on portraits; decorative images `alt=""`; `prefers-reduced-motion` resolves all reveals to visible.
- **Content sweeps:** pricing ✓ none; internal lore ✓ none; generic AI hype ✓ none.
- **Console:** no errors.

### Needs Brandon / David / Emery approval before launch
- All client-facing copy (the anonymized "Recent work" section was removed per team direction).
- Package names and the 3-hour Signal Session framing.
- Final hero statement choice (`Make AI make sense.`) and the supporting line.
- Launch items still outstanding per the agent-readability spec: `llms.txt` (clean, no internal lore), `robots.txt`, `sitemap.xml`, and the GPTBot training opt-out decision.
- Confirm `hello@linealab.ai` and "San Francisco · Bay Area" as the public contact + location.
- This page remains a 🧪 experiment until the team explicitly promotes it.
