---
group: Schema
category: Documentation
aliases:
  - Product Schema
  - UNDOXXING Product Frontmatter
tags:
  - schema
  - documentation
  - meta
---

# UNDOXXING Product Note Schema

This document defines the canonical frontmatter schema for all product notes in the UNDOXXING vault.

## Design Principles

- **One note per meaningful model tier** — variants that differ only in storage, color, or minor hardware are not scored separately
- **SKU expansion on backend** — the webapp/database maps multiple UPCs to a single canonical note; the vault stays readable
- **Offline-compatible** — the vault is a standalone privacy database, usable without the webapp
- **Open source ready** — GitHub-hosted, forkable, Obsidian-compatible

---

## Full Schema

```yaml
---
group: Product
category: [Smartphone / Smart Speaker / Laptop / Wearable / Tablet / Smart TV / Smart Home / Router / etc.]
brand: [Manufacturer name]
productLine: [Product family name, e.g. "iPhone 17"]
models:
  - name: [Model tier name]
    upc: []  # Array of UPCs for all storage/color variants of this tier
  - name: [Model tier name]
    upc: []
released: YYYY-MM-DD
status: [Current / Discontinued]
policyRetrieved: YYYY-MM-DD      # Date we ran the analysis
policyLastUpdated: YYYY-MM-DD    # Date manufacturer last updated their policy
policyUrl: https://...
ftcActions: [none / URL to FTC action]
severityTier: [1-5 or null if unscored]
severityPoints: [raw points or null]
scopeScore: [0-100 or null]      # % of possible data types collected
intensityScore: [0-100 or null]  # % of how badly collected data is mishandled
udxScore: [0-100 or null]        # geometric mean of scope × intensity
scoredDate: YYYY-MM-DD
scoredBy: [Claude / Human / Claude+Human]
aliases:
  - [Common name variants]
tags:
  - product
  - [brand lowercase]
  - [category lowercase]
  - [relevant surveillance vectors]
---
```

---

## Severity Tier Reference

| Tier | Score Range | Label |
|------|-------------|-------|
| 1 | 0–20 | Minimal |
| 2 | 21–40 | Low |
| 3 | 41–60 | Moderate |
| 4 | 61–80 | Hostile |
| 5 | 81–100 | Surveillance-grade |

---

## Score Dimensions

**Scope Score** — What percentage of possible IoT data types does this product collect by default?
`min(Σ Severity_i / 200, 1) × 100`

**Intensity Score** — Of the data it collects, how badly is it mishandled?
`min((Σ Score_i / Σ Severity_i) × 100, 100)`

**UDX Score** — Final score balancing both dimensions equally.
`√(Scope × Intensity)`

Only data collected BY DEFAULT is scored. Opt-in features are documented separately and excluded from scoring.

---

## UPC Mapping Logic

The vault holds one note per model tier. The backend database expands this into a full SKU table:

```
iPhone 17 Pro.md
  → iPhone 17 Pro 128GB Black        UPC: 123456789
  → iPhone 17 Pro 128GB White        UPC: 123456790
  → iPhone 17 Pro 256GB Black        UPC: 123456791
  → iPhone 17 Pro 256GB White        UPC: 123456792
  → ...all map to same score
```

Barcode scan → UPC lookup → canonical note → score returned.

Unknown product → Claude API call → algorithm runs → note written to vault → score served and cached.

---

## Scoring Methodology

Full methodology documented in UNDOXXING Analyzer Skill (v4.0).
Formula: `Score = Base Severity × Handling% × Capture Mode × Opt-Out Mode`

Policy must be retrieved via ToS Tracker API or web_fetch before scoring.
Web search snippets alone are insufficient — full policy text required.
