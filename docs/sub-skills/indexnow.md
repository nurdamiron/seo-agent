# /seo indexnow — IndexNow Implementation

IndexNow lets you push new or updated URLs to search engines the moment you publish — instead of waiting for their crawlers to discover the change.

## Command

```
/seo indexnow [url]
```

## Supported search engines (2026)

| Engine | Notes |
|---|---|
| Bing | Primary endpoint; propagates to DuckDuckGo |
| Yandex | yandex.com/indexnow |
| Naver | searchadvisor.naver.com |
| Seznam | seznam.cz |
| DuckDuckGo | Via Bing partnership (automatic) |

Google does **not** support IndexNow. It uses its own crawl system.

## Implementation (3 steps)

**Step 1 — Generate a key**
```bash
openssl rand -hex 32
# → e.g. a1b2c3d4e5f6...
```

**Step 2 — Create the key file**
Create `/[your-key].txt` on your server containing only the key:
```
a1b2c3d4e5f6...
```

**Step 3 — Notify on publish**
```bash
curl -X POST "https://api.indexnow.org/indexnow" \
  -H "Content-Type: application/json" \
  -d '{
    "host": "example.com",
    "key": "a1b2c3d4e5f6...",
    "keyLocation": "https://example.com/a1b2c3d4e5f6.txt",
    "urlList": [
      "https://example.com/new-article",
      "https://example.com/updated-page"
    ]
  }'
```

One API call notifies all participating engines simultaneously.

## robots.txt hint (optional but recommended)

```
IndexNow: a1b2c3d4e5f6...
```

## CMS integrations

| CMS | Plugin |
|---|---|
| WordPress | IndexNow for WordPress (official Bing plugin) |
| Next.js | Manual — trigger in `getStaticProps` / API route on publish |
| Webflow | Zapier webhook → IndexNow API |
| Shopify | IndexNow app (Bing) |

## What the skill checks

1. Key file accessible at `[url]/[key].txt`
2. `IndexNow:` line in `robots.txt`
3. Meta tag: `<meta name="indexnow-verification" content="[key]">`

If none found → generates implementation code ready to paste.
