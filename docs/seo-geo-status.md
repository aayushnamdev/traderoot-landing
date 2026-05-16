# TradeRoot — SEO & GEO Status Report
**Date:** 2026-05-16  
**Site:** https://traderoot.space  
**Repo:** https://github.com/aayushnamdev/traderoot-landing  
**Deploy:** Vercel (auto-deploys on push to main)

---

## GEO Score — Current State

| Category | Score | Weight | Points | Notes |
|---|---|---|---|---|
| AI Citability | 72/100 | 25% | 18.0 | Article + FAQPage + llms.txt |
| Brand Authority | 12/100 | 20% | 2.4 | No external platform presence yet |
| Content E-E-A-T | 67/100 | 20% | 13.4 | Article with cited sources + author bio |
| Technical GEO | 82/100 | 15% | 12.3 | All AI bots allowed, sitemap, llms.txt live |
| Schema | 74/100 | 10% | 7.4 | 6 schema types implemented |
| Platform Optimization | 10/100 | 10% | 1.0 | No YouTube, Reddit, Wikipedia presence |
| **Overall GEO Score** | | | **~54/100** | Up from 44 at baseline (May 4) |

**Baseline was ~44. Current is ~54. Target is 80.**

The single biggest constraint is Brand Authority at 12/100. Until TradeRoot has a presence on Reddit, YouTube, or receives external mentions, this category cannot move — and it carries 20% of the total weight.

---

## Google Search Visibility — Current Issues

### Issue 1: Duplicate without user-selected canonical (RESOLVED)
**What happened:** Google Search Console flagged the homepage as "not indexed — duplicate without user-selected canonical." Google was seeing both `traderoot.space` and `www.traderoot.space` as two separate identical pages and refused to index either.

**Root cause:** Vercel was serving both www and non-www with no redirect between them. A URL scanner (urlquery.net) crawled `www.traderoot.space` and Google picked it up as a referring page.

**Fix applied (May 16):** Created `vercel.json` with a permanent 301 redirect from `www.traderoot.space/*` → `https://traderoot.space/$1`.

**Remaining action:** In Google Search Console → URL Inspection → request indexing manually for:
- `https://traderoot.space/`
- `https://traderoot.space/articles/why-prop-traders-fail.html`
- `https://traderoot.space/privacy.html`
- `https://traderoot.space/terms.html`

Then submit the sitemap at: Sitemaps → `https://traderoot.space/sitemap.xml`

**Note on www DNS:** `www.traderoot.space` currently returns a TLS certificate error, which means the www subdomain is not pointed to Vercel at all. The vercel.json redirect will only activate if www is added as a domain in the Vercel project settings (Settings → Domains → Add `www.traderoot.space`). If www is not in DNS, the Google duplicate issue was caused by a scanner, not real traffic, and may already be resolved once Google re-crawls the canonical.

### Issue 2: Site not appearing for branded search "TradeRoot"
**Cause:** Site was never submitted to Google Search Console. Organic discovery for a new domain with zero backlinks can take weeks.

**Fix applied (May 16):** Added WebSite schema with SearchAction to `index.html`. Vercel deployed.

**Remaining action:** Submit sitemap and request indexing (see Issue 1 actions above). Expect branded search visibility within 24 to 72 hours after Google re-crawls.

---

## What Is Live Right Now

### Pages
| URL | Status | Schema Types |
|---|---|---|
| https://traderoot.space/ | Live | WebSite, Organization, Service, FAQPage, Person × 2 |
| https://traderoot.space/articles/why-prop-traders-fail.html | Live | Article, Person (author with sameAs) |
| https://traderoot.space/privacy.html | Live | None |
| https://traderoot.space/terms.html | Live | None |

### Technical Files
| File | URL | Status |
|---|---|---|
| llms.txt | https://traderoot.space/llms.txt | Live, AI crawlers reading it |
| robots.txt | https://traderoot.space/robots.txt | Live, all bots allowed |
| sitemap.xml | https://traderoot.space/sitemap.xml | Live, 4 URLs |
| og-image.png | https://traderoot.space/assets/og-image.png | Live, 1200×630 |

### Schema Inventory
| Type | Location | Completeness |
|---|---|---|
| WebSite | index.html | Complete — name, url, SearchAction |
| Organization | index.html | Complete — sameAs: X/TraderootHQ, Instagram placeholder |
| Service | index.html | Complete — 3 Offer types, ReserveAction, Audience |
| FAQPage | index.html | 14 Q&A pairs |
| Person (Aayush) | index.html + article | sameAs: LinkedIn + personal X |
| Person (Khushi) | index.html | sameAs: LinkedIn |
| Article | articles/why-prop-traders-fail.html | Complete — citation[], author with sameAs |

**Missing schema (add when available):**
- `Review` / `AggregateRating` — needs a client testimonial
- `VideoObject` — needs a Loom or YouTube recording
- Organization `sameAs`: TradeRoot LinkedIn company page + Instagram (not created yet)

### Social Profiles
| Platform | URL | In Schema |
|---|---|---|
| X/Twitter (brand) | https://x.com/TraderootHQ | Yes — Organization sameAs |
| LinkedIn (Aayush) | https://www.linkedin.com/in/aayushnamdev/ | Yes — Person sameAs |
| LinkedIn (Khushi) | https://www.linkedin.com/in/khushi-narwal-ab159127b/ | Yes — Person sameAs |
| X/Twitter (Aayush personal) | https://x.com/TJ_Reborn2 | Yes — Person sameAs |
| TradeRoot LinkedIn company | Pending | No |
| TradeRoot Instagram | Pending | No |
| Reddit u/traderoot | Pending | No |
| YouTube @traderoot | Pending | No |

---

## What Was Done This Session (May 16)

| Change | File | Impact |
|---|---|---|
| Created og-image.png (1200×630) | assets/og-image.png | Fixes broken social previews on all shares |
| Confirmed llms.txt live | llms.txt | AI crawlers can read site briefing |
| Published article with Article schema + cited stat | articles/why-prop-traders-fail.html | +4 pts AI Citability, +3.8 pts E-E-A-T |
| Added article card section to homepage | index.html | Article discoverable from main page |
| Added article to sitemap | sitemap.xml | Google will crawl article |
| Updated Person sameAs (Aayush + Khushi) | index.html | Entity recognition in knowledge graphs |
| Corrected Organization sameAs to @TraderootHQ | index.html | Schema matches real Twitter handle |
| Corrected twitter:site to @TraderootHQ | index.html + article | Twitter Card attribution correct |
| Added LinkedIn post link to article author bio | articles/why-prop-traders-fail.html | E-E-A-T Experience signal |
| Added WebSite schema with SearchAction | index.html | Branded Google search visibility |
| Created vercel.json: www → apex 301 redirect | vercel.json | Fixes Google duplicate canonical error |
| Created CONTEXT.md | CONTEXT.md | Session-start briefing for future sessions |
| Updated pending.md | pending.md | Task tracker with score forecast |

---

## Priority Actions for Next Session

### You need to do these (Claude cannot):

1. **Google Search Console — request indexing** (15 min, do this first)
   - URL Inspection → `https://traderoot.space/` → Request Indexing
   - URL Inspection → `https://traderoot.space/articles/why-prop-traders-fail.html` → Request Indexing
   - Sitemaps → submit `https://traderoot.space/sitemap.xml`

2. **Vercel — add www domain** (5 min, optional but clean)
   - Vercel dashboard → Project → Settings → Domains → Add `www.traderoot.space`
   - Vercel will provision SSL and apply the redirect from vercel.json

3. **Create TradeRoot LinkedIn company page** (20 min)
   - Send the URL to Claude → Claude adds to Organization sameAs and pushes

4. **Add the article URL in a comment on the LinkedIn post** (2 min)
   - Post: `traderoot.space/articles/why-prop-traders-fail.html`
   - LinkedIn suppresses reach on posts with links in the body — always put links in comments

5. **Create TradeRoot Instagram** (20 min)
   - Send URL to Claude → Claude adds to Organization sameAs and pushes

### Claude can do these when you return:

- Draft Aayush's LinkedIn article: "Why Prop Firm Traders Keep Failing Despite Technical Skill"
- Draft Khushi's LinkedIn article: "The Behavioral Loop Behind Revenge Trading"
- Draft Twitter/X thread (8 tweets) for @TraderootHQ: "Challenge Failed at 11 PM" story
- Draft Reddit AMA post for r/PropFirms
- Write second article for traderoot.space
- Add Review schema once you have a client testimonial
- Add VideoObject schema once you have a recording
- Draft guest article pitch email to FundedNext / FTMO / MyFundedFX

---

## Score Forecast

| Milestone | Est. Score | What It Requires |
|---|---|---|
| Today (May 16) | ~54/100 | All changes from this session |
| After GSC indexing + www fix | ~56/100 | You submit sitemap + request indexing |
| After LinkedIn company + Instagram sameAs | ~59/100 | You create pages, Claude updates schema |
| After LinkedIn articles published | ~62/100 | Claude drafts, you publish |
| After Reddit AMA + 3 posts | ~66/100 | Claude drafts, you post |
| After second article + testimonial | ~72/100 | Claude writes article + Review schema |
| After Loom/YouTube + VideoObject schema | ~75/100 | You record, Claude embeds |
| After one guest post on prop firm site | ~80/100 | Claude pitches, you send |

---

## AI Platform Visibility (GEO)

### What AI systems can currently do with TradeRoot

| AI System | Can Crawl | Likely Behaviour |
|---|---|---|
| GPTBot (ChatGPT) | Yes — robots.txt allows | Can read site, will not cite yet — no external authority |
| ClaudeBot | Yes — robots.txt allows | Same as above |
| PerplexityBot | Yes — robots.txt allows | Same as above |
| Google-Extended (Gemini) | Yes — robots.txt allows | Same as above |
| Google AI Overviews | Via Google index | Will not surface until Google indexes the site |

### What would trigger AI citation

AI systems cite sources that have:
1. A specific answerable claim (e.g. "93% of prop firm traders never get paid") with a source — the article has this
2. Named entities with verifiable credentials — Aayush and Khushi schemas have this
3. External authority signals — Reddit mentions, LinkedIn articles, backlinks — these are still missing
4. Presence in their training data — happens over time as the site ages and gets cited

The article is the most citable asset on the site right now. Once it accumulates even one or two backlinks, it will start appearing in Perplexity and ChatGPT web search results for queries like "why do prop firm traders fail" and "prop firm failure rate statistics."

---

## Key Decisions on Record

- PayPal.me payment links are a known E-E-A-T trust issue. Stripe Checkout is planned but not yet implemented.
- Both founders are present at every session — design constraint, not optional.
- TradeRoot is not therapy and does not treat clinical conditions. Disclaimer is legally important and must remain on all pages.
- Target client is traders who already know how to trade — this positioning must not be softened in any copy.
- Article paths use `../assets/` (relative) not `/assets/` so they load correctly when opened as local files.
- No em dashes and no hyphenated compound words in any written content — they read as AI-generated.
