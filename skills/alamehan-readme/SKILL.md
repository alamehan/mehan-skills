---
name: alamehan-readme
description: >-
  Author warm, human-first, bilingual GitHub documentation (README.md in English +
  README.id.md in natural Indonesian) paired with adaptive Dark/Light 2.5D kinetic
  @alamehan brand showcase SVG banners and collapsible <details> developer drawers
  for any @alamehan repository. Activate when asked to create, standardize, or
  upgrade a repository README in the @alamehan style.
---

# `@alamehan` Universal GitHub README Standard (`alamehan-readme` · V2)

> **Portable Single-File Skill & Master Prompt:** Self-contained in one `.md` file. Works automatically via global discovery (`~/.gemini/config/skills`) or when attached manually alongside any target repository.

## 1. Core Philosophy — Human First, Technical on Demand

Most developer READMEs fail non-engineers (Recruiters, Product Designers, PMs, Founders, and everyday users) by dumping terminal commands, acronyms, and folder trees in the first screen. Every `@alamehan` README follows **Progressive Audience Layering** (inspired by Portfolio V5's *All-HR / Balanced / Specialist* lenses):

1. **One Unified Visual Crown (`2.5D Kinetic @alamehan Showcase Banner`):** Open with one cohesive Dark/Light `<picture>` hero banner featuring the **real 2.5D animated `@alamehan` hardware keycap emblem** (3.2-second spring choreography: floating porcelain L-frame, staggered 3-blade mechanical wave, popping accent jewel orb, expanding concentric ripple ring, and rotating 4-point spark) paired with human-first editorial copy and 3 tactile value pills. **Never stack multiple clashing posters or light-only infographics down the page.**
2. **Open Upper Page = For Everyone (`All-HR + Balanced`):** Zero terminal code blocks, zero package paths, and zero unexplained acronyms above the fold. Make every visitor *feel why the project matters* in plain, engaging language, show what they can try right now without installing anything, and highlight 4–5 concrete product outcomes.
3. **Closed `<details>` Drawers = For Developers & AI Agents (`Specialist`):** Keep 100% of engineering rigor (install commands, CLI flags, theme/API tables, Mermaid architecture diagrams, directory maps, and design trade-offs) neatly organized inside **3 closed `<details>` accordions** above the author footer — clean by default, complete on click.

---

## 2. Smart Existing-README Decision Rule (Mode A vs. Mode B)

Before writing, inspect the repository's existing `README.md` and codebase tests/tooling:

- **Mode A · Self-Contained README (Default for Fresh, Standard, or Standalone Repos):**
  Put the human story in the open upper section and place the complete technical documentation inside the 3 `<details>` accordions in `README.md` and `README.id.md`.
- **Mode B · Two-Door Preservation (Mandatory When Existing `README.md` Is a Deep >150-Line Manual or Parsed by In-App Tooling/Tests):**
  **Never delete or flatten deep existing engineering specifications!**
  1. Preserve 100% of the original technical `README.md` verbatim inside `docs/SYSTEM-OVERVIEW.md` (and update any internal doc-reader or test pointers that expect pure HTML-free Markdown to reference `docs/SYSTEM-OVERVIEW.md`).
  2. Write `README.md` + `README.id.md` at the repository root as the welcoming public front door, summarizing key developer essentials inside `<details>` and linking prominently to `[Complete System & Replication Manual →](./docs/SYSTEM-OVERVIEW.md)`.

---

## 3. Adaptive 2.5D Kinetic `@alamehan` Showcase SVG Templates (`920×236`)

GitHub executes pure-CSS `@keyframes` (`transform`, `opacity`) inside local SVGs loaded via `<picture><img>`. All scaled/rotated elements below (`alm-glow`, `alm-ring`, `alm-orb`, `alm-spark`) are centered around `(0,0)` inside `<g transform="translate(cx, cy)">` so pivot points stay 100% locked across Chrome, Safari, Edge, Firefox, and mobile browsers.

**Customization Slots (XML-escape `&` as `&amp;`, `<` as `&lt;`, `>` as `&gt;`; never leave raw `&` even in comments):**
- `{{CATEGORY_BADGE}}`: Short uppercase domain label, e.g. `DESIGN SYSTEM`, `AGENT SKILLS`, `PORTFOLIO &amp; STUDIO`, `WEB APPLICATION`
- `{{PROJECT_TITLE}}`: Crisp project title (≤ 28 chars)
- `{{SUBTITLE_LINE_1}}` & `{{SUBTITLE_LINE_2}}`: Warm 2-line human value proposition (≤ 64 chars per line, zero CLI flags!)
- `{{PILL_1}}`, `{{PILL_2}}`, `{{PILL_3}}`: 3 concise outcome pills (≤ 28 chars each; adjust pill `width` / `x` if needed so spacing stays ~12px)
- **Accent Palette Slots:**
  - *Berry-Rose (e.g. Mehan DS):* Dark `#ff6b93` / `#e0366b` / `#9f1239`, Light `#d42a5f` / `#be185d` / `#fce7f3` (`pillBg` `#fdf2f6`, `pillBorder` `#f5cbd9`)
  - *Sapphire-Blue (e.g. Portfolio V5, Mehan Skills):* Dark `#60a5fa` / `#3b82f6` / `#1d4ed8`, Light `#2563eb` / `#1d4ed8` / `#dbeafe` (`pillBg` `#eff6ff`, `pillBorder` `#bfdbfe`)
  - *Emerald / Violet / Amber:* Derive matching vibrant dark highlight, mid jewel tone, and soft light tint.

### 3A. `assets/readme-header-dark.svg` Master Template

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 236" width="920" height="236" fill="none" role="img" aria-label="{{PROJECT_TITLE}} — @alamehan kinetic banner">
  <defs>
    <linearGradient id="cardBg" x1="0" y1="0" x2="920" y2="236" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#111827"/>
      <stop offset="55%" stop-color="#0b101d"/>
      <stop offset="100%" stop-color="#080c16"/>
    </linearGradient>
    <radialGradient id="stageAura" cx="0" cy="0" r="1" gradientUnits="userSpaceOnUse" gradientTransform="translate(118 118) scale(120)">
      <stop offset="0%" stop-color="{{ACCENT_MID}}" stop-opacity="0.24"/>
      <stop offset="100%" stop-color="{{ACCENT_MID}}" stop-opacity="0"/>
    </radialGradient>
    <linearGradient id="kcFace" x1="12" y1="6" x2="84" y2="88" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#1e293b"/>
      <stop offset="52%" stop-color="#0f172a"/>
      <stop offset="100%" stop-color="#070b14"/>
    </linearGradient>
    <linearGradient id="kcWell" x1="16" y1="12" x2="80" y2="84" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#090e1a"/>
      <stop offset="100%" stop-color="#152036"/>
    </linearGradient>
    <radialGradient id="kcGlow" cx="0" cy="0" r="1" gradientUnits="userSpaceOnUse" gradientTransform="scale(34)">
      <stop offset="0%" stop-color="{{ACCENT_BRIGHT}}" stop-opacity="0.36"/>
      <stop offset="100%" stop-color="{{ACCENT_MID}}" stop-opacity="0"/>
    </radialGradient>
    <linearGradient id="pTop" x1="24" y1="20" x2="68" y2="76" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#ffffff"/>
      <stop offset="70%" stop-color="#f1f5f9"/>
      <stop offset="100%" stop-color="#dbeafe"/>
    </linearGradient>
    <linearGradient id="pWall" x1="24" y1="22" x2="70" y2="78" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#94a3b8"/>
      <stop offset="100%" stop-color="#475569"/>
    </linearGradient>
    <linearGradient id="jewelGrad" x1="-5" y1="-5" x2="6" y2="6" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="{{ACCENT_SOFT}}"/>
      <stop offset="45%" stop-color="{{ACCENT_BRIGHT}}"/>
      <stop offset="100%" stop-color="{{ACCENT_DEEP}}"/>
    </linearGradient>
    <style>
      .sans { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif; }
      .mono { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace; }
      .alm-glow  { animation: glowPulse 3.2s cubic-bezier(0.4, 0, 0.2, 1) infinite; }
      .alm-frame { animation: frameFloat 3.2s cubic-bezier(0.34, 1.56, 0.64, 1) infinite; }
      .alm-b1    { animation: bladeWave1 3.2s cubic-bezier(0.34, 1.56, 0.64, 1) infinite; }
      .alm-b2    { animation: bladeWave2 3.2s cubic-bezier(0.34, 1.56, 0.64, 1) infinite; }
      .alm-b3    { animation: bladeWave3 3.2s cubic-bezier(0.34, 1.56, 0.64, 1) infinite; }
      .alm-orb   { animation: orbPop 3.2s cubic-bezier(0.34, 1.56, 0.64, 1) infinite; }
      .alm-ring  { animation: orbRipple 3.2s cubic-bezier(0.16, 1, 0.3, 1) infinite; }
      .alm-spark { animation: sparkGlint 3.2s cubic-bezier(0.34, 1.56, 0.64, 1) infinite; }
      .mote-a    { animation: moteFloat 4.6s ease-in-out infinite; }
      .mote-b    { animation: moteFloat 4.6s ease-in-out 2.3s infinite; }
      @keyframes glowPulse {
        0%, 100% { transform: scale(1); opacity: 0.72; }
        56% { transform: scale(1.18); opacity: 1; }
      }
      @keyframes frameFloat {
        0%, 100% { transform: translate(0px, 0px); }
        12% { transform: translate(0px, 1.2px); }
        32% { transform: translate(0px, -1.6px); }
        68% { transform: translate(0px, -1px); }
      }
      @keyframes bladeWave1 {
        0%, 100% { transform: translate(0px, 0px); }
        18% { transform: translate(-2.6px, -2.8px); }
        38% { transform: translate(0.8px, 0.8px); }
        68% { transform: translate(0px, -1px); }
      }
      @keyframes bladeWave2 {
        0%, 8%, 100% { transform: translate(0px, 0px); }
        26% { transform: translate(-2.8px, -2.8px); }
        46% { transform: translate(0.8px, 0.8px); }
        72% { transform: translate(0px, -1px); }
      }
      @keyframes bladeWave3 {
        0%, 16%, 100% { transform: translate(0px, 0px); }
        34% { transform: translate(-3px, -2.8px); }
        52% { transform: translate(1px, 0.8px); }
        76% { transform: translate(0px, -1px); }
      }
      @keyframes orbPop {
        0%, 42%, 100% { transform: scale(1); }
        49% { transform: scale(0.82); }
        58% { transform: scale(1.26); }
        72% { transform: scale(0.95); }
        84% { transform: scale(1.03); }
      }
      @keyframes orbRipple {
        0%, 50%, 100% { transform: scale(0.65); opacity: 0; }
        56% { transform: scale(1.05); opacity: 0.88; }
        82% { transform: scale(2.3); opacity: 0; }
      }
      @keyframes sparkGlint {
        0%, 50%, 84%, 100% { transform: scale(0) rotate(0deg); opacity: 0; }
        62% { transform: scale(1.18) rotate(45deg); opacity: 1; }
        76% { transform: scale(0.4) rotate(90deg); opacity: 0; }
      }
      @keyframes moteFloat {
        0%, 100% { transform: translate(0px, 0px); opacity: 0.45; }
        50% { transform: translate(0px, -5px); opacity: 0.95; }
      }
      @media (prefers-reduced-motion: reduce) {
        .alm-glow, .alm-frame, .alm-b1, .alm-b2, .alm-b3, .alm-orb, .alm-ring, .alm-spark, .mote-a, .mote-b { animation: none !important; }
      }
    </style>
  </defs>

  <!-- Outer Showcase Card -->
  <rect x="2" y="2" width="916" height="232" rx="22" fill="url(#cardBg)" stroke="#1e293b" stroke-width="1.5"/>
  <path d="M28 3.5H892" stroke="#ffffff" stroke-opacity="0.08" stroke-width="1"/>
  <circle cx="118" cy="118" r="112" fill="url(#stageAura)"/>

  <!-- Left Stage Pedestal and Ambient Motes -->
  <rect x="38" y="38" width="160" height="160" rx="36" fill="#090e1a" fill-opacity="0.65" stroke="#1e293b" stroke-width="1"/>
  <circle cx="52" cy="54" r="2.5" fill="{{ACCENT_BRIGHT}}" class="mote-a"/>
  <circle cx="184" cy="180" r="2" fill="{{ACCENT_SOFT}}" class="mote-b"/>

  <!-- 2.5D Kinetic @alamehan Hardware Keycap Emblem (Exact Vector Choreography) -->
  <g transform="translate(51.8, 51.8) scale(1.38)">
    <rect x="4" y="7.5" width="88" height="84.5" rx="22" fill="#03060d"/>
    <rect x="4" y="4" width="88" height="84" rx="22" fill="url(#kcFace)" stroke="#334155" stroke-width="1.2"/>
    <rect x="9" y="9" width="78" height="74" rx="17" fill="url(#kcWell)" stroke="#1e293b" stroke-width="1"/>
    <path d="M20 5.5H76" stroke="#94a3b8" stroke-width="1.3" stroke-linecap="round" opacity="0.42"/>
    <g transform="translate(54, 54)"><circle cx="0" cy="0" r="32" fill="url(#kcGlow)" class="alm-glow"/></g>

    <g class="alm-frame">
      <path d="M33.49 22.87H61.98C66.93 22.87 70.94 26.88 70.94 31.82H33.49V77.82C28.54 77.82 24.53 73.81 24.53 68.86V31.82C24.53 26.88 28.54 22.87 33.49 22.87Z" fill="url(#pWall)"/>
      <path d="M33.49 20.27H61.98C66.93 20.27 70.94 24.28 70.94 29.22H33.49V75.22C28.54 75.22 24.53 71.21 24.53 66.26V29.22C24.53 24.28 28.54 20.27 33.49 20.27Z" fill="url(#pTop)"/>
    </g>
    <g class="alm-b1">
      <path d="M51.07 47.46C53.98 42.48 61.03 38.44 66.80 38.44L64.46 42.45C61.54 47.43 54.50 51.47 48.73 51.47L51.07 47.46Z" fill="url(#pWall)"/>
      <path d="M51.07 45.16C53.98 40.18 61.03 36.14 66.80 36.14L64.46 40.15C61.54 45.13 54.50 49.17 48.73 49.17L51.07 45.16Z" fill="url(#pTop)"/>
    </g>
    <g class="alm-b2">
      <path d="M43.45 60.50C46.37 55.51 53.41 51.47 59.19 51.47L56.86 55.46C53.94 60.45 46.89 64.49 41.11 64.49L43.45 60.50Z" fill="url(#pWall)"/>
      <path d="M43.45 58.20C46.37 53.21 53.41 49.17 59.19 49.17L56.86 53.16C53.94 58.15 46.89 62.19 41.11 62.19L43.45 58.20Z" fill="url(#pTop)"/>
    </g>
    <g class="alm-b3">
      <path d="M35.83 73.52C38.74 68.54 45.79 64.49 51.56 64.49L49.22 68.49C46.31 73.48 39.26 77.52 33.49 77.52L35.83 73.52Z" fill="url(#pWall)"/>
      <path d="M35.83 71.22C38.74 66.24 45.79 62.19 51.56 62.19L49.22 66.19C46.31 71.18 39.26 75.22 33.49 75.22L35.83 71.22Z" fill="url(#pTop)"/>
    </g>

    <g transform="translate(65.54, 69.73)">
      <circle cx="0" cy="0" r="6.2" stroke="{{ACCENT_BRIGHT}}" stroke-width="2" class="alm-ring"/>
      <circle cx="0" cy="2.3" r="5.7" fill="#050811" opacity="0.65"/>
      <g class="alm-orb">
        <circle cx="0" cy="0" r="5.7" fill="url(#jewelGrad)"/>
        <circle cx="-1.84" cy="-1.83" r="1.75" fill="#ffffff" opacity="0.9"/>
      </g>
    </g>
    <g transform="translate(72.5, 62.5)">
      <path d="M0 -3.8L1 -1L3.8 0L1 1L0 3.8L-1 1L-3.8 0L-1 -1Z" fill="{{ACCENT_SOFT}}" class="alm-spark"/>
    </g>
  </g>

  <!-- Right Editorial Stage -->
  <rect x="232" y="40" width="{{BADGE_WIDTH}}" height="24" rx="12" fill="{{BADGE_BG_DARK}}" stroke="{{BADGE_BORDER_DARK}}" stroke-width="1"/>
  <text x="244" y="56" class="mono" fill="{{ACCENT_BRIGHT}}" font-size="11" font-weight="700" letter-spacing="0.03em">@alamehan&#160;·&#160;{{CATEGORY_BADGE}}</text>
  <text x="884" y="56" text-anchor="end" class="mono" fill="#64748b" font-size="11" font-weight="600" letter-spacing="0.04em">COMPLEX&#160;→&#160;SIMPLE</text>

  <text x="232" y="100" class="sans" fill="#f8fafc" font-size="30" font-weight="800" letter-spacing="-0.025em">{{PROJECT_TITLE}}</text>
  <text x="232" y="128" class="sans" fill="#cbd5e1" font-size="14.5">{{SUBTITLE_LINE_1}}</text>
  <text x="232" y="150" class="sans" fill="#94a3b8" font-size="14.5">{{SUBTITLE_LINE_2}}</text>

  <!-- 3 Tactile 2.5D Feature Pills -->
  <g transform="translate(232, 172)">
    <rect x="0" y="2" width="{{P1_W}}" height="28" rx="9" fill="#050811"/>
    <rect x="0" y="0" width="{{P1_W}}" height="28" rx="9" fill="#131c2e" stroke="#26334d" stroke-width="1"/>
    <circle cx="14" cy="14" r="3.2" fill="{{ACCENT_BRIGHT}}"/>
    <text x="24" y="18" class="sans" fill="#e2e8f0" font-size="12" font-weight="600">{{PILL_1}}</text>

    <g transform="translate({{P2_X}}, 0)">
      <rect x="0" y="2" width="{{P2_W}}" height="28" rx="9" fill="#050811"/>
      <rect x="0" y="0" width="{{P2_W}}" height="28" rx="9" fill="#131c2e" stroke="#26334d" stroke-width="1"/>
      <circle cx="14" cy="14" r="3.2" fill="{{ACCENT_BRIGHT}}"/>
      <text x="24" y="18" class="sans" fill="#e2e8f0" font-size="12" font-weight="600">{{PILL_2}}</text>
    </g>

    <g transform="translate({{P3_X}}, 0)">
      <rect x="0" y="2" width="{{P3_W}}" height="28" rx="9" fill="#050811"/>
      <rect x="0" y="0" width="{{P3_W}}" height="28" rx="9" fill="#131c2e" stroke="#26334d" stroke-width="1"/>
      <circle cx="14" cy="14" r="3.2" fill="{{ACCENT_BRIGHT}}"/>
      <text x="24" y="18" class="sans" fill="#e2e8f0" font-size="12" font-weight="600">{{PILL_3}}</text>
    </g>
  </g>
</svg>
```

### 3B. `assets/readme-header-light.svg` Master Template

Keeps the signature dark sculpted `@alamehan` hardware keycap (so the white 2.5D porcelain blades + jewel orb retain crisp contrast!) mounted with a soft tactile drop-shadow on a warm porcelain showcase card (`#ffffff` → `#f7f3ec`):

```xml
<!-- Same kinetic <g> & keyframes as 3A, with Light Showcase Card colors:
  cardBg: #ffffff -> #fbf8f3 -> #f5efe6, outer stroke: #e5ddd2
  pedestal rect: fill="#efe9df" fill-opacity="0.72" stroke="#e2d9cb"
  keycap shadow under base: <rect x="4" y="9" width="88" height="84" rx="22" fill="#0f172a" opacity="0.16"/>
  title fill="#141118", subtitle1 fill="#3b3442", subtitle2 fill="#635a6b"
  tactile pills: lip fill="#ded6c9", face fill="#ffffff" stroke="#e2d9cb", text fill="#1e1924"
-->
```

---

## 4. Exact V2 Page Blueprint (`README.md` & `README.id.md`)

Follow this clean, calm, top-to-bottom rhythm in both files (zero extra clashing banner images!):

### Part 1 · Open Human Layer (Visible Immediately — Zero Code Blocks!)

1. **Hero `<picture>` + Centered 1-Line Action Bar:**
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
2. **Warm Human Story (`## Why {{Short Name}} Exists` / `## Kenapa {{Short Name}} Dibuat`):**
   - Write **2 short, vivid paragraphs** in everyday human language:
     - *Paragraph 1:* The real frustration people run into today (without blaming or using buzzwords).
     - *Paragraph 2:* The smart, thoughtful Product Design + Engineering approach this project takes and how it feels to use.
3. **Try or Explore Without Setup (`## Try It Right Now` / `## Langsung Coba Sekarang`):**
   - A clean 3–4 row Markdown table (`What you want to do` | `Where to go`) guiding non-technical visitors, designers, and engineers to immediate live links, offline launchers, or guides — **zero terminal commands here**.
4. **What Makes It Special (`## Highlights` / `## Keunggulan Utama`):**
   - 4 to 5 concise, benefit-first bullet points written in clear human prose (explain outcomes like *"Readable in every light and dark mood automatically"*, not raw variable names).

---

### Part 2 · Collapsible Developer & Specialist Layer (`<details>` Accordions)

Add a subtle section heading (`## For Developers & Technical Details` / `## Detail Teknis & Panduan Developer`) followed by **3 flush-left `<details>` accordions**.

> **CRITICAL GITHUB MARKDOWN RULE:**
> 1. `<details>`, `<summary>`, and `</details>` MUST have **0 leading spaces** (flush left).
> 2. Always leave **one empty blank line immediately after `</summary>`** AND **one empty blank line immediately before `</details>`** so Markdown tables, code blocks, and `mermaid` diagrams render cleanly on GitHub!

```markdown
<details>
<summary><strong>🛠️ Quickstart, Installation &amp; CLI Commands</strong></summary>

(Copy-paste terminal commands, framework setup, AI kit / Portable CSS instructions)

</details>

<details>
<summary><strong>🏗️ Architecture, Preset Matrix &amp; Repository Map</strong></summary>

(Mermaid architecture diagram + clean directory table + verification command, plus link to docs/SYSTEM-OVERVIEW.md when using Mode B)

</details>

<details>
<summary><strong>🧭 Design Boundaries, Trade-offs &amp; Replication Guide</strong></summary>

(Honest scope decisions, version pinning rationale, and links to AGENTS.md / CLAUDE.md / replication playbooks)

</details>
```

---

### Part 3 · Warm `@alamehan` Signature Footer

Close cleanly with:
- **English:** `Designed and built with care by **[M. Raihan Rafiiful Allaam (@alamehan)](https://alamehan.github.io)** — *Product Designer & Product Engineer*. Released under the [MIT License](./LICENSE).`
- **Indonesian:** `Dirancang dan dibangun sepenuh hati oleh **[M. Raihan Rafiiful Allaam (@alamehan)](https://alamehan.github.io)** — *Product Designer & Product Engineer*. Dirilis di bawah [Lisensi MIT](./LICENSE).`

---

## 5. Mandatory Verification Checklist Before Finishing

1. **Zero Marketing Fluff & Zero Jargon Leak Above the Fold:** Ensure the open upper half contains zero code fences and reads naturally to a non-engineer in both English and Indonesian (`"kamu"`, never `"Anda"` or `"Mas"`).
2. **Strict `<details>` Spacing & Link Check:** Verify programmatically that every `<details>` has blank lines after `</summary>` and before `</details>`, every relative link resolves on disk, and every `.svg` has zero unescaped `&`.
3. **Full-Page GitHub Light & Dark Visual QA:** Render the complete README (both Light `#ffffff` and Dark `#0d1117`, testing closed and opened `<details>` states + 2 animation timestamps on the SVG banner) in headless Chromium via Playwright and inspect the `.png` screenshots before committing.
