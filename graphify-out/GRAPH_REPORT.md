# Graph Report - сайт  (2026-11-14)

## Corpus Check
- 2 files · ~11,234 words
- Verdict: corpus is large enough that graph structure adds value.
- Unclassified: 6 file(s) not represented in the graph (top: (none) 5, .css 1)

## Summary
- 45 nodes · 73 edges · 7 communities (6 shown, 1 thin omitted)
- Extraction: 90% EXTRACTED · 10% INFERRED · 0% AMBIGUOUS · INFERRED: 7 edges (avg confidence: 0.89)
- Token cost: 4,200 input · 1,850 output

## Graph Freshness
- Built from commit: `366066f7`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- Hero Circuit Animation & Equipment Carousel
- Authorized Vendor Brands & SVG Plaques
- Theme 3 Titanium Slate Design System
- Security Hardening (CSP, HSTS & XSS Guard)
- WhatsApp Diagnostic Calculator & State
- Sticky Header & Victory 121 Logo (#top)
- Yandex Webmaster Verification (yandex_feaf81d0e60efa70.html)

## God Nodes (most connected - your core abstractions)
1. `index.html (Main Page Markup)` - 13 edges
2. `Authorized 8 Brands Grid & Official Vendor Links (#brands)` - 12 edges
3. `renderSymptomChips()` - 8 edges
4. `styles.css (Theme 3 Royal Sapphire & Gold Design System)` - 8 edges
5. `WhatsApp Request Calculator (#calculator)` - 6 edges
6. `applyLanguage()` - 5 edges
7. `populateServiceModal()` - 5 edges
8. `Hero Section & Circuit Animation (.hero-section)` - 4 edges
9. `Variant 3: Royal Sapphire & Imperial Gold Accents (--gold-*)` - 4 edges
10. `README.md (Project Documentation & Runbook)` - 4 edges

## Surprising Connections (you probably didn't know these)
- `Authorized 8 Brands Grid & Official Vendor Links (#brands)` --references--> `Bang & Olufsen Official Monogram + Wordmark (bang-olufsen.svg)`  [EXTRACTED]
  index.html → assets/brands/bang-olufsen.svg
- `Authorized 8 Brands Grid & Official Vendor Links (#brands)` --references--> `Canon Official Red Vector Logo (canon.svg)`  [EXTRACTED]
  index.html → assets/brands/canon.svg
- `Authorized 8 Brands Grid & Official Vendor Links (#brands)` --references--> `Epson Official Blue Vector Logo (epson.svg)`  [EXTRACTED]
  index.html → assets/brands/epson.svg
- `Authorized 8 Brands Grid & Official Vendor Links (#brands)` --references--> `Катюша Cropped Official Logo (katusha.png)`  [EXTRACTED]
  index.html → assets/brands/katusha.png
- `Authorized 8 Brands Grid & Official Vendor Links (#brands)` --references--> `Kyocera Official Red Mark + Wordmark (kyocera.svg)`  [EXTRACTED]
  index.html → assets/brands/kyocera.svg

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **8 Official Authorized Vendor Brand Plaques** — index_brands_section, styles_vendor_plaque, assets_brands_canon, assets_brands_epson, assets_brands_sony, assets_brands_nikon, assets_brands_samsung, assets_brands_kyocera, assets_brands_katusha, assets_brands_bo [EXTRACTED 1.00]
- **Multi-Layer Website Security Architecture (CSP + Sanitization + .htaccess)** — htaccess_security, index_csp_meta, app_sanitizeusertext, index_contacts_section [EXTRACTED 1.00]
- **Interactive WhatsApp Diagnostic Request Pipeline** — index_calculator_section, index_custom_symptom_box, app_rendersymptomchips, app_syncdevicechipsui, app_syncbrandui, app_sanitizeusertext [EXTRACTED 1.00]

## Communities (7 total, 1 thin omitted)

### Community 0 - "Hero Circuit Animation & Equipment Carousel"
Cohesion: 0.27
Nodes (9): applyLanguage(), Bilingual Dictionary I18N (RU / KZ), populateServiceModal(), Service Catalog & Symptoms SERVICE_DETAILS, setCarouselSlide(), startCarousel(), stopCarousel(), Service Details Modal (<dialog #service-modal>) (+1 more)

### Community 1 - "Authorized Vendor Brands & SVG Plaques"
Cohesion: 0.20
Nodes (10): Bang & Olufsen Official Monogram + Wordmark (bang-olufsen.svg), Canon Official Red Vector Logo (canon.svg), Epson Official Blue Vector Logo (epson.svg), Катюша Cropped Official Logo (katusha.png), Kyocera Official Red Mark + Wordmark (kyocera.svg), Nikon Official Slanted Vector Logo (nikon.svg), Samsung Official Black Vector Wordmark (samsung.svg), SONY Official Black Vector Logo (sony.svg) (+2 more)

### Community 2 - "Theme 3 Titanium Slate Design System"
Cohesion: 0.47
Nodes (4): Hero Section & Circuit Animation (.hero-section), Dual Sapphire & Gold Electric Circuit Keyframes, styles.css (Theme 3 Royal Sapphire & Gold Design System), Responsive Breakpoints (1080px Tablet / 720px Mobile)

### Community 3 - "Security Hardening (CSP, HSTS & XSS Guard)"
Cohesion: 0.38
Nodes (6): About Victory 121 & Engineering Standards (#about), Contacts & Sandboxed Map (#contacts), Content-Security-Policy & Referrer Meta, index.html (Main Page Markup), Mobile Navigation Drawer (<dialog #mobile-drawer>), README.md (Project Documentation & Runbook)

### Community 4 - "WhatsApp Diagnostic Calculator & State"
Cohesion: 0.33
Nodes (7): renderSymptomChips(), sanitizeUserText(), Reactive Application State (state), syncBrandUI(), syncDeviceChipsUI(), WhatsApp Request Calculator (#calculator), Custom Symptom Input (#custom-symptom-box)

### Community 5 - "Sticky Header & Victory 121 Logo (#top)"
Cohesion: 0.67
Nodes (3): Victory 121 3D Globe Emblem (victory-globe.png), Sticky Header & Victory 121 Logo (#top), Victory 121 Logo Typography (.v121-logo)

## Knowledge Gaps
- **13 isolated node(s):** `Bang & Olufsen Official Monogram + Wordmark (bang-olufsen.svg)`, `Canon Official Red Vector Logo (canon.svg)`, `Epson Official Blue Vector Logo (epson.svg)`, `Катюша Cropped Official Logo (katusha.png)`, `Kyocera Official Red Mark + Wordmark (kyocera.svg)` (+8 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 15 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **1 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `index.html (Main Page Markup)` connect `Security Hardening (CSP, HSTS & XSS Guard)` to `Hero Circuit Animation & Equipment Carousel`, `Authorized Vendor Brands & SVG Plaques`, `Theme 3 Titanium Slate Design System`, `WhatsApp Diagnostic Calculator & State`, `Sticky Header & Victory 121 Logo (#top)`?**
  _High betweenness centrality (0.467) - this node is a cross-community bridge._
- **What connects `Bang & Olufsen Official Monogram + Wordmark (bang-olufsen.svg)`, `Canon Official Red Vector Logo (canon.svg)`, `Epson Official Blue Vector Logo (epson.svg)` to the rest of the system?**
  _13 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Why does `Authorized 8 Brands Grid & Official Vendor Links (#brands)` connect `Authorized Vendor Brands & SVG Plaques` to `Theme 3 Titanium Slate Design System`, `Security Hardening (CSP, HSTS & XSS Guard)`, `WhatsApp Diagnostic Calculator & State`?**
  _High betweenness centrality (0.356) - this node is a cross-community bridge._
- **Why does `styles.css (Theme 3 Royal Sapphire & Gold Design System)` connect `Theme 3 Titanium Slate Design System` to `Authorized Vendor Brands & SVG Plaques`, `Security Hardening (CSP, HSTS & XSS Guard)`, `Sticky Header & Victory 121 Logo (#top)`?**
  _High betweenness centrality (0.152) - this node is a cross-community bridge._