# SME Dashboard — UX Improvement Reference Notes
**Comparing:** `SME-Dashboard-v13.html` → `SME-Dashboard-UX-Improved-v1.html`  
**Branch:** `User-Friently-Wiki-App`  
**Date:** May 2026

---

## Summary
The improved version adds ~1,058 lines and removes ~1,027 from the original — a near-complete visual and structural overhaul focused on making the tool accessible to non-technical USPS staff (SMEs who are not data-savvy).

---

## Change List & Why It's More User-Friendly

| # | Change | What Changed | Why It's More User-Friendly |
|---|--------|-------------|------------------------------|
| 1 | **Design System Tokens** | Replaced all hardcoded hex colors with named CSS variables (`--blue`, `--gray-500`, `--shadow-md`) | Ensures visual consistency across every component — colors never drift between sections, making the UI feel polished and trustworthy |
| 2 | **Base Font Size: 13px → 15px** | `html, body { font-size: 13px }` increased to `15px` | 13px is below the comfortable reading threshold for most adults, especially on high-DPI screens; 15px reduces eye strain when reading long field descriptions |
| 3 | **WCAG-Compliant Warning Color** | Warning yellow changed from `#fdb913` (fails WCAG AA) to `#b45309` (accessible amber) | Users with low vision or color perception differences can now read warning labels; required by federal accessibility law |
| 4 | **Onboarding Banner** *(New)* | Added a dismissible tip banner at the top of the page (`role="note"`, `aria-label="Tip for new users"`) | First-time users get immediate guidance without reading separate documentation; dismissible so it doesn't clutter the workspace for returning users |
| 5 | **Progress Tracker Card** *(New)* | Welcome page now shows **Assigned to You**, **In Draft**, **Submitted**, **Completed**, and a visual progress bar (`role="progressbar"`) | SMEs tracking their own submissions need to see: work assigned, work being drafted, work submitted for review, and work completed — not a reviewer's perspective. Progress bar shows % of assigned work completed |
| 6 | **Beginner Mode Toggle** *(New)* ⭐ | Prominent toggle hides `.advanced-term`, `.col-advanced`, `.technical-hint` elements when enabled | Core feature of the non-data-friendly brief — strips technical jargon (partition keys, schema lineage) for non-technical SMEs; power users can toggle it off |
| 7 | **Acronym Tooltips** *(New)* | `.acronym` class with `data-tooltip` reveals definitions on hover/focus | Dashboard acronyms (CDAO, MDM, ETL) previously required Googling; definitions now appear inline without leaving the page |
| 8 | **Navigation Icons** | Each nav tab now includes an SVG icon (Home, Search, Document) beside the label | Icons give a second recognition cue beyond text — helpful for skimmers and users in a second language; tabs are easier to find at a glance |
| 9 | **Help Button Redesign** | Changed from solid blue `#0066cc` to transparent ghost style matching the header | The solid blue button competed visually with primary navigation; the ghost style signals "support is available" without demanding attention |
| 10 | **Step Badges: Text → Circle Icons** | "STEP 1 / STEP 2 / STEP 3" text badges replaced with circular SVG icon badges | Text step labels are redundant alongside numbered headings; icon badges are more scannable and communicate the nature of each step at a glance |
| 11 | **Call-to-Action Button** *(New)* | Large "Start Exploring →" primary button added below the step cards | Without a CTA, users on the Welcome page have no clear next step; the button removes ambiguity and reduces drop-off for non-technical users |
| 12 | **Status Filter Pills** *(New)* | Filter status controls redesigned as pill buttons with colored dot indicators (green / amber / red) | Color-coded pills are more scannable than plain checkboxes; users instantly see active filters without reading every label |
| 13 | **Color-Coded Status Badges** *(New)* | Asset cards show `.status-badge.full`, `.partial`, `.pending` with dot indicators | Documentation health is visible at a glance without clicking into each asset — critical for SMEs triaging which assets need attention |
| 14 | **Empty State Guidance** *(New)* | When no asset is selected, a numbered step guide with a large icon appears instead of a blank pane | Blank empty states feel broken to non-technical users; the guided state acts as a micro-tutorial and teaches the correct workflow |
| 15 | **Filter Sidebar Redesign** | Added subtitle text, section dividers, and moved Beginner Mode toggle to the very top | Placing Beginner Mode first signals it's a global priority setting; the subtitle gives context so users know what the sidebar is for |
| 16 | **Line Height & Text Width** | `line-height` increased from 1.55 → 1.6; description text capped at `max-width: 620px` | Full-width text lines are harder to read; the column cap keeps content comfortable and the extra line height improves scannability |
| 17 | **ARIA Labels & Semantic Roles** | Added `aria-label`, `aria-current="page"`, `role="region"`, `role="progressbar"`, `aria-hidden` on decorative elements | Screen reader and keyboard users can now navigate the page structure; required for federal Section 508 compliance |
| 18 | **Attribute Summary Banner** *(New)* | Banner above the asset detail table shows Total / Documented / Missing counts with color-coded values | SMEs don't need to scroll 50+ rows to assess documentation health; the banner delivers the "so what" immediately |

---

## Files Referenced

| File | Description |
|------|-------------|
| `SME-Dashboard-v13.html` | Original version before UX improvements |
| `SME-Dashboard-UX-Improved-v1.html` | Improved version with all changes above |
| `SME-Dashboard-feature:non-data-friendly-UI.html` | Intermediate working version |
| `SME_Dashboard_Documentation_v3.pdf` | Supplementary documentation |



UI Refinements & User Experience Changes

Change
Why More User-Friendly
1
CSS design tokens
Visual consistency across all components
2
Font size 13px → 15px
Easier reading, reduces eye strain
3
WCAG-compliant warning color
Readable by users with low vision; federal requirement
4
Onboarding banner
Immediate guidance for first-time users, dismissible
5
Progress tracker card metrics
SME submission workflow: Assigned → In Draft → Submitted → Completed; shows progress as % completed
6
Beginner Mode toggle 
Hides technical jargon for non-data SMEs — the core feature
7
Acronym tooltips
Definitions on hover; no more Googling postal acronyms
8
Nav tab icons
Second recognition cue beyond text; easier to scan
9
Help button redesign
Less visual noise; support feels accessible not intrusive
10
Circle icon badges on steps
More meaningful than "STEP 1" text labels
11
"Start Exploring" CTA button
Clear next action; removes drop-off confusion
12
Color-coded filter pills
Status filters are scannable at a glance
13
Status badges in asset list
Triage priority visible without clicking into each asset
14
Empty state guidance
Teaches workflow instead of showing a blank screen
15
Filter sidebar redesign
Beginner Mode surfaced first; context subtitle added
16
Line height & text width
Comfortable reading column; better scannability
17
ARIA labels throughout
Section 508 / screen reader compliance
18
Attribute summary banner
"So what" visible at a glance without scrolling
