# Ungapped Homepage — Structure & IA

## Navigation (top of page)

### Header — desktop

Layout: logo (left) → main nav (center-left) → utility (center-right) → CTAs (right)

```
[Ungapped logo]   Plattform ▾ | Tjänster ▾ | Use cases | Priser | Blogg | Resurscenter ▾   🔍 🌐 Logga in   [Testa gratis] [Boka demo]
```

Changes from current site:
- **REMOVED** "Karriär" (move to footer)
- **REMOVED** "GDPR" as top-level (move to footer)
- **REMOVED** "Inspiration" (consolidated into "Resurscenter")
- **REMOVED** hamburger menu entirely (everything visible in main nav)
- **ADDED** "Use cases" between Tjänster and Priser
- **ADDED** "Resurscenter" replacing "Inspiration" + including former hamburger items (Manualer, Sök gömd, Partners m.m.)
- **ADDED** 🔍 search icon visible in main nav
- **ADDED** 🌐 language switcher icon (replaces text-link)
- **MOVED to footer** GDPR, Karriär, Partners, Cookies, Sitemap

### Header — mobile

Logo (left) → hamburger (right). Inside hamburger: full nav stack including all top-level + sub-items + CTAs.

### Footer

Standard B2B-footer with columns:
- **Plattform** (E-post, SMS, Enkäter, Events, Marketing Automation)
- **Användningsområden** (Nyhetsbrev, Transaktionella mejl, Kundundersökningar, etc.)
- **Tjänster** (Rådgivning, Utbildning, Integrationer, Uppstartspaket)
- **Företag** (Om oss, Karriär, Partners, Kontakt)
- **Resurser** (Blogg, Kunskapsbank, Manualer, GDPR, Cookies)
- **Sociala** (LinkedIn, Facebook, Instagram, YouTube)

---

## Page sections (in order, hero down)

### Section 1 — Hero (fold 1) — Rule.io-inspired layout

**Reference:** Rule.io's homepage hero (https://rule.io). Product-centric, two-column, with actual product UI screenshot (not illustration) showing AI-augmentation visible to the eye.

Full-width section, white background with soft gradient blob (purple/pink/blue or Ungapped-branded coral/teal mix) decoratively positioned behind the H1 area. Two-column layout on desktop (text ~40% left, product UI screenshot ~60% right). Single column stacked on mobile (text first, visual second).

Layout details (left column, top to bottom):

1. **Decorative pre-headline element** — small flower/blomma icon from Ungapped logo (coral or teal) at top-left of column. Optional but adds brand signature similar to Rule's green crown.
2. **H1** — large, bold, dark, vertically stacked across 3-4 lines on desktop.
3. **Subheadline** — body-large size (18px), mid-gray, ~3-4 lines.
4. **Dual CTA row** — primary "Testa gratis" (coral solid) + secondary "Boka demo" (white with coral border/text). Side by side on desktop, stacked on mobile.
5. **Trust microcopy** under CTAs in small gray text: "Inget kreditkort krävs · Full tillgång under hela testperioden"

Layout details (right column):

- **Actual product UI screenshot** — NOT a generic illustration. Show Ungapped's editor/builder interface in real use. Ideally:
  - Main canvas: an email or campaign being built (with "Join the list" / "Welcome our customers" or similar Ungapped-style template visible)
  - Floating overlay: AI Assistant modal showing options like "Förbättra texten / Improve writing", "Justera ton / Adjust tone", "Fixa grammatik / Fix grammar", "Översätt till / Translate to"
  - Right sidebar (within screenshot): Blocks / Layouts / Stil tabs visible
  - Soft drop shadow on screenshot to give depth
- The screenshot should signal: "this is a modern, AI-augmented product, not a 2010-era email tool"

**No 3 USPs or trust badges in fold 1.** Those move to fold 2 (between hero and logo carousel) for better visual hierarchy.

### Section 1.5 — USPs + trust-bar (fold 2, between hero and logo carousel)

Full-width, soft background tint or white. Three columns of USPs (or one row at narrower breakpoints).

Components:
- **3 USP cards** with icon, headline, body (per copy.md)
- Below USPs: horizontal **trust-badges row** (Capterra 4.5★ · G2 4.3★ · GDPR by default · EU/Sverige · Kollektivavtal)

Visual treatment: each USP card has a subtle background tint or icon-led layout. Trust badges are inline pills or icon+text combos, separated by middle-dots.

### Section 2 — Logo carousel

Section with light gray background.
- Caption above carousel: "1000+ svenska organisationer väljer Ungapped"
- Horizontally scrolling logo strip, infinite loop
- ~10-12 logos representing customer mix

### Section 3 — Trust / Why Ungapped (4-card horizontal layout)

Reference: 4-card horizontal trust section (see project screenshot from Erik). Each card a vertical block with stat/word as visual anchor + supporting copy. First card has "UNIQUE" badge + filled coral background to stand out as the differentiator.

Layout:
- Full-width section, white or soft tint background (#F8F8F8 or very light teal #E5F7F7)
- Centered top: section pill "Trust" (yellow #F9D85A, fully rounded)
- Centered H2 (with possible last-word highlight)
- Centered subheadline (~2 lines)
- 4-column grid below, equal-width cards
- Card 1 stands out: filled coral or teal background, white text, with "UNIQUE" pill at top
- Cards 2-4: white background with subtle border (or very light tint), darker text
- Each card: large stat/headline at top (40-48px), small subheading, body copy below

On mobile: stack 4 cards vertically (or 2x2 grid on tablet).

CARDS:

**Card 1 (UNIQUE — coral/teal solid background, white text):**
- Top: red "UNIQUE" pill
- Big phrase (large, white): "Only us"
- Sub-headline (white, semibold): one short line about what's unique
- Body (white, smaller): 2-3 lines of supporting detail

**Card 2:**
- Big number/word (teal): "20 years"
- Sub-headline: "in market"
- Body: 2-3 lines

**Card 3:**
- Big phrase (teal): "In your language"
- Sub-headline: "European multi-language support"
- Body: 2-3 lines

**Card 4:**
- Top: small EU/GDPR badge or icon (~50px circle)
- Big phrase (teal): "GDPR by design"
- Sub-headline: "EU data residency"
- Body: 2-3 lines

Full copy in copy.md (English version is primary; Swedish version uses kollektivavtal as Card 1 differentiator).

### Section 4 — Omdömen (Testimonials)

Section with soft teal or light background.
- Section pill: "Omdömen"
- H2: "Vad våra kunder säger."
- Layout: hero quote at top (large), then 3 secondary quotes in a row, then review-aggregator-block at bottom

### Section 5 — Product overview

Section with light gray background.
- Section pill: "Plattform"
- H2: "Allt du behöver för digital kommunikation."
- Subheadline: "En plattform, fem verktyg. Allt du behöver för att kommunicera, mäta och växa."
- Five product cards in 2-3 column grid (e-post, SMS, enkäter, events, automation)

### Section 6 — "Så här kommer du igång"

Section with white or accent background.
- Section pill: "Kom igång"
- H2: "Från registrering till första kampanjen — på en eftermiddag."
- 4-step horizontal timeline (or vertical on mobile)
- Bottom CTA: "Starta din första kampanj"

### Section 7 — Industries we know inside-out (Gong-inspired)

Reference: Gong.io's "Trusted by high-performing revenue teams in every industry"-section. Two-column with text left + offset 4-card grid right. Highlighted text in headline. Distinctive coral/teal pill CTA.

Layout:
- Full-width section, white background
- Two-column on desktop: text left (~35-40%), cards right (~60-65%)
- Cards in **offset 2-column grid**: left column has cards 1 + 2 vertically aligned, right column has cards 3 + 4 offset DOWN by ~50% (creates staggered visual rhythm Gong uses)
- On mobile: stack everything single-column (text first, then 4 cards in row)

LEFT COLUMN content:
1. H2 with **highlighted last words** (use background-color highlight in coral or soft teal):
   - Swedish: "Branscher vi kan **inifrån och ut**"
   - English: "Industries we know **inside-out**"
2. Subheadline (mid-gray, ~3 lines):
   - Swedish: "Skräddarsydda lösningar för era specifika branschbehov. Compliance, säkerhet och support anpassat efter er verklighet — inte en generisk plattform pressad i er form."
   - English: "Tailored solutions for your industry's specific needs. Compliance, security, and support that match your reality — not a generic platform forced into your shape."
3. CTA pill (coral solid, fully rounded):
   - Swedish: "Se alla branschspecifika lösningar →"
   - English: "Explore industry solutions →"

RIGHT COLUMN — 4 industry cards:

Card styling:
- Light gray background (#F4F4F4 or similar)
- Rounded corners (16px)
- Padding 32px
- Icon top-left (~32px)
- Arrow icon top-right (~24px, in white circle background, indicates clickable)
- H3 below icon (bold, dark)
- Description below H3 (mid-gray, body, 3-4 lines)
- Hover state: subtle elevate + arrow color change to coral
- Whole card is clickable, links to /[industry]-page

Cards (in this order):

**Card 1 (top-left): Offentlig sektor / Public sector** 🏛️
**Card 2 (bottom-left): Medlemsorganisationer / Member organizations** 🤝
**Card 3 (top-right, offset down ~50%): Bygg & fastighet / Construction & real estate** 🏗️
**Card 4 (bottom-right, offset down ~50%): Skolor & lärosäten / Education** 🎓

(Full copy per card in copy.md.)

### Below section 7 (lighter edits)

- AI-Assistent block — keep as is, possibly move higher if feature is differentiating
- Final CTA section: "Osäker på vad du behöver? Kontakta oss så hjälper vi dig"
- Footer

---

## Visual hierarchy notes

- **Hero must establish trust within 5 seconds.** Use visible trust-badges + Swedish/Stockholm-anchoring + concrete proof.
- **Logo carousel is the second-strongest credibility signal.** Don't bury it.
- **"Why Ungapped" should answer: why not Mailchimp / Apsis / HubSpot?** Each card hits a real reason.
- **Step-by-step section is anti-friction tool.** Buyers who hesitate need to see "30 sek konto, 5 min import, 15 min första kampanj".

## Conversion tracking (for later — not part of HTML build)

Mark these elements with `data-track-cta` attributes:
- `data-track-cta="hero-primary"` → Testa gratis in hero
- `data-track-cta="hero-secondary"` → Boka demo in hero
- `data-track-cta="header-primary"` → Testa gratis in header
- `data-track-cta="header-secondary"` → Boka demo in header
- `data-track-cta="footer-primary"` → Final-CTA Testa gratis
- `data-track-cta="why-ungapped-card-N"` → Each "Why Ungapped" card
- `data-track-cta="step-bottom"` → Bottom CTA after step-by-step
