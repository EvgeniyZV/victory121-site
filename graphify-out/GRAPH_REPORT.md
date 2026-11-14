# Graph Report - сайт  (2026-11-14)

## Corpus Check
- 2 files · ~11,270 words
- Verdict: corpus is large enough that graph structure adds value.
- Unclassified: 6 file(s) not represented in the graph (top: (none) 5, .css 1)

## Summary
- 43 nodes · 69 edges · 7 communities (6 shown, 1 thin omitted)
- Extraction: 90% EXTRACTED · 10% INFERRED · 0% AMBIGUOUS · INFERRED: 7 edges (avg confidence: 0.89)
- Token cost: 4,200 input · 1,850 output

## Graph Freshness
- Built from commit: `6be0a97c`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- Authorized Vendor Brands & SVG Plaques
- Theme 3 Titanium Slate Design System
- Security Hardening (CSP, HSTS & XSS Guard)
- Hero Circuit Animation & Equipment Carousel
- WhatsApp Diagnostic Calculator & State
- Core Page Markup & UI Module 5
- Core Page Markup & UI Module 6

## God Nodes (most connected - your core abstractions)
1. `index.html (Main Page Markup)` - 13 edges
2. `Authorized 8 Brands Grid (#brands)` - 11 edges
3. `renderSymptomChips()` - 8 edges
4. `styles.css (Theme 3 Design System)` - 7 edges
5. `WhatsApp Request Calculator (#calculator)` - 6 edges
6. `applyLanguage()` - 5 edges
7. `populateServiceModal()` - 5 edges
8. `Sticky Header & Victory 121 Logo (#top)` - 4 edges
9. `README.md (Project Documentation & Runbook)` - 4 edges
10. `.htaccess HTTP Security Headers (HSTS, CSP, X-Frame-Options)` - 4 edges

## Surprising Connections (you probably didn't know these)
- `Authorized 8 Brands Grid (#brands)` --references--> `Bang & Olufsen Official Monogram + Wordmark (bang-olufsen.svg)`  [EXTRACTED]
  index.html → assets/brands/bang-olufsen.svg
- `Authorized 8 Brands Grid (#brands)` --references--> `Canon Official Red Vector Logo (canon.svg)`  [EXTRACTED]
  index.html → assets/brands/canon.svg
- `Authorized 8 Brands Grid (#brands)` --references--> `Epson Official Blue Vector Logo (epson.svg)`  [EXTRACTED]
  index.html → assets/brands/epson.svg
- `Authorized 8 Brands Grid (#brands)` --references--> `Катюша Cropped Official Logo (katusha.png)`  [EXTRACTED]
  index.html → assets/brands/katusha.png
- `Authorized 8 Brands Grid (#brands)` --references--> `Kyocera Official Red Mark + Wordmark (kyocera.svg)`  [EXTRACTED]
  index.html → assets/brands/kyocera.svg

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **8 Official Authorized Vendor Brand Plaques** — index_brands_section, styles_vendor_plaque, assets_brands_canon, assets_brands_epson, assets_brands_sony, assets_brands_nikon, assets_brands_samsung, assets_brands_kyocera, assets_brands_katusha, assets_brands_bo [EXTRACTED 1.00]
- **Multi-Layer Website Security Architecture (CSP + Sanitization + .htaccess)** — htaccess_security, index_csp_meta, app_sanitizeusertext, index_contacts_section [EXTRACTED 1.00]
- **Interactive WhatsApp Diagnostic Request Pipeline** — index_calculator_section, index_custom_symptom_box, app_rendersymptomchips, app_syncdevicechipsui, app_syncbrandui, app_sanitizeusertext [EXTRACTED 1.00]

## Communities (7 total, 1 thin omitted)

### Community 0 - "Authorized Vendor Brands & SVG Plaques"
Cohesion: 0.20
Nodes (10): syncBrandUI(), Bang & Olufsen Official Monogram + Wordmark (bang-olufsen.svg), Canon Official Red Vector Logo (canon.svg), Epson Official Blue Vector Logo (epson.svg), Катюша Cropped Official Logo (katusha.png), Kyocera Official Red Mark + Wordmark (kyocera.svg), Nikon Official Slanted Vector Logo (nikon.svg), Samsung Official Black Vector Wordmark (samsung.svg) (+2 more)

### Community 1 - "Theme 3 Titanium Slate Design System"
Cohesion: 0.22
Nodes (8): Victory 121 3D Globe Emblem (victory-globe.png), Hero Section & Circuit Animation (.hero-section), Sticky Header & Victory 121 Logo (#top), Electric Circuit Keyframes (v121-electric-current), styles.css (Theme 3 Design System), Responsive Breakpoints (1080px Tablet / 720px Mobile), Victory 121 Logo Typography (.v121-logo), Vendor White Plaque & Adapted SVG Sizing (.vendor-plaque)

### Community 2 - "Security Hardening (CSP, HSTS & XSS Guard)"
Cohesion: 0.32
Nodes (7): sanitizeUserText(), About Victory 121 & Engineering Standards (#about), Contacts & Sandboxed Map (#contacts), Content-Security-Policy & Referrer Meta, index.html (Main Page Markup), Mobile Navigation Drawer (<dialog #mobile-drawer>), README.md (Project Documentation & Runbook)

### Community 3 - "Hero Circuit Animation & Equipment Carousel"
Cohesion: 0.60
Nodes (3): setCarouselSlide(), startCarousel(), stopCarousel()

### Community 4 - "WhatsApp Diagnostic Calculator & State"
Cohesion: 0.50
Nodes (5): renderSymptomChips(), Reactive Application State (state), syncDeviceChipsUI(), WhatsApp Request Calculator (#calculator), Custom Symptom Input (#custom-symptom-box)

### Community 5 - "Core Page Markup & UI Module 5"
Cohesion: 0.50
Nodes (4): populateServiceModal(), Service Catalog & Symptoms SERVICE_DETAILS, Service Details Modal (<dialog #service-modal>), 6 Repair Services Bento Grid (#services)

## Knowledge Gaps
- **12 isolated node(s):** `Bang & Olufsen Official Monogram + Wordmark (bang-olufsen.svg)`, `Canon Official Red Vector Logo (canon.svg)`, `Epson Official Blue Vector Logo (epson.svg)`, `Катюша Cropped Official Logo (katusha.png)`, `Kyocera Official Red Mark + Wordmark (kyocera.svg)` (+7 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 14 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **1 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `index.html (Main Page Markup)` connect `Security Hardening (CSP, HSTS & XSS Guard)` to `Authorized Vendor Brands & SVG Plaques`, `Theme 3 Titanium Slate Design System`, `Hero Circuit Animation & Equipment Carousel`, `WhatsApp Diagnostic Calculator & State`, `Core Page Markup & UI Module 5`?**
  _High betweenness centrality (0.520) - this node is a cross-community bridge._
- **What connects `Bang & Olufsen Official Monogram + Wordmark (bang-olufsen.svg)`, `Canon Official Red Vector Logo (canon.svg)`, `Epson Official Blue Vector Logo (epson.svg)` to the rest of the system?**
  _12 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Why does `Authorized 8 Brands Grid (#brands)` connect `Authorized Vendor Brands & SVG Plaques` to `Theme 3 Titanium Slate Design System`, `Security Hardening (CSP, HSTS & XSS Guard)`?**
  _High betweenness centrality (0.369) - this node is a cross-community bridge._
- **Why does `styles.css (Theme 3 Design System)` connect `Theme 3 Titanium Slate Design System` to `Security Hardening (CSP, HSTS & XSS Guard)`?**
  _High betweenness centrality (0.159) - this node is a cross-community bridge._