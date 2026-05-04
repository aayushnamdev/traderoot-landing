# TradeRoot — Landing Page

Marketing landing page for [TradeRoot](https://traderoot.co), a performance coaching practice for prop firm and futures traders.

---

## What this is

A single-page site designed to convert cold traffic (Instagram, X) into booked sessions. The audience is skeptical, technically skilled, and has been burned by trading gurus before. The design signals "this is different" before a word is read.

Built in Claude Design, exported and hosted here as a static HTML page.

---

## The Product

TradeRoot offers 1-on-1 performance coaching sessions for traders who know their edge but can't execute it consistently. Both founders are present in every session — not just the first one.

**Founders:**
- **Aayush Namdev** — Prop trader (Apex Trader Funding + Alpha Capital Group), MA Psychology candidate at Chandigarh University, clinical training under Dr. Nitin Sethi and Japneet Bakhshi Clinic.
- **Khushi Narwal** — MA Psychology + BSc Mathematics, clinical training at a private psychology practice.

The method draws from psychodynamic tradition, identity and object relations theory, and Rogers' client-centered therapy (empathy, unconditional positive regard, congruence).

---

## Structure

```
traderoot-landing/
├── index.html        # Full landing page (self-contained HTML/CSS/JS)
└── assets/
    ├── aayush.jpg
    ├── khushi.jpg
    ├── khushi.png
    └── traderoot-logo.svg
```

No build step. No dependencies. Open `index.html` in a browser and it works.

---

## Design System

| Token | Value | Usage |
|---|---|---|
| Root Green | `#1C3A2E` | Hero, final CTA, nav on scroll |
| Warm White | `#F7F5F0` | Page background |
| Stone | `#E8E4DC` | Alternating sections, cards |
| Amber | `#C8974A` | CTA buttons only |
| Charcoal | `#2D2D2B` | Body text |

**Fonts:** Fraunces (headlines) + DM Sans (body) via Google Fonts.

**Aesthetic direction:** Forensic calm — like a very good doctor who takes their time.

---

## Page Sections

1. **Hero** — Root Green, headline, dual CTA (Book a session / 10-minute call)
2. **The Mirror** — 4 numbered statements that name the trader's loop
3. **Why Everything Else Failed** — Addresses discipline-level advice
4. **The Work** — 3-stage session method: Pattern Recognition → Origin Tracing → Witnessed Integration
5. **Evidence Beat** — Aayush's founder story as a blockquote
6. **Founders** — Staggered editorial layout with credentials
7. **The Foundation** — Psychodynamic, Object Relations, Rogers — the traditions this is built on
8. **Pricing** — Two cards: $47 single session (early access) / $340 four-session series
9. **FAQ** — 7 accordion items
10. **Final CTA** — Bookend Root Green section
11. **Footer** — Three-column with links, social, India crisis line disclaimer

---

## Deployment

Static file — deploy anywhere:

```bash
# Netlify drop
# Vercel
# GitHub Pages (already configured via this repo)
```

To run locally:

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

---

## Pricing (current)

| | Single Session | Four Sessions |
|---|---|---|
| Price | $47 (early access, first 15 clients) | $340 |
| Format | 60 min, video call | 6 weeks, flexible |
| Both founders | Yes | Yes |

After the first 15 spots, single sessions move to $97.

---

*Performance coaching, not therapy. TradeRoot does not diagnose or treat mental health conditions. If you are in distress, please contact iCall (9152987821) or Vandrevala Foundation (1860 2662 345).*
