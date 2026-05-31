# Каталог скиллов по нишам

Проверено: **2026-05-31** (звёзды — через GitHub API на эту дату). Все ссылки — живые репозитории.

> Большинство этих репо — для **Claude Code** (терминал). В Claude.ai (чат) их можно использовать, упаковав нужную папку `skill/` в `.zip` и загрузив через Settings → Capabilities.

---

## 🎯 Маркетинг / контент / SMM

| Репо | ⭐ | Что внутри | Установка |
|---|---|---|---|
| [`coreyhaines31/marketingskills`](https://github.com/coreyhaines31/marketingskills) | ~31k | Самый популярный маркетинг-пак: CRO, копирайтинг, SEO, аналитика, email-цепочки, growth | `/plugin marketplace add coreyhaines31/marketingskills` → `/plugin install marketing-skills` |
| [`boraoztunc/skills`](https://github.com/boraoztunc/skills) | ~73 | Копирайтинг (фреймворки Огилви), реклама, SEO, дизайн, контент-план | `git clone` → папку в `~/.claude/skills/` |

---

## 🛠 Разработка / workflow

| Репо | ⭐ | Что внутри | Установка |
|---|---|---|---|
| [`obra/superpowers`](https://github.com/obra/superpowers) | ~214k | Флагман экосистемы: брейншторм → план → исполнение по TDD, дебаг | `/plugin marketplace add obra/superpowers-marketplace` → `/plugin install superpowers@superpowers-marketplace` |
| [`Jeffallan/claude-skills`](https://github.com/Jeffallan/claude-skills) | ~9.5k | 66 скиллов для фуллстека: языки, бэк/фронт фреймворки, тесты, DevOps, API | копировать `SKILL.md` в `~/.claude/skills/` |

---

## 🔒 Безопасность

| Репо | ⭐ | Что внутри |
|---|---|---|
| [`briiirussell/cybersecurity-skills`](https://github.com/briiirussell/cybersecurity-skills) | ~217 | Кибербез для AI-агентов (Claude Code, Cursor, Codex) |
| [`BehiSecc/awesome-claude-skills`](https://github.com/BehiSecc/awesome-claude-skills) | ~9k | Список с упором на security: OWASP Top 10, Trail of Bits, редакция PII, env-secrets |

---

## 📦 Большие мульти-категорийные библиотеки

| Репо | ⭐ | Что внутри |
|---|---|---|
| [`alirezarezvani/claude-skills`](https://github.com/alirezarezvani/claude-skills) | ~17k | 337 скиллов: инженерия, маркетинг, продукт, compliance, C-level, ресёрч, операции |
| [`Jeffallan/claude-skills`](https://github.com/Jeffallan/claude-skills) | ~9.5k | 66 скиллов для фуллстек-разработки (см. выше) |

---

## 🌐 Подключение приложений (MCP)

| Инструмент | ⭐ | Что делает | Установка |
|---|---|---|---|
| **Rube** ([rube.app](https://rube.app), by [Composio](https://github.com/ComposioHQ/composio)) | ~29k | Коннектор к 500+ приложениям (Slack, GitHub, Notion, Gmail) одной авторизацией | Claude Desktop / Code → Settings → Connectors → Add custom connector → `https://rube.app/mcp` |

---

## 📚 Мета-каталоги (где искать ещё)

| Репо | ⭐ | Что внутри |
|---|---|---|
| [`anthropics/skills`](https://github.com/anthropics/skills) | ~145k | Официальный репо Anthropic — эталон и примеры |
| [`ComposioHQ/awesome-claude-skills`](https://github.com/ComposioHQ/awesome-claude-skills) | ~63k | Список с разбивкой по задачам (контент, ресёрч, Twitter и др.) |
| [`hesreallyhim/awesome-claude-code`](https://github.com/hesreallyhim/awesome-claude-code) | ~45k | Скиллы, хуки, slash-команды, оркестраторы, плагины |
| [`VoltAgent/awesome-agent-skills`](https://github.com/VoltAgent/awesome-agent-skills) | ~24k | 1000+ скиллов от Anthropic, Vercel, Stripe, Cloudflare и комьюнити |
| [`travisvn/awesome-claude-skills`](https://github.com/travisvn/awesome-claude-skills) | ~13k | Кураторский awesome-список с таймлайном и гайдами |

---

## ⚠️ Заметки

- У `coreyhaines31/marketingskills` есть форки-клоны с тем же описанием (`ayrshare/marketingskills` ~10⭐, `syntax-syndicate/marketing-skills` ~51⭐) — ставь **оригинал** от `coreyhaines31`.
- Перед установкой любого community-скилла бегло открой его `SKILL.md`: ты ставишь чужие инструкции, которые Claude будет исполнять у тебя. Доверяй проверенным авторам.
- В security-списках периодически всплывают и вычищаются фишинговые ссылки — слепо доверять каталогам на 100% не стоит.
- Звёзды и состав репо меняются — дата проверки в шапке.
