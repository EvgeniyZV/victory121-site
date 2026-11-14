# AGENTS.md — Victory 121 (`victory121.kz`)

> **MANDATORY RULE FOR ALL AI AGENTS (Antigravity, Gemini, Claude, Cursor, Codex):**
> **ALWAYS inspect the Graphify knowledge graph in `graphify-out/` FIRST before reading raw source files or making any edits.**

## Step 1: Consult the Graphify Knowledge Graph First
 This repository includes a pre-built **Graphify** knowledge graph in `graphify-out/`:
- **`graphify-out/wiki/index.md`** — Agent entry point with links to all 7 community articles and architectural hubs.
- **`graphify-out/GRAPH_REPORT.md`** — Full architectural summary: God Nodes (`index.html`, `app.js`, `styles.css`, `#calculator`, `#brands`, `calcState`), communities, and key relationships.
- **`graphify-out/graph.json`** — Machine-readable NetworkX node-link graph (`43 nodes`, `69 edges`, `7 communities`).
- **`graphify-out/graph.html`** & **`graphify-out/GRAPH_TREE.html`** — Interactive browser visualizations.

### CLI Commands (when `graphifyy` is installed via `pip install graphifyy`):
```bash
graphify query "<your question or feature>"
graphify explain "<node name>"
graphify path "<from node>" "<to node>"
graphify god-nodes
```

## Step 2: Project Architecture & Invariants
- **`index.html`** — Single-page responsive application with strict CSP (`<meta http-equiv="Content-Security-Policy">`), Hero equipment carousel, 8 official vendor brand plaques (`#brands`), 3-step WhatsApp diagnostic builder (`#calculator`) with custom issue input (`Другое — опишу свою неисправность`), B2B SLA contract tiers (`#b2b`), FAQ accordion (`#faq`), and sandboxed OpenStreetMap (`#contacts`).
- **`styles.css`** — Variant 3 (*Titanium Atelier & Sapphire Glow*): `#080D1A` obsidian background, `#10192E` slate surface, `#2563EB` sapphire, `#38BDF8` ice cyan. Option 1 header logo (`.v121-logo`: `Manrope ExtraBold` white `Victory` + `#38BDF8` `121`). Calibrated `.vendor-plaque` (`76px` height) and `.vendor-svg--*` classes.
- **`app.js`** — Zero-`innerHTML` (`replaceChildren()` + `textContent`) interactive controller with `sanitizeUserText()` XSS/control-char sanitizer, equipment carousel (`CAROUSEL_ITEMS`), brand-to-calculator deep linking (`[data-select-brand]`), and WhatsApp message generator (`https://wa.me/77019449547`).
- **`.htaccess`** — Production Apache security headers (`Strict-Transport-Security`, `X-Frame-Options: SAMEORIGIN`, `X-Content-Type-Options: nosniff`, `Referrer-Policy`, `Permissions-Policy`, `Content-Security-Policy`).

## Step 3: Update the Graph After Changes
Whenever you modify code or markup, keep `graphify-out/` up to date:
```bash
graphify update .
graphify export html
graphify export wiki
```

## Step 4: PS.kz / Plesk Hosting & Auto-Deploy (`victory121.kz`)
- **Hosting Server:** `srv-plesk14.ps.kz` (`195.210.46.14`), Plesk panel at `https://srv-plesk14.ps.kz:8443` (accessed via `https://console.ps.kz/plesk/shared/17766`).
- **Directories on Server:**
  - `/victory121-site` — **Active `Document Root` for `https://victory121.kz/`**, connected to `https://github.com/EvgeniyZV/victory121-site.git` (`main` branch) via Plesk Git with automatic webhook deployment on every `git push`.
  - `/new.victory121.kz` — Previous WordPress production directory (kept 100% intact for instant rollback).
  - `/backup_new_victory121_kz_before_switch.zip` (`199.1 MB`) — Full standalone ZIP backup of `/new.victory121.kz` stored in `/`.
  - `/httpdocs` — Legacy 2012–2024 archive directory (keep intact).
- **How to Roll Back if Ever Requested by User:**
  - In Plesk (`victory121.kz` -> **Настройки хостинга** / Hosting Settings), change **Корневая папка (`Document Root`)** from `victory121-site` back to `new.victory121.kz` and click **OK / Применить**.

