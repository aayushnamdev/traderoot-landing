# TradeRoot — Project Context

Load this at the start of any new session. Everything needed to continue work on the TradeRoot website and GEO strategy is here.

---

## What TradeRoot Is

Performance coaching for prop firm and futures traders. Not therapy. Uses clinical psychology methods (psychodynamic, object relations theory, Rogers' client-centred framework) to identify and interrupt the behavioural patterns that prevent skilled traders from executing consistently.

**Core proposition:** Your trading strategy isn't broken. Your operating system is.

**Target client:** Prop firm traders who pass their strategy but fail evaluations due to revenge trading, moving stop losses, cutting winners early. They already know how to trade technically — they cannot execute what they know.

**Not for:** Beginners, traders still learning strategy basics.

---

## Founders

### Aayush Namdev
- Role: Co-founder, Performance Coach, funded trader
- Credentials: MA Psychology candidate, Chandigarh University · Clinical training under Dr. Nitin Sethi and Japneet Bakhshi Clinic
- Trading: Funded at Apex Trader Funding ($100K) and Alpha Capital Group ($100K)
- LinkedIn: https://www.linkedin.com/in/aayushnamdev/
- Personal X: https://x.com/TJ_Reborn2
- Photo: assets/aayush.jpg

### Khushi Narwal
- Role: Co-founder, Psychologist
- Credentials: MA Psychology + BSc Mathematics, Chandigarh University / Delhi University · Clinical psychology practice background
- LinkedIn: https://www.linkedin.com/in/khushi-narwal-ab159127b/
- Personal X: pending
- Photo: assets/khushi.jpg (also khushi.png)

---

## Live URLs

### Site
| Page | URL |
|---|---|
| Homepage | https://traderoot.space |
| Article 1 | https://traderoot.space/articles/why-prop-traders-fail.html |
| Privacy Policy | https://traderoot.space/privacy.html |
| Terms | https://traderoot.space/terms.html |

### Assets
| Asset | URL |
|---|---|
| OG image (1200×630) | https://traderoot.space/assets/og-image.png |
| Favicon (SVG) | https://traderoot.space/assets/favicon.svg |
| Logo (SVG, full) | https://traderoot.space/assets/traderoot-logo.svg |
| Aayush photo | https://traderoot.space/assets/aayush.jpg |
| Khushi photo | https://traderoot.space/assets/khushi.jpg |

### AI / Crawler Files
| File | URL |
|---|---|
| llms.txt | https://traderoot.space/llms.txt |
| robots.txt | https://traderoot.space/robots.txt |
| sitemap.xml | https://traderoot.space/sitemap.xml |

---

## Social Profiles

| Platform | Handle / URL | Status |
|---|---|---|
| X/Twitter (brand) | https://x.com/TraderootHQ | Live |
| X/Twitter (Aayush personal) | https://x.com/TJ_Reborn2 | Live |
| LinkedIn (Aayush) | https://www.linkedin.com/in/aayushnamdev/ | Live |
| LinkedIn (Khushi) | https://www.linkedin.com/in/khushi-narwal-ab159127b/ | Live |
| LinkedIn (TradeRoot company page) | pending | Not created yet |
| Instagram (brand) | pending | Not created yet |
| Reddit (u/traderoot) | pending | Not reserved yet |
| YouTube (@traderoot) | pending | Not reserved yet |
| Substack (traderoot) | pending | Not reserved yet |

When new profiles are created: send URLs here → Claude updates Organization sameAs in index.html and pushes.

---

## File Tree

```
traderoot-landing/
├── index.html              # Main landing page (all sections, schema, JS)
├── privacy.html            # Privacy policy
├── terms.html              # Terms of service
├── llms.txt                # AI crawler briefing document
├── robots.txt              # Allows all bots incl. GPTBot, ClaudeBot, PerplexityBot
├── sitemap.xml             # All 4 pages with lastmod dates
├── CONTEXT.md              # This file — load at session start
├── pending.md              # GEO task tracker with score history
├── README.md               # Technical setup notes
├── articles/
│   └── why-prop-traders-fail.html   # Article 1 — by Aayush, 950 words
└── assets/
    ├── favicon.svg         # 64×64 tree+candlestick icon, Root Green bg
    ├── traderoot-logo.svg  # Full logo: tree + "TradeRoot" wordmark
    ├── og-image.png        # 1200×630 social share image
    ├── aayush.jpg          # Founder photo
    ├── khushi.jpg          # Founder photo
    └── khushi.png          # Founder photo (alt format)
```

---

## Tech Stack

| Layer | Tool |
|---|---|
| Hosting | Vercel (auto-deploys on push to main) |
| Repo | https://github.com/aayushnamdev/traderoot-landing |
| Branch | main |
| Build | None — static HTML, no build step |
| Fonts | Fraunces (headlines) + DM Sans (body) via Google Fonts |
| Booking | Cal.com — https://cal.com/traderoot/free-10-min-call |
| Payment | PayPal.me (temporary — Stripe Checkout planned) |
| Email | hello@traderoot.space |

**Deploy workflow:** Edit files → git add → git commit → git push origin main → Vercel deploys in ~30 seconds.

---

## Schema Inventory

All schema is in `index.html` as a single JSON-LD array. Article schema is in the article file.

| Schema Type | Location | Key Fields |
|---|---|---|
| Organization | index.html | name, url, logo, email, founder[], slogan, foundingDate, address, sameAs[] |
| Service | index.html | name, provider, offers[3], potentialAction (ReserveAction), audience |
| FAQPage | index.html | 14 Q&A pairs covering therapy/coaching distinction, behaviours, method, pricing |
| Person (Aayush) | index.html | jobTitle, worksFor, url, description, alumniOf, knowsAbout[], sameAs[LinkedIn, X] |
| Person (Khushi) | index.html | jobTitle, worksFor, url, description, alumniOf, knowsAbout[], sameAs[LinkedIn] |
| Article | articles/why-prop-traders-fail.html | headline, author (Person with sameAs), datePublished, citation[2], keywords |

**Missing schema (add when available):**
- Review / AggregateRating — needs a client testimonial first
- VideoObject — needs a Loom or YouTube recording
- WebSite with SearchAction
- Organization sameAs: TradeRoot LinkedIn company page, Instagram (not created yet)

---

## Brand Design System

| Token | Hex | Usage |
|---|---|---|
| Root Green | #1C3A2E | Hero bg, nav, CTA sections, schema dark blocks |
| Warm White | #F7F5F0 | Page background, body text on dark |
| Stone | #E8E4DC | Alternating sections, cards, stat rows |
| Amber | #C8974A | CTA buttons, accent text, pull quote colour |
| Charcoal | #2D2D2B | Body text |
| Teal Light | #5dcaa5 | Logo icon colour, URL text |
| Teal Mid | #1a8a6a | Logo secondary |
| Teal Dark | #0a5c48 | Logo tertiary |

**Fonts:** Fraunces (serif, headlines) · DM Sans (sans-serif, body)
**Aesthetic:** Forensic calm — like a very good doctor who takes their time.

---

## Pricing

| Product | Price | Details |
|---|---|---|
| Single session (early access) | $47 | 60 min, video, both founders, first 15 clients only (8 remaining as of May 2026) |
| Single session (standard) | $97 | After first 15 spots fill |
| Four-session series | $340 ($85/session) | Over 6 weeks, flexible scheduling |
| Free clarity call | $0 | 10 min with Khushi, no pitch |

---

## Content Published

### Articles
1. **Why 93% of Prop Firm Traders Never Get Paid, and Why It Is Rarely About Strategy**
   - URL: https://traderoot.space/articles/why-prop-traders-fail.html
   - Author: Aayush Namdev
   - Published: 2026-05-16
   - Word count: ~950
   - Key stat: FPFX Technology, 300,000+ accounts, 7% payout rate (Finance Magnates, 2025)
   - Concepts: object relations theory, internal working models, Rogers' congruence
   - Schema: Article with citation array, author sameAs

### Articles Drafted (not yet published)
- None yet. Next article candidates:
  - "Why You Move Your Stop Loss Even When You Know You Shouldn't" (Aayush)
  - "The Behavioral Loop Behind Revenge Trading" (Khushi — LinkedIn version exists as pending task)

---

## GEO Score Tracker

| Date | Score | What Changed |
|---|---|---|
| 2026-05-04 (baseline) | ~44/100 | Initial audit |
| 2026-05-16 | ~57/100 | og-image, article + schema, sameAs profiles, llms.txt confirmed |

**Category breakdown (current):**

| Category | Score | Weight | Points |
|---|---|---|---|
| AI Citability | 72/100 | 25% | 18.0 |
| Brand Authority | 12/100 | 20% | 2.4 |
| Content E-E-A-T | 67/100 | 20% | 13.4 |
| Technical GEO | 82/100 | 15% | 12.3 |
| Schema | 74/100 | 10% | 7.4 |
| Platform | 10/100 | 10% | 1.0 |
| **Total** | | | **~54/100** |

**Ceiling constraint:** Brand Authority at 12/100 with 20% weight. Requires LinkedIn + Reddit + external mentions to move.

---

## Writing Style Rules

- No em dashes (—). Replace with commas, colons, or split into two sentences.
- No hyphenated compound words (industry-wide, discipline-based, pre-conscious, client-centred, first-attempt). Rewrite as two words or restructure the phrase.
- These patterns read as AI-generated. Aayush flagged this explicitly.
- Write plainly. The site tone is forensic calm, not academic or salesy.

---

## Key Decisions Made

- PayPal.me is a known E-E-A-T trust issue but not yet replaced (Stripe Checkout is planned)
- Both founders are present at every session — this is a design constraint, not optional
- The method is not therapy and does not treat clinical conditions — the disclaimer is deliberate and legally important
- TradeRoot targets traders who already know how to trade (not beginners) — this is a positioning decision that should not be softened in copy
- Article paths use `../assets/` (relative) not `/assets/` (root-relative) so they work when opened locally as files
