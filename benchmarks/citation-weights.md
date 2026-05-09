# LLM Citation Weight Research — 2026

Annotated research data underpinning the scoring system in SKILL.md.

---

## Content Position Effect

**Finding:** 44.2% of all LLM citations come from the first 30% of page content.

**Source:** AutoGEO (ICLR 2026) — analysis of citation patterns across 10,000+ pages cited by GPT-4, Claude, and Gemini.

**Implication:** The first 30% of a page (typically 300–500 words) has 3.5× the citation probability of the remaining 70%.

---

## Content Freshness

**Finding:** 85% of Google AI Overview citations are from content published or updated within the last 2 years. 44% are from 2025.

**Source:** Analysis of 500,000 AIO citations, reported by BrightEdge Research (Q1 2026).

**Implication:** Content older than 2 years has significantly reduced AIO eligibility. `dateModified` in schema is read by Google.

---

## AI Platform Traffic Share (2026)

| Platform | Share of AI referral traffic | Conversion multiplier vs organic |
|---|---|---|
| ChatGPT | 55–60% | ~1x |
| Perplexity | 18–22% | **11x** |
| Gemini | ~8.7% | ~2x |
| Others | ~13% | varies |

**Source:** SparkToro AI referral traffic study, Q1 2026. Perplexity conversion rate from Perplexity internal data shared at SearchOn 2026.

---

## Content Format Citation Rates

| Format | Citation rate |
|---|---|
| Listicles | 21.9% |
| Articles (long-form) | 16.7% |
| Product pages | 13.7% |
| How-to guides | 12.1% |
| News articles | 9.3% |

**Source:** Princeton GEO Paper (arxiv.org/abs/2311.09735), updated with 2025 data.

---

## Definition-First Effect

**Finding:** Pages with a clear definition of the primary topic in the first 150 words receive significantly higher AI impression scores.

**Source:** AutoGEO ablation study (ICLR 2026). Pages with definition-first structure showed 34% higher citation rate vs pages with preamble-first structure.

---

## INP Failure Rate

**Finding:** 43% of sites fail the INP Core Web Vitals threshold (< 200ms) as of Q1 2026.

**Source:** Google CrUX data, March 2026. INP replaced FID as a ranking signal in March 2024.

---

## Organic Rank → AIO Correlation

**Finding:** Top-10 organic ranking is the strongest single predictor of Google AI Overview inclusion.

**Source:** Ahrefs analysis of 100,000 AIO citations (2025). 92% of AIO-cited pages rank in top 10 for the cited query.

**Implication:** AIO is not a replacement for organic SEO — it amplifies pages already ranking well.

---

## llms.txt Hallucination Reduction

**Finding:** Sites with a valid llms.txt file see 30–70% reduction in AI hallucinations about their brand/product.

**Source:** Early adopter data from llmstxt.org community (600+ sites as of Q1 2026). Not yet peer-reviewed — treat as directional.

---

## FAQ Schema → AIO Signal

**Finding:** FAQPage schema is the strongest single technical signal for Google AI Overview eligibility for informational queries.

**Source:** Google Search Central documentation + correlation analysis from Semrush (Q4 2025).

---

## Sources Index

| Source | URL | Reliability |
|---|---|---|
| AutoGEO (ICLR 2026) | github.com/cxcscmu/AutoGEO | High — peer-reviewed |
| Princeton GEO Paper | arxiv.org/abs/2311.09735 | High — peer-reviewed |
| BrightEdge Research Q1 2026 | brightedge.com/resources | Medium — industry |
| SparkToro AI Traffic Study | sparktoro.com | Medium — industry |
| Ahrefs AIO Analysis | ahrefs.com/blog | Medium — industry |
| Google CrUX | developers.google.com/web/tools/chrome-user-experience-report | High — primary |
| llmstxt.org community | llmstxt.org | Low — self-reported |
| pulserank.ai crawler list | pulserank.ai/ai-crawlers-user-agents | Medium — updated monthly |
