# Bauhaus Neo-Modernism — Project Overview

This repository contains a design research hub and a small prototype website exploring Bauhaus and neo-modernist principles on the web.

Purpose
- Collect research and technical design specifications for a Neo‑Modernism design system.
- Provide a lightweight HTML/CSS prototype that demonstrates the visual system and interaction patterns.

Repository layout (top-level)
- `bauhaus-website/` — Prototype website (HTML/CSS/JS). (In some commits this folder was tracked as a submodule.)
- `bauhaus-neo-modernism-research/` — In-depth research: references, technical specs, visual resources.

Note: Additional style guides, templates and docs referenced in earlier drafts live inside the `bauhaus-neo-modernism-research/` folder in this checkout; use `ls` to inspect nested folders.

How it was built
- Plain HTML, modular CSS, and lightweight JavaScript for small interactions.
- CSS variables and token files under `bauhaus-website/css/` implement colors, spacing, and type scale.
- Iterative design: research → design system → prototype pages (hero, poster cards, timeline, contact form).
- Commits include many focused visual iterations and accessibility improvements.

What you'll find in the prototype (`bauhaus-website`)
- `index.html` — single-page prototype that demonstrates the layout, poster cards, and hero section.
- `css/` — design tokens, layout, components, and decorative styles.
- `images/` — media used in the prototype (may be empty if the site is a submodule placeholder).
- `js/main.js` — small scripts for mobile menu and interactions.

Run locally (quick)
1. From repository root, serve files with Python:

```bash
# Python 3
python -m http.server 8000
# open http://localhost:8000/bauhaus-website/
```

2. Or open `bauhaus-website/index.html` directly in your browser.

Optional: use VS Code Live Server or `npx http-server` for a more robust local preview.

Notes about submodules and pushing
- The `bauhaus-website` folder has been used as a git submodule in some states. If you change files inside that folder you may need to commit within the submodule and then update the parent repo's submodule pointer.
  - From inside `bauhaus-website/`:

```bash
git add README.md index.html css/* js/*
git commit -m "docs/site: update README / styles"
git push origin <branch>
```

  ---
  # BAUHAUS NEO-MODERNISM — PROJECT README

  A concise, Bauhaus-inspired README for the repository root — minimalist, functional, and clear.

  ─────────────────────────────────────────────────────────────────────────────

  GOAL
  - Collect research and technical specifications for a Neo‑Modernism design system.
  - Prototype a lightweight, accessible HTML/CSS web presentation demonstrating the system.

  QUICK PREVIEW
  - Open: `bauhaus-website/index.html`
  - Serve: `python -m http.server 8000` → `http://localhost:8000/bauhaus-website/`

  PROJECT LAYOUT
  - `bauhaus-website/` — Prototype site (HTML, CSS, JS). May be a submodule in some repo states.
  - `bauhaus-neo-modernism-research/` — Research: references, specs, visual assets.

  Note: Additional guides, templates and docs referenced in previous drafts are stored inside the research folder in this checkout.

  CORE TOKENS (at-a-glance)
  - Colors: Bauhaus Blue `#0064B4` · Red `#E1000F` · Yellow `#FFED00` · Black/White
  - Type: Inter (variable) · Scale: 1.5 (Perfect fifth)
  - Spacing: 8px base (4px increments)
  - Grid: 12-column CSS Grid · Max width 1280px

  HOW THE PROTOTYPE WAS BUILT
  - Plain HTML + modular CSS + small JS for interactions (mobile menu, small animations).
  - Tokens live in `bauhaus-website/css/variables.css` for quick theming.
  - Iterative: research → tokens → visual experiments → polish (accessibility & contrast).

  WORKING WITH `bauhaus-website` (submodule notes)
  - If `bauhaus-website` appears as a submodule, edit and push inside the submodule first:

  ```bash
  cd bauhaus-website
  git checkout -b feat/site-fix
  git add index.html css/* js/*
  git commit -m "chore(site): update styles / README"
  git push origin feat/site-fix
  ```

  Then update the parent repo pointer:

  ```bash
  cd ..
  git add bauhaus-website
  git commit -m "chore: update bauhaus-website submodule pointer"
  git push origin master:main
  ```

  RECOMMENDED HOUSEKEEPING
  - Add a `LICENSE` (MIT recommended) for reuse clarity.
  - Add `.gitattributes` to normalize line endings on Windows.
  - Move large media to Git LFS or external CDN to keep repo small.
  - Add `CONTRIBUTING.md` and `CODE_OF_CONDUCT.md` for collaborators.

  WHAT WOULD HELP (handy next steps)
  - Generate responsive image sizes and use `srcset`.
  - Add GitHub Actions to lint HTML/CSS and run a simple accessibility test.
  - Add `README.md` inside `bauhaus-website/` (if using submodule, edit there).

  CONTRIBUTING (short)
  1. Fork → branch: `git checkout -b feat/your-change`
  2. Small focused commits
  3. Push to your fork and open a PR with screenshots

  STATUS (local, uncommitted)
  - Prototype: visual + interactive pages complete
  - Research hub: populated
  - This README: replaced locally per user request; no commit or push performed

  ─────────────────────────────────────────────────────────────────────────────
  Notes
  - I replaced the top-level README in the working tree following your Bauhaus styling request. I did not run any `git commit` or `git push` — the change is uncommitted.

  If you'd like I can:
  - commit and push this file to `origin/main` (tell me to proceed), or
  - rename `README-GITHUB.md` to `README.md` instead, or
  - add `LICENSE` / `CONTRIBUTING.md` templates before committing.

  Last edited: 2025-11-13 (local edit, uncommitted)

  =================================================================
  ||                      BAUHAUS NEO-MODERNISM                   ||
  ||   Minimal. Functional. Systematic. A design research & demo   ||
  =================================================================

  OVERVIEW
  - Purpose: collect research, define a pragmatic design system, and
    prototype a responsive, accessible web presentation inspired by
    Bauhaus and Swiss design principles.

  PROJECT LAYOUT (current checkout)
  ┌────────────────────────────────────────────────────────────────┐
  │ bauhaus-website/                Prototype site (HTML/CSS/JS)   │
  │ bauhaus-neo-modernism-research/ Research hub: refs, specs, img │
  └────────────────────────────────────────────────────────────────┘

  CORE TOKENS  ·  DESIGN SYSTEM (at-a-glance)
  - Colors  : Bauhaus Blue  #0064B4   · Red  #E1000F   · Yellow #FFED00
  - Type    : Inter (variable) — scale: 1.5 (Perfect Fifth)
  - Spacing : 8px base (4px multiples)
  - Grid    : 12-column CSS Grid — max-width 1280px

  HOW TO PREVIEW (quick)
  ```bash
  # Serve from repo root
  python -m http.server 8000
  # open http://localhost:8000/bauhaus-website/
  ```

  WORKFLOW NOTES (submodule awareness)
  - The `bauhaus-website/` folder has appeared as a submodule in
    previous commits. If changes are made inside that folder:

    1) Commit inside the submodule:
       cd bauhaus-website && git add . && git commit -m "..." && git push

    2) Update parent pointer and push:
       cd .. && git add bauhaus-website && git commit -m "chore: update submodule" && git push

  RECOMMENDED MAINTENANCE
  - Add `LICENSE` (MIT suggested)
  - Add `.gitattributes` to normalize CRLF on Windows
  - Move very large media to Git LFS or external CDN
  - Add `CONTRIBUTING.md` + `CODE_OF_CONDUCT.md` for collaborators

  DEVELOPER SUGGESTIONS (what would be helpful)
  - Optimize images, add `srcset` variants
  - Add GitHub Actions for HTML/CSS lint + basic accessibility checks
  - Add a small script to generate token docs from `css/variables.css`

  STYLE NOTES (Bauhaus spirit)
  - Keep content minimal and purposeful. Favor strong geometry,
    consistent spacing, a tight token system, and readable type.

  STATUS (local)
  - Prototype: visual + interaction iterations completed
  - Research: populated and linked
  - README: replaced locally with Bauhaus-styled layout (uncommitted)

  ────────────────────────────────────────────────────────────────
  If you want this change committed and pushed, tell me which remote
  and branch to push to (e.g. `origin main`) and whether to use
  `--force-with-lease` for safety on forced updates.

