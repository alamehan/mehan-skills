---
name: alamehan-readme
description: >-
  Author signature, universal, zero-bias bilingual GitHub documentation (README.md
  in English + README.id.md in natural Indonesian) paired with adaptive Dark/Light
  @alamehan Console ASCII-monogram SVG header banners for any @alamehan repository
  (design system, web app, single-HTML tool, CLI/SDK, API, or portfolio monorepo).
  Activate when asked to create, standardize, or upgrade a repository README in the
  @alamehan style.
---

# `@alamehan` Universal GitHub README Standard (`alamehan-readme`)

> **Portable Single-File Skill & Master Prompt:** Self-contained in one `.md` file. Works automatically as a global Antigravity skill or when attached manually alongside any repository.

## 1. Philosophy & Synthesis

Every `@alamehan` repository opens on GitHub with an unmistakable, high-craft visual and editorial identity distilled from three proven foundations — with **zero legacy product bias**:

1. **`@alamehan · Console` Visual Signature:** Adaptive Dark/Light terminal SVG header (`<picture>`) pairing the **exact rasterized 3-blade `@alamehan` ASCII monogram + project-accent jewel orb** on the left with a crisp command-prompt metadata readout (`COMPLEX -> SIMPLE`) on the right.
2. **`SuperDocs` Editorial Clarity:** Concrete mechanisms over marketing fluff, structured scannability (10-second hook → 60-second quickstart → deep architecture), honest scope boundaries, and natural human transcreation.
3. **`Tools Factory` Goal Routing & `ZapRepo` Identity Discipline:** Visitor-first `"Your Goal -> Start Here"` routing table, crisp project metadata, and consistent `@alamehan` author signature — **without** forcing single-HTML rules, mascots, or framework assumptions onto unrelated stacks.

---

## 2. Pre-Flight Audit & Mandatory 4-File Deliverable Set

Before writing a single line:
1. **Audit Real Codebase Truth:** Read root manifests (`package.json`, `Cargo.toml`, `pyproject.toml`), `.github/workflows/`, `bin/` or `scripts/`, `docs/`, and actual directory tree. Never invent commands, flags, URLs, or features. *(If the repository structure itself is messy or has broken script mismatches, run `alamehan-repo-tidy` first.)*
2. **Identify Project Shape & Accent:**
   - `TYPE`: e.g. `Design System`, `Web Application`, `Single-File Offline Tool`, `CLI & SDK`, `Monorepo Ecosystem`, `API Service`.
   - `ACCENT`: Pick the project's authentic primary brand hex (e.g. `#e0366b` strawberry-berry for Mehan Design System, `#3b82f6` sapphire blue for Tools Factory / general engineering repos, `#10b981` emerald, `#f59e0b` amber, `#7c3aed` violet) with accessible Light-mode (`ACCENT_LIGHT`) and Dark-mode (`ACCENT_DARK`) shades.
3. **Emit All 4 Synchronized Files:**
   - `assets/readme-header-dark.svg` (Dark console banner — `#0b101b` obsidian phosphor frame)
   - `assets/readme-header-light.svg` (Light console banner — `#fcfaf7` warm porcelain frame)
   - `README.md` (Primary global English edition)
   - `README.id.md` (1:1 structural parity in warm, natural Indonesian using `"kamu"` — never `"Anda"` or `"Mas"`)

---

## 3. Adaptive `@alamehan · Console` ASCII SVG Header Templates

GitHub strips `<script>` inside SVGs, but natively renders local repository SVGs via `<picture><source media="(prefers-color-scheme: dark)" ...>` with crisp system monospace, vector gradients, radial glows, and pure-CSS `@keyframes` (respecting `prefers-reduced-motion: reduce`).

The 13-row ASCII emblem below is mathematically rasterized from the canonical `@alamehan` 3-blade vector monogram:
- `.f` = Outer rounded corner frame
- `.b1`, `.b2`, `.b3` = Cascading 3 wing louvers
- `.orb` = Signature bottom-right jewel orb tinted with the project's accent color!

**Customization Slots (XML-escape `&` as `&amp;`, `<` as `&lt;`, `>` as `&gt;`):**
- `{{REPO_SLUG}}`: e.g. `mehan-design-system`
- `{{PROJECT_TITLE}}`: e.g. `Mehan Design System` (keep ≤ 32 chars so it fits `viewBox="0 0 920 264"` cleanly)
- `{{TAGLINE_LINE_1}}` & `{{TAGLINE_LINE_2}}`: Crisp 2-line plain-English essence (≤ 56 chars per line)
- `{{META_TYPE}}`: e.g. `Tactile UI & UX System`
- `{{META_STACK}}`: e.g. `Meta Astryx · React 19 · Portable CSS`
- `{{META_ENTRY}}`: e.g. `Web Studio · Offline STUDIO.html · CLI`
- `{{ACCENT_DARK}}` / `{{ACCENT_GLOW_DARK}}`: Vibrant dark-mode jewel hex (e.g. `#ff6b93` / `#e0366b`)
- `{{ACCENT_LIGHT}}` / `{{ACCENT_GLOW_LIGHT}}`: High-contrast light-mode jewel hex (e.g. `#d42a5f` / `#ff7597`)

### 3A. `assets/readme-header-dark.svg` Template

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 264" width="920" height="264" role="img" aria-label="{{PROJECT_TITLE}} — @alamehan console banner">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#0e1322"/>
      <stop offset="100%" stop-color="#090c15"/>
    </linearGradient>
    <radialGradient id="orbGlow" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="{{ACCENT_GLOW_DARK}}" stop-opacity="0.38"/>
      <stop offset="100%" stop-color="{{ACCENT_GLOW_DARK}}" stop-opacity="0"/>
    </radialGradient>
    <style>
      .mono { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace; }
      .sans { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif; }
      .f  { fill: #e2e8f0; font-weight: 700; }
      .w  { fill: #64748b; }
      .b1 { fill: #f8fafc; font-weight: 700; }
      .b2 { fill: #cbd5e1; font-weight: 700; }
      .b3 { fill: #94a3b8; font-weight: 700; }
      .orb { fill: {{ACCENT_DARK}}; font-weight: 700; }
      .dim { fill: #64748b; }
      .key { fill: #94a3b8; font-weight: 600; }
      .val { fill: #e2e8f0; }
      .acc { fill: {{ACCENT_DARK}}; font-weight: 700; }
      @keyframes blink { 0%, 49% { opacity: 1; } 50%, 100% { opacity: 0; } }
      @keyframes pulse { 0%, 100% { opacity: 0.76; } 50% { opacity: 1; } }
      .cur { animation: blink 1.15s steps(1) infinite; }
      .glow { animation: pulse 3.2s ease-in-out infinite; }
      @media (prefers-reduced-motion: reduce) { .cur, .glow { animation: none; } }
    </style>
  </defs>

  <!-- Outer Terminal Window -->
  <rect x="2" y="2" width="916" height="260" rx="16" fill="url(#bg)" stroke="#1e293b" stroke-width="1.5"/>
  <path d="M2 18C2 9.16 9.16 2 18 2H902C910.84 2 918 9.16 918 18V40H2V18Z" fill="#111827"/>
  <line x1="2" y1="40" x2="918" y2="40" stroke="#1e293b" stroke-width="1"/>

  <!-- Window Controls and Title Bar -->
  <circle cx="24" cy="21" r="5.5" fill="#ef4444" opacity="0.85"/>
  <circle cx="42" cy="21" r="5.5" fill="#f59e0b" opacity="0.85"/>
  <circle cx="60" cy="21" r="5.5" fill="#10b981" opacity="0.85"/>
  <text x="460" y="25" text-anchor="middle" class="mono dim" font-size="12">@alamehan&#160;·&#160;console&#160;—&#160;{{REPO_SLUG}}</text>
  <text x="896" y="25" text-anchor="end" class="mono acc" font-size="11">COMPLEX&#160;-&gt;&#160;SIMPLE</text>

  <!-- Left Stage: Recessed ASCII Monogram Well -->
  <rect x="24" y="56" width="256" height="188" rx="12" fill="#070a12" stroke="#1e293b" stroke-width="1"/>
  <circle cx="212" cy="206" r="42" fill="url(#orbGlow)" class="glow"/>
  <g class="mono" font-size="11.5">
    <text x="54" y="77"><tspan class="f">&#160;&#160;&#160;:=++++++++++++++++++-.&#160;&#160;&#160;</tspan></text>
    <text x="54" y="90"><tspan class="f">&#160;&#160;*@@@@@@@@@@@@@@@@@@@@@@-&#160;&#160;</tspan></text>
    <text x="54" y="103"><tspan class="f">&#160;:@@@@@@@@@@@@@@@@@@@@@@@@&#160;&#160;</tspan></text>
    <text x="54" y="116"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="b1">::+&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="129"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="b1">:*%@@%:&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="142"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="b1">:%@@%*:&#160;&#160;&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="155"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="b2">+**+-&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="168"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="b2">.+%@@@+&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="181"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;</tspan><tspan class="b2">+@@%*=.&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="194"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;</tspan><tspan class="b3">:+*++-</tspan><tspan>&#160;&#160;&#160;&#160;</tspan><tspan class="orb">.=++=:&#160;&#160;</tspan></text>
    <text x="54" y="207"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;</tspan><tspan class="b3">-#@@@#:</tspan><tspan>&#160;&#160;&#160;&#160;</tspan><tspan class="orb">:%@@@@@-&#160;</tspan></text>
    <text x="54" y="220"><tspan class="f">&#160;&#160;*@@@*</tspan><tspan class="b3">%@%#=:&#160;</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="orb">#@@@@%:&#160;</tspan></text>
    <text x="54" y="233"><tspan class="w">&#160;&#160;&#160;:=+=:</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="orb">.:::&#160;&#160;&#160;</tspan></text>
  </g>

  <!-- Right Stage: Command Prompt and Identity Readout -->
  <text x="306" y="76" class="mono" font-size="12.5"><tspan class="acc">❯</tspan><tspan class="val">&#160;alamehan&#160;inspect&#160;</tspan><tspan class="acc">{{REPO_SLUG}}</tspan><tspan class="dim">&#160;--lang=en,id</tspan></text>

  <text x="306" y="112" class="sans" fill="#f8fafc" font-size="26" font-weight="800" letter-spacing="-0.02em">{{PROJECT_TITLE}}</text>
  <text x="306" y="136" class="sans" fill="#cbd5e1" font-size="13.5">{{TAGLINE_LINE_1}}</text>
  <text x="306" y="155" class="sans" fill="#94a3b8" font-size="13.5">{{TAGLINE_LINE_2}}</text>

  <line x1="306" y1="171" x2="892" y2="171" stroke="#1e293b" stroke-width="1"/>

  <g class="mono" font-size="12">
    <text x="306" y="193"><tspan class="key">TYPE&#160;&#160;&#160;</tspan><tspan class="dim">│&#160;</tspan><tspan class="val">{{META_TYPE}}</tspan></text>
    <text x="306" y="213"><tspan class="key">STACK&#160;&#160;</tspan><tspan class="dim">│&#160;</tspan><tspan class="val">{{META_STACK}}</tspan></text>
    <text x="306" y="233"><tspan class="key">ENTRY&#160;&#160;</tspan><tspan class="dim">│&#160;</tspan><tspan class="val">{{META_ENTRY}}</tspan><tspan class="acc cur">&#160;█</tspan></text>
  </g>
</svg>
```

### 3B. `assets/readme-header-light.svg` Template

Identical `viewBox="0 0 920 264"` geometry and `&#160;` space-locked ASCII coordinates, tuned with a warm porcelain console frame and high-contrast slate typography:

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 920 264" width="920" height="264" role="img" aria-label="{{PROJECT_TITLE}} — @alamehan console banner">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#fffdfb"/>
      <stop offset="100%" stop-color="#f8f3ed"/>
    </linearGradient>
    <radialGradient id="orbGlow" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="{{ACCENT_GLOW_LIGHT}}" stop-opacity="0.30"/>
      <stop offset="100%" stop-color="{{ACCENT_GLOW_LIGHT}}" stop-opacity="0"/>
    </radialGradient>
    <style>
      .mono { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace; }
      .sans { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif; }
      .f  { fill: #18131a; font-weight: 700; }
      .w  { fill: #786f7c; }
      .b1 { fill: #18131a; font-weight: 700; }
      .b2 { fill: #3b3240; font-weight: 700; }
      .b3 { fill: #584d5e; font-weight: 700; }
      .orb { fill: {{ACCENT_LIGHT}}; font-weight: 700; }
      .dim { fill: #6e6473; }
      .key { fill: #514657; font-weight: 600; }
      .val { fill: #18131a; }
      .acc { fill: {{ACCENT_LIGHT}}; font-weight: 700; }
      @keyframes blink { 0%, 49% { opacity: 1; } 50%, 100% { opacity: 0; } }
      @keyframes pulse { 0%, 100% { opacity: 0.76; } 50% { opacity: 1; } }
      .cur { animation: blink 1.15s steps(1) infinite; }
      .glow { animation: pulse 3.2s ease-in-out infinite; }
      @media (prefers-reduced-motion: reduce) { .cur, .glow { animation: none; } }
    </style>
  </defs>

  <!-- Outer Terminal Window -->
  <rect x="2" y="2" width="916" height="260" rx="16" fill="url(#bg)" stroke="#e5ddd3" stroke-width="1.5"/>
  <path d="M2 18C2 9.16 9.16 2 18 2H902C910.84 2 918 9.16 918 18V40H2V18Z" fill="#f3ece3"/>
  <line x1="2" y1="40" x2="918" y2="40" stroke="#e5ddd3" stroke-width="1"/>

  <!-- Window Controls and Title Bar -->
  <circle cx="24" cy="21" r="5.5" fill="#ef4444" opacity="0.85"/>
  <circle cx="42" cy="21" r="5.5" fill="#f59e0b" opacity="0.85"/>
  <circle cx="60" cy="21" r="5.5" fill="#10b981" opacity="0.85"/>
  <text x="460" y="25" text-anchor="middle" class="mono dim" font-size="12">@alamehan&#160;·&#160;console&#160;—&#160;{{REPO_SLUG}}</text>
  <text x="896" y="25" text-anchor="end" class="mono acc" font-size="11">COMPLEX&#160;-&gt;&#160;SIMPLE</text>

  <!-- Left Stage: Recessed ASCII Monogram Well -->
  <rect x="24" y="56" width="256" height="188" rx="12" fill="#f3ede4" stroke="#e3d9cd" stroke-width="1"/>
  <circle cx="212" cy="206" r="42" fill="url(#orbGlow)" class="glow"/>
  <g class="mono" font-size="11.5">
    <text x="54" y="77"><tspan class="f">&#160;&#160;&#160;:=++++++++++++++++++-.&#160;&#160;&#160;</tspan></text>
    <text x="54" y="90"><tspan class="f">&#160;&#160;*@@@@@@@@@@@@@@@@@@@@@@-&#160;&#160;</tspan></text>
    <text x="54" y="103"><tspan class="f">&#160;:@@@@@@@@@@@@@@@@@@@@@@@@&#160;&#160;</tspan></text>
    <text x="54" y="116"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="b1">::+&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="129"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="b1">:*%@@%:&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="142"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="b1">:%@@%*:&#160;&#160;&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="155"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="b2">+**+-&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="168"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="b2">.+%@@@+&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="181"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;&#160;</tspan><tspan class="b2">+@@%*=.&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan></text>
    <text x="54" y="194"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;&#160;&#160;</tspan><tspan class="b3">:+*++-</tspan><tspan>&#160;&#160;&#160;&#160;</tspan><tspan class="orb">.=++=:&#160;&#160;</tspan></text>
    <text x="54" y="207"><tspan class="f">&#160;:@@@@+</tspan><tspan>&#160;</tspan><tspan class="b3">-#@@@#:</tspan><tspan>&#160;&#160;&#160;&#160;</tspan><tspan class="orb">:%@@@@@-&#160;</tspan></text>
    <text x="54" y="220"><tspan class="f">&#160;&#160;*@@@*</tspan><tspan class="b3">%@%#=:&#160;</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="orb">#@@@@%:&#160;</tspan></text>
    <text x="54" y="233"><tspan class="w">&#160;&#160;&#160;:=+=:</tspan><tspan>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</tspan><tspan class="orb">.:::&#160;&#160;&#160;</tspan></text>
  </g>

  <!-- Right Stage: Command Prompt and Identity Readout -->
  <text x="306" y="76" class="mono" font-size="12.5"><tspan class="acc">❯</tspan><tspan class="val">&#160;alamehan&#160;inspect&#160;</tspan><tspan class="acc">{{REPO_SLUG}}</tspan><tspan class="dim">&#160;--lang=en,id</tspan></text>

  <text x="306" y="112" class="sans" fill="#18131a" font-size="26" font-weight="800" letter-spacing="-0.02em">{{PROJECT_TITLE}}</text>
  <text x="306" y="136" class="sans" fill="#3b3240" font-size="13.5">{{TAGLINE_LINE_1}}</text>
  <text x="306" y="155" class="sans" fill="#584d5e" font-size="13.5">{{TAGLINE_LINE_2}}</text>

  <line x1="306" y1="171" x2="892" y2="171" stroke="#e5ddd3" stroke-width="1"/>

  <g class="mono" font-size="12">
    <text x="306" y="193"><tspan class="key">TYPE&#160;&#160;&#160;</tspan><tspan class="dim">│&#160;</tspan><tspan class="val">{{META_TYPE}}</tspan></text>
    <text x="306" y="213"><tspan class="key">STACK&#160;&#160;</tspan><tspan class="dim">│&#160;</tspan><tspan class="val">{{META_STACK}}</tspan></text>
    <text x="306" y="233"><tspan class="key">ENTRY&#160;&#160;</tspan><tspan class="dim">│&#160;</tspan><tspan class="val">{{META_ENTRY}}</tspan><tspan class="acc cur">&#160;█</tspan></text>
  </g>
</svg>
```

---

## 4. The Universal 7-Block `@alamehan` README Spine

Structure both `README.md` (English) and `README.id.md` (Indonesian) around these **7 adaptable blocks**:

### Block 1 · Console Banner + Language Switcher & Primary Links
Open directly with the adaptive `<picture>` banner followed immediately by the language bar and primary live/offline links:

```markdown
<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/readme-header-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="./assets/readme-header-light.svg" />
    <img alt="{{PROJECT_TITLE}} — @alamehan console banner" src="./assets/readme-header-light.svg" width="100%" />
  </picture>

  <p>
    <strong>English</strong> · <a href="./README.id.md">Bahasa Indonesia →</a>
    &nbsp;|&nbsp;
    <a href="{{PRIMARY_URL}}">Live Demo</a> · <a href="./LICENSE">MIT License</a>
  </p>
</div>
```
*(In `README.id.md`, flip the active pill to `<a href="./README.md">← English</a> · <strong>Bahasa Indonesia</strong>`.)*

### Block 2 · 10-Second Summary (`> [!TIP]`) & Goal-First Routing Table
- Write one crisp `> [!TIP]` callout explaining **who this project helps, what concrete problem it solves, and the fastest way to try it right now**.
- Follow with a `Your Goal -> Start Here` (`Tujuanmu -> Mulai dari Sini`) Markdown table routing real visitor personas (e.g. *Explore right now without installing*, *Use in a project / workflow*, *Understand architecture & design decisions*, *Extend or replicate for a new domain*, *AI Coding Agents*) to exact links or files.

### Block 3 · Why It Exists (Problem → Smart Leverage → Outcome)
- State the real friction people face today, the deliberate architectural decision this project makes, and the tangible outcome — backed by a clean visual diagram (`./assets/*.svg` or GitHub `mermaid`) or crisp comparison table.

### Block 4 · Start in 60 Seconds
- Always present the **lowest-friction path first** (Live URL, offline single-file HTML, or 1-click export), followed by clean copy-pasteable terminal commands for developers.

### Block 5 · Signature Capabilities (Adapted to Project Shape)
Present 4–6 concrete, bold-led capability highlights tailored to the repo's real shape:
- **Design System:** Perceptual color/contrast engine, ready-made visual themes, accessible primitive + extension layers, multi-target exports (AI Kit, React, Portable CSS, Figma W3C tokens).
- **Web App / Single-HTML Tool:** Core workflow stages, offline/privacy guarantees, export formats, keyboard & mobile ergonomics.
- **CLI / SDK / API:** Command matrix or API surface, zero-config defaults, validation/type safety, integration examples.
- **Monorepo / Portfolio:** Layered ecosystem map, flagship case studies/tools, quality gates, replication paths.

### Block 6 · System Architecture & Clean Repository Map
- Include one concise ```` ```mermaid ```` `flowchart LR` or `flowchart TB` (quoting node labels with special characters: `id["Label (Detail)"]`).
- Follow with a clean annotated directory tree or table matching the **actual** repository folders 1:1, plus the single verification command (`pnpm verify`, `cargo test`, `pytest`, etc.) and any cross-reference to deep docs (such as `./docs/...`, `./AGENTS.md`, `./CLAUDE.md`).

### Block 7 · Honest Scope (`<details>`) + `@alamehan` Author Signature & License
- Include a brief `<details><summary><strong>Scope, Trade-offs & Design Boundaries</strong></summary>...</details>` block stating clearly what the project intentionally focuses on vs. delegates (builds immediate senior-engineering trust).
- Close with the signature `@alamehan` footer:
  - English: `Crafted with Product Design & Engineering care by **[M. Raihan Rafiiful Allaam (@alamehan)](https://alamehan.github.io)** — *Product Designer & Product Engineer*.`
  - Indonesian: `Dirancang dan dibangun sepenuh hati oleh **[M. Raihan Rafiiful Allaam (@alamehan)](https://alamehan.github.io)** — *Product Designer & Product Engineer*.`
  - License links (`./LICENSE` and `./THIRD_PARTY_NOTICES.md` if present).

---

## 5. Five Binding Writing & Verification Laws

1. **Zero Marketing Fluff:** Never write *"revolutionary"*, *"magical"*, *"world-class"*, or *"next-gen"*. Name the real mechanism instead.
2. **Evergreen Prose:** Avoid temporal words (*"new"*, *"recently added"*) and brittle micro-tallies that go stale on routine updates; never present internal plumbing (*"uses localStorage"*, *"no API keys"*) as fake user features unless offline privacy is genuinely core to the workflow.
3. **Natural Bilingual Transcreation (`EN` ↔ `ID`):** `README.id.md` must read like warm, crisp, modern Indonesian written by a thoughtful Product Designer using *"kamu"* (never *"Anda"*, never *"Mas"*, never stiff literal translation), while keeping 100% identical headings, tables, Mermaid diagrams, and relative links.
4. **Zero Broken Links or Malformed XML:** Verify programmatically that every relative `[...](./...)` link in `README.md` and `README.id.md` resolves on disk, and parse both `.svg` files as strict XML (`&amp;`, `&lt;`, `&gt;`).
5. **Visual QA Render Check:** Whenever headless Chromium / Playwright is available, render `README` header SVGs in both Light and Dark themes (`920×264`) and inspect the screenshots to confirm crisp ASCII alignment, zero text clipping, and strong contrast.
