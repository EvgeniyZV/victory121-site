# Security Hardening (CSP, HSTS & XSS Guard)

> 8 nodes · cohesion 0.32

## Key Concepts

- **index.html (Main Page Markup)** (13 connections) — `index.html`
- **.htaccess HTTP Security Headers (HSTS, CSP, X-Frame-Options)** (4 connections) — `.htaccess`
- **README.md (Project Documentation & Runbook)** (4 connections) — `README.md`
- **sanitizeUserText()** (3 connections) — `app.js`
- **Contacts & Sandboxed Map (#contacts)** (2 connections) — `index.html`
- **Content-Security-Policy & Referrer Meta** (2 connections) — `index.html`
- **About Victory 121 & Engineering Standards (#about)** (1 connections) — `index.html`
- **Mobile Navigation Drawer (<dialog #mobile-drawer>)** (1 connections) — `index.html`

## Relationships

- [Theme 3 Titanium Slate Design System](Theme_3_Titanium_Slate_Design_System.md) (4 shared connections)
- [Hero Circuit Animation & Equipment Carousel](Hero_Circuit_Animation_&_Equipment_Carousel.md) (3 shared connections)
- [WhatsApp Diagnostic Calculator & State](WhatsApp_Diagnostic_Calculator_&_State.md) (2 shared connections)
- [Core Page Markup & UI Module 5](Core_Page_Markup_&_UI_Module_5.md) (2 shared connections)
- [Authorized Vendor Brands & SVG Plaques](Authorized_Vendor_Brands_&_SVG_Plaques.md) (1 shared connections)

## Source Files

- `.htaccess`
- `README.md`
- `app.js`
- `index.html`

## Audit Trail

- EXTRACTED: 18 (86%)
- INFERRED: 3 (14%)
- AMBIGUOUS: 0 (0%)

---

*Part of the graphify knowledge wiki. See [index](index.md) to navigate.*