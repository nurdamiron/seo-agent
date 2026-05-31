<div align="center">

# 🧠 Claude Code Skills — a Curated, Verified Catalog

**A hand-checked collection of Claude skills that actually work** — official Anthropic skills, Claude Code developer tooling, and marketing / SEO / LLM packs — plus a built-in **19-sub-skill SEO agent** you can run today.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skills-blue)](https://claude.ai/code)
[![SEO Agent](https://img.shields.io/badge/SEO%20Agent-v4.0-green)](SKILL.md)
[![Links verified](https://img.shields.io/badge/links%20verified-2026--05--31-brightgreen)](#)
[![Repos](https://img.shields.io/badge/curated%20repos-31-blue)](SKILLS-CATALOG.md)
[![Skills](https://img.shields.io/badge/skills-3000%2B-orange)](SKILLS-CATALOG.md)

**31 curated repos · 12 niches · 3000+ skills** (plus this repo's own 19-sub-skill SEO agent).
*Every external link below was verified live via the GitHub API on **2026-05-31**. No dead links, no inflated star counts.*

</div>

> ### 🇷🇺 Полный каталог по нишам → **[SKILLS-CATALOG.md](SKILLS-CATALOG.md)**
> 31 проверенный репо/источник в 12 нишах (маркетинг, дизайн, видео, финансы, наука, безопасность, MCP…) с реальными звёздами и командами установки.

---

## Contents

- [What is a Skill?](#what-is-a-skill)
- [Official skills (Anthropic)](#official-skills-anthropic)
- [Developer skills (Claude Code)](#developer-skills-claude-code)
- [Marketing / SEO / LLM skills](#marketing--seo--llm-skills)
- [Connect Claude to your apps (MCP)](#connect-claude-to-your-apps-mcp)
- [Where to find more — curated lists](#where-to-find-more--curated-lists)
- [⭐ Bonus: built-in SEO agent](#-bonus-built-in-seo-agent)
- [Contributing](#contributing)

---

## What is a Skill?

A **Skill** is a folder with a `SKILL.md` file — instructions, scripts, and resources that Claude loads *on demand* to do a specialized task in a repeatable way. Claude reads the description, decides when it's relevant, and pulls in the full instructions only when needed.

```bash
# Official marketplace (recommended)
/plugin marketplace add anthropics/skills
/plugin install document-skills@anthropic-agent-skills

# Or via the npx skills manager (vercel-labs/skills)
npx skills add https://github.com/<owner>/<repo>

# Or drop a skill folder in manually
git clone <skill-repo> ~/.claude/skills/<name>
```

In Claude.ai (paid plans) and the API you upload skills in Settings / via the Skills API. See the [official spec](https://github.com/anthropics/skills/tree/main/spec).

---

## Official skills (Anthropic)

From [`anthropics/skills`](https://github.com/anthropics/skills) — *~145k ⭐, the canonical source.* Document skills are source-available; the rest are Apache-2.0 examples.

| Skill | What it does |
|---|---|
| **[docx](https://github.com/anthropics/skills/tree/main/skills/docx)** · **[xlsx](https://github.com/anthropics/skills/tree/main/skills/xlsx)** · **[pptx](https://github.com/anthropics/skills/tree/main/skills/pptx)** · **[pdf](https://github.com/anthropics/skills/tree/main/skills/pdf)** | The "Document Suite" — Word / Excel / PowerPoint / PDF with formulas, tables, form fields. Works out of the box. |
| **[theme-factory](https://github.com/anthropics/skills/tree/main/skills/theme-factory)** | Apply your brand colors & fonts across every artifact |
| **[brand-guidelines](https://github.com/anthropics/skills/tree/main/skills/brand-guidelines)** | Enforce a brand system in generated content |
| **[skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator)** | Scaffold new, well-formed skills in minutes |
| **[mcp-builder](https://github.com/anthropics/skills/tree/main/skills/mcp-builder)** | Generate MCP servers |
| **[webapp-testing](https://github.com/anthropics/skills/tree/main/skills/webapp-testing)** · **[frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design)** | Drive/test web apps headlessly · produce production-grade UI |

More official packs worth knowing: **[financial-services-plugins](https://github.com/anthropics/financial-services-plugins)** *(~29k ⭐ — DCF/LBO/comps/M&A)* · **[claude-cookbooks](https://github.com/anthropics/claude-cookbooks)** *(~45k ⭐ — recipes incl. CSV→Excel→PPT→PDF)*.

---

## Developer skills (Claude Code)

| Skill / pack | What it does | Source |
|---|---|---|
| **Superpowers** | Turns Claude into a disciplined engineer: brainstorm → plan → execute, with TDD, git worktrees, and code review built in. Commands: `/superpowers:brainstorm`, `:write-plan`, `:execute-plan`, `:debug`. | [obra/superpowers](https://github.com/obra/superpowers) — *~214k ⭐* |
| **Vercel agent skills** | Official Vercel pack: React / Next.js best practices, UI audit, React Native, deploy. | [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) — *~27k ⭐* |
| **skill-creator** | The fastest way to build your own custom skills (social formats, content calendars, internal workflows). | [anthropics/skills](https://github.com/anthropics/skills/tree/main/skills/skill-creator) |

Superpowers installs via the Anthropic marketplace and also runs on Codex CLI, Gemini CLI, Cursor, and Copilot CLI.

---

## Marketing / SEO / LLM skills

| Pack | What it covers | Source |
|---|---|---|
| **Marketing Skills** | 50+ skills: CRO, copywriting, SEO, analytics, ads, lifecycle email, pricing, launch, programmatic SEO, schema. | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) — *~31k ⭐* |
| **Claude SEO** | 25 sub-skills + 18 sub-agents: technical SEO, hreflang, sitemap, schema, programmatic. | [AgriciDaniel/claude-seo](https://github.com/AgriciDaniel/claude-seo) — *~7.6k ⭐* |

> Need an SEO/GEO audit *right now*? Skip to the [built-in SEO agent](#-bonus-built-in-seo-agent) below — `/seo audit [url]`.

---

## Connect Claude to your apps (MCP)

| Tool | What it does | Install |
|---|---|---|
| **Rube** · by [Composio](https://github.com/ComposioHQ/composio) *(~29k ⭐)* | One MCP server → **500+ apps** (Slack, GitHub, Notion, Gmail, Linear…) with a single OAuth. | Add `https://rube.app/mcp` as a custom connector |
| **[googleworkspace/cli](https://github.com/googleworkspace/cli)** *(~27k ⭐)* | Full Gmail / Drive / Calendar / Sheets access via built-in MCP. | `npx skills add https://github.com/googleworkspace/cli` |

---

## Where to find more — curated lists

| List / tool | Scope | Stars |
|---|---|:--:|
| [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) | 1000+ skills & plugins across agents | ~63k ⭐ |
| [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) | Skills, hooks, slash-commands, orchestrators | ~45k ⭐ |
| [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | 1000+ skills from Anthropic, Vercel, Stripe… | ~24k ⭐ |
| [vercel-labs/skills](https://github.com/vercel-labs/skills) | The `npx skills` manager + `find-skills` | ~21k ⭐ |
| [travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills) | Curated list with timeline & guides | ~13k ⭐ |
| [skills.sh](https://skills.sh) | Leaderboard ranked by install count | 🌐 |

**→ Full niche-organized catalog (RU) with 31 verified repos: [SKILLS-CATALOG.md](SKILLS-CATALOG.md)**

---

## ⭐ Bonus: built-in SEO agent

This repo ships its own Claude Code skill: **a full technical + AI-era SEO auditor with 19 sub-skills**. Real data only — no hallucinated metrics.

```bash
# Install into your Claude Code skills directory
git clone https://github.com/nurdamiron/claude-code-skills ~/.claude/skills/seo
# or copy just the skill file
cp SKILL.md ~/.claude/skills/seo/SKILL.md
```

Run `/seo audit [url]` → PageSpeed (LCP/INP/CLS) data, LLM-readiness score, E-E-A-T assessment, AI Overviews eligibility, brand visibility across ChatGPT/Perplexity/Gemini, and generated `sitemap.xml` / `robots.txt` / `llms.txt` / `schema.json` / action plan.

<details>
<summary><b>All 19 sub-skills</b></summary>

| Command | Description |
|---|---|
| `/seo audit [url]` | Full site audit — runs all 19 checks |
| `/seo page [url]` | Single page deep analysis |
| `/seo content [url]` | E-E-A-T quality scoring |
| `/seo schema [url]` | JSON-LD structured data audit + fix |
| `/seo images [url]` | Alt text, WebP/AVIF, lazy loading |
| `/seo sitemap [url]` | XML sitemap from crawled URLs |
| `/seo hreflang [url]` | International SEO audit |
| `/seo local [url]` | Local business + Google Business Profile |
| `/seo geo [url]` | AI Overviews / GEO optimization |
| `/seo llm [url]` | LLM citation optimization |
| `/seo plan [url]` | Strategic SEO roadmap |
| `/seo competitor [url]` | Competitor gap analysis |
| `/seo content-opt [url]` | On-page optimization |
| `/seo programmatic [url]` | Programmatic pages at scale |
| `/seo brand [name] [url]` | AI brand visibility across ChatGPT/Perplexity/Gemini |
| `/seo intent [url]` | Search intent classification + mismatch detection |
| `/seo indexnow [url]` | IndexNow implementation check + setup |
| `/seo rewrite [url]` | AutoGEO content rewrites (ICLR 2026) |
| `/seo aio [keyword] [url]` | AI Overviews presence + eligibility |

**Scoring** (0–100): Technical 20 · Content/E-E-A-T 20 · LLM Readiness 18 · On-Page 17 · Core Web Vitals 10 · Schema 9 · Images 6.

</details>

Full docs: **[SKILL.md](SKILL.md)** · sub-skill details in [`docs/sub-skills/`](docs/sub-skills) · sample output in [`examples/`](examples).

<details>
<summary>Research & standards behind it</summary>

- [GEO Paper — Princeton (arxiv 2311.09735)](https://arxiv.org/abs/2311.09735)
- [AutoGEO — ICLR 2026 (cxcscmu/AutoGEO)](https://github.com/cxcscmu/AutoGEO)
- [llms.txt spec — llmstxt.org](https://llmstxt.org)
- [IndexNow — indexnow.org](https://indexnow.org)
- [Core Web Vitals — Google](https://developers.google.com/search/docs/appearance/core-web-vitals)
- [E-E-A-T — Google Search Central](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)

</details>

---

## Contributing

PRs welcome — add a skill or repo only if the link is **live** and the project is **real** (no inflated stars). Include a one-line "what it does" and the current star count. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT — see [LICENSE](LICENSE). Listed third-party skills/repos keep their own licenses.
