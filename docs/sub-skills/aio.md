# /seo aio — AI Overviews Presence Check

Check which queries trigger Google AI Overviews and whether your content qualifies for inclusion.

## Command

```
/seo aio [keyword] [url]
```

Example:
```
/seo aio "best CRM for startups" https://example.com/crm-guide
```

If keyword is omitted, the skill derives 3–5 queries from the page's H1, meta title, and H2s.

## What are AI Overviews?

Google AI Overviews (formerly SGE) are AI-generated answer boxes that appear above organic results for ~20% of queries in 2026. They cite specific pages, pulling excerpts directly into the answer.

Being cited in an AI Overview = top-of-SERP exposure without requiring #1 ranking.

## How Google selects AIO sources (2026 data)

| Factor | Impact |
|---|---|
| Top-10 organic ranking | Strongest predictor |
| Content freshness (< 2 years) | 85% of citations |
| FAQ schema present | Significant positive signal |
| speakable schema present | Moderate positive signal |
| Answer-first structure | High correlation |
| CSR (client-side rendering) | 0% — AI cannot index |
| Statistic density | Higher = more likely cited |

## Eligibility scoring (0–100)

| Check | Points |
|---|---|
| Page ranks top 10 for query | 30 |
| Content < 2 years old | 20 |
| FAQ schema present | 15 |
| Answer in first 150 words | 15 |
| Server-side rendered HTML | 10 |
| speakable schema | 10 |

## Output

```
╔══════════════════════════════════════════════════════════════╗
║  AI OVERVIEWS CHECK  |  example.com  |  2026-05-09           ║
╠══════════════════════════════════════════════════════════════╣
║  AIO Readiness Score: 72/100                                 ║
╚══════════════════════════════════════════════════════════════╝

  Keyword                  SERP Type   Top-3?  AIO Eligible?
  ─────────────────────────────────────────────────────────
  best CRM for startups    Commercial  NO      UNLIKELY
  what is CRM software     Info        YES     LIKELY
  CRM vs spreadsheet       Info        NO      POSSIBLE
  ─────────────────────────────────────────────────────────

  Blockers:
  [!] No FAQ schema — missing primary AIO signal
  [~] Content last modified 2024-01-15 — approaching 2-year threshold

  Quick wins:
  - Add FAQPage schema to /crm-guide
  - Add speakable markup to the definition section
  - Update dateModified and add fresh 2026 statistics
```

## Quick wins for AIO eligibility

1. **FAQ schema** — biggest single technical signal
2. **speakable schema** — targets AI Overviews + voice search
3. **Answer in first 150 words** — structure, not just content
4. **Refresh content date** — set dateModified, add 2026 data
5. **Get above position 10** — organic rank is the baseline gate
