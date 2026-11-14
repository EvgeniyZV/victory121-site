---
trigger: always_on
description: MANDATORY — Always inspect and query the Graphify knowledge graph in graphify-out/ FIRST before starting any task, editing files, or exploring the project.
---

# Mandatory Graphify-First Workflow (Victory 121)

This project maintains a live **Graphify** knowledge graph in `graphify-out/` (`graph.json`, `GRAPH_REPORT.md`, `wiki/index.md`, `graph.html`, `GRAPH_TREE.html`).

## 1. Check the Graph FIRST (Before Any Action)
Before reading raw source files, running broad searches, or making any changes to `index.html`, `styles.css`, `app.js`, `.htaccess`, or `assets/`:
1. **Start at the Graph Wiki / Report:** Read `graphify-out/wiki/index.md` or `graphify-out/GRAPH_REPORT.md` to understand the 7 architectural communities, God Nodes, and cross-file relationships.
2. **Query the Graph:** If the `graphify` CLI (`pip install graphifyy`) is installed, run:
   - `graphify query "<question>"` — scoped BFS/DFS context around relevant nodes
   - `graphify explain "<node_label>"` — detailed neighbors, source location, and relations for a specific node
   - `graphify path "<Node A>" "<Node B>"` — shortest path between two components
   - `graphify god-nodes` — top highest-degree architectural hubs
3. **Only after consulting the graph** should you open specific source files (`index.html`, `styles.css`, `app.js`) at the exact line numbers indicated by the graph.

## 2. Keep the Graph Synchronized After Edits
- After modifying any code, markup, styles, or documentation in this repository, update the knowledge graph before finishing or committing:
  - Run `graphify update .` (or rebuild `graphify-out/graph.json`, `graphify-out/GRAPH_REPORT.md`, `graphify export html`, and `graphify export wiki`).

## 3. Core Project Invariants (Recorded in the Graph)
- **Theme:** Variant 3 — *Titanium Atelier & Sapphire Glow* (`#080D1A` obsidian-titanium background, `#2563EB` sapphire, `#38BDF8` ice cyan).
- **Logo:** Option 1 — `Manrope ExtraBold` white `Victory` + glowing Ice Cyan `#38BDF8` `121` + 3D globe `./assets/victory-globe.png`.
- **Vendor Brand Policy:** All 8 official vendor logos in `./assets/brands/` (`canon.svg`, `epson.svg`, `sony.svg`, `nikon.svg`, `samsung.svg`, `kyocera.svg`, `katusha.png`, `bang-olufsen.svg`) are displayed on isolated white brand plaques (`.vendor-plaque`) in strict accordance with vendor brandbooks. Never apply CSS color-altering filters (`grayscale`, `invert`) to vendor logos.
- **Security:** Maintain strict CSP in `index.html` and `.htaccess`, `replaceChildren()` DOM updates, and `sanitizeUserText()` input sanitization in `app.js`.
