---
name: alamehan-readme
description: >-
  Author warm, human-first, bilingual GitHub documentation (README.md in English +
  README.id.md in natural Indonesian) paired with adaptive Dark/Light Porcelain SaaS
  2.5D kinetic @alamehan showcase SVG banners (with embedded Bricolage Grotesque,
  Figtree & Geist Mono designer fonts), a copy-ready GitHub About 1-liner, and
  collapsible <details> developer drawers. Activate when asked to create, standardize,
  or upgrade a repository README in the @alamehan style.
---

# `@alamehan` Universal GitHub README Standard (`alamehan-readme` · V3)

> **Portable Single-File Skill & Master Prompt:** Self-contained in one `.md` file. Works automatically via global discovery (`~/.gemini/config/skills`) or when attached manually alongside any target repository.

## 1. Core Identity — Porcelain SaaS Craft, Human Story First

Every `@alamehan` repository shares one unified visual and editorial signature aligned with **Portfolio V5 (`@alamehan`)**:

1. **`Porcelain SaaS` 2.5D Kinetic Showcase Crown (`920×236`, Light & Dark `<picture>`):**
   - Uses the canonical `@alamehan` **Porcelain SaaS** palette: crisp architectural porcelain-white (`#ffffff` → `#f1f6fc`) & slate-blue (`#2563eb`) in Light mode, and deep midnight slate (`#162138` → `#0d1424`) & luminous sapphire (`#60a5fa`) in Dark mode.
   - Features the **real 2.5D animated `@alamehan` hardware keycap** (3.2s spring choreography: floating porcelain L-frame, staggered 3-blade mechanical wave, popping jewel orb, expanding ripple ring, and rotating 4-point spark).
   - **Real Designer Typography Embedded Inside the SVG (`data:font/woff2;base64,...`):** Never let headlines fall back to generic OS fonts (`Segoe UI` / `Arial`). Embed **`Bricolage Grotesque`** (`800` Display Title), **`Figtree`** (`500–600` Subtitle & 2.5D Tactile Pills), and **`Geist Mono`** (`600` Eyebrow Badge & `COMPLEX → SIMPLE`) directly inside the SVG `<style>` so GitHub renders authentic designer typography on every OS with zero external network calls.
2. **Copy-Ready GitHub `"About"` One-Liner (`[Emoji] [Hook] — crafted by @alamehan`):**
   - Right below the Hero Banner and Language/Action Bar, place **one punchy single-sentence blockquote** (`115–150` characters):
     `> [1 Relevant Domain Emoji] [Magnetic human hook summarizing the entire project] — crafted by @alamehan`
   - Serves two purposes simultaneously: (a) gives README visitors an instant 5-second elevator pitch, and (b) gives the owner a verbatim 1-line description to copy-paste straight into GitHub's top-right **`About ⚙️ -> Description`** box (powering GitHub Profile pinned cards and social link previews!).
3. **Two-Layer Progressive Reading Flow (`All-HR / Balanced` Open + `Specialist` Closed):**
   - **Open Upper Page (For Everyone):** Zero terminal commands, zero code blocks, and zero dense acronyms. Tell the human story in 2 warm paragraphs, show how to try/explore with zero setup, and list 4–5 concrete benefit highlights.
   - **Closed `<details>` Drawers (For Developers & AI Agents):** Tuck installation commands, CLI flags, preset/API tables, Mermaid architecture diagrams, directory maps, and trade-offs inside **3 closed `<details>` accordions** above the author footer.

---

## 2. Smart Existing-README Decision Rule (Mode A vs. Mode B)

Inspect the repository's existing `README.md` and codebase tests/readers before editing:

- **Mode A · Self-Contained README (Default for Fresh or Standalone Repos):**
  Place the human narrative in the open top half and put 100% of developer documentation inside the 3 `<details>` accordions in `README.md` and `README.id.md`.
- **Mode B · Two-Door Preservation (Mandatory When Existing `README.md` Is a Deep >150-Line Manual or Read by In-App Tooling/Tests, e.g. `portfolio-v5`):**
  **Never discard existing engineering depth!**
  1. Preserve 100% of the original technical `README.md` verbatim inside `docs/SYSTEM-OVERVIEW.md` (updating any internal doc-reader or test pointers expecting raw-HTML-free Markdown to target `docs/SYSTEM-OVERVIEW.md`).
  2. Author root `README.md` + `README.id.md` as the welcoming public front door, with its `<details>` developer drawers linking prominently to `[Complete System & Replication Manual →](./docs/SYSTEM-OVERVIEW.md)`.

---

## 3. Generator Blueprint for `Porcelain SaaS` 2.5D Kinetic SVGs (`920×236`)

To embed real designer fonts (`Bricolage Grotesque`, `Figtree`, `Geist Mono`) without external runtime fetches, load the 3 Latin `.woff2` files from local workspace fonts if present or fetch them once during generation from jsDelivr (`@fontsource-variable/bricolage-grotesque`, `@fontsource-variable/figtree`, `@fontsource/geist-mono`) and inline them as `data:font/woff2;base64,...`:

```js
// Generation-time font loader (local workspace first, jsDelivr CDN fallback):
// 1. Display: @fontsource-variable/bricolage-grotesque/files/bricolage-grotesque-latin-opsz-normal.woff2
// 2. Body:    @fontsource-variable/figtree/files/figtree-latin-wght-normal.woff2
// 3. Mono:    @fontsource/geist-mono/files/geist-mono-latin-600-normal.woff2
```

### Canonical `Porcelain SaaS` SVG Structure (Dark & Light)

- **XML Safety:** Escape `&` as `&amp;`, `<` as `&lt;`, `>` as `&gt;` everywhere (never leave raw `&` even inside comments).
- **Cross-Browser Pivot Safety:** Keep all scaled/rotated elements (`alm-glow`, `alm-ring`, `alm-orb`, `alm-spark`) centered around `(0,0)` inside `<g transform="translate(cx, cy)">`.
- **Default `Porcelain SaaS` Color Tokens:**
  - **Light Mode:** Card `#ffffff` → `#f8fafc` → `#f1f6fc` (`stroke="#dbe3ee"`), pedestal `#edf2f7` (`stroke="#dbe3ee"`), badge `#eff6ff` / `#bfdbfe` / `#1d4ed8`, title `#0f172a`, subtitle `#334155` & `#475569`, pill lip `#cbd5e1`, pill face `#ffffff` (`stroke="#dbe3ee"`), jewel `#93c5fd` → `#3b82f6` → `#1d4ed8`.
  - **Dark Mode:** Card `#162138` → `#111a2e` → `#0d1424` (`stroke="#283856"`), pedestal `#0a101d` (`stroke="#223150"`), badge `#132342` / `#264378` / `#60a5fa`, title `#f8fafc`, subtitle `#cbd5e1` & `#a3b4cc`, pill lip `#060a12`, pill face `#1b2842` (`stroke="#2c3f63"`), jewel `#93c5fd` → `#60a5fa` → `#1d4ed8`.
  *(Only override the jewel accent if the user explicitly requests a custom project color; otherwise keep **Porcelain SaaS Blue** across the `@alamehan` family!)*

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 236" width="920" height="236" fill="none" role="img" aria-label="{{PROJECT_TITLE}} — @alamehan 2.5D kinetic banner">
  <defs>
    <!-- Gradients: cardBg, stageAura, kcFace, kcWell, kcGlow, pTop, pWall, jewelGrad -->
    <style>
      @font-face { font-family: 'MehanDisplay'; src: url('data:font/woff2;base64,{{BRICOLAGE_B64}}') format('woff2'); font-weight: 200 800; font-style: normal; }
      @font-face { font-family: 'MehanBody'; src: url('data:font/woff2;base64,{{FIGTREE_B64}}') format('woff2'); font-weight: 300 800; font-style: normal; }
      @font-face { font-family: 'MehanMono'; src: url('data:font/woff2;base64,{{GEIST_MONO_B64}}') format('woff2'); font-weight: 600; font-style: normal; }
      .display { font-family: 'MehanDisplay', -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif; font-weight: 800; }
      .body    { font-family: 'MehanBody', -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif; }
      .mono    { font-family: 'MehanMono', ui-monospace, SFMono-Regular, Menlo, Consolas, monospace; font-weight: 600; }
      /* 3.2s spring keyframes: glowPulse, frameFloat, bladeWave1..3, orbPop, orbRipple, sparkGlint, moteFloat + prefers-reduced-motion */
    </style>
  </defs>
  <!-- Left Stage: Pedestal + Motes + 2.5D @alamehan Keycap (translate(51.8, 51.8) scale(1.38)) -->
  <!-- Right Stage: @alamehan · {{CATEGORY_BADGE}} | COMPLEX → SIMPLE | Bricolage 31px Title | Figtree 2-Line Subtitle | 3 Tactile 2.5D Pills -->
</svg>
```

---

## 4. Exact V3 Page Blueprint (`README.md` & `README.id.md`)

### Part 1 · Open Human Layer (Zero Code Blocks Above the Fold!)

1. **Hero `<picture>` + Centered Language & Primary Action Bar:**
   ```markdown
   <div align="center">
     <picture>
       <source media="(prefers-color-scheme: dark)" srcset="./assets/readme-header-dark.svg" />
       <source media="(prefers-color-scheme: light)" srcset="./assets/readme-header-light.svg" />
       <img alt="{{PROJECT_TITLE}}" src="./assets/readme-header-light.svg" width="100%" />
     </picture>

     <p>
       <strong>English</strong> · <a href="./README.id.md">Bahasa Indonesia →</a>
       &nbsp;&nbsp;·&nbsp;&nbsp;
       <a href="{{PRIMARY_LINK}}"><strong>✨ {{PRIMARY_CTA}}</strong></a> ·
       <a href="./LICENSE">MIT License</a>
     </p>
   </div>
   ```
2. **Copy-Ready GitHub `"About"` One-Liner (Single-Sentence Hook Blockquote):**
   ```markdown
   > 🎨 {{Punchy 1-sentence hook summarizing the whole project in <= 150 chars}} — crafted by @alamehan
   ```
   *(Pick 1 domain-relevant leading emoji: e.g. `🎨` Design System, `⚡` Agent Skills / CLI, `✨` Portfolio / Creative Studio, `🧭` Productivity / Docs, `🛠️` Developer Tool. Always end with `— crafted by @alamehan` so GitHub's About sidebar, pinned profile cards, and social previews carry the `@alamehan` signature.)*
3. **Warm Human Story (`## Why {{Short Name}} Exists` / `## Kenapa {{Short Name}} Dibuat`):**
   - **2 short, vivid paragraphs** in everyday language: (1) the real human problem, and (2) the smart Product Design + Engineering approach and how it feels to use.
4. **Try or Explore Without Setup (`## Try It Right Now` / `## Langsung Coba Sekarang`):**
   - Clean 3–4 row table (`What you want to do` | `Where to go`) with zero terminal commands.
5. **Key Benefits (`## Highlights` / `## Keunggulan Utama`):**
   - 4 to 5 concise, outcome-led bullet points in plain human words.

---

### Part 2 · Collapsible Developer & Specialist Layer (`<details>` Accordions)

Under `## For Developers & Technical Details` (`## Detail Teknis & Panduan Developer`), include **3 flush-left `<details>` accordions**.

> **CRITICAL GITHUB MARKDOWN RULE:**
> 1. Flush `<details>`, `<summary>`, and `</details>` **0 spaces to the left margin**.
> 2. Leave **one empty blank line immediately after `</summary>`** AND **one empty blank line immediately before `</details>`** so tables, fenced code blocks, and `mermaid` diagrams render cleanly on GitHub.

1. `<details><summary><strong>🛠️ Quickstart, Installation &amp; CLI Commands</strong></summary>`
2. `<details><summary><strong>🏗️ Architecture, Specifications &amp; Repository Map</strong></summary>` *(link to `docs/SYSTEM-OVERVIEW.md` here when in Mode B)*
3. `<details><summary><strong>🧭 Design Boundaries, Trade-offs &amp; Replication Guide</strong></summary>`

---

### Part 3 · Warm `@alamehan` Signature Footer

- **English:** `Designed and built with care by **[M. Raihan Rafiiful Allaam (@alamehan)](https://alamehan.github.io)** — *Product Designer & Product Engineer*. Released under the [MIT License](./LICENSE).`
- **Indonesian:** `Dirancang dan dibangun sepenuh hati oleh **[M. Raihan Rafiiful Allaam (@alamehan)](https://alamehan.github.io)** — *Product Designer & Product Engineer*. Dirilis di bawah [Lisensi MIT](./LICENSE).`

---

## 5. Mandatory Verification Checklist

1. **Typography & Palette Proof:** Confirm `Bricolage Grotesque`, `Figtree`, and `Geist Mono` WOFF2 data URIs are embedded inside both SVGs and use the crisp `Porcelain SaaS` Light/Dark palette.
2. **GitHub `"About"` Check:** Confirm the opening `> [Emoji] ... — crafted by @alamehan` line is a single sentence (~115–155 chars) ready to paste straight into GitHub's `About` description.
3. **Strict `<details>` & Link Check:** Verify blank lines around `</summary>` and `</details>`, valid relative links, and strict XML entity escaping across all SVGs.
4. **Full-Page Light & Dark Visual QA:** Render both Light and Dark README pages in headless Chromium via Playwright and inspect the `.png` screenshots before committing.
