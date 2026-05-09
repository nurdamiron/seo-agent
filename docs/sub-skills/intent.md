# /seo intent — Search Intent Classification

Classify every page's search intent and catch mismatches before Google does.

## Command

```
/seo intent [url]
```

## The 4 intent types

| Type | User goal | Signals |
|---|---|---|
| **Navigational** | Find a specific site | Brand name in query, homepage |
| **Informational** | Learn something | /blog/, /guide/, /how-to/, /what-is/ |
| **Commercial** | Research before buying | /best-, /top-, /review/, /compare/ |
| **Transactional** | Act now | /buy/, /pricing/, /checkout/, /download/ |

## Classification process

1. Extract: title, H1, meta description, first 300 words, URL slug
2. Score intent signals from URL structure
3. Score intent signals from content
4. Compare URL signal vs content signal → flag mismatch

## Mismatch examples (high impact)

**Transactional URL + no pricing**
URL: `/buy-crm-software` — no price, no CTA, no trust badge.
Google sees: "This page says it's transactional but gives me an article."
Result: Low conversion score, ranking behind pages that match intent.

**Informational content + aggressive CTA**
URL: `/how-to-choose-crm` — 3 paragraphs, then "BUY NOW".
Google sees: Low E-E-A-T (content too shallow to be authoritative).
AI sees: Not citation-worthy (promotional content deprioritized).

**Commercial page with no comparison**
URL: `/best-project-management-tools` — lists one product.
Google sees: "Best" implies comparison; single-product page fails user intent.

## Output per page

```
Page: https://example.com/best-crm-software
Detected intent:    Commercial
Confidence:         High
Content alignment:  MISMATCH

Intent signals found:
+ URL contains "best-"
+ Title: "Best CRM Software 2026"
- No comparison table found
- No pros/cons section
- Only 1 product mentioned

Fix: Add comparison table with 3–5 alternatives, pros/cons per product,
     "best for" summary row. Minimum 1,200 words for commercial intent pages.
```
