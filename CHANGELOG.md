# Changelog

## v4.0 — 2026-05-09

### Added
- `/seo brand` — AI brand visibility tracking across ChatGPT, Perplexity, Gemini
- `/seo intent` — search intent classification (Navigational / Informational / Commercial / Transactional) with mismatch detection
- `/seo indexnow` — IndexNow implementation check with ready-to-use setup code
- `/seo rewrite` — AutoGEO content rewrites based on ICLR 2026 methodology
- `/seo aio` — Google AI Overviews presence and eligibility check
- `rewrite-suggestions.md` added to generated artifacts
- `IndexNow:` key hint added to generated `robots.txt`
- `docs/sub-skills/` — detailed documentation for all 5 new sub-skills
- `templates/` — llms.txt, robots.txt, and 4 JSON-LD schema templates
- `benchmarks/` — sourced research data for citation weights and crawler list
- `.github/` — issue templates, PR template, CI validation workflow

### Changed
- Data collection log updated from 5 steps to 7 (added index check + IndexNow check)
- Sub-skill count: 14 → 19
- Version bump: v3.0 → v4.0

---

## v3.0 — initial release

- 14 sub-skills: audit, page, content, schema, images, sitemap, hreflang, local, geo, llm, plan, competitor, content-opt, programmatic
- Scoring system: 7 categories, 100 points total
- Generated artifacts: sitemap.xml, robots.txt, llms.txt, schema.json, seo-action-plan.md
- Core Web Vitals via PageSpeed Insights API (no key required)
- LLM readiness scoring with llms.txt + AI crawler checks
- E-E-A-T quality assessment framework
