# Contributing

## What's worth contributing

- **New AI crawler user agents** — the list changes monthly; PRs with sources are merged fast
- **Updated research** — citation weight studies, AI Overview ranking factors, GEO data
- **Bug reports** — if a sub-skill produces wrong output for a real URL, open an issue with the URL
- **New sub-skills** — open an issue first to discuss before implementing
- **Examples** — real audit outputs in `/examples` (anonymize if needed)

## How to contribute

1. Fork the repo
2. Create a branch: `git checkout -b feature/your-thing`
3. Make changes to `SKILL.md`
4. Test by running the skill against at least one real URL
5. Open a PR with: what changed, why, and a source link if adding research data

## Editing SKILL.md

The skill is a single markdown file with clear section headers (STEP 1 through STEP 15).
Each section is self-contained. Keep edits surgical — don't restructure sections
unless there's a clear reason.

## Adding AI crawlers (STEP 7.2)

Format:
```
User-agent: [BotName]   # [platform] — [purpose]
```

Always include a source link in the PR (official docs or reliable tracking source).

## Style rules

- No fluff — every sentence should be actionable or factual
- Data must have a source (year + origin)
- New sub-skills need: process steps, output format, scoring criteria
