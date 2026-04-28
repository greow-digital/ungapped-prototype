# Ungapped Homepage — Asset Inventory

All visuals are placeholders during build. Erik will swap in real assets after.

## Logo (header)

**Slot:** `assets/logo.svg`
**Description:** Ungapped wordmark in teal `#1FB6B6`
**Placeholder:** Inline SVG with text "ungapped" in teal Open Sans Bold

## Hero product UI screenshot (Rule.io-style)

**Slot:** `assets/hero-product-ui.png`
**Description:** Actual Ungapped product UI screenshot in the editor view. Should signal "modern, AI-augmented product." Reference: Rule.io's hero (https://rule.io) which shows email builder + Ask AI overlay + Blocks/Layouts/Style sidebar.

**What the screenshot should contain:**
- Main canvas: an email or campaign being built in the editor. Use a real Ungapped-style template (e.g. "Välkommen till nyhetsbrevet" or "Join the list")
- Floating AI overlay (positioned over canvas): modal labeled "Ask AI" or "Ungapped AI" with options like:
  - Förbättra texten / Improve writing
  - Justera ton / Adjust tone
  - Fixa grammatik / Fix grammar
  - Översätt till / Translate to
- Right sidebar (within the screenshot frame): Blocks / Layouts / Stil tabs
- Subtle drop shadow on screenshot edges for depth
- Aspect ratio ~16:10 or 4:3, ~960x600 to ~1200x800 pixels

**Placeholder:** `https://placehold.co/1200x800/F4F4F4/1FB6B6?text=Ungapped+editor+with+AI+overlay`
**Notes:** Until real screenshot exists, build can use placeholder image OR mock the entire UI in HTML/CSS as a visual element (more work but more impressive — Rule.io does this with real interactive-looking screenshot).

## Hero decorative gradient blob

**Slot:** CSS only (no image needed)
**Description:** Soft, blurred gradient circle/blob positioned behind H1. Combine Ungapped brand colors:
- Coral `#E94B6E` at low opacity (10-20%)
- Teal `#1FB6B6` at low opacity (10-20%)
- Optional purple/pink accent for extra visual interest
**Implementation:** Pure CSS using `radial-gradient` + `filter: blur(60-100px)` on a positioned div behind the H1.

## Hero pre-headline decorative element

**Slot:** `assets/icons/blomma-logo-mark.svg`
**Description:** Small flower/blomma mark from Ungapped's logo (the icon part, without the "ungapped" wordmark). Coral or teal color. ~32-40px size, positioned top-left above H1. Adds brand signature similar to Rule.io's green crown.
**Placeholder:** Inline SVG flower/circle in coral or teal, ~32x32px

## Logo carousel (Section 2)

12 logos. All ~120x60px PNG with transparent background.

| # | Customer | Slot |
|---|---|---|
| 1 | Örnsköldsviks kommun | `assets/logos/ornskoldsvik.png` |
| 2 | JM | `assets/logos/jm.png` |
| 3 | IF Metall | `assets/logos/if-metall.png` |
| 4 | Avtalat | `assets/logos/avtalat.png` |
| 5 | Byggföretagen | `assets/logos/byggforetagen.png` |
| 6 | Chalmers | `assets/logos/chalmers.png` |
| 7 | SACO | `assets/logos/saco.png` |
| 8 | Spritmuseum | `assets/logos/spritmuseum.png` |
| 9 | Svenskt Näringsliv | `assets/logos/svenskt-naringsliv.png` |
| 10 | RFSL | `assets/logos/rfsl.png` |
| 11 | Kommunalarbetaren | `assets/logos/kommunalarbetaren.png` |
| 12 | SEKO | `assets/logos/seko.png` |

**Placeholder:** Use `https://placehold.co/120x60/F4F4F4/6B6B6B?text=LOGO` with the customer name as text

## "Why Ungapped" icons (Section 3)

| # | Icon | Slot |
|---|---|---|
| 1 | Swedish flag / shield | `assets/icons/svensk.svg` |
| 2 | Stack / boxes / unified | `assets/icons/plattform.svg` |
| 3 | Headset / chat / people | `assets/icons/support.svg` |

**Placeholder:** Inline SVG circles in teal with emoji 🇸🇪 📦 🤝

## Trust badges (Hero + Section 4)

| Badge | Slot | Note |
|---|---|---|
| Capterra 4.5★ | `assets/badges/capterra.svg` | Use real Capterra badge if linkable; placeholder pill OK |
| G2 4.3★ | `assets/badges/g2.svg` | Same — real if available, otherwise pill |
| Software Advice | `assets/badges/software-advice.svg` | Optional |
| GDPR-anpassat | `assets/badges/gdpr.svg` | Custom pill in teal |
| Kollektivavtal | `assets/badges/kollektivavtal.svg` | Custom pill |

**Placeholder:** Styled inline divs as pills with text + star

## Customer testimonial avatars (Section 4)

| # | Person | Slot |
|---|---|---|
| Hero | Monika P. | `assets/avatars/monika-p.jpg` |
| A | Victoria Säker | `assets/avatars/victoria-saker.jpg` |
| B | Yosef B. | `assets/avatars/yosef-b.jpg` |
| C | Martina Mofidi | `assets/avatars/martina-mofidi.jpg` |

**Placeholder:** Initials in colored circle (e.g. coral background, white "MP" / "VS" / "YB" / "MM")

## Product card thumbnails (Section 5)

| # | Product | Slot |
|---|---|---|
| 1 | E-post UI screenshot | `assets/products/email.png` |
| 2 | SMS UI screenshot | `assets/products/sms.png` |
| 3 | Survey UI screenshot | `assets/products/surveys.png` |
| 4 | Event UI screenshot | `assets/products/events.png` |
| 5 | Automation UI screenshot | `assets/products/automation.png` |

**Placeholder:** `https://placehold.co/480x320/F4F4F4/1FB6B6?text=Product+screenshot`

## Step-by-step thumbnails (Section 6)

Optional small screenshots for each of 4 steps.

| # | Step | Slot |
|---|---|---|
| 1 | Signup form | `assets/steps/signup.png` |
| 2 | Contact import | `assets/steps/import.png` |
| 3 | Campaign builder | `assets/steps/builder.png` |
| 4 | Analytics dashboard | `assets/steps/analytics.png` |

**Placeholder:** `https://placehold.co/240x160/F4F4F4/1FB6B6?text=Step+N`

## Industries icons / images (Section 7 — Gong-inspired offset cards)

Each card has TWO icons:
- Top-left: industry icon (~32px, can be emoji OR small SVG illustration in brand colors)
- Top-right: arrow icon (~24px, in white circle background, ~32px circle, indicates clickable card → industry-page)

| # | Segment | Top-left icon | Slot |
|---|---|---|---|
| 1 | Offentlig sektor / Public sector | 🏛️ or column/government building SVG | `assets/industries/public-sector.svg` |
| 2 | Medlemsorganisationer / Member orgs | 🤝 or hands/group SVG | `assets/industries/member-orgs.svg` |
| 3 | Bygg & fastighet / Construction & real estate | 🏗️ or crane/building SVG | `assets/industries/construction.svg` |
| 4 | Skolor & lärosäten / Education | 🎓 or graduation cap SVG | `assets/industries/education.svg` |

**Placeholder approach:** Use emoji directly in HTML for fastest implementation (works without custom SVGs and reads well at 32px+). Stretch goal: replace with small custom SVG icons in Ungapped brand colors (teal stroke or coral fill) for more refined feel.

**Arrow icon:** Inline SVG arrow-right (→) in white circle. Color shifts to coral on card hover. ~24px arrow inside ~32px circle.

## Decorative

- Teal dot pattern (background decoration in hero, similar to current site)
  - **Placeholder:** Pure CSS dotted pattern using `radial-gradient`
- Soft yellow/coral blob (occasional decorative shape)
  - **Placeholder:** CSS gradient circles

## Favicon

**Slot:** `assets/favicon.ico`
**Placeholder:** Generated from "U" in coral on white

## Open Graph / Social cards

**Slot:** `assets/og-image.png`
**Description:** 1200x630 OG image with H1 + logo + key visual
**Placeholder:** `https://placehold.co/1200x630/1FB6B6/FFFFFF?text=Ungapped`

---

## Asset checklist for Erik (post-build)

When the HTML build is done, Erik needs to:
1. Export real customer logos from current site (or get from customers)
2. Take fresh product screenshots (or use existing marketing assets)
3. Get headshots for testimonials (with permission)
4. Source/license a hero illustration
5. Verify Capterra/G2 badge usage rights and embed real badges
6. Generate favicon and OG image from final design
