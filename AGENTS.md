# AGENTS.md — Multi-Agent Entrypoint for `mehan-skills`

> **Applies to:** Antigravity / Gemini, Claude Code, OpenAI Codex, Cursor, Windsurf, and any AI coding agent authoring or updating skills inside **`mehan-skills`**.

## 1. Read Order

1. **[`README.md`](./README.md)** *(and **[`README.id.md`](./README.id.md)**)* — Skill catalog, global mounting instructions, and repository overview.
2. **[`skills/`](./skills)** — Individual skill directories (`skills/<skill-slug>/SKILL.md`).

---

## 2. Three Binding Authoring Rules

| Rule | Mandatory Standard |
|---|---|
| **1 · Single-File Portability (`1 Skill = 1 SKILL.md`)** | Every skill must live completely inside `skills/<skill-slug>/SKILL.md` (embedding any required templates, schemas, and verification checklists inline) so it works both via global auto-discovery (`~/.gemini/config/skills`) and when attached manually as a single `.md` file in any AI chat. |
| **2 · Valid Frontmatter & Clean Public Hygiene** | Start every `SKILL.md` with YAML frontmatter declaring `name` (lowercase hyphenated, matching `<skill-slug>`) and a third-person `description` stating **what** it does and **when** to activate it. Never include local machine paths or realistic provider secret prefixes. |
| **3 · Bilingual Catalog Parity (`EN` & `ID`)** | Whenever a skill is added, renamed, or retired under [`skills/`](./skills), update both [`README.md`](./README.md) and [`README.id.md`](./README.id.md) in the same commit and verify every relative link resolves cleanly. |
