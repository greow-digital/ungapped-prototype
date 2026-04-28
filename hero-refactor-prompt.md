# Hero Refactor — Paste-ready Prompt for Claude Code

Use this prompt if the initial build's hero doesn't match the Rule.io-inspired layout, or as a focused follow-up to upgrade the hero independently.

---

## Prompt to paste

```
Refactor the hero section of the Ungapped homepage build to follow the Rule.io-inspired layout instead of the original illustration-based hero. Reference: https://rule.io (their homepage hero shows actual product UI screenshot with AI Assistant overlay visible).

Apply to both index.sv.html and index.en.html if both exist.

NEW HERO LAYOUT:

Two-column on desktop (text ~40% left, product UI ~60% right). Single-column stacked on mobile (text first, visual second).

Background: white with a soft, blurred gradient blob positioned behind the H1 area. Use radial-gradient with Ungapped brand colors:
- Coral #E94B6E at 15% opacity
- Teal #1FB6B6 at 15% opacity
- Optional soft purple/pink accent
- Apply filter: blur(80px) for soft, atmospheric feel

LEFT COLUMN (top to bottom):

1. Small decorative pre-headline element (~32px) — Ungapped flower/blomma logo mark in coral or teal, top-left above H1. Acts as brand signature, similar to Rule.io's green crown.

2. H1 — large, bold, dark gray (#1A1A1A), 48-56px desktop, 36px mobile, line-height 1.1. Stack vertically across 3-4 lines on desktop.
   - Swedish: "Allt för digital kommunikation. Helt på svenska."
   - English: "All your digital communication. EU-native, by design."

3. Subheadline — body-large (18px desktop, 16px mobile), mid-gray (#6B6B6B), line-height 1.6, 3-4 lines.
   - Swedish: "Nyhetsbrev, SMS, enkäter, events och marketing automation. Svensk datalagring. Svensk support. GDPR by default. Sedan 2006."
   - English: "Email, SMS, surveys, events, and marketing automation. Built in Sweden, hosted in the EU, supported in your language. GDPR by default. Trusted by 1000+ organizations since 2006."

4. Dual CTA row — primary "Testa gratis / Start free 30-day trial" (coral solid bg) + secondary "Boka demo / Book a demo" (white bg with coral border, coral text). Side by side on desktop, stacked on mobile.

5. Trust microcopy below CTAs — small text (14px), gray, with middle-dot separator:
   - Swedish: "Inget kreditkort krävs · Full tillgång under hela testperioden"
   - English: "No credit card required · Full access during your trial"

REMOVE: any inline email signup form, any "Sign up" inline input. Hero should have ONLY the two CTA buttons.

RIGHT COLUMN — Product UI screenshot:

Show an actual product screenshot of Ungapped's editor in use. The screenshot should signal "modern, AI-augmented product."

Required visual elements within the screenshot:
- Main canvas: an email or campaign being built (use Ungapped-style template — e.g. "Välkommen / Join the list")
- Floating AI overlay positioned over the canvas: a modal labeled "Ask AI" or "Ungapped AI" with vertically stacked options:
  - Förbättra texten / Improve writing
  - Justera ton / Adjust tone
  - Fixa grammatik / Fix grammar
  - Översätt till / Translate to
- Right sidebar (within the screenshot): tabs labeled Blocks / Layouts / Stil
- Subtle drop shadow on the screenshot edges (box-shadow: 0 20px 60px rgba(0,0,0,0.12))

Implementation options:
A) Use a placeholder image for now: https://placehold.co/1200x800/F4F4F4/1FB6B6?text=Ungapped+editor+with+AI+overlay
B) (Stretch) Mock the entire UI in HTML/CSS as a visual element. More work but signals "real product" much better than a static placeholder. Rule.io does this. If you go this route:
   - Use rounded corners on the outer frame (12-16px)
   - Mock 3-4 toolbar icons at top
   - Mock the campaign canvas with placeholder text and a CTA button
   - Mock the floating AI modal with the 4 options listed above
   - Mock the right sidebar with the 3 tabs

Aspect ratio: ~16:10 or 4:3. Width should fill the right column.

USPs + TRUST BADGES — MOVE OUT OF FOLD 1:

The 3 USPs and trust-badges row should NO LONGER be inside fold 1. Move them to a new section between the hero and the logo carousel (call it "Section 1.5" or just the next section).

That new section: full-width, white or soft tint background. Three USP cards in a row (or stacked on mobile), each with icon + headline + body per copy.md. Below USPs: horizontal trust-badges row.

DELIVERABLE:

Updated hero HTML + CSS in index.html (or both .sv and .en versions). Verify at 375px, 768px, 1024px, 1280px viewports. Hero should fill the viewport on desktop, with H1 and subheadline visible without scrolling.

If you mock the product UI in HTML/CSS (option B), output a checklist of what UI elements were mocked vs left as placeholder.
```

---

## How to use this prompt

1. Open Claude Code in the `ungapped-homepage-build/` folder.
2. Paste the prompt above as a follow-up message.
3. Claude Code will refactor the hero to match Rule.io's product-centric layout.
4. Verify in browser at the four breakpoints listed.

## Why this matters

The current ungapped.se hero (and the original spec in homepage-structure.md before this refactor) used a generic illustration of a woman at a laptop with floating product mockups. That's the 2018-era approach.

Rule.io's hero — and the modern B2B SaaS standard — uses an **actual product UI screenshot with AI features visible**. That signals:
- The product is real, modern, capable
- AI is integrated, not bolted on
- The visitor can see what they'll be using

For Ungapped, this matters extra because:
1. They already have an AI Assistant feature — show it off, don't bury it.
2. Public sector + member orgs buyers are more conservative — seeing an actual product reduces "is this real?" friction.
3. Signals product-led-growth maturity even if PLG isn't the primary motion.
