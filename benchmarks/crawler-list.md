# AI Crawler User Agents — 2026

Maintained list of known AI crawler user agents. Updated as new crawlers are discovered.
Source: [pulserank.ai/ai-crawlers-user-agents](https://pulserank.ai/ai-crawlers-user-agents) + official documentation.

## OpenAI

| User-agent | Purpose | Respects robots.txt |
|---|---|---|
| `GPTBot` | Training data collection | Yes |
| `OAI-SearchBot` | ChatGPT search results | Yes |
| `ChatGPT-User` | User-triggered browsing | Yes |

Official docs: [platform.openai.com/docs/gptbot](https://platform.openai.com/docs/gptbot)

## Anthropic

| User-agent | Purpose | Respects robots.txt |
|---|---|---|
| `ClaudeBot` | Primary crawler | Yes |
| `Claude-SearchBot` | Claude search | Yes |
| `Claude-User` | User-triggered | Yes |

Official docs: [anthropic.com/claude-bot](https://www.anthropic.com/claude-bot)

## Google

| User-agent | Purpose | Respects robots.txt |
|---|---|---|
| `Google-Extended` | Gemini / AI Overviews training | Yes |
| `Google-CloudVertexBot` | Vertex AI | Yes |
| `Gemini-Deep-Research` | Deep research feature | Yes |
| `Googlebot` | Standard web crawl | Yes |
| `GoogleOther` | Experimental Google crawls | Yes |

## Perplexity

| User-agent | Purpose | Respects robots.txt |
|---|---|---|
| `PerplexityBot` | Primary crawler | Yes |
| `Perplexity-User` | User-triggered | **No** — ignores robots.txt by design |

**Important:** `Perplexity-User` is a user-triggered request and cannot be blocked via robots.txt. This is a documented Perplexity behavior.

## Apple

| User-agent | Purpose | Respects robots.txt |
|---|---|---|
| `Applebot` | Standard Apple crawler | Yes |
| `Applebot-Extended` | Apple AI / Siri | Yes |

Official docs: [support.apple.com/applebot](https://support.apple.com/en-us/111900)

## Other AI companies

| User-agent | Company | Purpose | Respects robots.txt |
|---|---|---|---|
| `DeepSeekBot` | DeepSeek | Training | Yes |
| `DuckAssistBot` | DuckDuckGo | DuckAssist AI answers | Yes |
| `YouBot` | You.com | AI search | Yes |
| `CCBot` | Common Crawl | Open dataset (used by many LLMs) | Yes |
| `Bytespider` | ByteDance/TikTok | AI training | Yes |
| `Amazonbot` | Amazon | Alexa + AI | Yes |
| `Meta-ExternalAgent` | Meta | AI features | Yes |
| `cohere-ai` | Cohere | Training | Yes |
| `AI2Bot` | Allen Institute | Research | Yes |

## Scrapers (often blocked)

These are not official AI company crawlers and are commonly blocked:

| User-agent | Notes |
|---|---|
| `GPTBot` variants with fake UA | Impersonators — not OpenAI |
| `SemrushBot` | SEO tool crawler |
| `AhrefsBot` | SEO tool crawler |

## Recommended robots.txt block

Copy this block into your robots.txt to allow all major AI crawlers:

```
User-agent: GPTBot
Allow: /

User-agent: OAI-SearchBot
Allow: /

User-agent: ChatGPT-User
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: Claude-SearchBot
Allow: /

User-agent: Claude-User
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: Google-Extended
Allow: /

User-agent: Google-CloudVertexBot
Allow: /

User-agent: Gemini-Deep-Research
Allow: /

User-agent: Applebot-Extended
Allow: /

User-agent: DeepSeekBot
Allow: /

User-agent: DuckAssistBot
Allow: /

User-agent: CCBot
Allow: /

User-agent: YouBot
Allow: /
```

---

*Last updated: 2026-05-09. Submit a PR if a crawler is missing or has changed behavior.*
