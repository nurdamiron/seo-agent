# /seo rewrite — AutoGEO Content Rewrites

Generate AI-optimized rewrites of your most citation-critical content based on AutoGEO methodology (ICLR 2026).

## Command

```
/seo rewrite [url]
```

## Why the first 30% matters

Research from the Princeton GEO paper and AutoGEO (ICLR 2026) shows:

- **44.2%** of all LLM citations come from the first 30% of page content
- Definition-first openings correlate with significantly higher AI impression scores
- LLMs favor content that directly answers a query within the first 150 words

Rewriting the opening section of a page is the highest-ROI content action for AI search visibility.

## The 8 AutoGEO rules

| Rule | Bad | Good |
|---|---|---|
| **Definition first** | "In today's digital landscape, managing projects is complex..." | "Project management software is a tool that..." |
| **Active voice** | "X was measured by our team" | "Our team measured X" |
| **Stat anchoring** | "significantly faster" | "43% faster (Gartner, 2025)" |
| **Question headings** | "Our Features" | "What features does [product] include?" |
| **Short sentences** | 35-word sentence | Two sentences, max 20 words each |
| **Bold key terms** | first use plain | first use **bolded** |
| **Inverted pyramid** | context → detail → answer | answer → detail → context |
| **No throat-clearing** | "It is important to understand that..." | [delete, start with the substance] |

## Output format

The skill produces `rewrite-suggestions.md` with side-by-side diffs:

```
## https://example.com/article

### H2: Our Approach to Data Security

ORIGINAL:
"In today's increasingly connected world, data security has become
more important than ever before. Many organizations struggle with
protecting sensitive information from malicious actors..."

REWRITTEN:
"**Data security** is the practice of protecting digital information
from unauthorized access, corruption, or theft. Organizations using
[Product] reduce breach risk by 67% (IBM Security Report, 2025).

The three core security layers in [Product] are encryption at rest,
zero-trust access control, and automated threat detection."

Changes applied:
+ Definition in sentence 1
+ Deleted throat-clearing opener
+ Added specific stat with source
+ Shortened avg sentence: 28 → 17 words
+ Bolded "Data security" at first use
```

## Sections the skill prioritizes

1. First paragraph (highest citation weight)
2. Each H2 first paragraph
3. Any section where heading is not phrased as a question
4. Conclusions or summaries (often cited for "in summary" snippets)

## Research sources

- AutoGEO (ICLR 2026): [github.com/cxcscmu/AutoGEO](https://github.com/cxcscmu/AutoGEO)
- Princeton GEO Paper: [arxiv.org/abs/2311.09735](https://arxiv.org/abs/2311.09735)
