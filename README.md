# seo-agent — Working Claude Skills, Curated

> A hand-checked collection of **Claude skills that actually work** — official Anthropic skills, developer tooling for Claude Code, and marketing / SEO / LLM skills — plus a built-in **19-sub-skill SEO agent** you can run today.
>
> Every external link below was verified live on **2026-05-31**. No dead links, no inflated star counts.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skills-blue)](https://claude.ai/code)
[![SEO Agent](https://img.shields.io/badge/SEO%20Agent-v4.0-green)](SKILL.md)

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

Install paths (Claude Code):

```bash
# Official marketplace (recommended)
/plugin marketplace add anthropics/skills
/plugin install document-skills@anthropic-agent-skills

# Or drop a skill folder in manually
git clone <skill-repo> ~/.claude/skills/<name>
```

In Claude.ai (paid plans) and the API you upload skills in Settings / via the Skills API. See the [official spec](https://github.com/anthropics/skills/tree/main/spec).

---

## Official skills (Anthropic)

From [`anthropics/skills`](https://github.com/anthropics/skills) — *~145k ⭐, the canonical source.* The document skills are source-available; the rest are Apache-2.0 examples.

| Skill | What it does |
|---|---|
| **[docx](https://github.com/anthropics/skills/tree/main/skills/docx)** | Create & edit Word documents — formatting, tables, formulas |
| **[xlsx](https://github.com/anthropics/skills/tree/main/skills/xlsx)** | Build Excel spreadsheets with formulas and charts |
| **[pptx](https://github.com/anthropics/skills/tree/main/skills/pptx)** | Generate PowerPoint decks |
| **[pdf](https://github.com/anthropics/skills/tree/main/skills/pdf)** | Read, fill, and manipulate PDFs (incl. form fields) |
| **[theme-factory](https://github.com/anthropics/skills/tree/main/skills/theme-factory)** | Apply your brand colors & fonts across every artifact |
| **[brand-guidelines](https://github.com/anthropics/skills/tree/main/skills/brand-guidelines)** | Enforce a brand system in generated content |
| **[skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator)** | Scaffold new, well-formed skills |
| **[mcp-builder](https://github.com/anthropics/skills/tree/main/skills/mcp-builder)** | Generate MCP servers |
| **[webapp-testing](https://github.com/anthropics/skills/tree/main/skills/webapp-testing)** | Drive and test web apps headlessly |
| **[frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design)** | Produce distinctive, production-grade UI |

> The four document skills (`docx / xlsx / pptx / pdf`) are the "Document Suite" — they work out of the box on paid Claude.ai and in Claude Code.

---

## Developer skills (Claude Code)

| Skill / pack | What it does | Source |
|---|---|---|
| **Superpowers** | Turns Claude into a disciplined engineer: brainstorm → plan → execute, with TDD, git worktrees, and code review built in. Commands: `/superpowers:brainstorm`, `/superpowers:write-plan`, `/superpowers:execute-plan`. | [obra/superpowers](https://github.com/obra/superpowers) — *~214k ⭐* |
| **Systematic Debugging** | 4-phase root-cause debugging loop. Ships *inside* Superpowers as `/superpowers:debug`. | [obra/superpowers](https://github.com/obra/superpowers) |
| **skill-creator** | The fastest way to build your own custom skills (social-media formats, content calendars, internal workflows) in minutes. | [anthropics/skills](https://github.com/anthropics/skills/tree/main/skills/skill-creator) |

Install Superpowers via the Anthropic marketplace — it also runs on Codex CLI, Gemini CLI, Cursor, and Copilot CLI.

---

## Marketing / SEO / LLM skills

| Pack | What it covers | Source |
|---|---|---|
| **Marketing Skills** | 50+ skills: CRO, copywriting, SEO, analytics, ads, lifecycle email, pricing, launch, programmatic SEO, schema. Organized by discipline; skills reference each other. | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) — *~31k ⭐* |

Highlights from that pack worth pulling on their own: `ai-seo` (get cited by ChatGPT / Perplexity / AI Overviews), `programmatic-seo`, `schema`, `seo-audit`, `copywriting`, `cro`, `competitors`, `directory-submissions`.

> Need an SEO/GEO audit *right now*? Skip straight to the [built-in SEO agent](#-bonus-built-in-seo-agent) in this repo.

---

## Connect Claude to your apps (MCP)

| Tool | What it does | Source |
|---|---|---|
| **Rube** | One MCP server that connects Claude to **500+ apps** (Slack, GitHub, Notion, Gmail, Linear, Airtable…) with a single OAuth. Ask Claude to "send the email" or "create the Linear issue" and it does it. | [rube.app](https://rube.app) · by [Composio](https://github.com/ComposioHQ/composio) — *~29k ⭐* |

Install in Claude Code / Desktop by adding the MCP URL `https://rube.app/mcp` as a custom connector, then authenticate the apps you want once.

---

## Where to find more — curated lists

Bigger registries when you want to browse the long tail (verified 2026-05-31):

| List | Scope | Stars |
|---|---|---|
| [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) | 1000+ skills & plugins across Claude + other agents | ~63k ⭐ |
| [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) | Skills, hooks, slash-commands, orchestrators, plugins | ~45k ⭐ |
| [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | 1000+ skills from Anthropic, Vercel, Stripe, Cloudflare, Figma… | ~24k ⭐ |
| [travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills) | Curated Claude skills & tools | ~13k ⭐ |
| [BehiSecc/awesome-claude-skills](https://github.com/BehiSecc/awesome-claude-skills) | Curated Claude skills | ~9k ⭐ |
| [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) | MCP servers (the connector layer under skills) | ~88k ⭐ |

---

## ⭐ Bonus: built-in SEO agent

This repo ships its own Claude Code skill: **a full technical + AI-era SEO auditor with 19 sub-skills**. Real data only — no hallucinated metrics.

```bash
# Install into your Claude Code skills directory
git clone https://github.com/nurdamiron/seo-agent ~/.claude/skills/seo
# or copy just the skill file
cp SKILL.md ~/.claude/skills/seo/SKILL.md
```

Then run `/seo audit [url]` and get PageSpeed (LCP/INP/CLS) data, an LLM-readiness score, E-E-A-T assessment, AI Overviews eligibility, brand visibility across ChatGPT/Perplexity/Gemini, and generated `sitemap.xml` / `robots.txt` / `llms.txt` / `schema.json` / action plan.

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

### Research & standards behind it

- [GEO Paper — Princeton (arxiv 2311.09735)](https://arxiv.org/abs/2311.09735)
- [AutoGEO — ICLR 2026 (cxcscmu/AutoGEO)](https://github.com/cxcscmu/AutoGEO)
- [llms.txt spec — llmstxt.org](https://llmstxt.org)
- [IndexNow — indexnow.org](https://indexnow.org)
- [Core Web Vitals — Google](https://developers.google.com/search/docs/appearance/core-web-vitals)
- [E-E-A-T — Google Search Central](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)

---

## Contributing

PRs welcome — add a skill or repo only if the link is **live** and the project is **real** (no inflated stars). Include a one-line "what it does" and, for collections, the current star count. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT — see [LICENSE](LICENSE). Listed third-party skills/repos keep their own licenses.
