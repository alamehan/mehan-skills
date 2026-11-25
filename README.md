<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/readme-header-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="./assets/readme-header-light.svg" />
    <img alt="Mehan Skills — @alamehan 2.5D kinetic banner" src="./assets/readme-header-light.svg" width="100%" />
  </picture>

  <p>
    <strong>English</strong> · <a href="./README.id.md">Bahasa Indonesia →</a>
    &nbsp;&nbsp;·&nbsp;&nbsp;
    <a href="./skills"><strong>✨ Browse Skills</strong></a> ·
    <a href="https://alamehan.github.io">Portfolio</a> ·
    <a href="./LICENSE">MIT License</a>
  </p>
</div>

> ⚡ Single-file playbooks that teach AI coding agents to untangle messy repos & write human-first bilingual docs — crafted by @alamehan

---

## Why Mehan Skills Exists

Every time you start a new project or open a fresh AI chat session, repeating the same standards — how a repository should be organized without breaking working code, or how documentation should speak clearly to both everyday readers and engineers — takes time and easily drifts when those instructions only live inside old conversations.

**Mehan Skills** turns repeatable Product Design and Product Engineering workflows by **[M. Raihan Rafiiful Allaam (`@alamehan`)](https://alamehan.github.io)** into **self-contained, single-file playbooks**. Each skill lives inside one `.md` file that your AI coding assistant can load automatically across every workspace, or that you can attach directly inside any web chat whenever you need consistent craft.

---

## Try or Explore Right Now

| What you want to do | Where to go |
|---|---|
| **Clean up a messy project folder safely without breaking anything** | Open **[`alamehan-repo-tidy`](./skills/alamehan-repo-tidy/SKILL.md)** |
| **Create a welcoming, bilingual GitHub README with a 2.5D animated header** | Open **[`alamehan-readme`](./skills/alamehan-readme/SKILL.md)** |
| **See other products, design systems & case studies by `@alamehan`** | Visit **[alamehan.github.io](https://alamehan.github.io)** |

---

## Highlights

- **One File, Complete Clarity:** Every skill is written inside a single `SKILL.md` file with all rules, visual templates, and quality checks included — nothing fragmented across extra folders.
- **Safe Repository Tidying (`alamehan-repo-tidy`):** Teaches AI agents to lock critical paths first, untangle messy scripts and folders, update every affected reference, and verify that everything still builds and passes tests.
- **Human-First Bilingual Documentation (`alamehan-readme`):** Guides AI agents to lead with a clear, approachable story, real embedded designer typography (`Bricolage Grotesque` + `Figtree` + `Geist Mono`), and collapsible developer drawers — paired in English and natural Indonesian.
- **Works Wherever You Work:** Auto-activates globally in local AI IDEs like Antigravity, or works by simply attaching one `.md` file in Claude, ChatGPT, Cursor, or Codex.

---

## For Developers & Technical Details

<details>
<summary><strong>🛠️ Quick Setup — Global Auto-Discovery &amp; Direct File Use</strong></summary>

### Option 1 · Automatic Global Discovery (Antigravity / Gemini)
Clone this repository once and link `./skills` to `~/.gemini/config/skills` so every skill inside this vault activates automatically across all local workspaces:

```powershell
# Windows PowerShell (no Administrator rights needed)
git clone https://github.com/alamehan/mehan-skills.git
cd mehan-skills
New-Item -ItemType Junction -Path "$HOME\.gemini\config\skills" -Target "$PWD\skills"
```

```bash
# macOS / Linux
git clone https://github.com/alamehan/mehan-skills.git
cd mehan-skills
ln -s "$PWD/skills" "$HOME/.gemini/config/skills"
```

### Option 2 · Direct Attachment (Claude Web, ChatGPT, Cursor, Codex)
Attach the single `SKILL.md` file from [`skills/`](./skills) alongside your target repository and ask the assistant to run that workflow.

</details>

<details>
<summary><strong>🏗️ Skill Catalog, Architecture &amp; Repository Map</strong></summary>

```mermaid
flowchart LR
  vault["mehan-skills<br/>Single-File Skill Vault"] --> tidy["skills/alamehan-repo-tidy/SKILL.md"]
  vault --> rdm["skills/alamehan-readme/SKILL.md"]
  vault --> next["skills/<next-skill>/SKILL.md"]
  tidy --> global["~/.gemini/config/skills<br/>(Global Auto-Discovery)"]
  rdm --> global
  next --> global
```

| Path | Role |
|---|---|
| [`skills/alamehan-repo-tidy/SKILL.md`](./skills/alamehan-repo-tidy/SKILL.md) | Non-destructive repository untangling, symmetric folder grouping, blast-radius reference tracing, and build/test parity verification. |
| [`skills/alamehan-readme/SKILL.md`](./skills/alamehan-readme/SKILL.md) | Adaptive `Porcelain SaaS` 2.5D kinetic `@alamehan` SVG templates (with embedded designer fonts), GitHub About hook, and progressive `EN`/`ID` README rules. |
| [`assets/`](./assets) | Adaptive Dark and Light `Porcelain SaaS` 2.5D kinetic `@alamehan` SVG showcase banners. |
| [`AGENTS.md`](./AGENTS.md) | Authoring rules (`1 Skill = 1 SKILL.md`, clean portable paths, and bilingual catalog sync). |

</details>

<details>
<summary><strong>🧭 Authoring Rules &amp; Design Boundaries</strong></summary>

- **Strictly Single-File Portability:** Each skill embeds its own instructions and checklists inline inside `skills/<slug>/SKILL.md` so it never breaks when shared or attached as a standalone file.
- **Portable Paths Only:** Snippets use `$PWD` and `$HOME` rather than machine-specific drive paths so cloning works identically on Windows, macOS, and Linux. See [`AGENTS.md`](./AGENTS.md) when adding new skills.

</details>

---

Designed and built with care by **[M. Raihan Rafiiful Allaam (`@alamehan`)](https://alamehan.github.io)** — *Product Designer & Product Engineer*. Released under the [MIT License](./LICENSE).
