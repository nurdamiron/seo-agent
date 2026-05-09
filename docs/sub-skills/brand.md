# /seo brand — AI Brand Visibility

Track how AI search engines currently describe your brand and detect gaps before they cost you traffic.

## When to use

- Before a PR campaign or product launch
- After a rebranding
- When you suspect competitors are outranking you in AI answers
- Periodically (monthly) to track drift in how AI describes you

## Command

```
/seo brand [brand-name] [url]
```

Example:
```
/seo brand "Stripe" https://stripe.com
```

## What it fetches

| Query | Purpose |
|---|---|
| `"[brand]" site:perplexity.ai` | What Perplexity users see |
| `what is [brand] [industry]` | Primary AI answer check |
| `[brand] review [year]` | Sentiment signals |
| `[brand] vs competitors` | Co-mention landscape |
| `[brand] [core product/service]` | Product association accuracy |

Also fetches `[url]/llms.txt` to verify brand description accuracy.

## Scoring (0–100)

| Factor | Points |
|---|---|
| Brand appears in top results for `"[brand]"` | 30 |
| Accurate description in search snippets | 25 |
| Appears for `[brand] vs` or `[brand] review` | 20 |
| Positive sentiment dominant | 15 |
| No entity disambiguation issues | 10 |

## Common issues found

**Entity confusion** — Your brand is being confused with a different company or product.
Fix: Add `Organization` schema with unambiguous `legalName` + `sameAs` to Wikidata.

**Missing from AI answers** — Brand doesn't appear for core queries.
Fix: Create llms.txt, add FAQ schema answering "What is [brand]?", build Wikidata entity.

**Stale description** — AI describes old product name, old service, or outdated info.
Fix: Update About page, refresh dateModified in schema, update llms.txt description.

**Negative co-mentions** — Brand appears alongside competitor with negative framing.
Fix: E-E-A-T content strategy — original research, case studies, statistics.

## Tips

- Run this before and after publishing a major piece of content to measure impact
- Wikidata entity = single highest-ROI action for brand AI visibility
- llms.txt brand description should match your Google Knowledge Panel description exactly
