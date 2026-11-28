---
name: alamehan-repo-tidy
description: >-
  Non-destructively untangle, reorganize, and standardize any software repository
  (monorepo, web app, single-HTML tool, design system, CLI/SDK, or backend service)
  while preserving 100% build, test, CI, export, and runtime parity. Activate this
  skill when the user asks to clean up, reorganize, untangle, or standardize a messy
  repository structure ("rapikan repo", "bereskan kabel kusut", "perapihan total").
---

# `@alamehan` Universal Repo Tidy & Untangler (`alamehan-repo-tidy`)

> **Portable Single-File Skill & Master Prompt:** Works natively as an auto-discovered skill or when attached as this single `.md` file alongside any target repository.

## Core Mandate — Clean Structure, Zero Broken Wires

Naive repository cleanups break working software because they move files before mapping the hidden contracts that depend on those paths. Every cleanup executed with this skill obeys one non-negotiable law:

> **Map every locked contract first, untangle internal structure cleanly, rewrite 100% of affected references atomically, and prove green-before / green-after parity across builds, types, tests, CI workflows, and runtime entrypoints.**

---

## Phase 1 — Sacred Contract & Entrypoint Lock (Before Moving Any File)

Inspect the repository root, manifests, build scripts, bundler configs, test configs, and `.github/workflows/` first. Classify every top-level and package-level path into two buckets:

1. **Locked Public & Framework Contracts (Keep Path Intact):**
   - Framework-mandated directories (`app/`, `pages/`, `public/`, `src/routes/`, `Cargo.toml`, `go.mod`, `pyproject.toml`, `astryx.integration.mjs` provider directories).
   - Public entrypoints and offline launchers (`index.html`, `STUDIO.html`, `WORKSHOP.html`, `README.md`, `README.id.md`, `LICENSE`, `AGENTS.md`, `CLAUDE.md`).
   - Published package contracts (`package.json` `"exports"`, `"main"`, `"types"`, `"bin"`, `"files"`) and public release URLs (`release/*.tgz`, GitHub Pages upload paths in `.github/workflows/*.yml`).
2. **Movable Internal Structure (Safe to Reorganize with Full Reference Trace):**
   - Loose OS helper scripts cluttering the root (`.cmd`, `.bat`, `.sh`, `.command`, scratch `.mjs`/`.py` helpers).
   - Cross-package build spaghetti (sub-packages reaching into `../sibling` or `../../release`).
   - Half-grouped source trees (mixing grouped folders like `src/catalog/` with loose sibling views/dialogs at `src/` root).
   - Flat mixed test directories dumping unit tests and browser E2E specs into a single ungrouped pile.
   - Redundant root config files, stale build/test output folders (`test-results/`, duplicate temporary bundles), and drifted script names or descriptions.

---

## Phase 2 — Pre-Tidy Baseline Snapshot

Before modifying structure:
1. Check `git status --short` so pre-existing uncommitted work is never lost or confused with generated debris.
2. Note the current build, typecheck, linter, unit-test, and E2E commands so post-tidy verification can prove 1:1 or better health.

---

## Phase 3 — The 6 Surgical Untangling Operations

Execute all structural improvements coherently rather than leaving half-finished migrations:

### 1. Root Surface Minimalism
- Keep the repository root limited to true top-level manifests, primary offline/app entrypoints, governance docs, and clean top-level directories (`apps/`, `packages/`, `src/`, `assets/`, `bin/`, `docs/`, `release/`, `scripts/`, `tests/`).
- Relocate loose OS convenience launchers (`dev-*.cmd`, `verify-*.command`, setup wrappers) into `scripts/` (updating `cd /d "%~dp0.."` or `cd "$(dirname "$0")/.."` inside moved scripts so their working directory still resolves to the repository root!).
- Consolidate redundant root configs where safe (for example, keeping a clean root `tsconfig.json` as the shared base and placing test-only path aliases in `tests/tsconfig.json` so package `.d.ts` bundlers never inherit test path overrides).
- Delete leftover temporary directories (`test-results/`, `playwright-report/`, intermediate `dist-single/` copies) and configure test runners to write transient artifacts to `os.tmpdir()` or gitignored cache paths so running tests never re-dirties the repository root.

### 2. Decouple Cross-Boundary Build Spaghetti
- Each package or module in `packages/*` or `apps/*` must build **only its own `dist/` output**.
- Never let a sub-package build script reach sideways into `../sibling` or upward into `../../release`. Extract cross-package packaging (such as running `npm pack` across multiple workspaces, copying portable bundles into `release/`, or emitting root single-file HTML launchers) into a dedicated root orchestrator script (`scripts/pack-release.mjs` or equivalent) wired cleanly into the root `build` script.
- Verify `.github/workflows/*.yml` still runs cleanly with the decoupled build steps.

### 3. Symmetric Source & Test Topology
- **Source symmetry:** Inside application `src/` trees, avoid mixing domain subfolders with loose peer views and dialogs at `src/` root. Group top-level tab/page screens into `src/views/` and shared shell elements/modals into `src/components/`, keeping `src/` root crisp (`App.tsx`, `main.tsx`, global state, i18n, and stylesheet).
- **Test symmetry:** Split mixed test folders into clear suites such as `tests/unit/` (fast unit, math, CLI, and repo-governance proofs) and `tests/e2e/` (browser, visual, and accessibility specs). Update test runner configs (`vitest.config.*`, `playwright.config.*`, `tests/tsconfig.json`) to match the new subdirectories.

### 4. Exhaustive Blast-Radius Reference Trace
Whenever any file or directory moves, search the **entire repository** before running builds and update every reference in one atomic pass:
- Static and dynamic ES/TS imports (`from './...'`, `from '../...'`, `import('...')`), `import.meta.dirname` relative depth (`..` vs `../..`).
- CSS `url(...)` paths, HTML `<script>`/`<link>` tags, SVG/image asset references.
- `package.json` `"scripts"`, `"files"`, `"exports"`, `"bin"`, bundler entrypoints (`vite.config.*`, `tsup.config.*`), and CI workflow YAML paths.
- Relative Markdown links (`[label](./path)`) across `README.md`, `README.id.md`, `AGENTS.md`, `CLAUDE.md`, `docs/`, and in-app help copy.

### 5. Command, CLI & Metadata Convergence
- Make root manifest script names (`build`, `dev`, `typecheck`, `test:unit`, `test:e2e`, `verify`) match `AGENTS.md`, `CLAUDE.md`, `README.md`, and CI workflows **1:1** — zero "ghost commands" documented in Markdown that fail in the terminal.
- Remove hardcoded repository URLs or scopes inside helper CLIs when they can be read dynamically from root `package.json` (`repository.url`, workspace `@scope/*`).
- Purge hardcoded local machine paths (such as Windows drive roots or personal user home directories) and stale early-iteration descriptions or counts across `package.json` and sub-package `README.md` files.

### 6. Automated Repo-Integrity Lock
- If the repository has a unit test suite, include or update a fast structural test asserting that:
  1. Every exported file in `package.json#exports` exists on disk after build.
  2. Every relative link (`](./...)`) in root governance/README docs resolves to an existing file or folder.
  3. Zero source or documentation files leak hardcoded local drive paths.

---

## Phase 4 — Mandatory Post-Tidy Parity Gate

Never conclude a repository cleanup on file moves alone. Run the complete verification chain sequentially:

1. **Full Build & Packaging:** Rebuild all packages, apps, single-file bundles, and `release/` artifacts from scratch.
2. **Static Analysis:** Run strict typechecking (`tsc --noEmit` / `mypy` / `cargo check` / `go vet`) and framework/provider linters (`astryx integration check --strict`, ESLint, etc.) with `0` errors.
3. **Unit & E2E Suites:** Run all unit tests and browser/integration tests to `100%` pass.
4. **Clean Working Tree Check:** Run `git status --short` to confirm zero untracked temporary build/test debris remains on disk.
