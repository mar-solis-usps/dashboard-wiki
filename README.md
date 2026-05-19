# Postal Data Wiki — SME Dashboard

A browser-based HTML prototype for the USPS **Subject Matter Expert (SME) Dashboard**, part of the internal Data Governance tooling. This prototype allows SMEs to review, edit, and approve AI-generated names and descriptions for data assets in the Postal Data Wiki.

---

## Live Preview

> After enabling GitHub Pages, the prototype is available at:
> `https://mar-solis-usps.github.io/dashboard-wiki/SME-Dashboard-UX-Improved-v1.html`

No installation or login required — open the link in any browser and interact with the full navigation.

---

## What This Prototype Does

Subject Matter Experts use this dashboard to:

- **Browse data assets** (tables, datasets) assigned to their business area
- **Review AI-generated field labels and descriptions** side by side with current values
- **Edit suggestions** to use plain, business-friendly language
- **Save drafts** or **submit changes** for data steward approval
- **Track review progress** across assigned assets

---

## Files

| File | Description |
|------|-------------|
| `SME-Dashboard-UX-Improved-v1.html` | Latest version — UX-improved, new-user friendly |
| `SME-Dashboard-v13.html` | Previous version (v13) for reference |
| `SME-Dashboard-feature:non-data-friendly-UI.html` | Original feature branch file (pre-improvement) |
| `SME_Dashboard_Documentation_v3.pdf` | Full feature documentation (v3) |
| `images/` | Logo assets (SVG) |

---

## What Was Improved (v1 → UX-Improved-v1)

This version addresses the **non-data-friendly UI** issue identified in the feature branch. Key changes made for new users:

| Area | Change |
|------|--------|
| Readability | Base font increased from 13px to 15px |
| Beginner Mode | Moved to top of filter panel, on by default, with a visual toggle |
| Status labels | Replaced cryptic `● ◐` symbols with color pill badges (Needs Review / Fully Reviewed) |
| Filter panel | Status dropdown replaced with plain-English button pills |
| Welcome page | Added live progress card (assigned / completed / pending) |
| Step icons | Replaced emoji with clean SVG line icons |
| Empty states | Added illustrated empty states with step-by-step guidance |
| Table headers | Larger font, "AI" badge chips marking AI-suggested columns |
| Modal | Title now shows the specific field name; footer reorganized (Cancel / Save Draft / Submit) |
| Accessibility | WCAG 2.1 AA colors, ARIA labels, visible focus rings throughout |
| Logo | Embedded inline SVG so it renders correctly when hosted remotely |

---

## Pages

The prototype has three navigable tabs:

1. **Home** — Welcome screen with progress summary and step-by-step guide
2. **Explore Assets** — Filter, search, and browse data assets; view and edit field descriptions
3. **Review Changes** — View submitted suggestions by status (Draft, Submitted, Approved, Rejected)

---

## Branch

| Branch | Purpose |
|--------|---------|
| `main` | Stable baseline |
| `User-Friently-Wiki-App` | Active development — UX improvements for new users |

---

## Design Standards

- **Brand colors:** USPS Blue `#004B87`, USPS Red `#DA291C`
- **Accessibility:** WCAG 2.1 AA — minimum 4.5:1 contrast ratio, keyboard navigable, ARIA roles
- **Typography:** System font stack (`-apple-system, Segoe UI, sans-serif`), 15px base
- **Logo:** CDAO (Chief Data and Analytics Office)

---

## Contact

Design & UX — Mar Solis, USPS Data Governance Team
