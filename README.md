# seo-agent

> A Claude Code skill with 19 sub-skills for technical SEO, E-E-A-T, GEO, LLM optimization, and AI Overviews. Real data only — no hallucinated metrics.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blue)](https://claude.ai/code)
[![SEO](https://img.shields.io/badge/SEO-v4.0-green)](SKILL.md)

---

## What it does

Run `/seo audit [url]` and get a full technical + AI-era SEO report with:

- Real PageSpeed Insights data (LCP, INP, CLS)
- LLM readiness score (llms.txt, AI crawler access, entity clarity)
- E-E-A-T quality assessment from live HTML
- Search intent classification per page
- AI Overviews eligibility check
- Brand visibility across AI engines (ChatGPT, Perplexity, Gemini)
- AutoGEO content rewrites (ICLR 2026 methodology)
- Generated artifacts: sitemap.xml, robots.txt, llms.txt, schema.json, action plan

---

## Install

```bash
# Clone into your Claude Code skills directory
git clone https://github.com/nurdamiron/claude-seo-skill ~/.claude/skills/seo

# Or manually copy SKILL.md
cp SKILL.md ~/.claude/skills/seo/SKILL.md
```

The skill activates automatically when you type `/seo` in Claude Code.

---

## Sub-skills (19)

| Command | Description |
|---|---|
| `/seo audit [url]` | Full site audit — runs all 19 checks |
| `/seo page [url]` | Single page deep analysis |
| `/seo content [url]` | E-E-A-T quality scoring |
| `/seo schema [url]` | JSON-LD structured data audit + fix |
| `/seo images [url]` | Alt text, WebP/AVIF, lazy loading |
| `/seo sitemap [url]` | XML sitemap generation from crawled URLs |
| `/seo hreflang [url]` | International SEO audit |
| `/seo local [url]` | Local business + Google Business Profile |
| `/seo geo [url]` | AI Overviews / GEO optimization |
| `/seo llm [url]` | LLM citation optimization |
| `/seo plan [url]` | Strategic SEO roadmap |
| `/seo competitor [url]` | Competitor gap analysis |
| `/seo content-opt [url]` | On-page optimization |
| `/seo programmatic [url]` | Programmatic pages at scale |
| 🆕 `/seo brand [name] [url]` | AI brand visibility across ChatGPT/Perplexity/Gemini |
| 🆕 `/seo intent [url]` | Search intent classification + mismatch detection |
| 🆕 `/seo indexnow [url]` | IndexNow implementation check + setup guide |
| 🆕 `/seo rewrite [url]` | AutoGEO content rewrites (ICLR 2026) |
| 🆕 `/seo aio [keyword] [url]` | AI Overviews presence + eligibility check |

---

## Scoring System

Every audit produces a score from 0–100:

```
Technical SEO       20 pts   crawlability, HTTPS, architecture, CWV
Content / E-E-A-T   20 pts   depth, authorship, citations, freshness
LLM Readiness       18 pts   llms.txt, AI crawlers, entity clarity
On-Page SEO         17 pts   title, meta, headings, URL, internal links
Core Web Vitals     10 pts   LCP, INP, CLS — real PSI data only
Schema Markup        9 pts   JSON-LD types, validity, rich snippet eligibility
Images               6 pts   alt text, WebP/AVIF, lazy loading
```

Grades: A+ (90–100) → A (80–89) → B+ (70–79) → B (60–69) → C (50–59) → D (<50)

---

## Generated Artifacts

After every full audit, the skill writes these files:

| File | Contents |
|---|---|
| `sitemap.xml` | Only verified 200-status URLs |
| `robots.txt` | All 2026 AI crawlers allowed |
| `llms.txt` | Per llmstxt.org spec |
| `schema.json` | Organization + WebSite + Article + FAQ JSON-LD |
| `seo-action-plan.md` | Prioritized fixes with effort tags |
| `rewrite-suggestions.md` | AutoGEO rewrites: original → optimized |

---

## New in v4.0

### `/seo brand` — AI Brand Visibility
Tracks how AI search engines describe your brand today. Runs targeted WebSearch queries to surface what ChatGPT, Perplexity, and Google show when users ask about you. Detects inaccuracies, missing entity signals, and competitor co-mentions.

### `/seo intent` — Search Intent Classification
Classifies every page as Navigational / Informational / Commercial / Transactional and flags mismatches between what the URL/title promises and what the content delivers. Mismatch = lost rankings.

### `/seo indexnow` — IndexNow Audit
Checks if your site has IndexNow implemented (key file, robots.txt hint, meta tag). Provides exact implementation code if missing. Supported by Bing, Yandex, Naver, Seznam — instant indexing on content publish.

### `/seo rewrite` — AutoGEO Content Rewrites
Based on AutoGEO (ICLR 2026). Analyzes your actual page content and produces concrete rewrites of the first 30% — the zone that carries 44.2% of all LLM citation weight. Shows original → rewritten side-by-side with a list of applied rules.

### `/seo aio` — AI Overviews Presence
Checks which of your target keywords trigger Google AI Overviews and whether your content is eligible for inclusion. Detects blockers (CSR, missing FAQ schema, stale content) with actionable fixes.

---

## AI Era SEO Facts (2026)

- **44.2%** of LLM citations come from the first 30% of page content
- **85%** of Google AI Overview citations are from content < 2 years old
- **Perplexity** inline citations convert at **11x** organic search rate
- **43%** of sites fail the INP Core Web Vitals threshold
- **CSR pages = 0%** AI citation rate — bots can't execute JavaScript
- **ChatGPT** = 55–60% of all AI referral traffic in 2026

---

## Data Limitations

This skill uses only publicly accessible data. It cannot access:

- Backlinks (requires Ahrefs / Semrush / Moz)
- Full site crawl (requires Screaming Frog / Sitebulb)
- GSC impressions/CTR (requires Google Search Console access)
- Real field CWV data (requires Chrome UX Report)

These limitations are always reported in the audit output.

---

## Research & Standards

- [GEO Paper — Princeton (arxiv 2311.09735)](https://arxiv.org/abs/2311.09735)
- [AutoGEO — ICLR 2026 (cxcscmu/AutoGEO)](https://github.com/cxcscmu/AutoGEO)
- [llms.txt spec — llmstxt.org](https://llmstxt.org)
- [AI Crawler user agents — pulserank.ai](https://pulserank.ai/ai-crawlers-user-agents)
- [IndexNow — indexnow.org](https://indexnow.org)
- [Core Web Vitals — Google](https://developers.google.com/search/docs/appearance/core-web-vitals)
- [E-E-A-T — Google Search Central](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)

---

## Contributing

PRs welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

Areas where help is most valuable:
- New AI crawler user agents as they emerge
- Updated citation weight research
- Real-world audit examples in `/examples`

---

## License

MIT — see [LICENSE](LICENSE)
