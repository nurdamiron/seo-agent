# Example: /seo audit output

This is a sample output to illustrate the format. All data in a real audit comes from live fetches.

```
╔══════════════════════════════════════════════════════════════╗
║  SEO ANALYZER v4.0  |  example.com                           ║
╚══════════════════════════════════════════════════════════════╝

  Fetching data — no simulation, real results only

  [1/7]  HTML + meta + schema ......................... done
  [2/7]  robots.txt + sitemap.xml ..................... done
  [3/7]  llms.txt ..................................... 404 not found
  [4/7]  PageSpeed Insights (mobile + desktop) ........ done
  [5/7]  HTTP headers (curl -sI) ...................... done
  [6/7]  Search index (site:example.com) .............. done
  [7/7]  IndexNow key file ............................ 404 not found

╔══════════════════════════════════════════════════════════════╗
║  SEO HEALTH REPORT  |  example.com  |  2026-05-09            ║
╠══════════════════════════════════════════════════════════════╣
║  SCORE: 61/100   [██████░░░░]   Grade: B                     ║
╚══════════════════════════════════════════════════════════════╝

  Category            Points    Bar              Weight
  ────────────────────────────────────────────────────
  Technical SEO       16/20   [████████░░]      20%
  Content / E-E-A-T   13/20   [██████░░░░]      20%
  LLM Readiness        9/18   [█████░░░░░]      18%   <- AI era
  On-Page SEO         12/17   [███████░░░]      17%
  Core Web Vitals      6/10   [██████░░░░]      10%
  Schema Markup        3/ 9   [███░░░░░░░]       9%
  Images               2/ 6   [███░░░░░░░]       6%
  ────────────────────────────────────────────────────
  TOTAL               61/100  [██████░░░░]

  Core Web Vitals (real PSI data):
  LCP [mobile]: 3.2s  NEEDS WORK
  INP [mobile]: 180ms GOOD
  CLS [mobile]: 0.08  GOOD
  Performance:  54% mobile  |  81% desktop

╔══════════════════════════════════════════════════════════════╗
║  CRITICAL 2   HIGH 4   MEDIUM 5   LOW 3                      ║
╚══════════════════════════════════════════════════════════════╝

-- CRITICAL ─────────────────────────────────────────────────
  [!] llms.txt missing — AI crawlers have no structured site map
  [!] No FAQ schema anywhere on site — zero AIO eligibility signal

-- HIGH ──────────────────────────────────────────────────────
  [#] GPTBot blocked in robots.txt — invisible to ChatGPT
  [#] LCP 3.2s on mobile — fails Core Web Vitals threshold (< 2.5s)
  [#] No author schema on blog posts — E-E-A-T gap
  [#] IndexNow not implemented — slow Bing indexing on publishes

-- MEDIUM ────────────────────────────────────────────────────
  [~] Meta descriptions missing on 3 pages found in sitemap
  [~] No dateModified in Article schema (only datePublished)
  [~] og:image missing on /about page
  [~] Heading hierarchy broken: H1 → H3 (H2 skipped) on /services
  [~] No Organization sameAs to Wikidata or LinkedIn

-- LOW ───────────────────────────────────────────────────────
  [-] Server header leaks: "Apache/2.4.51"
  [-] 2 images missing alt text
  [-] Twitter Card meta tags absent

-- DATA LIMITATIONS ──────────────────────────────────────────
  Backlinks           requires Ahrefs / Semrush / Moz
  Full site crawl     requires Screaming Frog / Sitebulb
  GSC data            requires Google Search Console access
  Real INP field data requires Chrome UX Report (CrUX)
  Holistic CWV score  requires GSC Core Web Vitals report
──────────────────────────────────────────────────────────────

╔══════════════════════════════════════════════════════════════╗
║  GENERATED FILES                                             ║
╠══════════════════════════════════════════════════════════════╣
║  sitemap.xml           — built from crawled URLs             ║
║  robots.txt            — all AI crawlers allowed             ║
║  llms.txt              — site map for LLMs                   ║
║  schema.json           — JSON-LD ready to paste              ║
║  seo-action-plan.md    — prioritized fixes with effort tags  ║
║  rewrite-suggestions.md — AutoGEO content rewrites           ║
╚══════════════════════════════════════════════════════════════╝
```
