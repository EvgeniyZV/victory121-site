# Graph Report - сайт  (2026-11-14)

## Corpus Check
- Corpus is ~11,270 words - fits in a single context window. You may not need a graph.

## Summary
- 46 nodes · 76 edges · 5 communities
- Extraction: 91% EXTRACTED · 9% INFERRED · 0% AMBIGUOUS · INFERRED: 7 edges (avg confidence: 0.89)
- Token cost: 4,200 input · 1,850 output

## Community Hubs (Navigation)
- Hero Circuit Animation & Equipment Carousel
- Authorized Vendor Brands & SVG Plaques
- Theme 3 Titanium Slate Design System
- Security Hardening (CSP, HSTS & XSS Guard)
- WhatsApp Diagnostic Calculator & State

## God Nodes (most connected - your core abstractions)
1. `index.html (Main Page Markup)` - 14 edges
2. `Authorized 8 Brands Grid & Official Vendor Links (#brands)` - 12 edges
3. `renderSymptomChips()` - 8 edges
4. `styles.css (Theme 3 Royal Sapphire & Gold Design System)` - 8 edges
5. `WhatsApp Request Calculator (#calculator)` - 6 edges
6. `applyLanguage()` - 5 edges
7. `populateServiceModal()` - 5 edges
8. `.htaccess HTTP Security Headers (HSTS, CSP, X-Frame-Options)` - 5 edges
9. `Sticky Header & Victory 121 Logo (#top)` - 4 edges
10. `Hero Section & Circuit Animation (.hero-section)` - 4 edges

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

## Communities (5 total, 0 thin omitted)

### Community 0 - "Hero Circuit Animation & Equipment Carousel"
Cohesion: 0.27
Nodes (9): applyLanguage(), Bilingual Dictionary I18N (RU / KZ), populateServiceModal(), Service Catalog & Symptoms SERVICE_DETAILS, setCarouselSlide(), startCarousel(), stopCarousel(), Service Details Modal (<dialog #service-modal>) (+1 more)

### Community 1 - "Authorized Vendor Brands & SVG Plaques"
Cohesion: 0.20
Nodes (10): syncBrandUI(), Bang & Olufsen Official Monogram + Wordmark (bang-olufsen.svg), Canon Official Red Vector Logo (canon.svg), Epson Official Blue Vector Logo (epson.svg), Катюша Cropped Official Logo (katusha.png), Kyocera Official Red Mark + Wordmark (kyocera.svg), Nikon Official Slanted Vector Logo (nikon.svg), Samsung Official Black Vector Wordmark (samsung.svg) (+2 more)

### Community 2 - "Theme 3 Titanium Slate Design System"
Cohesion: 0.24
Nodes (8): Victory 121 3D Globe Emblem (victory-globe.png), Hero Section & Circuit Animation (.hero-section), Sticky Header & Victory 121 Logo (#top), Dual Sapphire & Gold Electric Circuit Keyframes, styles.css (Theme 3 Royal Sapphire & Gold Design System), Responsive Breakpoints (1080px Tablet / 720px Mobile), Victory 121 Logo Typography (.v121-logo), Vendor White Plaque & Adapted SVG Sizing (.vendor-plaque)

### Community 3 - "Security Hardening (CSP, HSTS & XSS Guard)"
Cohesion: 0.31
Nodes (7): About Victory 121 & Engineering Standards (#about), Contacts & Sandboxed Map (#contacts), Content-Security-Policy & Referrer Meta, index.html (Main Page Markup), Mobile Navigation Drawer (<dialog #mobile-drawer>), README.md (Project Documentation & Runbook), Yandex Webmaster Verification (yandex_feaf81d0e60efa70.html)

### Community 4 - "WhatsApp Diagnostic Calculator & State"
Cohesion: 0.40
Nodes (6): renderSymptomChips(), sanitizeUserText(), Reactive Application State (state), syncDeviceChipsUI(), WhatsApp Request Calculator (#calculator), Custom Symptom Input (#custom-symptom-box)

## Knowledge Gaps
- **13 isolated node(s):** `Mobile Navigation Drawer (<dialog #mobile-drawer>)`, `About Victory 121 & Engineering Standards (#about)`, `Responsive Breakpoints (1080px Tablet / 720px Mobile)`, `Yandex Webmaster Verification (yandex_feaf81d0e60efa70.html)`, `Victory 121 3D Globe Emblem (victory-globe.png)` (+8 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 15 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `index.html (Main Page Markup)` connect `Security Hardening (CSP, HSTS & XSS Guard)` to `Hero Circuit Animation & Equipment Carousel`, `Authorized Vendor Brands & SVG Plaques`, `Theme 3 Titanium Slate Design System`, `WhatsApp Diagnostic Calculator & State`?**
  _High betweenness centrality (0.526) - this node is a cross-community bridge._
- **What connects `Mobile Navigation Drawer (<dialog #mobile-drawer>)`, `About Victory 121 & Engineering Standards (#about)`, `Responsive Breakpoints (1080px Tablet / 720px Mobile)` to the rest of the system?**
  _13 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Why does `Authorized 8 Brands Grid & Official Vendor Links (#brands)` connect `Authorized Vendor Brands & SVG Plaques` to `Theme 3 Titanium Slate Design System`, `Security Hardening (CSP, HSTS & XSS Guard)`?**
  _High betweenness centrality (0.358) - this node is a cross-community bridge._
- **Why does `styles.css (Theme 3 Royal Sapphire & Gold Design System)` connect `Theme 3 Titanium Slate Design System` to `Security Hardening (CSP, HSTS & XSS Guard)`?**
  _High betweenness centrality (0.153) - this node is a cross-community bridge._