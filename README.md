# Ungapped Homepage Rebuild — Build Brief

## Mission

Build a new homepage for **ungapped.se** that keeps the existing brand visuals (teal/coral palette, sans-serif type, soft rounded cards, generous spacing) but implements a sharper conversion-optimized structure based on a CRO audit + customer review analysis (G2 + Capterra, 28 reviews).

## Context

Ungapped is a Swedish digital marketing platform (founded 2006, part of Liana Technologies / Ilkka Group). Sells email marketing, SMS, surveys, events, and marketing automation.

Primary ICP: Swedish public sector (kommuner, regioner, myndigheter, förvaltningar) + trust-sensitive B2B (member organizations, schools, financial services, healthcare). Main differentiators: **Swedish data residency, Swedish-language support, 20 years in market, all-in-one platform, kollektivavtal.**

The current homepage (see `current-homepage-screenshot.png` in this folder when added, or visit https://ungapped.se) is visually clean but suffers from:
- H1 is poetic and undifferentiating ("Som digital kommunikation borde vara") — could be Mailchimp, HubSpot, anyone
- USPs are buried below feature lists (in fold 3-6)
- No logo carousel for social proof
- No review-aggregator badges (Capterra 4.5★, G2 4.3★)
- No "Why Ungapped" reasoning block
- No step-by-step onboarding visualization
- Hamburger menu coexists with main nav (unusual)
- "Karriär" + "GDPR" take primary nav slots that should be in footer

## Deliverable

A single self-contained `index.html` file with embedded CSS and minimal vanilla JS (for logo carousel scroll + testimonial rotation). Requirements:

- **Responsive** (mobile-first, breakpoints: 480px / 768px / 1024px / 1280px)
- **Visually faithful** to existing Ungapped brand (see `brand-guidelines.md`)
- **Accessible** (semantic HTML5, alt text, ARIA where needed, decent contrast)
- **Fast** (vanilla HTML/CSS/JS — no React, no heavy frameworks)
- **Copy-faithful** to `copy.md` (do not invent new copy)

Use **placeholders for all images** (logos, product screenshots, illustrations, icons). List every placeholder in `assets.md` so Erik can swap real assets in later. Use `https://placehold.co/` style URLs or simple SVG placeholders inline.

## How to use this folder

1. Read `brand-guidelines.md` — colors, typography, spacing, components, voice
2. Read `homepage-structure.md` — the 6 sections and IA/nav specification
3. Read `copy.md` — all actual text per section (do not paraphrase)
4. Read `assets.md` — list of placeholder images and what each represents
5. Build `index.html` per the spec
6. Verify by opening in a browser at multiple viewport widths

## Important constraints

- **Build BOTH languages, but English is the priority.** Erik will present the prototype to international CEOs in English. The English version (`index.en.html` etc.) is the polished showcase. The Swedish version (`index.sv.html`) ships alongside but English copy is the one that must be perfect.
- **English copy is European-positioned**, not Swedish-internal. Drop Sweden-only references like "kollektivavtal" or "Stockholm" in the English version. Use "European", "EU data residency", "GDPR by design", "in your language", "Built in Europe" framings instead. Swedish version keeps the Swedish references (kollektivavtal, Stockholm) for local resonance.
- **No em-dashes** in copy. Use colon, period, or hyphen instead.
- **No invented testimonials.** Only use the quotes provided in `copy.md` (sourced from G2, Capterra, and current Ungapped site).
- **Trust badges are real.** Capterra 4.5★ (10 reviews), G2 4.3★ (18 reviews).
- **Hero is the most important section.** Spend disproportionate effort getting H1, sub, CTAs, USPs, and trust-bar right.

## Stretch goals (after MVP works)

- Light scroll animations (fade-in on intersection observer) — keep tasteful
- Hover states on all interactive elements
- "Sticky" CTA on scroll-down past hero
- Dark mode toggle (only if trivial)

## Output structure

```
ungapped-homepage-build/
├── index.sv.html              # Swedish homepage
├── index.en.html              # English homepage
├── signup.sv.html             # Swedish signup page (split-pane, Rule.io-style)
├── signup.en.html             # English signup page
├── boka-demo.sv.html          # Swedish demo booking page (Funnel-style, 2-step form)
├── boka-demo.en.html          # English demo booking page
├── assets/                    # Placeholder images (or links in HTML)
├── README.md                  # This file
├── brand-guidelines.md        # Visual + voice spec
├── homepage-structure.md      # 6-section IA + nav spec
├── copy.md                    # All copy, ready to use (bilingual)
├── assets.md                  # Asset placeholder inventory
├── navigation-prompt.md       # Follow-up: nav restructure
├── hero-refactor-prompt.md    # Follow-up: hero (Rule.io-style with product UI)
├── signup-page-prompt.md      # Follow-up: signup page (Rule.io-style split-pane)
└── demo-page-prompt.md        # Follow-up: demo booking page (Funnel-style, 2-step form)
```

**Build order recommendation:**
1. Read README.md + brand-guidelines.md + homepage-structure.md + copy.md + assets.md
2. Build index.sv.html + index.en.html (homepage)
3. Build signup.sv.html + signup.en.html (see signup-page-prompt.md)
4. Build boka-demo.sv.html + boka-demo.en.html (see demo-page-prompt.md)
5. If hero or nav don't match spec, apply hero-refactor-prompt.md or navigation-prompt.md as follow-up corrections

## Reference flow for Claude Code

```
1. Open all four .md files
2. Confirm understanding by listing the 6 sections + naming the 3 hero USPs
3. Build index.html in one go (target: 600-1200 lines, embedded CSS)
4. Self-test at 375px / 768px / 1280px widths
5. Output a checklist of what's done vs what's a placeholder
```
